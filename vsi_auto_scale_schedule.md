---

copyright:
  years: 2014, 2021
lastupdated: "2021-05-19"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Managing traffic spikes with schedule-based auto scaling
{: #managing-schedule-based-auto-scaling}

Web traffic spikes can be a good thing and a bad thing. Traffic spikes are good in the sense that more people are using your site. Traffic spikes can be bad because of how a surge in activity can affect your response times. {{site.data.keyword.cloud}} auto scale provides you with ability to automatically scale your servers up or down to support your business needs. You can use schedule-based auto scaling to control the traffic spikes. 
{:shortdesc}

## Before you begin
{: #before-you-begin-schedule-based-auto-scale}

First, go to the device menu and make sure that you have the correct account permissions to complete the tasks.

* Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. If you are not the account administrator, your user account must include permission to use auto scale. For more information about updating permissions to use auto scale, see [Setting up user permissions for auto scale](/docs/virtual-servers?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Adding an auto scale group
{: #add-auto-scale-group}

In this scenario, a Dallas, Texas-based social website experiences activity spikes during weekends. Two virtual servers are the minimum requirement by the site Monday through Friday. However, two more virtual servers are needed every weekend to account for the increased traffic. The following steps take you through how to set up auto scale to support schedule-based scaling.

1. From the **Devices** menu, select **Auto Scale**.
2. Select **Add Auto Scale Group**.
3. Set up an auto scale group by first entering a **Group Name**, for example, Weekend Scale Up Group, and then select the data center.
4. Select the server termination policy. For example, if you choose **Oldest**, the server with the oldest provisioned date is selected when scaled down.
5. Indicate whether your group is to be a multi-VLAN scale group and how to balance scaling down across the configured VLAN pairs.
6. Select the public and private VLANs on which you want to provision your servers. If the servers are to be accessed from public internet (if the VLAN is running web servers), leave **Private Network Only** cleared.
7. Set the **Minimum Member Counts** to 2 and **Maximum Member Counts** to 4. Set the **Cooldown Period** to 0. Because of schedule-based scaling, no statistics are gathered to trigger scaling actions.

## Defining member configuration for your group
{: #define-member-configuration}

1. Locate **Member Configuration** and enter a **Hostname** and **Domain** for the scaling server. Subsequent servers added to the group have unique suffixes that are appended to the hostname.
2. Specify the hardware configuration of computing instances (cores, RAM)
3. Select an operating system if you want to install the minimal operating system. You can also use a public image or private image to provision your instances.
4. If the instances require more steps to install extra software, specify the URL of a post-install script to install the software. (If you use a load balancer for the group, the post-install scripts are run before a member is placed behind a load balancer.)

## Setting up policies
{: #set-up-policies}

In this scenario, the social website is using schedule-based scaling. Two policies are needed: one to scale the servers up on Friday afternoons, and a second to scale the servers down on Sunday evenings. The first policy is to scale up servers.

1. Locate **Policies** and click **Add Policy**. Enter the **Policy Name** (Example: Friday Scale Up).
2. Select the group cooldown option for the **Cooldown Period**.
3. Click **Add Trigger**, and specify a repeating trigger by selecting **Every** in the first drop-down menu, then select **Friday** and **10:00 PM**\* from the subsequent drop-down menus. (With the **Advanced Edit** checkbox, you can enter the trigger frequency in crontab–like notation.)
4. Click the **Scale By** drop-down box under **Action** and select **Relative**. Enter 2 in the **Members field**.
5. Click **Add Policy** again to specify the second policy that scales the servers down on Sunday evenings. The cooldown period is the same as the group’s cooldown. The trigger is every Sunday at 1:00 AM*, with a relative scale action of -2.
6. The time that is entered in the **Triggers** field is based on UTC time, which is why you need to select 10:00 PM for 5:00 PM Central Daylight Time and 1:00 AM for 8:00 PM Central Daylight Time. During Central Standard Time, the times would be 9:00 AM and midnight because UTC or GMT doesn’t acknowledge Daylight Saving Time. See the [World Time Server ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} site for a time converter.

## Adding a local load balancer
{: #adding-a-local-load-balancer}

If you have a local load balancer set up, you can use it to load balance your auto scale group.

1. Locate **Local Load Balancers** and click **Add Load Balancer**.
2. Click **View VIP Settings** (opens a separate page) to see local load balancers available in your account, and order new one if needed. A load balancer needs an associated service group to use with an auto scale group. Make sure that the load balancer is located in the data center of your auto scale group.
3. Click **Add Load Balancer** on the **Add Auto Scale Group** page, click the drop-down arrow for Virtual IP, and select your load balancer.
4. Click the drop-down arrows for **Service Group**, **Service Port**, and **Service Health Check Type** and select the appropriate values.
5. Click **Add Group** to save your group.
6. If all your data centers, networks, and so on, are correctly specified, your auto scale group is created. Click the group on the **View All Groups** screen to see your group details.

The result of setting up a schedule-based scaling is that two members are automatically provisioned to meet the minimum requirement of the website. On Fridays at 5:00 PM Central Time, two more members are automatically provisioned when the first policy trigger fires. Then, on Sundays at 8:00 PM Central Time, two members are reclaimed thanks to the second policy trigger. If you specify a load balancer, all members that are created either at creation, or on Friday, are behind the load balancer after you run the custom post-install script.
