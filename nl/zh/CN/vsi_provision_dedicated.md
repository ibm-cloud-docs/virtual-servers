---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 供应专用主机和实例
{: #ordering-vs-dedicated}

对于如何供应专用实例，有两个选项。第一个是通过 {{site.data.keyword.Bluemix}} 目录，第二个是通过 {{site.data.keyword.slportal_full}}。目录和 {{site.data.keyword.slportal}}需要唯一登录标识。目录的用户名和密码无法用于登录到门户网站，反之亦然。
请参阅[注册 {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}以设置 {{site.data.keyword.Bluemix_notm}} 目录或 {{site.data.keyword.slportal}}凭证。
{:shortdesc}

## 登录到 Bluemix 目录
要登录到 {{site.data.keyword.Bluemix_notm}} 目录以开始供应专用主机和专用主机实例，请使用以下步骤。 

1. 打开新的浏览器窗口，然后输入 [https://console.ng.bluemix.net/catalog/](https://console.ng.bluemix.net/catalog/){: new_window}。
2.	单击**登录**链接（右上角）。 
3.	输入您的电子邮件或 IBM 标识，然后单击**继续**。
4.	输入密码，然后单击**登录**。
5.	选择**基础架构 > 计算**。
6.  单击**虚拟服务器**磁贴。
7.	选择**专用虚拟服务器**选项。
8.  单击**创建**。 

这将显示 {{site.data.keyword.slportal}}的主页。

## 登录到客户门户网站
要登录到 {{site.data.keyword.slportal}}以开始订购专用主机和专用主机实例，请使用以下步骤。

1.	打开新的浏览器窗口，然后输入 [https://control.softlayer.com](https://control.softlayer.com){: new_window}。 
2.	输入用户名和密码，并单击**登录**，或者单击**使用 IBM 标识登录**。
3.	输入您的电子邮件或 IBM 标识，然后单击**继续**。
4.	输入密码，然后单击**登录**。

这将显示 {{site.data.keyword.slportal}}的主页。

## 供应专用主机 
要供应专用主机，请使用以下步骤。

1.	单击**设备**图标。
2.  单击**每小时专用虚拟服务器**或**每月专用虚拟服务器**链接。 

   **注**：专用服务器是私有服务器。

这会将您转至*配置云服务器*页面。在此页面中，可以订购与专用主机关联或不关联的专用实例。有关订购实例的更多信息，可访问[供应专用主机实例](#provision-dedicated-instances)。

4.	单击表单右侧的**创建主机**按钮。
5.	输入以下信息：
    
    <table>
    <CAPTION>表 1. 专用主机供应选项</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>数量</td>
    <td>输入要订购的专用主机数。请注意，每个供应订单只能部署两个专用主机。</td>
    </tr>
    <tr>
    <td>位置</td>
    <td>选择要布置主机的 {{site.data.keyword.cloud}} Data Center。有关适用的数据中心的列表，请参阅“关于”。</td>
    </tr>
    <td>专用主机</td>
    <td>缺省值为 56 个内核 X 242 RAM X 1.2 TB</td>
    </tr>
    </TBODY>
    </table>
    
    “订单摘要”会显示在*配置*页面的右侧。 
    
6.  单击**添加到订单**按钮。
7.  确认*结帐*页面上的选择内容，然后向下滚动到*专用主机高级系统配置*。
8.  输入以下信息：

    <table>
    <CAPTION>表 2. 专用主机高级系统配置</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>POD 选择</td>
    <td>单击下拉框，并选择要布置专用主机的 POD。</td>
    </tr>
    <tr>
    <td>主机名</td>
    <td>输入服务器的永久名称或临时名称，例如 server1。</td>
    </tr>
    <tr>
    <td>域</td>
    <td>输入不会与因特网域名冲突的子域名，例如 test.acme.com。</td>
    </tr>
    </TBODY>
    </table>

9.  单击**云服务条款**复选框。
10. 确认或输入付款信息，然后单击**提交**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

    将向您的管理员发送一系列电子邮件 - 确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后直接转至**设备详细信息**页面。另一个选项是直接登录到 {{site.data.keyword.slportal}}。

## 供应专用主机实例
{: #provision-dedicated-instances}
您可以通过两种方法（通过**设备**菜单或**设备**图标）来供应专用主机实例。

### 通过设备菜单供应专用主机实例
{: #ordering-dedicated-devices-menu}

第一个选项是通过 {{site.data.keyword.slportal}}主页中的**设备**菜单来供应专用主机实例。以下步骤将引导您逐步完成此过程。

1.	单击**设备 > 设备列表**。 
 
    *设备*页面将显示您帐户中的所有设备类型 - 专用主机、虚拟服务器、裸机服务器和 NetScaler 应用程序交付控制器。 

2.	通过单击**设备名**下主机的链接来选择专用主机实例的主机。
    
    这将显示*设备详细信息*页面的**配置**选项卡。**凭单**选项卡将列出您的活动支持凭单，**分配**选项卡显示所选计费周期的内存使用情况。有关选项卡的更多信息，请参阅“使用设备详细信息管理专用主机和实例”。

3.	向下滚动到**实例**框架。

    专用主机的计费方式（按月或按小时）决定了专用主机实例的计费方式。请注意，如果有按月计费的主机，那么可以同时供应按小时和按月计费的专用主机实例。在供应实例时，有两个链接可用：**添加每小时**和**添加每月**。按小时计费的专用主机只能供应按小时计费的专用主机实例，并且只会看到**添加每小时**链接。 

4.	如果主机是按小时计费的，请单击**添加每小时**链接；如果主机是按月计费的，请单击**添加每月**链接。这会将您重定向到*配置云服务器*页面。 

5.	输入以下信息：
       
    <table>
    <CAPTION>表 3. 专用主机实例选项</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>数量</td>
    <td>要在单个主机上部署的专用主机实例数。</td>
    </tr>
    <tr>
    <td>布置</td>
    <td>
    <ul>
    <li>自动分配 - {{site.data.keyword.Bluemix_notm}} 会自动将实例分配给某个主机，而不是由您指定主机。实例将布置到具有容量的数据中心内。如果自动分配实例，那么不会使用任何专用主机的容量。</li>
    <li>指定主机 - 与您的帐户关联的专用主机将显示在“专用主机”下。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>专用主机</td>
    <td>从要供应实例的列表中选择专用主机。</td>
    </tr>
    <tr>
    <td>计算实例</td>
    <td> 为供应订单中的每个实例选择内存和 CPU。</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> 为供应订单中的每个实例选择 RAM。</td>
    </tr>
    <tr>
    <td>操作系统</td>
    <td>为实例选择操作系统。请注意，如果服务器与操作系统之间存在冲突，将发出错误消息。例如，在 Microsoft SQL Server 上选择 Linux。</td>
    </tr>
    <tr>
    <td>第一个磁盘</td>
    <td>为订单中每个实例选择 SAN 或“本地”。</td>
    </tr>
    <tr>
    <td>附加磁盘</td>
    <td>可以为每个专用主机实例供应最多四个附加引导磁盘 - SAN 或“本地”。</td>
    </tr>
    <td>网络选项</td>
    <td> 选择相应的选项或使用缺省值。</td>
    </tr>
    <tr>
    <td>附加组件</td>
    <td> 选择相应的选项或使用缺省值。</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

6.	单击**添加到订单**按钮。
7.  在*高级系统配置*下的*结帐*页面上，输入以下信息：

<table>
    <CAPTION>表 4. 专用主机实例高级系统配置</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>VLAN 选项</td>
    <td>如果已经订购了至少一个服务器，请将新服务器添加到您帐户下的 VLAN 中。</td>
    </tr>
    <tr>
    <td>供应脚本</td>
    <td>提供允许您在供应后自动执行某些步骤的脚本。</td>
    </tr>
    <tr>
    <td>SSH 密钥</td>
    <td>提供您的 SSH 密钥的公用密钥，该密钥允许您在供应服务器之后登录到服务器。</td>
    </tr>
    <tr>
    <td>用户元数据</td>
    <td>定制供应脚本的可选元数据。</td>
    </tr>
    <tr>
    <td>主机名</td>
    <td>输入服务器的永久名称或临时名称，例如 server1。</td>
    </tr>
    <tr>
    <td>域</td>
    <td>输入不会与因特网域名冲突的子域名，例如 test.acme.com。</td>
    </tr>
    </TBODY>
    </table>

8.  单击**云服务条款**和**第三方服务协议**复选框。
9. 确认或输入付款信息，然后单击**提交**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。


一旦供应了专用主机实例，您将收到一封电子邮件。

### 通过设备图标供应专用主机实例
供应专用主机实例的第二个选项是使用 {{site.data.keyword.slportal}}主页上的**设备**图标。以下步骤将引导您逐步完成此过程。

1.	单击**设备**图标，然后在“专用虚拟服务器”下，选择**每小时**或**每月**。
2.	执行[通过设备菜单供应专用主机实例](#ordering-dedicated-devices-menu)下的各步骤，从第 5 步开始。

### 后续步骤
供应虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。


