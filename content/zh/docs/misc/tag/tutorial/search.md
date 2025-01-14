---
title: "通过标签搜索资源"
date: 2022-01-20T15:12:36+08:00
weight: 30
description: >
    在资源列表支持通过标签搜索符合条件的资源
---

{{% alert title="说明" %}}
标签键和标签值都支持搜索，此外还支持以下搜索规则：

- 默认为contains搜索标签键或标签值；
- n* 表示以n开头的标签键或标签值；
- *n 表示以n结尾的标签键或标签值；
- !n 表示不包含n（英文状态！）的标签键或标签值；
{{% /alert %}}

1. 在虚拟机列表中，单击列表上方 **_"标签"_** 按钮，根据标签过滤搜索符合条件的资源。
    - 选择无标签资源，将筛选出所有不带标签的资源。
    - 选择一个或多个标签键，若不选择标签值，将筛选出所有带指定标签键的资源。当选择具体标签值时，将筛选出所有带指定标签键和值的资源。
      
      ![](../../images/tagsearch1.png) 