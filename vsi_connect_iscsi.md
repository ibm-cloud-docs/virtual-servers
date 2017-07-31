---



copyright:
  years: 2017
lastupdated: "2017-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Connecting to an iSCSI LUN in Linux for CentOS/RHEL 7 
{: #connecting-iscsi}

To interact with an iSCSI LUN in Linux-based operating systems, you must connect to the LUN by entering a series of commands in the terminal based on the operating system being used to perform the interactions.  The tool used to interact with an iSCSI LUN in a Linux-based OS is dependent upon the type and version of the OS installed on the device.
{:shortdesc}

## CentOS 7 and RHEL 7
1. Install iscsi-initiator and multipath mapper for Linux.

   ```
   yum -y install iscsi-initiator-utils device-mapper device-mapper-multipath
   ```
   {: codeblock}
   
2. Create the iscsid.conf configuration file.
     
3. Backup the original configuration.
   ```
   cp /etc/iscsi/iscsid.conf{,.save}
   ```  
   {: codeblock}
   
4. Open the */etc/iscsi/iscsid.conf* file with a text editor and replace the contents with the following information.

    ```
    node.startup = automatic
    node.session.auth.username = ISCSI_USER
    node.session.auth.password = ISCSI_PASS
    discovery.sendtargets.auth.username = ISCSI_USER
    discovery.sendtargets.auth.password = ISCSI_PASS
    node.session.timeo.replacement_timeout = 120
    node.conn[0].timeo.login_timeout = 15
    node.conn[0].timeo.logout_timeout = 15
    node.conn[0].timeo.noop_out_interval = 10
    node.conn[0].timeo.noop_out_timeout = 15
    node.session.iscsi.InitialR2T = No
    node.session.iscsi.ImmediateData = Yes
    node.session.iscsi.FirstBurstLength = 262144
    node.session.iscsi.MaxBurstLength = 16776192
    node.conn[0].iscsi.MaxRecvDataSegmentLength = 65536
    ```
    {: codeblock}
    
5. Start iscsid.
   ```
    /etc/init.d/iscsi start
   ``` 
   {: codeblock}
   
6. Run a discovery against the iscsi target host.
   ```
   iscsiadm -m discovery -t sendtargets -p [IP Address in StorageLayer]
   ```  
   {: codeblock}
   
7. Connect to the iscsi target host.
   ```
   iscsiadm -m node -T [output from above starting with iqn.] -p [IP Address in storagelayer] -l
   ```  
   {: codeblock}
   
8. Restart the iscsi service (Since node.startup was set to automatic in iscsid.conf it will automatically login to the target host).
   ```
    /etc/init.d/iscsi restart
   ```
   {: codeblock}
 
