---



copyright:
  years: 2018
lastupdated: "2018-10-31"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Placement groups

With placement groups for {{site.data.keyword.BluVirtServers}}, you can use public instances to build for high availability within a data center, or provide an additional level of fault tolerance within a larger deployment.
{:shortdesc}

Create your placement group, then assign up to 5 new virtual server instances. With the spread rule, each of your virtual servers are provisioned on different physical hosts.

To get started, follow these steps:
 
1. From your browser, open [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) and log in to your account.
2. On the Placement Groups page, click **Add Placement Group**.
3. Enter a name, description, and data center for the placement group, and click **Add**.
4. Locate the **Order** section and click **Devices**.
5. On the Devices page, click **Hourly** for one of the Virtual Server offerings.
6. Complete any other necessary information and click **Add to Order**. The Checkout page opens.
7. You can select any existing placement groups. **Spread** means that the instances are be on different physical hardware.
8. Finally, click **Submit Order**.

##Limitations
Existing instances cannot be added to a placement group; you can only add a virtual server instance to a placement group at provisioning. 

To remove an instance from a placement group, you must delete or reclaim the instance.
     
## Next Steps

To create and manage new placement groups, see [Managing placement groups](vsi_managing_placegroup.html).
