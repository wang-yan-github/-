---
layout: post
title: google 开发使用技巧及插件
category: 工具
tags: [ google, vimium ]
description: 
---
## [vimium](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb) 插件
### 浏览当前页面：

    ？          显示帮助对话框以获取所有可用键的列表
    h           左滚动
    j           向下滚动
    k           向上滚动
    l           向右滚动
    gg          滚动到页面顶部
    G           滚动到页面底部
    d           向下滚动半页
    u           向上滚动半页
    f           在当前选项卡中打开一个链接
    F           在新标签中打开链接
    r           重新加载
    gs          查看源代码
    i           进入插入模式 - 所有命令都将被忽略，直到您点击esc退出
    yy          将当前网址复制到剪贴板
    yf          将链接URL复制到剪贴板
    gf          循环前进到下一帧

### 导航到新页面：

    o           打开URL，书签或历史记录条目
    O           在新选项卡中打开URL，书签，历史记录条目
    b           打开书签
    B           在新选项卡中打开书签

### 使用find：

    /          进入查找模式 - 输入您的搜索查询，然后按Enter键进行搜索或按esc取消
    n          循环前进到下一个查找匹配
    N          循环回到上一个查找匹配

### 浏览您的历史记录：

    H          回到历史
    L          在历史上前进

### 操纵标签：

    J，gT      左边有一个标签
    K，gt      去右边一个标签
    g0         转到第一个标签
    g $        转到最后一个标签
    t          创建标签
    x          关闭当前选项卡
    X          恢复关闭选项卡（即展开'x'命令）
    T          搜索打开的标签页

### 其他高级浏览命令：

    ]]        按照标有“下一个”或“>”的链接。浏览分页网站很有帮助。
    [[        请点击标有'previous'或'<'的链接。浏览分页网站很有帮助。
    <af>      在新标签页中打开多个链接
    gi        聚焦页面上的第一个（或第n个）文本输入框
    gu        在URL层次结构中上升一级

Vimium支持命令重复，例如，点击'5t'将快速连续打开5个标签。ESC（或<c  -  [>）将清除队列中的任何部分命令，并且还将退出插入和查找模式。

## 发行说明，请参阅：

    - https://github.com/philc/vimium#release-notes