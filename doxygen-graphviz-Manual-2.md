## 1. 问题的产生

当分析一个很复杂的项目源代码时，如何有效的分析函数间的调用关系呢？从网上搜索到了如下方法：使用doxygen和graphviz来自动分析函数间的调用关系。

## 2. 工具简介

> Doxygen is the de facto standard tool for generating documentation from annotated C++ sources, but it also supports other popular programming languages such as C, Objective-C, C#, PHP, Java, Python, IDL (Corba, Microsoft, and UNO/OpenOffice flavors), Fortran, VHDL, Tcl, and to some extent D.

> Graphviz is open source graph visualization software. Graph visualization is a way of representing structural information as diagrams of abstract graphs and networks. It has important applications in networking, bioinformatics,  software engineering, database and web design, machine learning, and in visual interfaces for other technical domains.

## 3. 生成函数调用图

#### (1) 下载并安装以下两种工具

[doxygen](http://www.stack.nl/~dimitri/doxygen/index.html) & [graphviz](http://www.graphviz.org/)

注意下载时，选择的是windows版本，还是mac版本。

如果安装过程中弹出“打不开 XXX，因为它来自身份不明的开发者”请进入如下网址寻找解决办法：
http://jingyan.baidu.com/article/f71d60377960651ab741d140.html

#### (2) 运行DoxyWizard，弹出Doxygen配置界面

[[/img/doxygen-graphviz-Manual-2/wizard_project.png]]

选择Scan recursively则递归分析源代码目录中的子目录内的源代码。

[[/img/doxygen-graphviz-Manual-2/wizard_mode.png]]

[[/img/doxygen-graphviz-Manual-2/wizard_output.png]]

[[/img/doxygen-graphviz-Manual-2/wizard_diagrams.png]]

[[/img/doxygen-graphviz-Manual-2/expert_build.png]]

[[/img/doxygen-graphviz-Manual-2/expert_dot_1.png]]

[[/img/doxygen-graphviz-Manual-2/expert_dot_2.png]]

由于使用到了Graphviz，所以要设置Dot选项，勾选HAVE_DOT，并设置DOT_PATH为Graphviz的bin目录。(注意：MAC的Graphviz的bin目录不在安装包内，一般是在/usr/local/bin/,实在找不到就到终端用ls一层一层的查找)

[[/img/doxygen-graphviz-Manual-2/run.png]]

另外，若Doxygen出现中文乱码问题：

设置如下：

Expert选项卡-> Project:

DOXYFILE_ENCODING:UTF-8

OUTPUT_LANGUAGE:Chinese

Expert选项卡-> InPut:

INPUT_ENCODING:GB2312

这样生就可以正确生成含有中文的文档了。

## References
1. [用doxygen+graphviz生成函数调用流程图](http://www.jianshu.com/p/fe4b6b95dca5)