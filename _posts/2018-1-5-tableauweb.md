---
layout: article
title:  "如何把tableau 应用到web项目中去"
categories: infovis
image: 
  teaser: logo.jpg
  
---

#### 简要：
      
	  将视图嵌入网页
      使用共享嵌入代码：每个视图顶部的共享链接可以复制和粘贴到网页中的嵌入代码。
      编写自己的嵌入代码：增强tableau提供的嵌入代码，或者生成自己的代码。
      使用tableau javascript API：可以在自己的web应用程序代码中使用 

###### 用户发布一个视图到Tableau server上时，可以通过web方式连接Tableau server，有的用户需要把这些视图嵌入自己web应用中如何实现：

将视图嵌入网页：
可以将交互式 Tableau 视图嵌入到网页、博客、wiki 页面、Web 应用程序和 Intranet 门户中。嵌入式视图会随着基础数据的变化或工作簿在 Tableau Server 上的更新而更新。嵌入的视图遵守 Tableau Server 上使用的相同许可和权限限制。也就是说，若要查看嵌入在网页中的 Tableau 视图，访问视图的用户也必须在 Tableau Server 上具有帐户。 作为替代方案，如果您有基于内核的许可证，您可以选择“启用来宾账户”，这样用户无需登录就能加载视图。

###### 可以按照以下方式嵌入视图：

使用共享嵌入代码：每个视图顶部的共享链接提供了您可以复制和粘贴到网页中的嵌入代码。
编写自己的嵌入代码：您可以增强 Tableau 提供的嵌入代码，或者生成自己的代码。无论采用哪种方式，都可以使用那些用于控制工具栏、选项卡等的参数。
使用 Tableau JavaScript API： 您可以在自己的 Web 应用程序代码中使用 Tableau JavaScript 对象。
Tableau JavaScript API可以使web应用嵌入工作表和仪表盘以进行访问交互，而不是直接连接Tableau server。

[Tableau JavaScript API介绍](http://onlinehelp.tableau.com/current/api/js_api/zh-cn/help.htm)























