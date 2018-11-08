---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 供应专用实例

对于如何供应专用实例，有两个选项。第一个是通过 {{site.data.keyword.Bluemix}} 目录，第二个是通过 {{site.data.keyword.slportal_full}}。目录和 {{site.data.keyword.slportal}}需要唯一登录标识。目录的用户名和密码无法用于登录到门户网站，反之亦然。
请参阅[注册 {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} 以设置 {{site.data.keyword.Bluemix_notm}} 目录或 {{site.data.keyword.slportal}}凭证。
{:shortdesc}

## 供应专用虚拟服务器实例
{: #provision-dedicated-instances}
可以通过 {{site.data.keyword.cloud_notm}} 目录或 {{site.data.keyword.slportal}} 来供应专用虚拟服务器实例。
 

### 通过 IBM Cloud 目录供应专用虚拟服务器实例 
要通过 {{site.data.keyword.cloud_notm}} 目录来供应专用虚拟服务器实例，请完成以下步骤：

  1. 使用您的唯一凭证来登录到 [{{site.data.keyword.cloud_notm}} 目录 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/catalog/){: new_window}。 
  2. 在**计算基础架构**部分中，单击**虚拟服务器**磁贴。
  3. 选择**专用虚拟服务器**选项。
  4. 单击**创建**。
  5. 在**专用主机**部分，选择**自动分配**。随后，{{site.data.keyword.cloud_notm}} 会自动将实例分配给所选数据中心内的主机。
  
     **注**：对于专用主机，请选择**指定主机**或**创建主机**。有关专用主机和专用主机实例的更多信息，请参阅[专用虚拟服务器](../vsi/vsi_dedicated.html)。
     
  5. 填写专用虚拟服务器实例的所有相关信息。 
  6. 复查订单摘要后，单击**第三方服务协议**复选框。 
  7. 单击**供应**。

### 通过客户门户网站供应专用虚拟服务器实例
要通过 {{site.data.keyword.slportal}} 来供应专用虚拟服务器实例，请完成以下步骤：

1. 使用您的唯一凭证来登录到 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。
2. 找到**订购**部分，然后单击**设备**。这将显示**订购 SoftLayer 产品和服务**窗口。 
3.  在“专用虚拟服务器”下，选择**每小时**或**每月**。这会将您重定向到*配置云服务器*页面。 

4.	输入以下信息：
       
    <table>
    <CAPTION>表 1. 专用主机实例选项</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>数量</td>
    <td>要部署的专用实例数。</td>
    </tr>
    <tr>
    <td>布置</td>
    <td>
    <ul>
    <li>自动分配 - {{site.data.keyword.Bluemix_notm}} 会自动将实例分配给所选数据中心内的主机。</li>
    <li>指定主机 - 用于专用主机实例。有关专用主机和专用主机实例的更多信息，请参阅[专用虚拟服务器](../vsi/vsi_dedicated.html)。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>数据中心</td>
    <td>选择要在其中供应实例的数据中心。</td>
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
    <td>可以为每个专用实例供应最多四个附加引导磁盘 - SAN 或“本地”。</td>
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

5.	单击**添加到订单**按钮。这会将您重定向到“结帐”页面。
6.  在*高级系统配置*下的*结帐*页面上，输入以下信息：

    <table>
    <CAPTION>表 2. 专用实例高级系统配置</CAPTION>
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

7.  单击**云服务条款**和**第三方服务协议**复选框。
8. 确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

    将向您的管理员发送一系列电子邮件 - 确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后直接转至**设备详细信息**页面。另一个选项是直接登录到 {{site.data.keyword.slportal}}。

## 后续步骤
供应虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。

