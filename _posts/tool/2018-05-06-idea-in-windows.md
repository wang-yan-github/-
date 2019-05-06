---
layout: post
title: IDEA Intellij 小技巧和插件
category: 工具
tags: [IdeaVim , IDEA, plugins ]
description: 
---

## Intellij IDEA plugins 插件无法下载
- Appearence & Behavior - System Settings - Updates - User Secure Connection，取消勾选该选项
    ![](https://wang-yan-blog.oss-cn-beijing.aliyuncs.com/tool-idea-in-plugins.png)
    
## IntelliJ IDEA 配合vim使用

### postfix
如果你还不知道怎么用，请看**Perferences**-**Editor**-**Genral-Postfix Completion**。有很多常用的快捷操作，比如new, nn，opt 。

### Live Templates
配置位置**Perferences**-**Editor**-**Live Templates**
默认比如：

- psvm: main方法
- psfs: 字符串常量
- pv: public void method

强大在于可以自定义，比如我编写一些pojo类时，为了简化代码，我一般使用lombok插件如：
```
@Getter
@Setter
@ToString
public class UserVO {
    private String name;
    private Long id;
}
```
再快一点，三个注解都是可以快速生产，于是我自定义一个:
![](https://wang-yan-blog.oss-cn-beijing.aliyuncs.com/tool-idea-in-live-templates.png)

再比如写单元测试，测试方法体也很有必要创建一个模板：
```
@org.junit.Test
public void $METHOD_NAME$Test_$EXPECT$() {
    $END$
}
```
可以根据自己的习惯和需求定义，创建方式见[creating-and-editing-live-templates](https://www.jetbrains.com/help/idea/creating-and-editing-live-templates.html)

- 快捷方式冲突
    ![](https://wang-yan-blog.oss-cn-beijing.aliyuncs.com/tool-idea-in-vim-keymap.png)
        只需要输入gs，按tab键即可自动生成代码。


    
### :action命令


http://thoreauz.com/2019/04/21/idea-keyboard-shortcuts/
https://kidneyball.iteye.com/blog/1814028
https://kidneyball.iteye.com/blog/1828427
https://www.zhihu.com/question/21551426/answer/105003969
https://www.zhihu.com/question/21551426/answer/105003969