## 使用步骤

[[/img/doxygen-graphviz-Manual-1/wizard_project.png]]
![](img/doxygen-graphviz-Manual-1/wizard_project.png?raw=true)

[[/img/doxygen-graphviz-Manual-1/wizard_mode.png]]

[[/img/doxygen-graphviz-Manual-1/wizard_output.png]]

[[/img/doxygen-graphviz-Manual-1/wizard_diagrams.png]]

[[/img/doxygen-graphviz-Manual-1/expert_project.png]]

[[/img/doxygen-graphviz-Manual-1/expert_build.jpg]]

[[/img/doxygen-graphviz-Manual-1/expert_dot.png]]

## 配置选项

### Expert(Project)

**TAB_SIZE** 主要是帮助文件中代码的缩进尺寸，譬如@code和@endcode段中代码的排版，建议符合习惯，设置成4。

**OPTIMIZE_OUTPUT_FOR_C** 这个选项选择后，生成文档的一些描述性名称会发生变化，主要是符合C习惯。如果是纯C代码，建议选择。

**SUBGROUPING** 这个选项选择后，输出将会按类型分组。

### Expert(Build)

**EXTRACT_ALL** 表示输出所有的函数，但是private和static函数不属于其管制。

**EXTRACT_PRIVATE** 表示输出private函数。

**EXTRACT_STATIC** 表示输出static函数。同时还有几个EXTRACT，相应查看文档即可。

**HIDE_UNDOC_MEMBERS** 表示那些没有使用doxygen格式描述的文档（函数或类等）就不显示了。当然，如果EXTRACT_ALL被启用，那么这个标志其实是被忽略的。

**INTERNAL_DOCS** 主要指是否输出注解中的@internal部分。如果没有被启动，那么注解中所有的@internal部分都将在目标帮助中不可见。

**CASE_SENSE_NAMES** 是否关注大小写名称，注意，如果开启了，那么所有的名称都将被小写。对于C/C++这种字母相关的语言来说，建议永远不要开启。

**HIDE_SCOPE_NAMES** 域隐藏，建议永远不要开启。

**SHOW_INCLUDE_FILES** 是否显示包含文件，如果开启，帮助中会专门生成一个页面，里面包含所有包含文件的列表。

**INLINE_INFO** 如果开启，那么在帮助文档中，inline函数前面会有一个inline修饰词来标明。

**SORT_MEMBER_DOCS** 如果开启，那么在帮助文档列表显示的时候，函数名称会排序，否则按照解释的顺序显示。

**GENERATE_TODOLIST** 是否生成TODOLIST页面，如果开启，那么包含在@todo注解中的内容将会单独生成并显示在一个页面中，其他的GENERATE选项同。

**SHOW_USED_FILES** 是否在函数或类等的帮助中，最下面显示函数或类的来源文件。

**SHOW_FILES** 是否显示文件列表页面，如果开启，那么帮助中会存在一个一个文件列表索引页面。

### Expert(Messages)

**QUIET** 如果开启，那么表示关闭编译时的输出信息。

**WARN_FORMAT** 表示日志输出的格式，没必要修改。

**WARN_LOGFILE** 表示信息是否输出到LOG文件，因为有DoxyWizard的存在，所以这个选项没有必要使用。

### Expert(HTML)

**CHM_FILE** 表示输出的chm文件路径

**GENERATE_CHI** 表示索引文件是否单独输出，建议关闭。否则每次生成两个文件，比较麻烦。  
           
**TOC_EXPAND** 表示是否在索引中列举成员名称以及分组（譬如函数，枚举）名称。

## References
1. [用doxygen+graphviz自动化生成代码文档（附详细教程）](http://www.cnblogs.com/tianzhijiexian/p/4392924.html)
2. [doxygen规范与配置选项](http://blog.chinaunix.net/uid-23670869-id-2948890.html)
