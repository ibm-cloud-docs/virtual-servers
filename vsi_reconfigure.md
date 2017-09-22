---



copyright:
  years: 2017
lastupdated: "2017-08-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Re-configuring an existing virtual server
{: #reconfiguring-virtual-servers}

After a virtual server is provisioned, you can upgrade or downgrade its configuration at any time.  

**Important note:** There are various public virtual servers available in pre-set flavors. For a limited time, you can modify any virtual servers that were available before pre-set flavors. Then, you will be required to migrate or cancel the existing instances and reorder. 

You cannot modify the individual core, RAM, or disk size of a virtual server that uses flavors. You must pick a different flavor that has the pre-set cores, RAM, and disk size you need. The virtual server flavor you select determines the valid cores, RAM, and disk sizes.  

Dedicated virtual servers are more customizable; therefore, you can modify the individual cores, RAM, and disk sizes.

Use the following steps to reconfigure an existing virtual server.
{:shortdesc}

## Modifying an existing virtual server (that uses pre-set flavors)
1. From the Device List, click the name of the virtual server that you want to reconfigure.
2. On the **Configuration** tab, you can click **Modify** or **Modify device configuration** to update the following items. 
  <dl>
  <dt>Size</dt>
  <dd>Select a new size.</dd>
  <p><note>Note: When you modify a flavor that uses local storage, you cannot switch to a flavor that uses non-local storage. Likewise, when you modify a flavor that uses non-local storage, you cannot switch to a flavor that uses local storage.
  </note></p>
  </dl>
3. After you specify changes for the virtual server, complete the configuration update.
  <dl>
  
  <dt>Upgrade date</dt>
  <dd>You can click the Immediately check box for an immediate update, or schedule a time for the update to become active.</dd>

  <dt>Upgrade time</dt>
  <dd>Enter the date (YYYY-MM-DD) for the update to become active.</dd>

  <dt>Notes</dt>
  <dd>Enter any applicable notes for your device. </dd>
  </dl>

4. Click **Continue**.
5. Review your order confirmation for accuracy.  Click **Edit** to edit your upgrade.
6. Click **Confirm** to confirm your order and apply the changes to your device.

## Modifying an existing virtual server (before pre-set flavors) or a dedicated virtual server
1. From the Device List, click the name of the virtual server that you want to reconfigure.
2. On the **Configuration** tab, you can click **Modify** or **Modify device configuration** to update the following items. 
  
  <dl>

  <dt>Cores</dt>
  <dd>Select the number of cores for the update, if applicable.</dd>

  <dt>RAM</dt>
  <dd>Select the amount of RAM to apply to your device, if applicable.</dd>

  <dt>Max Speed</dt>
  <dd> Select the new uplink port speeds for your device, if applicable.</dd>

  <dt>Public bandwidth</dt>
  <dd>Select the amount (in GB) of public bandwidth for your device, if applicable.  </dd>
  </dl>
  
3. On the **Storage** tab, you can click **Modify** or **Modify device configuration** to reconfigure the storage that is assigned to your virtual server.
   
   **Note:** For public virtual servers, if you are upgrading local storage and require more core or RAM, you might lose your secondary disk. When you modify a virtual server flavor that uses local storage, the flavor is pre-set for you and flavors that are not comparable cannot be selected.  

4. After you specify changes for the virtual server, complete the configuration update.
  <dl>
  
  <dt>Upgrade date</dt>
  <dd>You can click the Immediately check box for an immediate update, or schedule a time for the update to become active.</dd>

  <dt>Upgrade time</dt>
  <dd>Enter the date (YYYY-MM-DD) for the update to become active.</dd>

  <dt>Notes</dt>
  <dd>Enter any applicable notes for your device. </dd>
  </dl>

5. Click **Continue**.
6. Review your order confirmation for accuracy.  Click **Edit** to edit your upgrade.
7. Click **Confirm** to confirm your order and apply the changes to your device.
