---

copyright:
  years: 2020, 2024
lastupdated: "2020-09-21"

keywords: SAP NetWeaver, {{site.data.keyword.cloud_notm}}, network connectivity, SSH tunnelling, Software Provisioning Manager, SAP GUI

subcollection: sap

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# SSH tunneling
{: #ssh_tunneling}

This section describes SSH tunneling for specific SAP methods such as SAP GUI and Software Provisioning Manager (formerly known as SAPINST). 
{: shortdesc}

## SAP GUI
{: #sap_gui}

Establish an SSH tunnel from your client machine to the cloud server. For example, if your client machine is running on a Windows operating system, run the following command:

`ssh -o ServerAliveInterval=60 -o ServerAliveCountMax=600 -4 -L 3200:localhost:3200 -N -f -l root <Public IP Address> -p 22`

In this command, 3200 is the port number that is used to connect to an application server with instance number 00. You might have to change it to connect to a different application server, for example, 3202 for instance number 02.

## SAP Software Provisioning Manager
{: #swpm}

Establish an SSH tunnel from your client machine to the cloud server. For example, if your client machine is running on a Windows operating system, run the following command:

`ssh -o ServerAliveInterval=60 -o ServerAliveCountMax=600 -4 -L 4237:localhost:4237 -N -f -l root 149.81.129.28 -p 22`

4237 is the default port that is used by Software Provisioning Manager. You might have to change it if the Software Provisioning Manager execution suggests a different port.

### Generic Command
{: #swpm-ssh}

`ssh -o ServerAliveInterval=60 -o ServerAliveCountMax=600 -4 -L $localport:localhost:$remoteport -N -f -l root $host -p 22`

For more information about SSH port forwarding and SAP ports, see [SSH Port Forwarding with PuTTY](https://documentation.help/PuTTY/using-port-forwarding.html){: external}.

## SSH configuration issues such as missing host keys
{: #ssh-config-issues}

For SSH tunnelling, missing SSH host keys must be generated. For more information, see [Setting up an SSH client](https://www.ibm.com/support/knowledgecenter/STSLR9_8.3.1/com.ibm.fs9200_831.doc/svc_ssh_215ubh_copy.html){: external}.
