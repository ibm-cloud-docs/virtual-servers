---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 常见问题：服务器（常规）

## “从映像引导”和“从映像装入”有什么区别？
“从映像引导”和“从映像装入”都利用的是现有映像模板，模板应用于设备以替换现有操作系统或作为操作系统的补充来尝试补救现有问题。引导过程和装入过程的主要区别在于所使用的映像类型。执行“从映像引导”或“从映像装入”过程时，请确保已备份您可能希望恢复的所有数据。

   * “从映像引导”是一种设备引导方法，所用映像或者是 {{site.data.keyword.BluSoftlayer_full}} 提供的用于系统恢复的 ISO，或者是在 {{site.data.keyword.slportal_full}}中使用*导入映像*功能上传的 ISO。ISO 可以是设备操作系统的干净版本，也可以是可用于尝试补救设备问题的恢复磁盘。
   * “从映像装入”是一种操作系统重装方法，利用的是已从设备中捕获的映像模板或在 {{site.data.keyword.slportal}}中使用*映像导入*功能上传的映像模板。*从映像装入*选项使用 VHD 执行重装，这会擦除设备的所有数据，并将现有操作系统和文件替换为所选映像的“如新”版本。

## 为什么无法连接到 KVM 控制台？
如果无法连接到 KVM 控制台，请查看下面的故障诊断技巧以帮助解决该问题。如果发生其他问题，请联系支持人员。有关联系支持人员的更多信息，请参阅[获取帮助和支持](../vsi/vsi_ts_index.html)。

   * KVM 控制台是一个 Java applet。必须安装 Java 后，才能访问该控制台。有关安装 Java 的更多信息，请参阅[免费 Java 下载 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.java.com/en/download/){: new_window}。  
   * 如果安装了 Java，请确保已使用 VPN 建立连接。如果未建立连接，那么在尝试连接到需要 VPN 连接的 KVM 控制台时，会显示警告。
   * 在连接过程中，KVM 控制台可能会生成一个或多个弹出框。从 {{site.data.keyword.slportal}}启用弹出窗口以确保可以建立连接。
   * 您可能会收到错误“Java 应用程序已被安全设置阻止。”对于裸机 iKVM 设备，必须将 IPMI 设备的 IP 地址添加为例外。对于 VSI 设备，确保允许“https://control.softlayer.com”和 KVM 的 IP 地址。有关更多信息，请参阅 [Why are Java applications blocked by your security settings with the latest Java?![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}。
   * 如果满足了上述条件，而您却收到错误称“在 main.jar 中缺少必需的许可权清单”，这说明尚未在 Java 控制面板中启用 Java applet。在 Java SE V7 中，此设置作为 Oracle 的安全预防措施引入。在控制面板中启用 applet 可解决此问题。

     **注**：如果将 Mac OSX 与 Google Chrome 配合使用，请参阅 Java Web 站点上的“安装和使用 Mac Java 7 的信息和系统需求”。

   * 如果在尝试通过标准 Java 连接到 VSI 时因出错而失败，那么也可以尝试使用 VNC。

如果已完成上述所有检查，却仍无法连接到 KVM 控制台，请联系支持人员以获取对问题进行故障诊断的其他帮助。如果已连接到控制台，但连接到设备时发生问题，请确保用于访问设备的凭证有效。根据需要，联系帐户管理员以验证凭证。

## 我丢失了服务器密码。该如何进行恢复？
如果服务器的 root 用户或 Administrator 用户密码突然失效，那么在联系支持人员之前，可以检查一些事项。

   * 密码是复制并粘贴的吗？如果不是，请尝试这样做。另外，请将密码粘贴到记事本中，以确保复制密码时不会意外包含任何空格。
   * 如果服务器上有 cPanel，那么是否有可能因登录失败而导致 cPHulk 阻止了您的 IP 地址？如果是，可以使用 KVM 或 IPMI 来访问服务器，并在 cPHulk 中将您的 IP 地址列入白名单，使该 IP 地址紧跟在“/scripts/cphulkdwhitelist”后面。
   * 最近有人尝试通过在 {{site.data.keyword.slportal}}中修改服务器密码来更改该密码吗？在 {{site.data.keyword.slportal}}中更改密码仅会更改显示为密码的内容，而不会更改服务器使用的密码。如果发生这种情况，可以联系支持人员，他们通常可以恢复原始有效密码。
   * 您可能需要引导至操作系统的急救方式才能重置密码。有关更多信息，请参阅[启动急救内核](/docs/vsi/vsi_launch_rescue.html)。

如果检查了上面所有各项，却仍无法使用密码连接到服务器，请使用凭单联系支持人员，并请求密码重置。支持人员将需要重新引导服务器来重置密码，因此请确保您已准备好核准重新引导和/或提供您希望执行此操作的维护时间范围。大多数密码重置可以在 15 分钟内完成。在 {{site.data.keyword.slportal}}中，可以通过转至**支持 > 添加凭单**来创建凭单，并使用主题“*重新引导和控制台访问权*”。

## 是否支持 LVM 分区作为有效的文件系统？
LVM（逻辑卷管理）在 Linux 中提供对文件系统的逻辑管理。在 {{site.data.keyword.BluSoftlayer}} 环境中，不支持 LVM 作为可引导分区方案。虚拟服务器实例无法使用 LVM 排序，并且导入将 LVM 用作引导分区的映像将无法供应。如果在引导分区上需要 LVM，那么对于某些操作系统，裸机产品可以在引导时支持 LVM。通过正确的操作系统支持和配置，可以将辅助 VSI 磁盘用于 LVM 分区；但是，请务必注意，LVM 并不是 Flex 映像或映像模板支持的文件系统。如果还有进一步的问题，请开具凭单来联系能为您提供帮助的支持团队。

## 客户主机上预配置的 161.26.0.0/16 路径
{{site.data.keyword.BluSoftlayer}} 将在所有新供应的服务器上启用一条新路径以支持未来的产品。
   * 该路径将 161.26.0/16 范围 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) 内的任一地址指向后端专用网络。
   * 此 IP 块由 IANA 分配给 {{site.data.keyword.BluSoftlayer_notm}}，并且不会在公共因特网上公布。
   * 只有 {{site.data.keyword.BluSoftlayer_notm}} 系统的地址处于此范围内。
   * 客户服务器、虚拟服务器和 Vyatta 网关上的 ACL 将需要更新，以允许客户主机使用配置了此范围之外 IP 地址的 Infrastructure 服务。

## 如何为各种操作系统添加新路径

   <table>
   <CAPTION>表 1. 按操作系统添加路径</CAPTION>
   <THEAD>
   <TR>
   <th>操作系统</th>
   <th>步骤</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard 和 Windows 2003 Enterprise</td>
   <td>
   在命令行中，通过输入以下命令来添加持久路径：
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   在命令行中，通过输入以下命令来添加持久路径：
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   <tr>
   <td>Windows 2008 Web、Windows 2008 Standard、Windows 2008 Enterprise 和 Windows 2008 Datacenter</td>
   <td>
   在命令行中，通过输入以下命令来添加持久路径：
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
    <tr>
   <td>RedHat、Fedora 和 CentOS</td>
   <td>
   通过编辑/创建以下文件来创建新路径：<i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>创建该文件后，必须在其中添加以下信息：<i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   <tr>
   <td>Ubuntu 和 Debian</td>
   <td>
   在 <i>/etc/network/interfaces</i> 文件中，将以下行添加到文件末尾：
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>注</b>：将 172.16.0.26 替换为机器所在的子网的网关，该网关应该与为 10.0.0./8 路径定义的网关相同。</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>使用以下命令将该路径添加到 ESXi 主机：
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>在 /etc/systemd/network 中创建名为 10-static.network 的静态路径文件，其内容如下所示：<blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>注</b>：将 10.0.0.1 替换为专用网关 IP 地址。</td>
   </tr>
   </TBODY>
   </table>
   
   <a name="top"></a>

## 能否使监视系统在服务器停止响应时，发出自动重新引导操作并向支持技术人员发出警报？

可以，通过订购**从监视故障自动重新引导**服务，可以将监视系统设置为自动重新引导服务器，并在发出监视警报时，向支持技术人员发出凭单。我们还提供了附加服务 **NOC 监视**，通过此服务，您将在发生监视问题时收到个人通知。要了解有关这两种产品的更多信息，请参阅[服务器监视 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.softlayer.com/services/monitoring/){:new_window}。

## 什么是 CVSup 镜像？

可以根据运行的本地 CVSup 镜像进行更新。确保 supfile 具有以下条目：

```
*default host=cvsup.service.softlayer.com
```
{:pre }

distfiles 也是镜像项，可以从 freebsd.org 获取。可以将以下行添加到 */etc/make.conf* 文件，以首先尝试从本地存储库进行下载：

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

如果找不到该文件，将访问单个端口 Makefile 并移至下一个镜像。



