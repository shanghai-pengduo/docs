---
title: "删除记录"
date: 2021-11-25T16:17:44+08:00
weight: 50
description: >
    删除DNS解析记录
---

该功能用于删除解析记录。

**单个删除**

1. 在左侧导航栏，选择 **_"网络/网络服务/DNS解析"_** 菜单项，进入DNS解析页面。
2. 单击域名名称项，进入DNS解析详情页面。
2. 单击“记录”页签，进入记录页面。
3. 单击记录右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"删除"_** 菜单项，弹出操作确认对话框。
4. 单击 **_"确定"_** 按钮，完成操作。

**批量删除**

1. 在记录列表选择一个或多个记录，单击列表上方 **_"删除"_** 按钮，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

```
# 删除记录
$ climc dns-recordset-delte <记录id>
```