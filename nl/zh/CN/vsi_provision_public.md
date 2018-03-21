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

# 供应公共实例
{: #ordering-vs-public}

## 开始之前
有两个选项可供应公共虚拟服务器实例。第一个是通过 {{site.data.keyword.Bluemix}} 目录，第二个是通过 {{site.data.keyword.slportal_full}}。目录和 {{site.data.keyword.slportal}}需要唯一登录标识。目录的用户名和密码无法用于登录到门户网站，反之亦然。
{:shortdesc}

开始之前，请查看以下先决条件。

  1. 确保您已设置 {{site.data.keyword.Bluemix_notm}} 目录或 {{site.data.keyword.slportal}}凭证。 
  
     **注**：对于 {{site.data.keyword.Bluemix_notm}} 目录，您必须具有升级的帐户才能订购虚拟服务器。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](https://console.bluemix.net/docs/admin/softlayerlink.html)。
  
  2. 如果尚未查看可供您使用的部署选项，请执行此操作。有关更多信息，请参阅[部署选项：公共虚拟服务器](../vsi/vsi_public.html)。

## 登录 
确保您已通过 {{site.data.keyword.Bluemix_notm}} 目录或 {{site.data.keyword.slportal}}登录： 

  <table>
   <CAPTION>表 1. 选择登录位置</CAPTION>
   <THEAD>
   <TR>
   <th>如果要使用以下对象登录...</th>
   <th>请执行以下操作...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud 目录</td>
   <td>
   <ol>
   <li>打开新的浏览器窗口，然后输入 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>。</li>
   <li>单击<b>登录</b>链接（右下角）。</li>
   <li>输入您的电子邮件或 IBM 标识，然后单击<b>继续</b>。</li>
   <li>输入密码，然后单击<b>登录</b>。</li>
   <li>选择<b>基础架构</b> > <b>计算</b>。</li>
   <li>单击<b>虚拟服务器</b>磁贴。</li>
   <li>选择<b>公共虚拟服务器</b>选项。</li>
   <li>单击<b>创建</b>。这将打开 {{site.data.keyword.slportal}}的主页。</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>客户门户网站</td>
   <td>
   <ol>
   <li>打开新的浏览器窗口，然后输入 <a href="https://control.softlayer.com">https://control.softlayer.com</a>。</li>
   <li>输入用户名和密码，然后单击<b>登录</b>。或者，单击<b>使用 IBM 标识登录</b>。然后，输入您的电子邮件或 IBM 标识，并单击<b>继续</b>。输入密码，然后单击<b>登录</b>。这将打开 {{site.data.keyword.slportal}}的主页。</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 供应公共虚拟服务器实例
{: #ordering-public-instance}
完成先决条件后，可以开始供应公共虚拟服务器实例。您可以通过两种方法（通过**设备**菜单或**设备**图标）来供应公共实例。

### 通过设备图标供应公共虚拟服务器实例
要通过*设备*图标来供应公共虚拟服务器实例，请完成以下步骤：

1.  在 {{site.data.keyword.slportal}}中，找到**订购**部分，然后单击**设备**。
2.  在“设备”页面上，对其中一个虚拟服务器产品，单击**每小时**或**每月**。
3.  在*配置云服务器*页面上，填写所有相关信息。
4.  单击**添加到订单**按钮以继续。
5.  确认或编辑服务器的域信息。
5.  单击**云服务条款**和**第三方服务协议**复选框。
6.  确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后转至*设备详细信息*页面。您还可以直接登录到 {{site.data.keyword.slportal}}。

### 通过设备菜单供应公共虚拟服务器实例
{: #ordering-public-devices-menu}

您还可以通过 {{site.data.keyword.slportal}}主页上的*设备*菜单来供应公共虚拟服务器实例。 

1. 单击**设备 > 设备列表**。

   “设备”页面将显示您帐户中的所有设备类型：专用主机、虚拟服务器、裸机服务器和 NetScaler 应用程序交付控制器。
2. 单击右上角的**订购设备**链接。
3. 在“设备”页面上，对其中一个虚拟服务器产品，单击**每小时**或**每月**。
4. 在*配置云服务器*页面上，填写所有相关信息。
5. 单击**添加到订单**按钮以继续。
6. 确认或编辑服务器的域信息。
7. 单击**云服务条款**和**第三方服务协议**复选框。
8. 确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后转至*设备详细信息*页面。您还可以直接登录到 {{site.data.keyword.slportal}}。

### 后续步骤
供应虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。
