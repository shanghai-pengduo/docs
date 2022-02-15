---
title: "重置密码"
date: 2022-02-08T11:14:04+08:00
weight: 70
description: >
    重置裸金属服务器上管理员用户的密码
---

该功能用于更新裸金属服务器上的管理员用户的密码，管理员密码在Linux系统下为root用户的密码。

{{% alert title="注意" color="warning" %}}
- 仅在裸金属服务器关机状态下支持重置密码操作。
- 绑定密钥的裸金属服务器无法进行重置密码操作。
- 通过ISO启动方式创建的裸金属不支持重置密码操作。
{{% /alert %}}

**重置密码**

1. 在左侧导航栏，选择 **_"主机/主机/裸金属"_** 菜单项，进入裸金属页面。
2. 单击裸金属服务器右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"重置密码"_** 菜单项，弹出重置密码对话框。
3. 设置管理员密码。
    - 随机生成：随机生成管理员密码，用户可在裸金属列表密码列查看复制管理员密码。
    - 手工输入：可手动设置管理员密码。
4. 默认勾选“重置密码后自动启动”，可根据需要取消勾选，单击 **_"确定"_** 按钮，完成操作。

**批量重置密码**

1. 在左侧导航栏，选择 **_"主机/主机/裸金属"_** 菜单项，进入裸金属页面。
2. 在裸金属列表中勾选一个或多个关机状态的裸金属服务器，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"重置密码"_** 菜单项，弹出重置密码对话框。
3. 设置管理员密码。
    - 随机生成：随机生成管理员密码，用户可在裸金属列表密码列查看复制管理员密码。
    - 手工输入：可手动设置管理员密码。
4. 默认勾选“重置密码后自动启动”，可根据需要取消勾选，单击 **_"确定"_** 按钮，完成操作。