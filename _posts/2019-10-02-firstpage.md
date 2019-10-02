---
layout: post
title: "jekyll搭建个人微博的详细步骤"
description: "为了记录学机器学习乃至深度学习过程中，一些令人感动的知识点特开此博，希望大家以后多多指教。"
tag: "过程分享帖"
---

### 本地发布
1、选中clone下来的主题,git bash
2、在bash中输入 bundle exec jekyll server 或者 jekyll server
3、打开chrome输入localhost:4000，即可查看目录(期间如果修改yml以外的文件，修改后，重载，若修改yml重新jekyll server)

### 模版套用
1、一篇文章是markdown文件， 即MD文件，每一篇md文章都需要文件头，

举个例子：

# - - -

layout: post

title: "jekyll搭建个人微博的详细步骤"

description:"为了记录学机器学习乃至深度学习过程中，一些令人感动的知识点特开此博，希望大家以后多多指教。"

tag: "过程分享帖"

# - - -

2、其中layout决定你发的文章放在哪儿，打开_layputs可以发现有三个选择page  、 post 、 default三个选项，选择post，那么md文章需要放在_post文件夹下
      这些头文件配置是必须的

3、此外注意：MD文件的名字不能是中文

4、日期

1）可以放在头文件声明中

举个例子：

# - - -

layout: post

title: "iOS 9 变化笔记"

date: 2015-09-26 18:15:06 

description: "iOS9 变化笔记, 以及工作中常遇到的问题"

tag: iOS

# - - -

2）日期也可以写在文件名中

举个例子：

2019-10-02-文件名.md

### 模版格式
>1、整个模版都无需缩进


>2、一级标签+正常字体

举个例子：

# ###  一级标签名
   正文部分

>3、二级标签+注意点分类

举个例子

# ### 二级标题
# >1. 观点1
# >2. 观点2
# >3. 观点3

或者

# **二级标题: **
# >1. 观点1
# >2. 观点2
# >3. 观点3

>4、代码框

举个例子

# ```bash
(null): warning: /var/folders/p4/z7zy68r92hd3p5ry5g2v3k_8rlwzzr/C/org.llvm.clang.dalmo/ModuleCache/1TXZDLI9N2EMV/Foundation-3DFYNEBRQSXST.pcm: No such file or directory。
# ```

>5、超链接

1)单独行超链接

# - [iOS9AdaptationTips] (url) 
# - [iOS9学习系列] (url) 
# - [iOS9-day-by-day] (url)

2）字体超链接

转载请注明：[关键字] (url) » [点击阅读原文] (url)

注意：(url)要紧跟着前面的关键字方框

>6、单独重点行

 "* 选择项目——>点击Target——>点击Build Setttings——>搜索栏里搜bitcode——>把Enable 

>7、正常字体（不用缩进）

>8、注释掉md文件的执行代码

用   #+空格+内容   去注释掉能够运行的md符号命令