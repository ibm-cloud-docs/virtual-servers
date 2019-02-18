---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# About portable storage volumes

Portable storage volumes are auxiliary storage solutions that are exclusively available on {{site.data.keyword.BluVirtServers_short}}. They can be connected to one virtual server at a time. They are also an ideal solution if you want to transfer data between virtual servers that exist in any data center on {{site.data.keyword.cloud}}'s network. Portable storage volumes are useful for database applications that require access to raw, unformatted block-level storage and for moving large data sets between {{site.data.keyword.BluVirtServers_short}}.

When a portable storage volume is attached to a virtual server in a different data center than the original virtual server, {{site.data.keyword.cloud}}'s internal system copies the volume to the SAN in the new data center. The system then verifies the integrity of the copied volume and removes the original portable volume from the original data center SAN.

## Next steps
For more information about how to use portable storage volumes, see the following tasks:
* [Accessing portable storage](/docs/vsi/storage/access-portable-storage-screen.html)
* [Editing the portable storage description](/docs/vsi/storage/edit-description-portable-storage-volume-psv.html)
