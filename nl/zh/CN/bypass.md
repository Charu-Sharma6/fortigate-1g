---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 绕过防火墙规则

要绕过防火墙规则，请执行以下步骤：

1. 从浏览器中，打开[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，然后登录到您的帐户。
2. 在客户门户网站导航中，转至**网络 > IP 管理 > VLAN**，然后单击要绕过的防火墙设备。
3. 在**设备详细信息**页面中的**配置**选项卡上，可以使用**操作**下拉菜单来选择**设置路由旁路**，也可以在**状态：**部分中单击**绕过规则**按钮。 

	此外，还可以选择路由时绕过防火墙。要完成此操作，可以单击**路由时绕过**按钮。不管是哪种方式，都应该会显示确认对话框。单击**是**以确认操作。绕过规则大约会在两分钟后生效。在旁路方式下，“状态”将为“正在绕过防火墙路由流量”。

## 重新启用规则

要重新启用规则，请按照以上指示信息，到达设备的**配置**选项卡，然后单击**操作**下拉菜单，选择**设置路由旁路**。此时将显示确认对话框。单击**是**以确认操作。“状态”将在两分钟后重新变回“正在通过防火墙路由流量”。
