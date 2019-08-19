---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQs: Auto scale
{: #faqs-auto-scale}

## Does auto scale support Bare Metal Auto Scale instances?
{: faq}

Currently, auto scale doesn't support Bare Metal Auto Scale instances.

## Does auto scale work with load balancers?
{: faq}

Yes, auto scale currently works for local load balancers and uses a portion of the load balancer API. For more information, see [Scale Load Balancers](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What are the different auto scale termination policies?
{: faq}

There are three auto scale termination policies: newest, oldest, and closest to next charge. These describe how the group chooses what member to take away when scaling down. For more information, see [Termination Policy](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What are auto scale policies?
{: faq}

A policy holds a set of actions and a set of triggers. Policies typically are composed of these elements: name, cooldown, action, and triggers. For more information, see [Policies](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What are auto scale triggers?
{: faq}

Triggers are conditionals that can be satisfied (only when the group is active). There are three types of triggers: one-time, repeating, and resource-use. For more information, see [Triggers](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What is the Maximum Member Count?
{: faq}

It's the most members that a group allows to be present. For more information, see [Maximum Member Count](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What is Minimum Member Count?
{: faq}

It's the fewest members that a group allows to be present. For more information, see [Minimum Member Count](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## What is an auto scale asset?
{: faq}

An asset is a fixed member in a group that doesn't contribute to the member count and isn't automatically controlled in any way. The asset is present to provide additional information to the policy triggers. For instance, an asset can contribute to the whole group CPU percentage if CPU percentage is being used as a trigger. Currently, a group can have only  virtual guest assets and there's no limit to how many. Additionally, a group isn't required.

## What is an auto scale group?
{: faq}

A group (scale group) is a group-specific collection of assets, members, scale load balancers, VLANs, and policies. A group has all the parameters for scaling including the member count boundaries and the scaled virtual server instance member templates.

## What is an auto scale member?
{: faq}

A member is a scaled unit in a group. Members are automatically provisioned or reclaimed based on policy actions. Currently, all members are virtual server instances. On an active group, there are never fewer members than the minimum or more members than the maximum. Although members are usually added by actions of a policy, they can also be manually added by a user.
