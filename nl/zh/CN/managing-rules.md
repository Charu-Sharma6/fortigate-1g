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

# 管理防火墙规则（策略）

FortiGate 使用了“策略”这一概念，具体包括接受/拒绝流量、应用安全概要文件、执行流量整形、记录流量以及计划策略应用的时间范围等功能。要组合策略，必须先创建将参与此策略的对象。 

1. 使用凭证登录到设备。您可以在[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window} 中的**设备详细信息**页面上找到凭证。请按照“如何[管理 FortiGate Security Appliance](managing-fsa.html)”指示信息来查找凭证。
2. 登录到设备后，浏览到**策略和对象**菜单，然后选择要管理的协议（例如，IPv4 或 IPv6）。系统会根据最左侧的序列号对流量实施策略。用户可以在列表中将策略拖动到较高位置以便较早实施策略，反之亦然。
3. 要添加策略，请单击**新建**并参考以下字段定义：

    **传入接口：**对于入口规则，此为面向公众的接口（外部接口）；对于出口规则，此为面向计算的接口（内部接口）。

    **源地址：**此为流量的源 IP。必须将该 IP 添加到“对象”菜单上的“地址”列表中。请注意，“全部”选项可用。

    **源用户：**这会将策略应用于在“用户和设备”面板上创建的用户或组。

    **源设备类型：**这会将策略应用于在“用户和设备”面板上创建的设备。

    **目标地址：**此为流量的目标 IP。必须将该 IP 添加到“对象”菜单上的“地址”列表中。请注意，“全部”选项可用。

    **计划：**用于确定要在何时运行策略。“始终”选项可用。您还可以在“对象”菜单中的“计划”下创建计划。

    **服务：**用于确定要将策略应用于哪个服务。“全部”选项以及多个标准服务可用。您可以在“对象”菜单中的“服务”下添加更多服务。

    **操作：**接受或拒绝流量。 

    **防火墙/网络选项：**启用或禁用 NAT 及其关联的选项。

    **安全概要文件：**为每个选项提供开关，并允许关联概要文件。

    **流量整形：**允许您配置可用于流量的最大和保证（最小）带宽。您还可以在基于 IP 的整形器上设置最大连接限制。 

    DSCP 设置无效，因为 IBM Cloud 平台会忽略用户生成的 QoS 信息。

    **日志记录选项：**用于配置何时记录“允许”的流量。此设置（尤其是“捕获包”选项）会占用设备资源。

    **注释：**用户生成的注释

    **启用此策略：**启用或禁用策略

## 简单的“允许全部”Web 流量进入 Web 服务器的规则示例

***传入接口：*** *外部 VLAN*

***源地址：*** *全部*

***源用户：** *空白*

***源设备类型：*** *空白*

***传出接口：*** *内部 VLAN*

***目标地址：*** *x.x.x.x（Web 服务器 IP）*

***计划：*** *始终*

***服务：*** *HTTP*

***操作：*** *接受*

***NAT：*** *关闭*

***安全概要文件：*** *使用标准*

***流量整形：*** *关闭*

***记录允许的流量：*** *打开（安全事件）*

***注释：*** *Web 服务器流量 x.x.x.x*

***启用此策略：*** *打开*
