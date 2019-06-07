---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Managing traffic spikes with resource-based auto scaling
{: #managing-resourced-based-auto-scaling}

Launching a new product or having a sale on an existing product can cause a spike in traffic on your website. A spike in traffic can affect your response time, which affects your customers’ experience with your website. {{site.data.keyword.cloud}} auto scale enables you to automatically respond to traffic spikes. You can use resource-based auto scaling to control these traffic spikes.
{:shortdesc}

## Before you begin
First, navigate to the device menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. If you are not the account administrator, your user account must include permission to use auto scale. For more information about updating permissions to use auto scale, see [Setting up user permissions for auto scale](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Adding an auto scale group
{: #adding-auto-scale-group}

For example, a Dallas, Texas-based e-commerce website requires three virtual servers to be online at all times. Business spikes between the hours of 9:00 AM and 5:00 PM every weekday when the company holds online sales. To help sustain website response times, three more virtual servers are needed during these times. Additionally, when public inbound traffic averages over 5 MB per second across all virtual servers for 10 minutes, two more virtual servers should be provisioned. When traffic falls below 5 MB per second, those extra virtual servers should be canceled and removed. The goal is to have no more than five virtual servers handling the traffic surge, which keeps the weekday virtual servers from being impacted by the extra weekday traffic. The following steps take you through how to set up auto scale to support resource-based scaling.

1. From the **Devices** menu, select **Auto Scale**.
2. Select **Add Auto Scale Group**.
3. Set up an auto scale group by first entering a **Group Name**, for example, Weekend Scale Up Group, and then select the data center.
4. Select the server termination policy. For example, if you choose **Oldest**, the server with the oldest provisioned date is selected when scaling down.
5. Indicate whether your group is to be a multi-VLAN scale group and how to balance scaling down across the configured VLAN pairs
6. Select the public and private VLANs on which you want your servers provisioned. If the servers are to be accessed from public internet (if the VLAN is running web servers), leave **Private Network Only** cleared.
7. Set the **Minimum Member Counts** to 3 and **Maximum Member Counts** to 6. Set the **Cooldown Period** to 0. Because this is schedule-based scaling, there are no statistics gathered to trigger scaling actions.

## Defining member configuration for your group
{: #defining-member-configuration}

1. Locate **Member Configuration** and enter a **Hostname** and **Domain** for the scaling server. Subsequent servers added to the group have unique suffixes that are appended to the host name.
2. Specify hardware configuration of computing instances (cores, RAM, and so on.)
3. Select an operating system if you want to install the minimal operating system. You can also use a **Public Image** or **Private Image** to provision your instances.
4. If the instances require extra steps to install additional software, specify the URL of a **Post-Install Script** to install the software. (If you use a load balancer for the group, the post-install scripts are run before a member is placed behind a load balancer.)

## Setting up policies
{: #setting-up-policies}

In the scenario, the e-commerce website is using resource-based scaling. Two policies are needed: one to have a relative scale action of +3 for the needed time frame, and a second to have an absolution action of 3 when the spike is over. The first policy is to add the resources.

1. Scroll down to **Policies** and click **Add Policy**. Enter the **Policy Name**, (Weekday Scale Up).
2. Select the group cooldown option for the **Cooldown Period**.
3. Click **Add Trigger**, and specify a repeating trigger by selecting **Every** in the first drop-down menu, then highlight **Monday, Tuesday, Wednesday, Thursday,** and **Friday** and **2:00 PM**\* from the subsequent drop-down boxes. (The **Advanced Edit** check box lets you enter the trigger frequency in crontab–like notation.)
4. Click the **Scale By** drop-down box under **Action** and select **Exact**. Enter 3 in the **Members** field.
5. Click **Add Policy** again to specify the second policy that removes the servers every afternoon. The cooldown period is the same as the group’s cooldown. The trigger is every Monday, Tuesday, Wednesday, Thursday, and Friday at 10:00 PM\*, with an exact scale action of 3. The time that is entered in the **Triggers** field is based on UTC time, which is why you need to select 2:00 PM for 9:00 AM Central Daylight Time and 10:00 PM for 5:00 PM Central Daylight Time. During Central Standard Time, the times would be 1:00 PM and 9:00 PM because UTC/GMT does not acknowledge Daylight Saving Time. See the [World Time Server ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} site for a time converter.
6. Set up another group with cooldown of 0, named, for example, Traffic Burst Group, with a minimum member count of 0 and a maximum of 5. Use the same settings for group and member configuration as the Weekday Scale Up group, except for the group name.
7. Click **Add Policy** to add the second policy that controls the two additional servers when public inbound traffic averages over 5 MB per second across all virtual servers for 10 minutes.
8. Enter the **Policy Name**, for example, Traffic Burst Group.
9. Select the group cooldown option for the **Cooldown Period**.
10. Click **Add Trigger**. Leave the default **If my** in the first box and select **Public Network Incoming Mbps** for the second box. Leave the default > sign in the third box. In the fourth box, enter **5** (5 MB), enter **600** in the fifth box and select **Seconds** in the last box to represent 10 minutes.
11. Click the **Scale By** drop-down box under **Action** and select **Relative**. Enter 2 in the **Members** field.
12. Click **Add Policy** again to specify the second policy that removes the servers when the traffic has decreased to fewer than 5 Mbps\*The cooldown period will be the same as the group’s cooldown. The trigger is if my public network incoming Mbps is less than 5 (5 Mbps) for a period of 600 seconds (10 minutes).

When both groups are created, the Weekday Scale Up group creates three servers (the minimum). On weekdays, at 9:00 AM Central Time, three more servers are added, and at 5:00 PM Central Time, the servers are removed. There is no other way for the members to be added or removed from that group. In a completely separate Traffic Burst Group, two servers are added for every 10 minutes in which the inbound public traffic across all members averages at 5 MB per second, until it hits the group maximum of five. After the inbound public traffic stays under that amount for 10 minutes, all servers in this group are removed.

