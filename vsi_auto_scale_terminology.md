---

copyright:
  years: 2014, 2021
lastupdated: "2021-05-19"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Auto scale terminology
{: #auto-scale-terminology}

Use the following terms to increase your understanding of the auto scale feature.

* **Auto Scale group:** An auto scale group is a set of identical servers and, optionally, a load balancer, which is defined by the launch configuration that you set up. The group can scale up and down in response to load, as defined by the scaling policy that you configure and bound by your scaling group configuration.
* **<a name="group_name"></a>Group name:** A group name must be unique on the account and is required before a scaling group can be defined. The group name can be edited at any time.
* **<a name="cooldown"></a>Group cooldown:** The period after any status change in the auto scale group before a policy can be considered "active" and start again. A cooldown is required; it can be set to 0, which is effectively off. A cooldown can't be set for over 10 days. The cooldown period provides the auto scale group time to recalibrate and metric averages to reflect changes.
  * **Auto Scale group cooldown:** The amount of time that must pass after a group becomes active before any policy action can run.
  * **Policy cooldown:** Just like the group cooldown, except it overrides the setting for this policy only. If not provided, the group cooldown value is used.
* **<a name="member"></a>Member:** A group contains members, which are virtual servers that are automatically scaled by the group.
* **<a name="min_virtual_member"></a>Minimum Member Count:** The fewest number of members that are allowed in an auto scale group. Users can guarantee an auto scale group with an active status never has fewer members than the set number. If the actual number of members is less than the current member count, members are automatically created to reach the minimum. If VLANs are present on the auto scale group and not associated with a billing item, the value must be at least 1.
* **<a name="max_virtual_member"></a>Maximum Member Count:** The most number of members that are allowed in an auto scale. Users can guarantee that an auto scale group with an active status never has more members than the set number. If during create or edit, the actual number of members is more than the current member count, members are automatically removed to reach the maximum.
* **Assets:** An existing server on the account that is never scaled with the group, but can participate in metric collection numbers. Currently, only virtual server assets are supported. An auto scale group isn't required to have any assets.
* **<a name="status"></a>Status:** An auto scale group’s status is a derived value based on what its members are doing and whether the group issuspended. The following are statuses for an auto scale group:
  * **Scaling:** Used when any members aren't provisioned or have an active provision transaction. In scaling status, an auto scale group can't be triggered for scaling and only non-actionable properties can be edited.
  * **Busy:** Used when any members have an active transaction but the transaction isn't a provisioning or reclaim transaction. In busy status, an auto scale group can't be triggered for scaling and only non-actionable properties can be edited.
  * **Suspended:** Used when a member isn't scaling or busy, but is set to Suspended. In Suspended status, an auto scale group can't be triggered for scaling. However, any property can be edited. Any actions that would occur as a result of a group create or edit don't occur until the user resumes the auto scale group. An auto scale group can be suspended manually by the user or automatically if a scaling error occurs in the auto group. An auto scale group can be resumed only by a user.
  * **Active:** An auto scale group is active if it isn't scaling, busy, or suspended. When active, an auto scale group value can be edited and all triggers can be started.
* **<a name="termination"></a>Termination Policy:** The termination policy is how the auto scale group chooses which member to remove when scaled down. Three policies are available to choose from.
  * **Newest:** The member that is provisioned most recently isremoved.
  * **Oldest:** The member whose provision date is the oldest is removed.
  * **Closest to next charge:** The member that is coming closest to the next charge is removed. Since members are invoiced by the hour, closest to next charge is the member that used up the most minutes of the current hour.
* **<a name="multi-vlan"></a>Multi-VLAN scale group:** A group that has servers that are provisioned to multiple VLANs. In addition to the existing scale group rules, rules are applied that specifically govern multi-VLAN scale group:
  * All VLANs must be purchased for a multi-VLAN scale group.
  * More than one public or private VLAN isn't allowed on a single router.
  * The VLAN with the lowest number of members is selected when scaling, providing its public and private pair, if provided.
  * The VLAN with the lowest number of members is selected when scaling, providing its public and private pair, if provided.
* **<a name="balanced term"></a>Balanced Termination setting:** If the balanced termination flag is set, the scale group scales down members in a way to preserve even balance across the configured VLAN pairs. The termination policy is used if there's uncertainty about which member to use to maintain balance (for example, having the same number of members on two or more VLAN pairs). If the flag isn't set, the termination policy is used regardless of how many members are on each VLAN.
* **Member Template:** A member template is on the auto scale group and “tells” the group the order of the virtual servers within the group. Things to keep in mind when a member template is used:
  * The account ID must be provided and it must be the same as the Auto Scale group.
  * If specified, billing must be set to hourly.
  * If data center is given, it must be in the same regain and contain the VLANs on the group.
  * VLANs can't be given to the template. If the user needs to specify VLANs for members, they must use the Auto Scale group's VLANs.
  * If any load balancers are set up on the Auto Scale group, the template can't be private network only.
* **<a name="vlan"></a>VLANs:** The user can optionally provide a collection of VLANs for the provisioning of member servers. Only one pair of VLANs can be provided per router. If multiple VLAN pairs are provided for multiple routers, the scaling system ensures that members are added evenly across routers. See “balanced termination setting” to learn more about evenly removing members across multiple VLAN pairs.
  * Auto Scale attempts to reuse a public VLAN you have behind the router. A new public VLAN is created on the same router if a public VLAN isn't selected, and only private isn't indicated.
  * Auto Scale can't create a group without a Private VLAN selected when a Public is. You might see the error "Invalid guest template, error: Only the front-end VLAN was specified. Specify the backend VLAN as well. All public VLANs must have a paired private VLAN Balanced termination can be only enabled on multi-VLAN-balanced scale groups". This doesn't apply to Private Network Only groups.
* **<a name="scalelb"></a>Scale Load Balancers:** A group can contain load balancer settings to be applied to members when provisioning is complete. The option to scale load balancers currently works only with local load balancers and uses some of the load balancer API. The load balancer virtual IP address must be on the same account as the auto scale group. The load balancer must also be in a valid location in accordance with the VLAN, virtual server data center, and region. Currently, if any load balancers are provided, the virtual server must provide the data center. The virtual server is automatically placed behind the load balancer during provisioning. Items that comprise a scale load balancer include:
  * **Virtual IP address ID:** The load balancer ID to use.
  * **Service port:** The incoming port. An existing service group record is used if present for this port. Otherwise, the record is created with some of the following information.
  * **Allocation Percent:** The percentage of connections-per-second that the virtual server is allocated from the total connections-per-second pool of the virtual IP. For example, if the virtual IP has 250 connections-per-second and the value is 25 percent, other virtual servers that are on that virtual IP can be only allocated up to 75 percent of the other connections-per-second. It‘s not a burstable maximum, but a pure allocation from the pool whether the connections are used or not. If the virtual server exists for the specific port, the number must match the existing allocation percent.
  * **Routing Method:** How the traffic is routed among the servers. If the virtual server exists for the specific port, the number must match the existing routing method.
  * **Routing Type:** The type of routing to be performed among the servers. If the virtual server exists for the specific port, the number must match the existing routing type.
  * **<a name="health_check"></a>Health check:** The type of checks to do on the servers. If HTTP_CUSTOM checks, attributes can be provided for the HTTP method, URL, and expected response.
  * **Port:** The port to be used during health checks and when traffic is sent to from the load balancer.
* **<a name="policies"></a>Policies:** An auto scale group can have any number of policies. A policy holds a set of actions and a set of triggers. Triggers are optional and might not be provided if the user would rather start the policy's actions manually. Only one trigger must be satisfied for the action to be started. A policy consists of:
  * **Name:** A policy must be given a name and the name must be unique in the Auto Scale group.
  * **Policy Cooldown:** Setting a policy cooldown is optional, however if provided, it overrides the group cooldown for when a policy can start being triggered following a group status change. It has nothing to do with the source of the group status change and can be considered active after a group is made active.
  * **<a name="actions"></a>Actions:** Currently the only type of action is a scale action. Actions can be only started on active groups. Scale actions include the following action types:
    * **Amount:** The number of members to scale. The number can be positive or negative, and the value is dependent upon the scale type.
    * **Scale Type:** Three scale types exist – absolute, relative, and percent:
      * **Absolute ("Exact" in the GUI):** Absolute forces the auto scale group to a set number of members, regardless of the current member count. Absolute scaling can include scaling up, down, or not at all. The number must be within the minimum and maximum range of the group.
      * **<a name="relative"></a>Relative:** Relative scale results in the auto scale group scaled up or down by the specific amount. Regardless of the amount, the system makes sure that the auto scale group isn't scaled down under its minimum or over its maximum. For example, a group's minimum is 5, its current count is 7, and the relative scale amount is -4. The count is treated as though it's only -2 at invocation time since it can't scale under 5.
      * **Percent:** Percent scale results in the auto scale group scaling up or down based on a positive or negative percentage. The number is a percent of the current auto scale group member count. Any extra percent after the decimal point is always ignored. If the percent scale amount is zero, it is automatically treated as -1, or 1, depending on whether the original percentage value was positive or negative. For example, if a group has 27 members and the amount is 12 (for 12 percent), it would mean 3.24 members, which rounds to 3. But if the group only had two members, it would mean 0.24 members, which usually would round to 0 but automatically rounds up to at least 1.
  * **<a name="triggers"></a>Triggers:** Triggers are conditionals that can be satisfied. Three types of triggers exist – one-time, repeating, and resource-use:
    * **One-time:** One-time trigger takes a single date and starts if the auto scale group is active. All times are in UTC format.
    * **<a name="triggers_repeat"></a>Repeating:** Repeating trigger takes a cron-formatted schedule and triggers based on that schedule if the group is active.
    * **Resource-use:** Resource-use trigger has a collection of resource watches. When all the resource watches are met, the trigger is considered satisfied.
      * **Watches:** A resource watch is a single set of parameters to watch a certain metric value across all members and assets of the auto scale group. The parameters are:
        * **Algorithm:** This is the algorithm for combining metric values. The only algorithm that is supported is Exponential Weighted Moving Average (EWMA).
        * **Metric:** Metrics are based on the following values:
          * **CPU percent:** The CPU percentage.
          * **Network in on private network:** The incoming bytes per second on the private virtual interface.
          * **Network out on private network:** The outgoing bytes per second on the private virtual interface.
          * **Network in on public network:** The incoming bytes per second on the public virtual interface.
          * **Network out on private network:** The outgoing bytes per second on the public virtual interface.
        * **Operator:** The value used to check whether a metric is under or over a certain value. The only value that is accepted is the literal greater than (>) or less than (<) character.
        * **Period:** The number of seconds the metric is aggregated over when compared to the specific value. The metric aggregation starts, isn't considered valid until it collected for at least the period. For example, if a group has a cooldown of 300 seconds and a resource watch that aggregates a metric over 500 seconds, the watch can't be satisfied until 800 seconds pass. Metrics are considered invalid until the cooldown passes. The aggregated value is also considered invalid until it built up for at least the number of seconds in the aggregation period. A period can't be less than 2 minutes or more than two days.
        * **Value:** The value to compare against. For CPU percent metric, it must be in the range 5 - 100. For network metrics, it must be no less than 0.
