<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. 有三种方式可以加载文件：</a></li>
<li><a href="#sec-2">2. 使用eval-after-load可以推迟一段代码的执行</a></li>
<li><a href="#sec-3">3. emacs中的变量作用域</a>
<ul>
<li><a href="#sec-3-1">3.1. buffer-local变量</a>
<ul>
<li><a href="#sec-3-1-1">3.1.1. 声明buffer-local变量</a></li>
<li><a href="#sec-3-1-2">3.1.2. buffer相关函数</a></li>
<li><a href="#sec-3-1-3">3.1.3. 文件中的本地变量列表</a></li>
</ul>
</li>
<li><a href="#sec-3-2">3.2. 变量本地化</a></li>
</ul>
</li>
<li><a href="#sec-4">4. elisp中的数据类型</a>
<ul>
<li><a href="#sec-4-1">4.1. Number</a>
<ul>
<li><a href="#sec-4-1-1">4.1.1. Integer</a></li>
<li><a href="#sec-4-1-2">4.1.2. Float</a></li>
</ul>
</li>
<li><a href="#sec-4-2">4.2. Sequence</a>
<ul>
<li><a href="#sec-4-2-1">4.2.1. Array</a></li>
<li><a href="#sec-4-2-2">4.2.2. List</a></li>
</ul>
</li>
<li><a href="#sec-4-3">4.3. hashtable</a></li>
<li><a href="#sec-4-4">4.4. symbol</a>
<ul>
<li><a href="#sec-4-4-1">4.4.1. 符号的组成</a></li>
<li><a href="#sec-4-4-2">4.4.2. 符号的形成</a></li>
</ul>
</li>
<li><a href="#sec-4-5">4.5. Char</a>
<ul>
<li><a href="#sec-4-5-1">4.5.1. Control characters</a></li>
<li><a href="#sec-4-5-2">4.5.2. Meta Character</a></li>
<li><a href="#sec-4-5-3">4.5.3. Shift Character</a></li>
<li><a href="#sec-4-5-4">4.5.4. Alt Character</a></li>
<li><a href="#sec-4-5-5">4.5.5. Hyper Character</a></li>
<li><a href="#sec-4-5-6">4.5.6. Super Character</a></li>
</ul>
</li>
<li><a href="#sec-4-6">4.6. 其他类型</a></li>
<li><a href="#sec-4-7">4.7. 循环结构</a></li>
<li><a href="#sec-4-8">4.8. 数据类型之间的转换</a></li>
</ul>
</li>
<li><a href="#sec-5">5. elisp中的等于</a>
<ul>
<li><a href="#sec-5-1">5.1. eq</a></li>
<li><a href="#sec-5-2">5.2. equal</a></li>
<li><a href="#sec-5-3">5.3. =</a></li>
<li><a href="#sec-5-4">5.4. /=</a></li>
<li><a href="#sec-5-5">5.5. eql</a></li>
<li><a href="#sec-5-6">5.6. char-equal</a></li>
<li><a href="#sec-5-7">5.7. string=</a></li>
<li><a href="#sec-5-8">5.8. string-equal</a></li>
<li><a href="#sec-5-9">5.9. equal-includeing-properties</a></li>
</ul>
</li>
<li><a href="#sec-6">6. 变量名命名习惯</a></li>
<li><a href="#sec-7">7. 获取参数的几种方法</a>
<ul>
<li><a href="#sec-7-1">7.1. 变量`argv`获取command-line 参数</a></li>
<li><a href="#sec-7-2">7.2. 变量`current-prefix-arg`获取universal-argument</a></li>
<li><a href="#sec-7-3">7.3. interactive</a></li>
</ul>
</li>
<li><a href="#sec-8">8. 光标位置</a>
<ul>
<li><a href="#sec-8-1">8.1. 函数</a></li>
</ul>
</li>
<li><a href="#sec-9">9. 光标移动</a>
<ul>
<li><a href="#sec-9-1">9.1. 函数</a></li>
</ul>
</li>
<li><a href="#sec-10">10. 控制结构</a>
<ul>
<li><a href="#sec-10-1">10.1. 顺序结构</a></li>
<li><a href="#sec-10-2">10.2. 条件表达式</a></li>
<li><a href="#sec-10-3">10.3. 组合条件</a></li>
<li><a href="#sec-10-4">10.4. 循环</a></li>
<li><a href="#sec-10-5">10.5. 使用catch/throw模拟goto语句</a></li>
</ul>
</li>
<li><a href="#sec-11">11. Elisp中的异常机制</a>
<ul>
<li><a href="#sec-11-1">11.1. 使用singal/error/condition-case模拟try catch语句</a>
<ul>
<li><a href="#sec-11-1-1">11.1.1. error类型</a></li>
<li><a href="#sec-11-1-2">11.1.2. 抛出error</a></li>
<li><a href="#sec-11-1-3">11.1.3. 处理Error</a></li>
</ul>
</li>
<li><a href="#sec-11-2">11.2. 使用unwind-protect模拟finally语句</a></li>
</ul>
</li>
<li><a href="#sec-12">12. Elisp中的变量</a>
<ul>
<li><a href="#sec-12-1">12.1. 全局变量</a></li>
<li><a href="#sec-12-2">12.2. 常量</a></li>
<li><a href="#sec-12-3">12.3. 局部变量</a></li>
<li><a href="#sec-12-4">12.4. Buffer-Local变量</a></li>
<li><a href="#sec-12-5">12.5. File-Local变量</a></li>
<li><a href="#sec-12-6">12.6. Directory-Local变量</a>
<ul>
<li><a href="#sec-12-6-1">12.6.1. 相关函数</a></li>
</ul>
</li>
<li><a href="#sec-12-7">12.7. Terminal-Lock变量</a></li>
<li><a href="#sec-12-8">12.8. 空变量</a></li>
<li><a href="#sec-12-9">12.9. 变量别名</a></li>
<li><a href="#sec-12-10">12.10. 废弃变量</a></li>
<li><a href="#sec-12-11">12.11. 受限的变量</a></li>
<li><a href="#sec-12-12">12.12. 变量的作用域</a>
<ul>
<li><a href="#sec-12-12-1">12.12.1. 动态作用域</a></li>
<li><a href="#sec-12-12-2">12.12.2. 静态作用域</a></li>
</ul>
</li>
<li><a href="#sec-12-13">12.13. 泛化变量(Generalized Variables)</a></li>
<li><a href="#sec-12-14">12.14. 取变量值</a></li>
</ul>
</li>
<li><a href="#sec-13">13. Customization</a>
<ul>
<li><a href="#sec-13-1">13.1. Common Item Keywords</a></li>
<li><a href="#sec-13-2">13.2. customization groups</a></li>
<li><a href="#sec-13-3">13.3. customizable variable</a>
<ul>
<li><a href="#sec-13-3-1">13.3.1. Customization Type</a></li>
</ul>
</li>
<li><a href="#sec-13-4">13.4. customizable face</a></li>
</ul>
</li>
<li><a href="#sec-14">14. Loading</a>
<ul>
<li><a href="#sec-14-1">14.1. Load命令</a></li>
<li><a href="#sec-14-2">14.2. Autoload</a></li>
<li><a href="#sec-14-3">14.3. Features</a></li>
<li><a href="#sec-14-4">14.4. 查找定义所在的文件</a></li>
<li><a href="#sec-14-5">14.5. Unloading</a></li>
<li><a href="#sec-14-6">14.6. Hooks</a></li>
</ul>
</li>
<li><a href="#sec-15">15. Byte Compilation</a>
<ul>
<li><a href="#sec-15-1">15.1. 相关函数</a></li>
<li><a href="#sec-15-2">15.2. 编译期执行语句</a></li>
<li><a href="#sec-15-3">15.3. Compiler Errors</a></li>
<li><a href="#sec-15-4">15.4. Disassembly</a></li>
</ul>
</li>
<li><a href="#sec-16">16. Reading and Printing Lisp Objects</a>
<ul>
<li><a href="#sec-16-1">16.1. Input Stream</a>
<ul>
<li><a href="#sec-16-1-1">16.1.1. Input Functions</a></li>
</ul>
</li>
<li><a href="#sec-16-2">16.2. Output Stream</a>
<ul>
<li><a href="#sec-16-2-1">16.2.1. Output Functions</a></li>
<li><a href="#sec-16-2-2">16.2.2. Output Variables</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#sec-17">17. Documentation</a>
<ul>
<li><a href="#sec-17-1">17.1. 获取doc-string</a></li>
<li><a href="#sec-17-2">17.2. 替换doc-string中的key binding</a></li>
<li><a href="#sec-17-3">17.3. 将键序列输出为文本格式</a></li>
</ul>
</li>
<li><a href="#sec-18">18. Elisp中的函数</a>
<ul>
<li><a href="#sec-18-1">18.1. Elisp中函数的分类</a></li>
<li><a href="#sec-18-2">18.2. 获取函数信息</a></li>
<li><a href="#sec-18-3">18.3. 匿名函数</a>
<ul>
<li><a href="#sec-18-3-1">18.3.1. 获取匿名函数</a></li>
<li><a href="#sec-18-3-2">18.3.2. 参数列表</a></li>
<li><a href="#sec-18-3-3">18.3.3. 函数描述字符串(docstring)</a></li>
<li><a href="#sec-18-3-4">18.3.4. 交互模式声明</a></li>
</ul>
</li>
<li><a href="#sec-18-4">18.4. 命名函数</a>
<ul>
<li><a href="#sec-18-4-1">18.4.1. declare form</a></li>
</ul>
</li>
<li><a href="#sec-18-5">18.5. 调用函数</a></li>
<li><a href="#sec-18-6">18.6. 废弃函数</a></li>
<li><a href="#sec-18-7">18.7. 内联函数</a></li>
<li><a href="#sec-18-8">18.8. 函数声明</a></li>
<li><a href="#sec-18-9">18.9. 判断function是否安全</a></li>
</ul>
</li>
<li><a href="#sec-19">19. Advising Emacs Lisp Functions</a>
<ul>
<li><a href="#sec-19-1">19.1. Core Advising Primitives</a></li>
<li><a href="#sec-19-2">19.2. Advising Named Functions</a></li>
</ul>
</li>
<li><a href="#sec-20">20. 宏</a>
<ul>
<li><a href="#sec-20-1">20.1. 宏与函数的不同</a></li>
<li><a href="#sec-20-2">20.2. 定义宏</a></li>
<li><a href="#sec-20-3">20.3. 宏扩展</a></li>
</ul>
</li>
<li><a href="#sec-21">21. 调试ELisp程序</a>
<ul>
<li><a href="#sec-21-1">21.1. debugger</a>
<ul>
<li><a href="#sec-21-1-1">21.1.1. 配置何时进入debugger</a></li>
<li><a href="#sec-21-1-2">21.1.2. debugger使用说明</a></li>
<li><a href="#sec-21-1-3">21.1.3. debugger内部实现使用到的变量与函数</a></li>
</ul>
</li>
<li><a href="#sec-21-2">21.2. edebug</a>
<ul>
<li><a href="#sec-21-2-1">21.2.1. 使用Edebug的一般步骤</a></li>
<li><a href="#sec-21-2-2">21.2.2. Edebug中的命令</a></li>
<li><a href="#sec-21-2-3">21.2.3. Edebug中的输出格式</a></li>
<li><a href="#sec-21-2-4">21.2.4. Trace Buffer</a></li>
</ul>
</li>
<li><a href="#sec-21-3">21.3. test coverage</a>
<ul>
<li><a href="#sec-21-3-1">21.3.1. 使用步骤</a></li>
<li><a href="#sec-21-3-2">21.3.2. 高亮说明</a></li>
<li><a href="#sec-21-3-3">21.3.3. give advice to the test coverage too</a></li>
</ul>
</li>
<li><a href="#sec-21-4">21.4. Profiling</a></li>
</ul>
</li>
<li><a href="#sec-22">22. Command Loop</a>
<ul>
<li><a href="#sec-22-1">22.1. Command Loop概述</a></li>
<li><a href="#sec-22-2">22.2. Command</a></li>
<li><a href="#sec-22-3">22.3. Disabling Commands</a></li>
<li><a href="#sec-22-4">22.4. Command History</a></li>
<li><a href="#sec-22-5">22.5. 如何分辨Command是否通过Interactive方式调用</a></li>
<li><a href="#sec-22-6">22.6. generic command</a></li>
<li><a href="#sec-22-7">22.7. 获取Command Loop中的信息</a></li>
<li><a href="#sec-22-8">22.8. Command的prefix argument</a></li>
<li><a href="#sec-22-9">22.9. Quitting</a></li>
<li><a href="#sec-22-10">22.10. Keyboard Macro</a></li>
</ul>
</li>
<li><a href="#sec-23">23. InputEvent</a>
<ul>
<li><a href="#sec-23-1">23.1. Keyboard Event</a>
<ul>
<li><a href="#sec-23-1-1">23.1.1. 普通按键事件</a></li>
<li><a href="#sec-23-1-2">23.1.2. 功能键事件</a></li>
<li><a href="#sec-23-1-3">23.1.3. 以字符串表示keyboard event</a></li>
</ul>
</li>
<li><a href="#sec-23-2">23.2. Mouse Events</a>
<ul>
<li><a href="#sec-23-2-1">23.2.1. 点击事件</a></li>
<li><a href="#sec-23-2-2">23.2.2. 拖拽事件</a></li>
<li><a href="#sec-23-2-3">23.2.3. Button-Down事件</a></li>
<li><a href="#sec-23-2-4">23.2.4. Repeat Event</a></li>
<li><a href="#sec-23-2-5">23.2.5. Motion Events</a></li>
<li><a href="#sec-23-2-6">23.2.6. Focus Events</a></li>
<li><a href="#sec-23-2-7">23.2.7. 其他System Event</a></li>
</ul>
</li>
<li><a href="#sec-23-3">23.3. 特殊Events</a></li>
<li><a href="#sec-23-4">23.4. 区分Events</a></li>
<li><a href="#sec-23-5">23.5. 获取Mouse Events中的信息</a></li>
<li><a href="#sec-23-6">23.6. 获取scroll bar event中的信息</a></li>
<li><a href="#sec-23-7">23.7. 捕获Input Event</a></li>
<li><a href="#sec-23-8">23.8. Modifying and Translating Input Events</a></li>
<li><a href="#sec-23-9">23.9. Event Input的其他特性</a></li>
</ul>
</li>
<li><a href="#sec-24">24. 关于输入法</a></li>
<li><a href="#sec-25">25. Keymaps</a>
<ul>
<li><a href="#sec-25-1">25.1. Key Sequences</a></li>
</ul>
</li>
<li><a href="#sec-26">26. Number相关函数</a></li>
<li><a href="#sec-27">27. 二进制函数</a></li>
<li><a href="#sec-28">28. 字符串处理相关函数</a>
<ul>
<li><a href="#sec-28-1">28.1. 判断函数</a></li>
<li><a href="#sec-28-2">28.2. 获取字符串的函数</a></li>
<li><a href="#sec-28-3">28.3. 字符串操作</a></li>
<li><a href="#sec-28-4">28.4. Format函数</a></li>
</ul>
</li>
<li><a href="#sec-29">29. list相关函数</a>
<ul>
<li><a href="#sec-29-1">29.1. 判断函数</a></li>
<li><a href="#sec-29-2">29.2. 获取list中的元素</a></li>
<li><a href="#sec-29-3">29.3. 创建cons cell和list</a></li>
<li><a href="#sec-29-4">29.4. 修改list变量</a>
<ul>
<li><a href="#sec-29-4-1">29.4.1. 会破坏原参数中的值</a></li>
<li><a href="#sec-29-4-2">29.4.2. 不破坏原参数的值</a></li>
</ul>
</li>
<li><a href="#sec-29-5">29.5. alist相关函数</a>
<ul>
<li><a href="#sec-29-5-1">29.5.1. 获取alist</a></li>
<li><a href="#sec-29-5-2">29.5.2. 根据key取key-value键值对</a></li>
<li><a href="#sec-29-5-3">29.5.3. 根据value查找key-value键值对</a></li>
<li><a href="#sec-29-5-4">29.5.4. 更新新值/添加新值</a></li>
<li><a href="#sec-29-5-5">29.5.5. 删除键值对</a></li>
</ul>
</li>
<li><a href="#sec-29-6">29.6. Property list相关函数</a></li>
</ul>
</li>
<li><a href="#sec-30">30. 环状结构体相关函数</a></li>
<li><a href="#sec-31">31. Sequences相关函数</a>
<ul>
<li><a href="#sec-31-1">31.1. Array相关函数</a>
<ul>
<li><a href="#sec-31-1-1">31.1.1. Vector相关函数</a></li>
<li><a href="#sec-31-1-2">31.1.2. Char-Table相关函数</a></li>
<li><a href="#sec-31-1-3">31.1.3. Bool-vector相关函数</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#sec-32">32. HashTable相关函数</a>
<ul>
<li><a href="#sec-32-1">32.1. 判断函数</a></li>
<li><a href="#sec-32-2">32.2. 创建hash-table</a></li>
<li><a href="#sec-32-3">32.3. 添加item / 修改item的值</a></li>
<li><a href="#sec-32-4">32.4. 删除item</a></li>
<li><a href="#sec-32-5">32.5. 获取某item的值</a></li>
<li><a href="#sec-32-6">32.6. 获取hash中的属性</a></li>
<li><a href="#sec-32-7">32.7. 为hash-map中的所有键值对调用函数处理</a></li>
<li><a href="#sec-32-8">32.8. 获取hash-map中的所有key值 / value值</a></li>
<li><a href="#sec-32-9">32.9. 修改Hash-table的比较方法</a></li>
</ul>
</li>
<li><a href="#sec-33">33. Symbol相关函数</a>
<ul>
<li><a href="#sec-33-1">33.1. symbol组成部分</a></li>
<li><a href="#sec-33-2">33.2. 获取symbol</a></li>
<li><a href="#sec-33-3">33.3. 其他函数</a></li>
<li><a href="#sec-33-4">33.4. symbol中的property</a></li>
<li><a href="#sec-33-5">33.5. 标准symbol property说明</a></li>
</ul>
</li>
<li><a href="#sec-34">34. Region/Mark相关函数</a></li>
<li><a href="#sec-35">35. Evaluation</a>
<ul>
<li><a href="#sec-35-1">35.1. `(反引号)</a></li>
<li><a href="#sec-35-2">35.2. 函数</a></li>
<li><a href="#sec-35-3">35.3. 选项</a></li>
</ul>
</li>
<li><a href="#sec-36">36. 缓冲区</a>
<ul>
<li><a href="#sec-36-1">36.1. 获取buffer对象</a></li>
<li><a href="#sec-36-2">36.2. buffer操作</a></li>
<li><a href="#sec-36-3">36.3. 获取缓冲区内容</a></li>
<li><a href="#sec-36-4">36.4. buffer内容处理相关函数</a>
<ul>
<li><a href="#sec-36-4-1">36.4.1. 删除操作</a></li>
<li><a href="#sec-36-4-2">36.4.2. 插入操作</a></li>
<li><a href="#sec-36-4-3">36.4.3. 查找/替换操作</a></li>
</ul>
</li>
<li><a href="#sec-36-5">36.5. 保存现场</a></li>
</ul>
</li>
<li><a href="#sec-37">37. 窗口</a>
<ul>
<li><a href="#sec-37-1">37.1. 获得窗口对象</a></li>
<li><a href="#sec-37-2">37.2. 窗口操作</a></li>
<li><a href="#sec-37-3">37.3. 窗口信息</a></li>
</ul>
</li>
<li><a href="#sec-38">38. 文件</a>
<ul>
<li><a href="#sec-38-1">38.1. 文件读写</a></li>
<li><a href="#sec-38-2">38.2. 文件信息</a></li>
<li><a href="#sec-38-3">38.3. 文件名相关函数</a></li>
<li><a href="#sec-38-4">38.4. 文件操作</a></li>
<li><a href="#sec-38-5">38.5. 临时文件</a></li>
<li><a href="#sec-38-6">38.6. 神奇的handler</a></li>
</ul>
</li>
<li><a href="#sec-39">39. Dired-mode相关函数</a></li>
<li><a href="#sec-40">40. 执行命令</a></li>
<li><a href="#sec-41">41. Register函数</a></li>
<li><a href="#sec-42">42. Org相关函数</a>
<ul>
<li><a href="#sec-42-1">42.1. 取entry属性</a></li>
<li><a href="#sec-42-2">42.2. 取entry的tag list</a></li>
<li><a href="#sec-42-3">42.3. 取entry的TODO state</a></li>
<li><a href="#sec-42-4">42.4. 判断哪些state是完成状态</a></li>
</ul>
</li>
<li><a href="#sec-43">43. 版本信息</a></li>
<li><a href="#sec-44">44. wait function</a></li>
</ul>
</div>
</div>

# 有三种方式可以加载文件：<a id="sec-1" name="sec-1"></a>

-   load
-   autoload
-   require

# 使用eval-after-load可以推迟一段代码的执行<a id="sec-2" name="sec-2"></a>

(eval-after-load "触发条件的文件" 待执行的代码)
这里，第一个参数的值必须跟上面三种方式加载文件时的值一模一样

# emacs中的变量作用域<a id="sec-3" name="sec-3"></a>

## buffer-local变量<a id="sec-3-1" name="sec-3-1"></a>

### 声明buffer-local变量<a id="sec-3-1-1" name="sec-3-1-1"></a>

-   make-variable-buffer-local
    各个缓冲区都有各自的buffer-local变量
-   make-local-variable
    当前缓冲区产生一个局部变量,其他缓冲区仍然使用全局变量(推荐使用)

### buffer相关函数<a id="sec-3-1-2" name="sec-3-1-2"></a>

1.  with-current-buffer

        ;使其中的body表达式在指定的缓冲区里执行(使用指定buffer的配置信息执行body表达式)
        (with-current-buffer buffer
        body)

2.  get-buffer

        ;得到缓冲区名字的对应缓冲区对象,如果没有这个名字的缓冲区,返回nil
        (get-buffer buffer-name)

3.  default-value

        ;访问符号的全局变量的值
        (default-value symbol)

4.  setq-default

        ;修改符号作为全局变量的值
        (setq-default symbol-name)

5.  local-variable-p

        ;测试变量是不是buffer-local的
        (local-variable-p symbol [buffer对象])

6.  buffer-local-value

        ;得到其他缓冲区内的buffer-local变量值
        (buffer-local-value 符号 buffer对象)

7.  default-boundp

        ;判断符号是否有全局值
        (default-boundp 符号)

8.  makunbound

        ;使一个变量的值重新为空
        (makunbound 符号)

9.  kill-local-variable

        ;清除一个buffer-local变量
        (kill-local-variable 符号)

10. kill-all-local-variables

        ;清除所有的buffer-local变量,但是带有属性permanent-local的不会清除,带有这些标记的变量一般都是和缓冲区模式无关的
        (kill-all-local-variables)

### 文件中的本地变量列表<a id="sec-3-1-3" name="sec-3-1-3"></a>

-   "本地变量列表"可以位于任何文件的结尾位置,它的形式如下所示
    
        Local variables:
        var1 : value1
        var2 : value2
        ...
        eval : form1
        eval : form2
        ...      
        End:
    
    这里定义的var自动是buffer-local的,类似宏一样,value被认为是被引用的
    这里的form则会自动执行.
-   可以通过在.emacs中加入
    
        (setq enable-local-variables 'query)
    
    来阻止"本地变量列表"生效

## 变量本地化<a id="sec-3-2" name="sec-3-2"></a>

-   普通变量通过make-localvariable或make-variable-buffer-local变为buffer－local的
    -   make-variable-buffer-local使指定的变量在每个buffer中都是独立的
    -   make-local-variable使变量在当前buffer是独立的，而其他buffer依然共享全局变量
-   hook变量智能通过make-local-hook变为buffer-local的

# elisp中的数据类型<a id="sec-4" name="sec-4"></a>

## Number<a id="sec-4-1" name="sec-4-1"></a>

### Integer<a id="sec-4-1-1" name="sec-4-1-1"></a>

根据机器的不同,Integer有不同的区间(分别由变量most-positive-fixnum和most-negative-fixnum来指示). 但elisp规定最少的范围是从-536870912到536870911. 

任何超过Integer范围的值都认为是Float型

默认,Integer用10进制来表示数,但也可以用
-   \#bNNNN表示二进制数
-   \#oNNNN表示八进制数
-   \#xNNNN表示十六进制数
-   \#MrNNNN表示M进制的数

### Float<a id="sec-4-1-2" name="sec-4-1-2"></a>

Elisp中Float的取值范围与C中的double型一样.

Float使用INF表示无穷大. Float还有一个特殊值名为NaN. 当数学函数计算非法表达式时会返回该值. 

    (/ 0 0.0)                               ;-0.0e+NaN
    (/ -0 0.0)                              ;-0.0e+NaN
    (/ 1 0.0)                               ;1.0e+INF
    (/ -1 0.0)                              ;-1.0e+INF

1.  相关函数

    -   判断是否为NAN
        
        (isnan x)
    
    -   (frexp x)
        
        返回一个元组(S . E),使得S\*2<sup>E</sup> == x,S的值在[0.5 1)
    
    -   (ldexp S E)
        
        返回Float值x 使得x == S\*2<sup>E</sup>
    
    -   (copysign x1 x2)
        
        假设x1 `= S1*2^E1, x2 =` S2\*2<sup>E2</sup>,则返回S1\*2<sup>E2的值</sup>
    
    -   (logb x)
        
        返回log2(x)的值,向下取整. 例如(logb 10) => 3

## Sequence<a id="sec-4-2" name="sec-4-2"></a>

-   获取sequence的长度
    
    (length mySequence)
    
    需要注意的是length不能对点列表和环形列表求长度,但是可以用safe-length代替

### Array<a id="sec-4-2-1" name="sec-4-2-1"></a>

除了char-table之外,创建其他类型的Array都需要指定一个固定长度.

char-table的长度是由character code的范围所决定的,不能人工指定

1.  vector

    vecotr是sequence的一个子类型
    -   如何创建一个vector
        -   使用字面量语法:[val1 val2 val3&#x2026;]
        
        -   使用函数(vector val1 val2 val3&#x2026;)
    
    -   获取vector的长度
        
        (length myVector)
    
    -   获取element
        
        (elt mySeq index)    # index从0开始
    
    -   设置element
        
        (aset mySeq index value)
    
    -   将多个Sequence组合成一个vector
        
        (voncat seq1 seq2 &#x2026;)
    
    -   将vector转换成list
        
        (append myVector nil)

2.  bool-vector

    -   bool-vector只能存放nil或t
    -   bool-vector的输出格式与字符串类似,但在前面加上\`#&长度\`作为标识:
        
            #&长度"内容"                            ;这里的长度表示bool-vector的长度,内容的二进制为vector的内容,内容的现实方式为字符串
            (make-bool-vector 3 t)                  ; => #&3"^G" ?\C-g == 7
            (make-bool-vector 3 nil)                ; => #&3"^@" ?\C-@ == 0
            (equal #&3"\377" #&3"\007")             ; => t

3.  char-tables

    -   类似vector,但它使用Character作为索引.
    -   char-tables的输出格式与vector类似,但前面加上\`#<sup>\`作为标示</sup>
    -   每个char-table对象都有一个symbol类型的"subtype",可以用于标识char-table的用处, 使用函数char-table-subtyple来查询该subtype
    -   char-table的subtype中的属性\`char-table-extra-slots\`决定了该char-table的扩展slot的个数(0-10之间)
    -   每个char-table都可以有一个父char-table,子char-table从父char-table中继承索引的值.
    -   char-table还能够设定一个默认值.若发现char-table指定index的值为nil,则返回该默认值.

4.  string

    -   elisp中的string是不可变的.
    -   string中不能包含?\H-N ?\A-N ?\s-N 这些字符
    -   string中可以包含文本属性,包含文本属性的输出格式为:
        
            #("characters" property-data...)
    -   Emacs中,对字符串作比较的函数只有string=,string<函数,没有string>函数

### List<a id="sec-4-2-2" name="sec-4-2-2"></a>

list是sequence的一个子类型
-   创建一个list
    -   使用list函数:(list v1 v2&#x2026;)
    
    -   使用字面表达式'(v1 v2&#x2026;)

-   获取element
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="left">Function</th>
    <th scope="col" class="left">Purpose</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="left">(car ℓ)</td>
    <td class="left">first element</td>
    </tr>
    
    
    <tr>
    <td class="left">(nth n ℓ)</td>
    <td class="left">nth element (start from 0)</td>
    </tr>
    
    
    <tr>
    <td class="left">(car (last ℓ))</td>
    <td class="left">last element</td>
    </tr>
    
    
    <tr>
    <td class="left">(cdr ℓ)</td>
    <td class="left">2nd to last elements</td>
    </tr>
    
    
    <tr>
    <td class="left">(nthcdr n ℓ)</td>
    <td class="left">nth to last elements</td>
    </tr>
    
    
    <tr>
    <td class="left">(butlast ℓ n)</td>
    <td class="left">without the last n elements</td>
    </tr>
    </tbody>
    </table>

-   获取list的长度
    
    (length mySeq)

-   在list头添加element
    
    (cons x myList)

-   合并两个list
    
    (append list1 list2)
    
    由此可以得出,在list尾部添加element的方法为
    
    (append myList (list myVal))

-   修改list的函数
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <tbody>
    <tr>
    <td class="left">Function</td>
    <td class="left">Purpose</td>
    </tr>
    
    
    <tr>
    <td class="left">(pop ℓ)</td>
    <td class="left">Remove first element from the variable. Returns the removed element.</td>
    </tr>
    
    
    <tr>
    <td class="left">(nbutlast ℓ n)</td>
    <td class="left">Remove last n elements from the variable. Returns the new value of the variable.</td>
    </tr>
    
    
    <tr>
    <td class="left">(setcar ℓ x)</td>
    <td class="left">replaces the first element in ℓ with x. Returns x.</td>
    </tr>
    
    
    <tr>
    <td class="left">(setcdr ℓ x)</td>
    <td class="left">replaces the rest of elements in ℓ with x. Returns x.</td>
    </tr>
    </tbody>
    </table>

1.  association list / alist

    alist中的item是顺序的,且可以有重复键值
    
    在elisp中,alist中可以存在某些element不是cons cell的情况,alist查询函数会自动略过这些异常的element
    association list类似于C语言中的map,它的结构为
    
        (defvar *alist-example* '((key1 value1)
                                        (key2 value2)))

2.  Property list / plist

    plist的作用类似alist,也是用list表示一组键值对.
    
    plist的key为symbol,它的结构为
    
        (key1 value1 key2 (value2) key3 "value3") ;=>键值对的对应关系为key1->value1;key2->'(value2);key3->"value3"
    
    每一个symbol都可以attach一个plist
    
    需要注意的是,plist中的 **key必须是唯一的** ,相比来说alist就没有这个限制了.

## hashtable<a id="sec-4-3" name="sec-4-3"></a>

hash table类似alist一样提供了键值配对的功能. 但比起alist来说,有如下三个方面的不同

-   在搜索大量的键值对集合时,使用hash table的搜索速度比alist快得多
-   hash table中的的item是非排序的,不能有重复键值
-   两个hash table对象无法共享同一个结构体,而两个alist对象之间有可能使用共同的tail

hash table的输出格式以#s开头后接hash table的属性和内容

    #s(hash-table size 65 test eql rehash-size 1.5 rehash-threshold 0.8 data
                  ())

## symbol<a id="sec-4-4" name="sec-4-4"></a>

-   Lisp中symbol类似于其他语言中的变量,但是它不仅仅只存储一个值.
-   列表的第一个表达式如果是一个符号,解释器会查找这个表达式的函数值.如果函数值是另一个符号,则会继续查找这个符号的函数值
-   symbol中,\\失去了转义的功能,因此'\\t就是't而不时'<TAB>
-   一个符号既可以有value,也可以有function,即一个symbol可以同时求值和当作函数用

### 符号的组成<a id="sec-4-4-1" name="sec-4-4-1"></a>

-   符号名称:使用函数symbol-name获取

-   符号值: 使用函数symbol-value获取
    -   使用boundp测试符号是否有值
    -   以\`:\`开头的符号的值不能变

-   函数:  使用symobl-function获取
    -   使用fboundp测试符号是否设置了函数
    -   其实function slot不仅仅可以存放function,还可以存放macro,symbol,keyboard marcro,keympa和autoload object

-   属性列表:使用symbol-plist获取
    -   使用get/put来访问/修改某个属性值
    -   使用plist-get/plist-put来访问/设置属性列表中的属性
    -   属性列表是一个形如(prop1 value1 prop2 value2)的关联列表,但无法删除一个属性
    -   可用使用属性列表来存储function的状态

### 符号的形成<a id="sec-4-4-2" name="sec-4-4-2"></a>

当elisp读取到一个symbol时,它会先在一个名为\`obarray\`的vector中检查是否已经存在这个symbol, 若不存在,则elisp reader创建新的symbol并添加到obarray中(创建并添加symbol的过程被成为"interning",而该symbol被成为是"interned symbol").

如果想避免intern一个symbol,可以在符号名前加上\`#::\`,这些符号被称为\`uninterned symbols\`

    (intern-soft "abc") ; => nil
    'abc ; => abc
    (intern-soft "abc") ; => abc
    (intern-soft "abcd") ; => nil
    '#:abcd ; => abcd
    (intern-soft "abcd") ; => nil

obarray也是一种类型名称

由于在elisp中,obarray就是一个vector,因此可以使用(make-vecotr LENGTH 0)来创建一个空的obarray, 而要把symbol插入一个obarray,则必须使用如下的intern系列函数来进行.
-   intern
-   intern-soft
-   unintern
-   mapatoms

## Char<a id="sec-4-5" name="sec-4-5"></a>

类似C,Elisp中的Char其实就是integer(值从0到(max-char)的范围都可以认为是character). Char类型的字面量结构为\`?字母\`,例如

    (message "%d" ?A)      ;65
    (message "%d" ?\.)     ;46 标点一般在前面加\
    (message "%d" ?我)     ;25105
    
    ?\a ;=> 7                 ; control-g, `C-g'
    ?\b ;=> 8                 ; backspace, <BS>, `C-h'
    ?\t ;=> 9                 ; tab, <TAB>, `C-i'
    ?\n ;=> 10                ; newline, `C-j'
    ?\v ;=> 11                ; vertical tab, `C-k'
    ?\f ;=> 12                ; formfeed character, `C-l'
    ?\r ;=> 13                ; carriage return, <RET>, `C-m'
    ?\e ;=> 27                ; escape character, <ESC>, `C-['
    ?\s ;=> 32                ; space character, <SPC>
    ?\\ ;=> 92                ; backslash character, `\'
    ?\d ;=> 127               ; delete character, <DEL>
    ?\uNNNN                                 ;这里N为16进制数,表示U+NNNN的Unicode字符
    ?\U00NNNNNN                             ;
    
    ?\x十六进制代码            ; ?\x41 = \?A
    ?\三个八进制代码           ; ?\001 = `C-a`

-   没有charp,因为字符就是整数,但是有char-or-string-p函数
-   使用char-equal比较字符时,需要注意case-fold-search变量的值,t表示忽略大小写

### Control characters<a id="sec-4-5-1" name="sec-4-5-1"></a>

Ctrl-N的字面表达式为\`?\\<sup>字母\`</sup>(这里的字母不区分大小写)

    ?\^I ; == ?\^i  == C-i == 9

还可以表示为\`?\C-字母\`

    ?\C-g                                   ;== ?\^g == C-g

需要注意的是,?\C-G不时?\C-S-g的意思,它跟?\C-g的意义一样
由于历史的原因,Emacs把<DEL>看成是C-?

### Meta Character<a id="sec-4-5-2" name="sec-4-5-2"></a>

M-N的字面表示方式为\`?\M-字母\`

### Shift Character<a id="sec-4-5-3" name="sec-4-5-3"></a>

?&sect;-N

### Alt Character<a id="sec-4-5-4" name="sec-4-5-4"></a>

?\A-N

### Hyper Character<a id="sec-4-5-5" name="sec-4-5-5"></a>

?\H-N

### Super Character<a id="sec-4-5-6" name="sec-4-5-6"></a>

?\s-N

## 其他类型<a id="sec-4-6" name="sec-4-6"></a>

-   Buffer
-   Marker
-   Window
-   Frame
-   Terminal
-   Window Configuration
-   Frame Configuration
-   Process
-   Stream
    -   nil指\`standard-input\`和\`standard-output\`
    -   t指代\`从minibuffer输入\`或输出到\`echo area\`
-   Keymap
-   Overlay
    Overlay用来給buffer的一部分内容加上不同的显示风格
-   Font

## 循环结构<a id="sec-4-7" name="sec-4-7"></a>

需要使用\`#N=\`和\`#N#\`来定义循环点和引用循环点,这里N为数字

    '(#1=(a) b #1#)
    #1='(a #1#)

## 数据类型之间的转换<a id="sec-4-8" name="sec-4-8"></a>

-   number-to-string / string-to-number
-   concat可以将序列转换成字符串
    
        (concat '(?a ?b ?c ?d ?e)) ; => "abcde"
        (concat [?a ?b ?c ?d ?e]) ; => "abcde"
-   vconcat可以把字符串转换成向量
    
        (vconcat "abdef") ; => [97 98 100 101 102]
-   append可以把字符串转换成一个列表
    
        (append "abcdef" nil) ; => (97 98 99 100 101 102)
-   (byte-to-string BYTE)
-   大小写转换
    
    elisp通过case table来确定大小写的对应关系,每个buffer都可以设置自己的case table.
    
    -   (downcase string-or-char)
    
    -   (upcase string-or-char)
    
    -   (capitalize string-or-char)
        
        string中的所有单词都被格式化为capitalize的格式
        
        若参数为char类型,则效果跟upcase一样
    
    -   (upcase-initials string-or-char)
        
        对string中的每个单词的第一个字母转化了大写字母,其他字母不变.

-   转换数字为Float型
    
    (float number)

-   转换数字为Integer型
    
    有8个函数可以用来转换Float到Integer型. 有些函数都带有一个可选参数DIVISOR, 若传入了DIVISOR则返回NUMBER/DIVISOR的整数化的值. 若DIVISOR为0,则Elisp报arith-error
    
    (truncate number &optional divisor) / (ftruncate float)
    
    截断小数位
    
    (floor number &optional divisor) / (ffloor float)
    
    截断成一个更小的整数
    
    (ceiling number &optional divisor) / (fceiling float)
    
    截断成一个更大的整数
    
    (round number &optional divisor) / (fround float)
    
    转换成最近的整数,若小数为为0.5,则转换为偶数,例如(round 1.5)=>2 (round 2.5)=>2

-   字符串与数字之间的相互转换
    
    (string-to-number "N" &optional base) 
    
    (number-to-string N)
    
    (format "%d" N)

-   Object转换为String
    
    (format "%s" object)
    
    (prin1-to-string object)

-   String转换为Object
    
    (read-from-string string)

-   symbol转换为string
    
    (symbol-name symbol)

-   string转换为symbol
    
    (intern string)

# elisp中的等于<a id="sec-5" name="sec-5"></a>

## eq<a id="sec-5-1" name="sec-5-1"></a>

eq用于判断两个Object是否为同一个Object

## equal<a id="sec-5-2" name="sec-5-2"></a>

equal用于判断两个Object是否有相同的内部结构(这通常意味着两个Object的类型是一样的,即0 不equal 0.0).

equal在比较两个string时,不会比较他们的属性,需要比较属性的话,使用equal-including-properties来代替

即使两个buffer的内容一样,equal这两个buffer时也不相等

由于equal会对两个Object的各个组成部分递归调用equal,因此在处理循环结构时,可能会陷入死循环.

## =<a id="sec-5-3" name="sec-5-3"></a>

=一般用于数字之间的比较,且0=0.0

## /=<a id="sec-5-4" name="sec-5-4"></a>

数字间的不等于

## eql<a id="sec-5-5" name="sec-5-5"></a>

eql类似eq,但在处理数字是,会同时比较数字的类型和值.因此(eql 1.0 1)=>nil;(eql 1.0 1.0)=>t

## char-equal<a id="sec-5-6" name="sec-5-6"></a>

比较两个character是否相等,默认忽略大小写差异,若变量\`case-fold-search\`nil(默认为t),则比较时区分大小写

    (char-equal ?x ?x)                      ; => t
    (let ((case-fold-search nil))
      (char-equal ?x ?X))                   ; => nil

## string=<a id="sec-5-7" name="sec-5-7"></a>

string=接收string或symbol的参数. 使用string=的时候一定会区分大小写,而跟变量\`case-fold-search\`无关. 而且在比较时,string的text properties不参与比较.

    (string= "abc" 'abc)                    ;=>t

## string-equal<a id="sec-5-8" name="sec-5-8"></a>

string=的别名

## equal-includeing-properties<a id="sec-5-9" name="sec-5-9"></a>

# 变量名命名习惯<a id="sec-6" name="sec-6"></a>

-   -hook 一个在特定情况下调用的函数列表，比如关闭缓冲«时，进入某个模式时。
-   -function值为一个函数
-   -functions 值为一个函数列表
-   -flag 值为nil或non-nil
-   -predicate 值是一个作判断的函数，返回nil或non-nil
-   -program 或-command 一个程序或shell名令名
-   -form 一个表达式
-   -forms 一个表达式列表。
-   -map 一个按键映射（keymap）
-   命名以空格开头的缓冲区是临时的,用户不需要关系的缓冲区

# 获取参数的几种方法<a id="sec-7" name="sec-7"></a>

## 变量\`argv\`获取command-line 参数<a id="sec-7-1" name="sec-7-1"></a>

当使用emacs &#x2013;script xxx.el args时,为了获取command-line参数,可以在xxx.el中使用变量\`argv\`获取参数列表

## 变量\`current-prefix-arg\`获取universal-argument<a id="sec-7-2" name="sec-7-2"></a>

emacs命令可以使用C-u传递universal-argument.

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Key Input</th>
<th scope="col" class="left">Value of current-prefix-arg</th>
</tr>
</thead>

<tbody>
<tr>
<td class="left">No universal arg called.</td>
<td class="left">nil</td>
</tr>


<tr>
<td class="left">【Ctrl+u -】</td>
<td class="left">Symbol -</td>
</tr>


<tr>
<td class="left">【Ctrl+u - 2】</td>
<td class="left">Number -2</td>
</tr>


<tr>
<td class="left">【Ctrl+u 1】</td>
<td class="left">Number 1</td>
</tr>


<tr>
<td class="left">【Ctrl+u 4】</td>
<td class="left">Number 4</td>
</tr>


<tr>
<td class="left">【Ctrl+u】</td>
<td class="left">List '(4)</td>
</tr>


<tr>
<td class="left">【Ctrl+u Ctrl+u】</td>
<td class="left">List '(16)</td>
</tr>
</tbody>
</table>

## interactive<a id="sec-7-3" name="sec-7-3"></a>

-   若interactive的参数以\*开头，则意义是，如果当前buffer是只读的，则不执行该函数
-   interactive可以后接字符串,表示获得参数的方式
    -   p 接收C-u的数字参数
        
        也可以不用P参数,直接在代码中判断current-prefix-arg的值
    -   r region的开始/结束位置
    -   n 提示用户输入数字参数,n后面可用接着提示符
    -   s 提示用户输入字符串参数
    -   若函数接收多个input,需要用\\n来分隔
-   interactive可以后接一个form,form的求值结果应该是一个list,这个list的值作为参数的实参
    
    在form中一般会用到如下几个函数用于获取用户输入
    
    -   read-string
    -   read-file-name
    -   read-directory-name
    -   read-regexp
    -   y-or-n-p
    -   read-from-minibuffer
    -   使用变量\`current-prefix-arg\`来判断是否有universal-argument

# 光标位置<a id="sec-8" name="sec-8"></a>

## 函数<a id="sec-8-1" name="sec-8-1"></a>

-   获取光标当前位置
    
    (point)

-   获取region的开始和结束位置
    
    (region-beginning) / (region-end)

-   当前行的开始/结束位置
    
    (line-beginning-position) / (line-end-position)

-   获取当前buffer的开始/结束位置
    
    (point-min) / (point-max)

-   得到行号
    
    line-number-at-pos

-   测试是否在buffer头/尾
    
    bobp(beginning of buffer predicate)和eobp(end of buffer predicate)

-   测试是否在行首/尾
    
    bolp(beginning of line predicate)和eolp(end of line predicate)

# 光标移动<a id="sec-9" name="sec-9"></a>

## 函数<a id="sec-9-1" name="sec-9-1"></a>

-   按单个字符移动
    
    goto-char /forward-char /backward-char

-   跳转到指定字符串的位置
    
    (search-forward myStr)  ;光标位于myStr的尾部
    
    (search-backward myStr) ;光标位于myStr的头部

-   正则查询
    
    (re-search-forward myRegex) / (search-forward-regexp myRegex)
    
    (re-search-backward myRegex) / (search-backward-regexp myRegex)

-   跳到第一个不是"a"-"z"的位置
    
    (skip-chars-forward "a-z")
    
    (skip-chars-backward "a-z")

-   跳到buffer的开头/末尾
    
    beginning-of-buffer / end-of-buffer

-   按词移动
    
    forward-word /backward-word

-   按行移动
    
    没有backward-line,而且每次移动都是移动到行首的,所以(forward-line 0)可以移动到当前行的行首
    
    (forward-line N) N可以为负数,表示backward-line

-   移动到行首/尾
    
    (beginning-of-line)
    
    (end-of-line)

# 控制结构<a id="sec-10" name="sec-10"></a>

## 顺序结构<a id="sec-10-1" name="sec-10-1"></a>

-   (progn bodys)
    顺序执行bodys,bodys中的最后一个form的返回值为progn的返回值

-   (prog1 form1 bodys)
    类似progn,但form1的返回值为prog1的返回值

-   (prog2 form1 form2 bodys)
    类似progn,但form2的返回值为prog2的返回值

## 条件表达式<a id="sec-10-2" name="sec-10-2"></a>

-   (if condition then-form else-bodys)
    注意,then-form只能是一句form,而else-bodys可以为多个form,事实上它包含了一个隐含的progn

-   (when condition then-bodys)

-   (unless condition else-bodys)

-   (cond clauses)
    一个clause的格式为(condition bodys)
    
    clause的格式也可以为(condition),这样的话,cond的返回值为非nil的condition的返回值

-   (pcase EXP BRANCH1 BRANCH2 BRANCH3 &#x2026;)
    一个BRANCH的格式为(UPATTERN BODYS)
    
    pcase先计算EXP的值,并将值与各个BRANCH中的UPATTERN相比较,若相等,则执行相应的BODYS
    
        (pcase (get-return-code x)
          ('success       (message "Done!"))
          ('would-block   (message "Sorry, can't do it now"))
          ('read-only     (message "The shmliblick is read-only"))
          ('access-denied (message "You do not have the needed rights"))
          (code           (message "Unknown return code %S" code)))
    
    UPATTERN可以是下面几种格式
    
    -   \`(QPATTERN1 . QPATTERN2)
        该模式匹配一个cons cell,它的car匹配QPATTERN1,而cdr匹配QPATTERN2
        
            (setq form '(1 . 2))
            (pcase form
              (`(,x . ,y) (message "%s + %s = %s" x y (+ x y)))) ;这里x绑定为值1,y绑定为值2
                                                    ;=>"1 + 2 = 3"
    -   \`ATOM
        该模式匹配任何\`equal\` ATOM的atom
        
            (pcase (get-return-code x)
              (`success       (message "Done!"))
              (`would-block   (message "Sorry, can't do it now"))
              (`read-only     (message "The shmliblick is read-only")) ;注意,symbol前需要用反引号引起来
              (`access-denied (message "You do not have the needed rights"))) ;这里access-denied为atom,使用equal来进行匹配
    -   \`,UPATTERN
        该模式匹配任何符合UPATTERN的object,并会绑定object到UPATTERN中的变量中
        
            (setq form '(add 1 2))
            (pcase form
              (`(add ,x ,y) (message "%s + %s = %s" x y (+ x y)))) ;这里x绑定为值1,y绑定为值2
            ;=>"1 + 2 = 3"
    -   SYMBOL
        该模式匹配任何object,并且将该symbol绑定到object上.
        
            (pcase (get-code x)
              (code (message "code is %s" code)))   ;这里code为一个symbol,它的值为(get-code x)的结果
    -   -
        该模式匹配任何object,但与SYMBOL不同在于不会将object绑定到任何symbol上
    -   (pred PRED)
        返回(PRED object)的值
        
            (pcase x
              ((pred numberp) (message "x is number"))
              ((pred stringp) (message "x is string")))
    -   (or UPATTERN1 UPATTERN2 &#x2026;)
        任何一个UPATTERN匹配都行
    -   (and UPATTERN1 UPATTERN2 &#x2026;)
        所有UPATTERN都必须匹配
    -   (guard EXP)
        若EXP的计算结果为非nil,则匹配,否则不匹配

## 组合条件<a id="sec-10-3" name="sec-10-3"></a>

-   (not condition)

-   (and conditions)

-   (or conditions)

## 循环<a id="sec-10-4" name="sec-10-4"></a>

-   (while condition bodys)
    while先判断condition的值,只要condition为非nil,则循环执行bodys,bodys可以为空.
    
    要模拟repeat bodys until condition,可以使用如下的结构
    
        (while (bodys
                (not condition)))

-   (dolist (var list [result]]) bodys)
    对list的每个element,绑定到变量var中,然后执行bodys中的语句,最后返回result的计算结果(默认为nil).
    
        (defun reverse (list)
          (let (value)
            (dolist (elt list value)
              (setq value (cons elt value)))))

-   (dotimes (var count [result]) bodys)
    类似dolist,但var的值的范围为[0,count)

## 使用catch/throw模拟goto语句<a id="sec-10-5" name="sec-10-5"></a>

可以在catch中使用throw来跳出循环,throw语句会跳转到catch处,例如

    ;; (catch tag bodys)
    (defun foo-outer ()
      (catch 'foo
        (foo-inner)))
    
    ;; (throw tag value)
    (defun foo-inner ()
      ...
      (if x
          (throw 'foo t))                   ;这里第一个参数必须与catch的第一个参数匹配. 第二个参数t,作为catch的返回值
      ...)
    ;; 从这个例子中可以看出,throw可以跨函数间捕获

throw会根据其第一个参数来查询匹配的catch,匹配的catch它的第一个参数需要eq throw的第一个参数.

catch语句的返回值由throw的第二个参数决定

若有多个catch可供匹配,则最内层那个catch被匹配. 

throw操作退出多个lisp结构时,就好像正常退出这些lisp结构一样. 
具体来说,throw操作会这些lisp结构中使解绑用let绑定的变量,退出了save-excursion语句后,会还原buffer和postion. 退出save-restriction语句后,会还原narrowing状态. 它还会调用unwind-protect语句定义的清理动作.

若一个throw的tag没有相应的catch tag来匹配,则会抛出\`no-catch\`错误. 错误内容为throw语句中的\`(tag value)\`

# Elisp中的异常机制<a id="sec-11" name="sec-11"></a>

## 使用singal/error/condition-case模拟try catch语句<a id="sec-11-1" name="sec-11-1"></a>

elisp中也提供了类似C++中的异常机制,在elisp中,其被称为error. 

大多数的error会在调用primitive function时自动抛出. 当然你也可以使用函数\`error\`和\`signal\`手工抛出error.

需要注意的是,C-g触发的quitting,它的处理方式跟error类似,但并不是error

每个error都需要一个错误说明信息,来说明抛出error的原因. 

### error类型<a id="sec-11-1-1" name="sec-11-1-1"></a>

就好像C++有各种不同类型的异常一样,elisp也有不同类型的error. error的类型使用error symbol来标识. 每个error有且仅有一个error symbol

同样的,跟C++类似,error处于一种被称为error-condition的继承体系内,每个error-condition由condition-name来标识,一个error可以属于多个error-condition.

理论上,\`'error\`处于error-condition的最顶端,但quit是个例外,quit属于一种error-condition但它不是一种error,它的父类就是quit自己

若要定义自己的error,可以使用define-error函数.
-   (define-error symbol message &optional parent)
    
    定义一个新error,它的error-symbol为参数symbol. 它继承于参数parent所表示的error-condition(默认为error),
    
    参数message需要是一个字符串,当该error被抛出,而没有handler捕获时,elisp使用该字符串作为error message. 
    
    下面是一个定义error的例子
    
        (define-error 'new-error "A new error" 'my-own-errors) ;error message一般第一个字母是大写的

### 抛出error<a id="sec-11-1-2" name="sec-11-1-2"></a>

-   (error format-string &rest args)
    
    抛出一个error,该error的错误说明信息为(format format-string args)

-   (signal error-symbol data)
    
    signal函数抛出一个名为error-symbol的error. 
    
    参数error-symbol必须是由\`define-error\`定义的symbol. 
    data参数则是与error环境相关的一系列lisp object,其lisp object中的个数和意义,对不同的error-symbol有不同的要求
    
    若抛出的error没有被处理,则error-symbol和data这两个参数被用来输出出错信息. 
    
    一般情况下,出错信息由error-symbol的error-message property来提供. data则一般用来提供产生error的上下文环境.
    但若error-symbol为error,则错误信息为(car data),且(car data)必须为string型. file-error类则有其特殊的处理模式.
    
        (signal 'error '("asdbs" (car 1) (cas 1))) ;error--> asdbs: (car 1), (cas 1)
        (signal 'wrong-number-of-arguments '(x y)) ; error--> Wrong number of arguments: x, y
        (signal 'no-such-error '("My unknown error condition")) ; error--> peculiar error: "My unknown error condition"

-   (user-error format-string &rest args)
    
    user-error跟error函数类似,但是它使用user-error作为error-symbol而不是error.
    
    如名称所示,一般用该函数抛出用户级的error,而不是代码级的error,即它不会进入debug模式(即使debug-on-error为非nil)

### 处理Error<a id="sec-11-1-3" name="sec-11-1-3"></a>

类似C++中的异常机制,elisp中的error也可以定义多个error-handler来捕获它,但只有最靠近error发源地的error-handler会用来处理该error.

若抛出的error,没有对应的error handler来处理它,则根据变量\`debug-on-error\`来决定是调用debug来处理该error(t),还是直接终止程序输出error(nil).

-   (condition-case var protected-form error-handler-bodys)
    
    可以使用condition-case来定义error handler.例如
    
        (condition-case nil
            (delete-file filename)
          (error nil))
    
    condition-case的第一个参数var是一个变量,当参数protected-form正常执行时,该变量只能在error-handler的代码中才能被使用,这时该变量的值为'(error-symbol . data)'. error-handler可以根据该变量中所描述的错误信息来进行操作.
    var参数也可以是nil,表示没有这样一个描述error信息的变量.
    就像写C++代码一样,有时候,需要重新抛出error,以便让外面的代码捕获到该error,则可以这样做:
    
        (signal (car var) (cdr var))
    
    我们称呼condition-case的第二个参数为"protected form"(在上例中,就是(delete-file filename))
    
    "protected form"后面的参数则为定义的error handlers. 每个error-handler的格式为(condition-names handler-bodys). 
    这里,conditon-names可以是一个error-condition名称或一个由error-condition名称组成成列表. 在上面的例子中,\`error\`为conditon-name表示所有类型的error.
    
    捕获到error后,condition-case的返回值为error-handler的执行结果. 若没有error发生,则返回protectd-form的计算结果.
    下面是一些error-handler的例子
    
        (error nil)
        
        (arith-error (message "Division by zero"))
        
        ((arith-error file-error)
         (message
          "Either division by zero or failure to open a file"))

一般情况下,若抛出的error被error-handler所捕获,则不会进入debug模式,但若希望调试那些被condition-case捕获的error,可以设置变量\`debug-on-signal\`为非nil. 
你也可以设置某些特定的error在捕获前,先进入debug模式,方法是在error-handler的conditon-name前加上\`debug\`,例如:

    (condition-case nil
        (delete-file filename)
      ((debug error) nil))

需要注意的是,这里condition-name前的debug并不意味着一定会进入debug模式,还需要将\`debug-on-error\`设置为非nil才行.

-   (condition-case-unless-debug var protected-form error-handler-bodys)
    
    类似condition-case,但只在不启用debug的情况下才其作用(即\`debug-on-error\`为nil)

-   (error-message-string error-descriptor)
    
    输出error-descriptor(即condition-case中的第一个参数var)所表示的字符串.

-   (ignore-errors body)
    
    执行body语句,并忽略任何抛出的error. 若body执行时不抛error,则返回body的计算结果,否则返回nil

-   (with-demoted-errors format bodys)
    
    该宏就像是ignore-error的温和版本. 它不会直接忽略掉error的发生,相反,它会使用format来将error转换为一条message输出.
    
    参数format必须为格式字符串,且必须有且仅有一个"%S"作为占位符.
    
    需要注意的是,在with-demoted-errors宏中,它是使用conditon-case-unless-debug来捕获error,而不是conditon-case. 因此需要在关闭debug-on-error,才能起作用.

## 使用unwind-protect模拟finally语句<a id="sec-11-2" name="sec-11-2"></a>

类似java中的finally语句,elisp也提供了unwind-protect来保证清理动作一定会执行.

-   (unwind-protect body-form cleanup-forms&#x2026;)
    
    unwind-protect保证执行完body-form后,无论执行过程中是否直接调用throw跳出body-form,还是抛出error,还是正常执行,都会执行cleanup-forms中的语句.
    
    与finally类似,unwind-protect语句只保证body-form执行失败后会执行cleanup-forms中的语句,而不能保证cleanup-forms中如果出了问题,还会执行后面的语句.
    
    与finally不同的是,若body-form正常结束,则unwind-protect的返回值为 **body-form** 的计算结果,而若body-form非正常退出,则不返回任何值(??),而不是返回cleanup-forms的值.

# Elisp中的变量<a id="sec-12" name="sec-12"></a>

在Elisp中,一个变量就是一个lisp symbol. 变量名为该symbol的名称,变量值为该symbol的value cell中存储的值.

与C++中的变量不同的是,Elisp中的变量可以指向任何类型的数据,而且可以为变量设置一个doc-string,用于说明该变量的用处.

## 全局变量<a id="sec-12-1" name="sec-12-1"></a>

可以使用defvar,defconst,defcustom来定义全局变量.

-   (defvar symbol &optional value doc-string)
    
    定义名为symbol-name的变量,并初始化值为value.
    
        (defvar project-root "~/project/"
          "项目根目录")
    
    若省略value的值,则定义出来的变量为空变量.不能直接被访问.
    
        (defvar void-var)
        void-var                                ;Lisp error: (void-variable void-var)
    
    **需要注意的是:** 若symbol已经有值,则defvar并不会更改symbol的值.
    
        (defvar var 'some-value)
        var                                     ;some-value
        (defvar var 'other-value)
        var                                     ;some-value
    
    另外,defvar绑定的是symbol在动态域下的默认值,它并不会影响symbol的buffer-local值,也不改变symbol的静态绑定值.

-   (defconst symbol value &optional doc-string)
    
    与defvardefconst也定义一个名为symbol-name的变量,它的值为value.
    
    另外,defconst绑定的也是symbol在动态域下的默认值,它并不会影响symbol的buffer-local值,也不改变symbol的静态绑定值.
    
    它跟defvar不一样的地方在与,它总是使symbol赋值为value,而不管是否已经有值.
    
    但正如名称所表示的,它表示定义的变量通常应该是一个常量. 不 **建议** 修改它的值(但不是强制性的)

## 常量<a id="sec-12-2" name="sec-12-2"></a>

在Elisp中,nil,t和任何以\`:\`开头的symbol(我们常常称呼这种symbol为keyword)都是系统的保留常量. 

任何对这些系统的保留常量的值进行修改的动作,都会抛出\`setting-constant\` error.

还有一类是用户使用defconst来自定义的常量,对这类常量的值进行修改,并不会抛出error,而且修改行为也能成功

## 局部变量<a id="sec-12-3" name="sec-12-3"></a>

与C++一样,函数中的参数,天生就是局部变量,它的作用范围就是整个函数内部. 

而要实现类似C++的代码块内的局部变量({}内定义的局部变量),需要使用let\*语句.

-   (let\* (bings&#x2026;) forms&#x2026;)
    
    这里,bingding为定义局部变量的语句,在这里定义的局部变量,只能在后面的bodys中访问.
    
    每个bingding可以是一个symbol,这表示定义一个局部变量,并且该局部变量的值为nil.
    也可以是一个(symbol value-form)格式的list,表示定义一个局部变量,并且该局部变量的值为value-form的计算结果. 当然value-form也可以省略,表示nil.
    
    下面是一个例子
    
        (setq y 2)                              ; => 2
        
        (let* ((y 1)
               (z y))    
          (list y z))                           ; => (1 1)

-   (let (bindings&#x2026;) bodys&#x2026;)
    
    类似let\*语句, **但是需要注意的是:** let语句中,在整个(bingings)没有完成之前,所有的局部变量都是不生效的. 举个例子
    
        (setq y 2)                              ; => 2
        ;; 这里在执行(z y)时,局部变量y还未生效,这时的y是全局变量y,即它的值为2
        (let ((y 1)
              (z y))
          (list y z))                           ; => (1 2)

## Buffer-Local变量<a id="sec-12-4" name="sec-12-4"></a>

Buffer-Local变量应该说是Elisp所特有的一种变量类型了. 这种变量的作用域仅限于某个buffer.

换句话说,一个变量它在不同作用域下有不同的绑定值. 若它处于buffer作用域下,则该变量的值根据buffer的不同而不同. 而之前提到的与buffer无关的动态作用域的值,我们称它为变量的默认值.

**需要注意:** 即使一个变量被标记为buffer-local变量,当使用defvar和defconst时,改变的依然是它的默认值.而不是buffer作用域下的值.

-   (make-local-variable symbol)
    
    可以使用命令\`make-local-variable\`来标注一个变量为Buffer-Local变量. 这时,该变量在当前buffer中的值变得跟其他buffer独立开来. 在当前buffer中,该变量处于buffer作用域中,而在其他buffer中则共享该变量的默认值.
    
    该变量在buffer作用域下的值,在创建时与该buffer的默认值是一样的.
    
    若一个变量是terminal-local变量,则该函数会抛出error. terminal-local变量不能有buffer作用域下的值.
    
    **注意:** 不要用该函数来将hook变量设置为buffer-local变量,而应该在使用add-hook和remove-hook时将local参数设为t

-   (setq-local symbol-name value)
    
    将symbol变量标注为buffer-local变量,同时赋值为value. 它等于是先调用make-local-variable后再用setq进行赋值.

-   (make-variable-buffer-local symbol)
    
    也可以使用命令\`make-variable-buffer-local\`来标注一个变量在所有的buffer中都处于buffer-local作用域下,包括那些还未被创建的buffer. 我们称呼这种变量为automatically buffer-local变量
    
    所有buffer中的值一开始时默认就是该变量的默认值.
    
    当symbol变量的默认值为空时,该语句会自动为变量在buffer作用域下的值赋值为nil.

-   (defvar-local symbol-name value &optional docstring)
    
    定义以symbol-name为名称的变量,并赋初值为value,并把该变量标注为自动的buffer-local变量.
    
    该红等价于先执行make-variable-buffer-local,然后再执行defvar

-   (local-variable-p symbol &optional buffer)
    
    判断symbol所表示的变量在buffer中是否为buffer-local变量,若省略buffer参数则指的当前buffer.
    
    **注意:该函数在判断automatically buffer-local变量时返回nil**
    
        (defvar-local a 1)                     ;这时a为automatically buffer-local变量
        (local-variable-p 'a)                  ;=>nil

-   (local-variable-if-set-p symbol &optional buffer)
    
    跟local-variable-p类似,但当symbol为automatically buffer-local变量时,该函数也返回t
    
        (defvar-local a 1)                     ;这时a为automatically buffer-local变量
        (local-variable-if-set-p 'a)           ;=> t

-   (buffer-local-value symbol buffer)
    
    返回symbol变量在指定buffer中的buffer作用域中的值, 若symbol变量在指定buffer中没有buffer-local绑定值,则返回它的默认值.

-   (buffer-local-variables &optional buffer)
    
    以list的方式返回当前buffer中的所有buffer-local变量. 若buffer参数被省略,则表示当前buffer.
    
    返回的list中的每个元素的格式为'(symbol . value), 但若symbol变量在buffer作用域下的值为空(不是nil),则元素的格式只是单个的symbol
    
        (make-local-variable 'foobar)
        (makunbound 'foobar)
        (make-local-variable 'bind-me)
        (setq bind-me 69)
        (setq lcl (buffer-local-variables))
        ;; =>
            (foobar                             ;foobar为void变量,格式为单个的symbol
            (bind-me . 69))                     ;bind-me变量有值,因此格式为(symbol . value)

-   (kill-local-variable symbol)
    
    删除symbol变量在当前buffer中的buffer-local标识,使之在当前buffer中作为一个普通变量来处理. 
    
    **要注意的是:** 若对一个automatical buffer-local变量执行该函数,则该变量在当前buffer中访问时会作为一个普通变量来处理,然而, **一旦对这个变量再次赋值,该变量又变成为buffer-local变量**

-   (kill-all-local-variables)
    
    删除当前buffer中所有buffer-local变量(包括函数)的buffer-local标识,但那些标注为"permanent"的变量和"permanent-local-hook"属性为非nil的函数除外.
    
    该函数返回nil
    
    **该函数执行的第一件事就会执行change-major-mode-hook,因为它会把当前buffer的major mode先改为fundamental mode**
    
    <span class="underline">所谓标注为permanent的变量,指的是symbol的permanent-local属性为非nil</span>

当在某buffer中标注某变量问buffer-local变量后,再使用setq来更改变量值时只会更改该变量在该buffer作用域下的值了,要想更改它的默认值,需要使用语句set-default / setq-default了
-   (setq-default symbol1-name value1 symbol2-name value2 &#x2026;)
    
    设置每个变量的默认值

-   (set-default symbol value)
    
    设置symbol变量的默认值

同样的,使用let对一个buffer-local变量进行局部绑定时,修改的也是该变量在buffer作用域下的值.

## File-Local变量<a id="sec-12-5" name="sec-12-5"></a>

在文件中指定了某个变量为File-local变量后,当某个buffer访问该文件后,相关变量自动成为buffer-local变量.

处于安全考虑,若某个File-local变量为函数或S表达式,则只有那些明确标记为safe的file-local变量才会自动生效,其他的file-local变量需要用于认可才回生效.

你可以通过修改一个变量的safe-local-variable属性来决定哪些值对于该参数来说是有效的,该属性接收该参数的值,返回非nil则表示该参数safe(有效),nil表示unsafe(无效).

此外,当Emacs读取file-local变量时,\`read-circle\`变量会临时设为nil. 

-   变量enable-local-variables
    
    该变量控制了是否让file-local变量生效. 
    
    该变量有可以设置为:
    
    1.  t (默认)
        
        表示自动生效那些标记为safe的变量,而那些unsafe的变量需要提示用户确认后才生效
    
    2.  :safe
        
        只有标记为safe的变量才生效,其他的unsafe变量不生效
    
    3.  :all
        
        所有的变量,不管safe或unsafe,都生效
    
    4.  nil
        
        所有的变量,不管safe或unsafe,都不生效
    
    5.  其他
        
        素有变量,不管safe或unsafe,都需要用户确认过之后才生效

-   变量inhibit-local-variables-regexps
    
    该变量是一个由正则表达式组成的list. 如果某个文件名符合list中某元素的个正则表达式,则该文件中的file-loca变量不生效

-   (hack-local-variables &optional mode-only)
    
    启用该buffer所访问file中的file-local变量.
    
    **注意:** 执行该函数时,会按照变量\`enable-local-variables\`的不同值,而有不同的生效方式.
    
    该函数执行前会触发\`before-hack-local-variables-hook\`,执行后会触发\`hack-local-variables-hook\`
    
    若mode-only参数为非nil,则之后名为"mode:"的file-local变量会生效,若文件中指明了"mode:",则该函数返回该函数值,否则返回nil

-   变量file-local-variables-alist
    
    该变量一定为buffer-local变量,它是一个存储了file-local变量信息的alist. 
    
    每个file-local-variables-alist中元素的格式为\`(VAR . VALUE)\`,这里VAR为file-local变量,value为变量的值.
    
    当Emacs访问一个文件时,它其实是先将所有的file-local变量收集了起来存入file-local-variables-alist变量中,然后再调用hack-local-variables函数来让他们生效.

-   配置项safe-local-variable-values
    
    该变量是一个由\`(VAR . VALUE)\`组成的list. 这里VAR为变量名,而VALUE为VAR的值,并且该值被认为是safe的.

-   (safe-local-variable-p symbol value)
    
    判断給symbol变量设置为value是否safe

-   (risky-local-variable-p symbol)
    
    该函数判断symbol变量是否认为是risky
    
    risky的变量在生效前,除非明确被设置到\`safe-local-variable-value\`中,佛则一定需要经过用户的确认. 
    
    所谓risky变量,指的是它的属性\`risky-local-variable\`为non-nil的变量. 
    
    此外,任何以\`-command\`,\`-frame-alist\`,\`-function\`,\`functions\`,\`-hook\`,\`-hooks\`,\`-form\`,\`-forms\`,\`-map\`,\`map-alist\`,\`-mode-alist\`,\`-program\`和\`-predicate\`结尾的变量都自动认为是risky的.

-   变量ignored-local-variables
    
    该变量的值为由变量组成的list, 该list中的对应变量不能被设置为file-local变量,即使在文件中将它设置为file-local变量,也无效果.

-   配置型enable-local-eval
    
    \`:Eval\`是一个明显的潜在漏洞,因此Emacs通常在处理该函数时都要经过用户的确认.
    
    通过设置enable-local-eval值,可以改变这一行为. 该变量可以有三个值:
    
    1.  t
        
        表示无条件执行
    
    2.  nil
        
        表示无条件不执行
    
    3.  其他(默认为'mayb)
        
        表示询问用户.

-   配置型safe-local-eval-forms
    
    该变量为一个由正则表达式组成的list. 当\`Eval:\`参数的值能够匹配上其中一个正则的S表达式,则认为是安全的.
    
    如果\`Eval:\`参数的值为一个调用函数的S表达式,且调用的函数拥有\`safe-local-eval-function\`属性,则该属性所表示的函数被用来判断该S表达式是否为安全的. \`safe-local-eval-function\`函数得值,可以是一个函数列表,表示其中任何一个函数返回t即为安全,也可以是t,表示所有的S表达式都安全.
    
    由于Text属性值也可能包含要被调用的函数,因此它也认为是一个潜在的漏洞, 因此,若一个变量的值为带有Text属性的String,则该string的Text属性被忽略.

## Directory-Local变量<a id="sec-12-6" name="sec-12-6"></a>

在目录中指定了某个变量为Directory-local变量后,当某个buffer访问该目录(极其子目录)下的文件后,相关变量自动成为buffer-local变量.

有两种方式来定义directory-local变量:

1.  把他们放到特定的文件中,该文件名由常量\`dir-locals-file\`决定,默认为\`.dir-locals.el/<sub>dir</sub>-locals\`
    
    基于速度的考虑,一般在访问远程文件时,会禁用该特性,但通过设置变量\`enable-remote-dir-locals\`为t,可以为远程文件也打开该特性.
    
    dir-locals-file文件的格式为一个list,其中每个元素的格式可以是:
    
    -   (major-mode . directory-local-variable-value-alist)
        
        表示当指定major-mode开启时,对应的directory-local变量生效
    
    -   (nil. directory-local-variable-value-alist)
        
        表示对所有major-mode,对应的directory-local变量生效
    
    -   (subdirectory-name-string . dir-locals-file-format-list)
        
        表示对于指定子目录下的所有文件,directory-local变量生效.
    
    下面是一个例子:
    
        ((nil . ((indent-tabs-mode . t)
        (fill-column . 80)))
        (c-mode . ((c-file-style . "BSD")
        (subdirs . nil)))  ; =>这里subdirs不是变量名,而是一个关键字,表示该设置,只对当前目录下的文件有效,而对子目录下的文件无效.
        ("src/imported"
        . ((nil . ((change-log-default-name
        . "ChangeLog.local"))))))
    
    由于手工修改该文件格式会比较容易出错,因此Emacs提供了命令add-dir-local-variable/delete-dir-local-variable/copy-file-locals-to-dir-locals命令来维护directory-locale变量

2.  为目录定义"project class"
    
    首先使用函数dir-locals-set-class-variables定义一组变量/值的键值对的集合.
    
        (dir-locals-set-class-variables 'unwritable-directory
                                        '((nil . ((some-useful-setting . value)))))
    
    然后使用函数dir-locals-set-directory-class函数为目录分配这组键值对的集合
    
        (dir-locals-set-directory-class
         "/usr/include/" 'unwritable-directory)

### 相关函数<a id="sec-12-6-1" name="sec-12-6-1"></a>

-   (hack-dir-local-variables)
    
    为访问当前目录(及子目录)下文件的所有buffer开启directory-local变量
    
    该函数通过调用函数dir-locals-set-class-variables和dir-locals-set-directory-class来完成此操作.

-   (hack-dir-local-variables-non-file-buffer)
    
    为当前buffer启用directory-local变量,一般用于那些non-file buffer中.
    
    对这些non-file buffer开启directory-local变量时会从\`default-directory\`和它的父目录中查找directory-local变量的定义

-   (dir-locals-set-class-variables project-class  dir-locals-file-format-list)
    
    该函数定义一组directory-local变量及其值,并分配改组变量为project-class
    
        (dir-locals-set-class-variables 'unwritable-directory
                                        '((nil . ((some-useful-setting . value)))))

-   (dir-locals-set-directory-class directory project-class &optioinal mtime)
    
    为directory(及其子目录下)下的所有文件分配project-class所表示的directory-local变量.
    
    当Emacs从\`.dir-locals.el\`文件中读取directory-local变量时,也是通过调用该函数来实现的,这是会带上mtime参数.
    
    mtime参数存储的是\`.dir-locals.el\`的modification time. Emacs使用该时间来检查已有的directory-local变量是否依然有效.

-   变量dir-locals-class-alist
    
    该变量是一个alist,它维护了project-class及对应directory-local变量的对应关系.

-   变量dir-locals-directory-cache
    
    该变量是一个alist,它维护了目录名称,对应的project-class和对应\`.dir-locals.el\`的modification time

-   变量enable-dir-local-variables
    
    是否启用directory-locall变量特性.

## Terminal-Lock变量<a id="sec-12-7" name="sec-12-7"></a>

## 空变量<a id="sec-12-8" name="sec-12-8"></a>

前面说到,变量的值其实就是取得symbol中的value cell中存储的对象. 当symbol中的value cell没有存储任何对象时(nil也是一个对象),这时访问该变量会抛出\`void-variable\` error. 我们称这种变量为空变量.
(**NOTE:** 上述的情况在Emacs默认的动态作用域下是成立的,若明确指定了静态作用域,则另当别论了,但这种情况比较少用到)

那么创建这种空变量呢? 这就需要用到makeunbound函数了.

-   (makeunbound symbol)
    
    将当前作用域下的局部变量symbol中的value cell清空,使之成为空变量.

若要判断某个变量是否为空变量,则可以使用boundp函数

-   (boundp symbol)
    
    该函数检查symbol的value cell是否有值,若有值则返回t,否则返回nil. 因此我们也可以定义函数
    
        (defun void-variable-p (variable)
          (null (boundp variable)))
    
    下面是一些boundp的例子
    
        (boundp 'abracadabra)          ; Starts out void.
        ;; => nil                          
        (let ((abracadabra 5))         ; Locally bind it.
          (boundp 'abracadabra))
        ;; => t
        (boundp 'abracadabra)          ; Still globally void.
        ;; => nil
        (setq abracadabra 5)           ; Make it globally nonvoid.
        ;; => 5
        (boundp 'abracadabra)
        ;; => t

## 变量别名<a id="sec-12-9" name="sec-12-9"></a>

变量及其别名公用同一个值,修改其中一个也会同时更改另一个值.

-   (defvaralias new-alias base-variable &optional docstring)
    
    为base-variable定义一个名为new-alias的变量别名,可以为这个别名分配一个新的docstring
    
    该函数返回base-variable

-   (indirect-variable alias-variable)
    
    返回别名链中最末端的那个非别名变量
    
    若出现了循环定义的别名,则该函数抛出\`cyclic-variable-indirection\` error

## 废弃变量<a id="sec-12-10" name="sec-12-10"></a>

-   (make-obsolete-variable obsolete-variable current-variable when &optional access-type)
    
    在编译时警告一个变量即将废弃不用了,其中:
    
    参数obsolete-variable为即将不用的变量
    
    参数current-variable若为symbol,则会提示用新的变量current-variable代替老的变量obsolete-variable. 若current-name为string,则直接警告该string.
    
    参数when指明了obsolete-variable从什么时候开始废弃,通常为一个表示版本号的字符串.
    
    参数access-type指明了对obsolete-variable的哪种操作会触发警告,可以使'get或'set

-   (define-obsolete-variable-alias obsolete-variable current-variable &optional when docstring)
    
    该宏创建obsolete-variable为current-variable的别名,并标记obsolete-variable为即将废弃的变量. 
    
    该宏其实等价于:
    
        (defvaralias OBSOLETE-NAME CURRENT-NAME DOCSTRING)
        (make-obsolete-variable OBSOLETE-NAME CURRENT-NAME WHEN)

## 受限的变量<a id="sec-12-11" name="sec-12-11"></a>

默认情况下,一个Lisp变量的值可以是任何的Lisp object. 但有些变量不是用Lisp来定义的,而是用C来定义. 这些用C定义的变量有可能只能存储特定类型的值. 如果变量类型为:

-   DEFVAR<sub>LISP</sub>
    
    该变量跟在lisp中定义的变量一样,它的值可以是任意的.

-   DEFVAR<sub>INT</sub>
    
    该变量的值只能是整型

-   DEFVAR<sub>BOOL</sub>
    
    该变量的值只能为t或者nil
    
    其中变量\`byte-boolean-vars\`中列出了所有类型的DEFVAR<sub>BOOL的变量</sub>

## 变量的作用域<a id="sec-12-12" name="sec-12-12"></a>

与C++不同的是,Elisp中的变量默认情况下是处于动态作用域中. 当然,Elisp也支持静态作用域. 

### 动态作用域<a id="sec-12-12-1" name="sec-12-12-1"></a>

当一个变量处于动态作用域中时,这就意味着,这个变量的值是受到运行环境的影响的. 举个例子:

    (setq foo 'outer)                       ;outer
    (defun say-foo()
      foo)                                  
    
    (say-foo)                               ;=>outer
    (let ((foo 'inner))
      (say-foo))                            ;=>inner,在调用say-foo的运行环境中,foo的值为局部定义的'inner,因此say-foo的返回值为'inner
    
    (say-foo)                               ;=>outer, 在调用say-foo的运行环境中,foo的值为全局值'outer,因此say-foo的返回值为'outer

拥有动态作用域值的变量被成为special-variable,可以使用函数special-variable-p来判断一个symbol是否为special variable.
-   (special-variable-p symbol)
    
    判断symbol所表示的变量是否为special-variable. (由defvar,defconst和defcustom定义的变量都是special variable)

-   

elisp实现动态作用域的方法很简单,每个symbol都由一个value cell,这个value cell所持有的值就是该变量在当前动态作用域下的值. 当为该变量创建一个动态局部作用域时,elisp将当前value cell的值压入一个栈中,并将该symbol的value cell存上新值. 当退出该动态局部作用域时,Elisp从栈中弹出以前的值,并重新存入symbol的value cell中.

### 静态作用域<a id="sec-12-12-2" name="sec-12-12-2"></a>

当一个变量处于静态作用域下时,该变量的值在定义该变量处就已经被确定了,即它的值为定义环境的值. 例如

事实上,Elisp使用一个alist来存储静态作用域中各变量与值的关系. 这种alist的结构为\`'((symbol1 value1)(symbol2 value2)&#x2026; t)\`. 
这种alist可以作为eval函数的第二个参数用来指明eval执行语句的静态作用域环境.

可以使用lexical-let和lexical-let\*来创建静态作用域. 这两个语句的语法跟let和let\*一样,但BODY中的lambda函数会创建闭包.

## 泛化变量(Generalized Variables)<a id="sec-12-13" name="sec-12-13"></a>

泛化变量(Generalized Variables)或称位置列表(place form)其实就是变量值所被存储的内存地址.

泛化变量可能是: 一个普通的lisp变量或者aref,car,caar,cadr,cdr,cdar,cddr,elt,get,gethash,nth,nthcdr,symbol-function,symbol-plist,symbol-value,default-value,frame-parameter,terminal-parameter,keymap-parent,match-data,overlay-get,overlay-start,overlay-end,process-buffer,process-filter,process-get,process-sentinel,window-buffer,window-display-table,window-dedicated-p,window-hscroll,window-parameter,window-point,window-start函数的返回值.

-   (setf place-form1 value1 place-form2 value2&#x2026;)
    
    可以使用setf宏来操作泛化变量. 它的作用类似setq,但setq只能为symbol赋值,而setf可以为任何泛化变量赋值. 例如
    
        (setq a '(1 2 3))                       ;(1 2 3)
        (setf (cadr a) 'two)                    ;将a中的第二个元素的值改为two
        a                                       ;(1 two 3)

-   (gv-define-simple-setter name setter-function &optional fix-return)

-   (gv-define-setter name arglist &rest body)

## 取变量值<a id="sec-12-14" name="sec-12-14"></a>

当在静态作用域下,Elisp取变量值时,它会先查看该变量是否存在静态作用域下的绑定值. 然后再查看该变量的动态作用域下的绑定值(即该symbol的value cell所存储的值)

除了直接引用变量可以取得变量值外,还可以使用symbol-value函数来获取变量的动态作用域下的值
-   (symbol-value symbol)
    
        (defvar num 123)
        (symbol-value 'num)                     ;123
    
    **需要注意的是:** 该函数只能用来获取symbol动态绑定的值,而不能用在静态环境下获取它静态绑定的值
    
        (lexical-let ((num 234))
          (symbol-value 'num)                   ;123
          num)                  ;234

-   (buffer-local-value symbol buffer)
    
    返回symbol变量在指定buffer中的buffer作用域中的值, 若symbol变量在指定buffer中没有buffer-local绑定值,则返回它的默认值.

-   (default-value symbol)
    
    取symbol变量的默认值

-   (default-boundp symbol)
    
    判断symbol变量的默认值是否为不为空

-   

# Customization<a id="sec-13" name="sec-13"></a>

emacs中可以使用\`defcustom\`定义customizable variables, 使用defface定义customizable face,使用defgroup定义cutomization group.

## Common Item Keywords<a id="sec-13-1" name="sec-13-1"></a>

defcustom,defgroup,defface这些定义配置项的函数/宏,都接收keyword参数. 

所有这些keyword参数,除了\`:tag\`之外,都可以联合使用. 下面是一些通用的参数说明.

-   :tag LABEL
    
    LABEL为一个字符串类型. 该参数表示使用LABEL取代被定义item的名称作为该item的标签.

-   :group GROUP
    
    定义item所属的组别. 一个item可以同时属于多个组别,因此你可以多次使用该参数

-   :link LINK-DATA
    
    在该item的说明文档后面增加一个外部链接. 其中LINK-DATA可以以下格式:
    
    你还可以在LINK<sub>DATA的第一个元素后面加上\`</sub>:tag NAME\`用来表示链接显示为NAME. 例如\`(info-link :tag "foo" "(emacs)Top")'会创建一个链接连接到Emacs手册,但是显示为foo
    
    -   (custom-manual INFO-NODE)
        
        链接到Info node. INFO-NODE为Info文档中某node的名称,像"(emacs)Top"这样的. 
        
        该链接显示为[manual]
    
    -   (info-link INFO-NODE)
        
        类似custom-manual,只是链接的显示为Info node的名称
    
    -   (url-link URL)
        
        链接到web页面, 点击它会使用变量\`browse-url-browser-function\`定义的Web浏览器打开
    
    -   (emacs-library-link LIBRARY)
        
        连接到Emacs Lisp library文件.
    
    -   (file-link FILE)
        
        连接到某个文件,Emacs会用find-file函数打开它
    
    -   (function-link FUNCTION)
        
        链接到某个函数的说明文档,当点击它,会使用describe-function来获取函数说明
    
    -   (variable-link VARIABLE)
        
        连接到某个变量的说明文档
    
    -   (custom-group-link GROUP)
        
        链接到其他的group

-   :load FILE
    
    在显示item前先加载FILE

-   :require FEATURE
    
    当保存item的值时,执行(require 'FEATURE)

-   :version VERSION
    
    表示该item第一次出现在版本为VERSION的Emacs中,或该item的默认值或意义在版本为VERSION的Emacs中更改了.
    
    VERSION为字符串类型

-   :package-version '(PACKAGE . VERSION)
    
    表示该item第一次出现在版本为VERSION的PACKAGE中,或该item的默认值或意义在版本为VERSION的PACKAGE中更改了.
    
    PACKAGE应该是一个符号,为package的正式名称. 而VERSION应该为字符串类型.
    
    若PACKAGE为Emacs自带的,则PACKAGE和VERSION需要在变量\`customize-package-emacs-version-alist\`中

## customization groups<a id="sec-13-2" name="sec-13-2"></a>

-   (defgroup group members doc [keyword value]&#x2026;)
    
    定义新的名为group的客户化组. 该客户化组中包含members为内容.
    
    参数group为一个不被quote的symbol.
    
    参数members为由cusomiztion items组成的list,表示这些items属于某个group. 然而实际上一般该参数都为nil,而是定义item时使用:group关键字来标识该item所属的group
    
    members的元素格式为(NAME WIDGET). 这里NAME为表示item的symbol. 而WIDGET为item的类型(custom-variable,custom-face,custom-group)
    
    当对group设置了:version参数,则所有属于该group的其他item,默认继承该参数值
    
    defgroup可以使用:prefix关键字参数
    
    :prefix PREFIX
    
    表示若该group中的item以PREFIX为前缀,而变量\`custom-unlispify-remove-prefixes\`为非nil, 则该item的tag在显示时会忽略掉该PREFIX.
    
    一个group可以设置忽略任意数量的prefix

## customizable variable<a id="sec-13-3" name="sec-13-3"></a>

defcusomter的语法与defvar有点类似,但是它还可以接收很多keyword参数.

-   (defcustom var standard-value doc [keyword value]&#x2026;)
    
    参数var为不被quote的symbol. 它表示定义的可配置变量.
    
    参数standard-value为一个表达式,它的计算值作为var的默认值
    
    参数doc为对该变量的说明.
    
    若在defcustom中没有通过:group关键字设置所属的group,则在相同文件中最后defgroup的组会自动作为该item的所属组.
    
    defcustom支持的keyword参数有:
    
    -   :type TYPE
        
        标注该客户化变量的类型,它指定了哪些值是合理的,如何显示这些值.
        
        也可以在defcustomer后使用函数(custom-add-frequent-value customization-item value)来增加选值范围
    
    -   :options VALUE-LIST
        
        指定可选值的范围,该可选值的范围并不具有约束性.
        
        该keyword只有在type为hook,plist和alist时才有效
    
    -   :set SETFUNCTION
        
        当使用Customize更改该配置项时,实际上调用的是SETFUNCTION函数,该函数接收两个参数:配置项和新值. 默认SETFUNCTION函数为set-default
    
    -   :get GETFUNCTION
        
        当获取该配置项的值时,实际上是调用了GETFUNCTION函数. 该函数接收一个参数:配置项, 并返回某个值. 默认GETFUNCTION为\`default-value'
    
    -   :initialize FUNCTION
        
        当defcustom语句被执行时,实际上是调用了FUNCTION函数. 该函数接收两个参数:配置项和默认值.
        
        elisp预定义了一些可选的FUNCTION:
        
        -   \`custom-initialize-set'
        
        -   \`custom-initialize-default'
        
        -   \`custom-initialize-reset'
        
        -   \`custom-initialize-changed'
        
        -   \`custom-initialize-safe-set'
        
        -   \`custom-initialize-safe-default'
    
    -   :risky VALUE
        
        设置该配置项变量的\`risky-local-variable'属性为VALUE
    
    -   :safe FUNCTION
        
        设置该配置项变量的\`safe-local-variable'属性为FUNCTION
    
    -   :set-after VARIABLES

-   (custom-reevaluate-setting customizable-arg)
    
    可以用该函数在defcustom外,重新对customizablen-arg进行赋值

-   (custom-variable-p arg)
    
    判断arg是否为可配置变量, 这意味着这个变量是带有\`standard-value'属性的symbol或者带有\`custom-autoload'属性的symbol,或者由其他可配置变量组成的alist

-   (custom-set-variables &rest args)
    
    根据arg中的说明,更改配置项
    
    每个arg的格式为'(配置项 配置项的值表达式 [is-NOW [REQUEST-features-list [doc-string]]])

### Customization Type<a id="sec-13-3-1" name="sec-13-3-1"></a>

所有的customization type都实现为widget. customization widget可以通过\`C-M-i'或\`M-<TAB>'来补全

1.  Simple Types

    -   'sexp
        
        任意lisp object
    
    -   'integer
    
    -   'number
    
    -   'float
    
    -   'string
    
    -   'regexp
    
    -   'character
    
    -   'file
        
        配置项必须是一个文件名称
    
    -   '(file :must-match t)
        
        配置项必须是一个已存在的文件名称
    
    -   'directory
        
        配置项必须是目录
    
    -   'hook
        
        该配置项必须是一个函数列表
    
    -   'symbol
    
    -   'function
        
        该配置项必须是一个lambda表达式或函数名
    
    -   'variable
        
        该配置必须是一个变量名称
    
    -   'face
    
    -   'boolean
    
    -   'key-sequence
    
    -   'coding-system
    
    -   'color

2.  Composite Types

    -   '(cons CAR-TYPE CDR-TYPE)
        
        该配置项必须是cons cell. 并且它的car必须为CAR-TYPE,cdr必须为CDR-TYPE
    
    -   '(list ELEMENAT1-TYPE ELEMENT2-TYPE &#x2026; ELEMENTn-TYPE)
        
        该配置项为由n个元素组成的list,每个元素都需要跟相应的ELEMENT-TYPE相匹配
    
    -   '(group ELEMENAT1-TYPE ELEMENT2-TYPE &#x2026; ELEMENTn-TYPE)
        
        类似'(list ELEMENAT1-TYPE ELEMENT2-TYPE &#x2026; ELEMENTn-TYPE),区别在于list使用element的tag来作为element value的标签,而group不作标签
    
    -   '(vector ELEMENAT1-TYPE ELEMENT2-TYPE &#x2026; ELEMENTn-TYPE)
        
        类似'(list ELEMENAT1-TYPE ELEMENT2-TYPE &#x2026; ELEMENTn-TYPE)
        
        区别在于配置项的类型必须是vector
    
    -   '(alist :key-type KEY-TYPE :value-type VALUE-TYPE)
        
        配置项为alist类型,且每个cons ceil元素的car必须是KEY-TYPE的,cons ceil的cdr必须是VALUE-TYPE
        
        :key-type参数与:value-type可以省略,默认为'sexp
    
    -   '(plist :key-type KEY-TYPE :value-type VALUE-TYPE)
        
        类似'(alist :key-type KEY-TYPE :value-type VALUE-TYPE),只是配置项为plist类型,且KEY-TYPE默认为symbol类型而不是sexp
    
    -   '(choice CUSTOMIZE-TYPE1 CUSTOMIZE-TYPE2 &#x2026; CUSTOMIZE-TYPEn)
        
        配置项可以是CUSTOMIZE-TYPES中的任意一种.
        
        可以在CUSTOMIZE-TYPE中通过:tag关键字来指明配置项为某种TYPE时的label.例如
        
            (choice (integer :tag "Number of spaces")
                    (string :tag "Literal text"))
    
    -   '(radio CUSTOMIZE-TYPE1 CUSTOMIZE-TYPE2 &#x2026; CUSTOMIZE-TYPEn)
        
        类似'(choice CUSTOMIZE-TYPE1 CUSTOMIZE-TYPE2 &#x2026; CUSTOMIZE-TYPEn),只是显示时使用radio button的方式显示而不是用菜单显示
    
    -   '(const VALUE)
        
        该配置项的值必须为VALUE. 常与choice搭配
    
    -   '(other VALUE)
        
        表示配置项可以接收任意的lisp值,但是该配置项实际上总是被赋值为VALUE.
        
        other主要用在choice中作为最后一个元素使用. 例如:
        
            (choice (const :tag "Yes" t)
                    (const :tag "No" nil)
                    (other :tag "Ask" foo)
    
    -   '(function-item FUNCTION)
        
        类似const,但是它的值必须是function.
    
    -   '(variable-item VARIABLE)
        
        类似const,但是它的值必须是表示某个变量的symbol
    
    -   '(set TYPE1 TYPE2 &#x2026; TYPEn)
        
        该配置项必须是一个list,且每个list中元素类型必须匹配TYPES中的其中一种
    
    -   '(repeat ELEMENT-TYPE)
        
        该配置项必须是一个list,并且每个元素都是ELEMENT-TYPE的
    
    -   '(restricted-sexp :match-alternatives CRITERIA)
        
        该配置项的值可以是任一的lisp对象,但是必须匹配CRITERIA中的任一条件.
        
        CRITERIA是一个list,其中每个元素可以是:一个predicate function或者A quoted constant
        
            ;; allows integers, `t' and `nil' as legitimate values.
            (restricted-sexp :match-alternatives
                             (integerp 't 'nil))

3.  Type Keywords

    在定义配置项的:type时,可以在customizaton type name symbol后指定以下的keyword-argument对:
    
    -   :value DEFAULT
        
        提供默认值. 当某种类型不能包含nil时,特别有用.
    
    -   :format FORMAT-STRING
        
        显示配置项值时的格式.
        
        <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
        
        
        <colgroup>
        <col  class="left" />
        
        <col  class="left" />
        </colgroup>
        <thead>
        <tr>
        <th scope="col" class="left">占位符</th>
        <th scope="col" class="left">说明</th>
        </tr>
        </thead>
        
        <tbody>
        <tr>
        <td class="left">%[BUTTON%]</td>
        <td class="left">以按钮的样式显示文本BUTTON,其:action属性说明了当该按钮被点击时作什么操作</td>
        </tr>
        
        
        <tr>
        <td class="left">%{SAMPLE}</td>
        <td class="left">以\`:sample-face'的样式显示文本SAMPLE</td>
        </tr>
        
        
        <tr>
        <td class="left">%v</td>
        <td class="left">显示为该配置项的value</td>
        </tr>
        
        
        <tr>
        <td class="left">%d</td>
        <td class="left">显示为该配置项的documentation string</td>
        </tr>
        
        
        <tr>
        <td class="left">%h</td>
        <td class="left">类似%d,但当配置项的doc-string超过一行时,会提供一个按钮隐藏/显示剩下的行</td>
        </tr>
        
        
        <tr>
        <td class="left">%t</td>
        <td class="left">显示为该配置项的tag</td>
        </tr>
        
        
        <tr>
        <td class="left">%%</td>
        <td class="left">显示为%</td>
        </tr>
        </tbody>
        </table>
    
    -   :action ACTION
        
        当点击button时执行的操作. 这里ACTION为一个函数,它会接收两个参数:点击的按钮所在widget和点击事件
    
    -   :button-face FACE
        
        提供:button-face的显示样式,它会用于显示FORMAT-STRING中的%[&#x2026;%]中的内容
    
    -   :button-prefix PREFIX / :button-suffix SUFFIX
        
        指明在显示button的前后文本. 他们的值可以是:
        
        nil: 不显示多于的文本
        
        string: 显示文本
        
        symbol: 显示symbol的值
    
    -   :tag TAG
        
        指定TAG(字符串类型)作为配置项为该类型时的tag
    
    -   :doc DOC
        
        指定DOC作为配置项为该类型时的doc-string
    
    -   :help-echo MOTION-DOC
    
    -   :match FUNCTION
        
        使用FUNCTION判断配置项的值是否匹配该类型,FUNCTION为一个函数,它接收两个参数:表示CUSTOMIZATION TYPE的widget和配置项的值
    
    -   :validate FUNCTION
        
        使用FUNCTION校验配置项的值是否有效. FUNCTION函数接收一个参数:表示CUSTOMIZATION TYPE的widget. 若该函数判断widget是当前值是有效的,则返回 **nil** ,否则返回包含无效数据的widget,并设置该widget的\`:error'属性为出错描述.

4.  Defining New Types

    定义新Type就是为一个Composite Types命一个名字. 由于一个type就是一个widget,因此使用define-widget来实现
    
        (define-widget 'binary-tree-of-string 'lazy
          "A binary tree made of cons-cells and strings."
          :offset 4
          :tag "Node"
          :type '(choice (string :tag "Leaf" :value "")
                         (cons :tag "Interior"
                               :value ("" . "")
                               binary-tree-of-string
                               binary-tree-of-string)))
    
    这里define-widget的第一个参数为表示新widget type的symbol. 
    
    第二个参数为一个已经存在的widget,表示新widget type的类别,一般用'lazy
    
    第三个参数为doc-string
    
    :type参数描述了所代表的composite type说明

## customizable face<a id="sec-13-4" name="sec-13-4"></a>

-   (custom-set-faces &rest args)
    
    根据arg,更改face配置项.
    
    一个arg的格式为'(FACE SPEC [is-Now [doc-string]])

# Loading<a id="sec-14" name="sec-14"></a>

## Load命令<a id="sec-14-1" name="sec-14-1"></a>

-   (load filename &optional missing-ok nomessage nosuffix must-suffix)
    
    load先查找filename.elc文件,再查找filename.el文件,再查找filename文件
    
    若开启了Auto-Compression-mode(默认开启),则load在查找后一个文件前还会查找前一个文件的压缩版本(参见变量\`jka-compr-load-suffixes').
    
    若nosuffix参数为非nil,则load不会查找filename.elc和filename.el,但不影响auto-compression-mode的作用
    
    若must-suffix参数为非nil,则load认为加载的文件名后缀必须为.el和.elc(或他们的压缩版本),除非filename中包含了明确的目录名称.
    
    若参数missing-ok,则在找不到要加载的文件时,不抛出错误,只是返回nil
    
    若\`load-prefer-newer'配置项为非nil,则load会挑选filename.elc和filename.el中最近较新的那个来加载
    
    若filename为相对路径,则load会在变量\`load-path'中定义的路径中查询,查询到的第一个存在文件作为要加载的文件. 需要注意的是:需要在\`load-path'中添加nil才回在当前路径搜索要load的文件
    
    load在加载文件时,会同时设置变量\`load-file-name'的值为加载文件的文件名.
    
    若load顺利加载文件,则返回t

-   (load-file filename)
    
    加载filename所明确指定的文件,并不会为它添加.el会.elc后缀(但不影响Auto Compression Mode的作用)
    
    若filename为相对路径,则认为是相对于当前路径来说的. (该函数并不涉及到load-path变量)

-   (load-library library)
    
    类似load

-   变量\`load-file-name'
    
    存储的是load时实际加载的文件名称.

-   变量\`load-in-progress'
    
    若Emacs正在加载某个文件,则该值为非nil,否则为nil

-   变量\`load-read-functioin'
    
    该变量指明的函数,用于替代\`load'和\`eval-region'中的\`read'函数
    
    该变量默认为nil,表示\`read'

-   变量\`load-suffixes'
    
    load在搜索文件时,会根据该变量中设置的后缀,添加到filename参数后面来寻找文件.
    
    默认为'(".elc" ".el")

-   变量\`load-file-rep-suffixes'
    
    This is a list of suffixes that indicate representations of the same file.
    
    该变量一般以""开头,若开了Auto Compression Mode则会把\`jka-compr-load-suffixes'的内容也加进去.

-   (get-load-suffixes)
    
    返回load函数尝试添加的文件后缀. 它的值一般是\`load-suffixes'与\`load-file-rep-suffixes'的集合.

-   配置项load-prefer-newer
    
    若该配置项为非nil,则load会检测所有可能的加载文件,并挑选最新的那个来加载

-   变量load-path
    
    load函数搜索加载文件的路径列表,nil表示当前工作目录
    
    可以在运行emacs时用-L选项指定load-path的值
    
    对于每个load-path中的目录,emacs都会去检查是否有subdirs.el这个文件,若存在该文件,则加载它. 由emacs自动生成的subdirs.el会自动将该目录下的所有以 **字母与数字结尾** 的子目录路径添加到load-path中.

-   命令(locate-library library &optional nosuffix path interactive-call)
    
    找到指定library所表示的精确文件名. 它的搜索方式与load一致.
    
    参数nosuffix与load参数中的一样. 非nil表示不添加.elc和.el后缀
    
    若PATH为非nil,则表示用参数PATH的值代替load-path的值
    
    当作为命令运行locate-library时,参数interactive-call的值为t,则会在echo area中显示file name,否则函数直接返回文件名称

-   命令(list-load-path-shadows &optional stringp)
    
    该命令列出隐藏的Emacs Lisp文件的列表. 
    
    所谓隐藏文件指的是这样一些文件,虽然在load-path中有定义其目录,但是由于在搜索到其目录之前已经发现了符合条件的加载文件,因此load命令无法加载到这些文件.
    
    参数stringp指定是以字符串的形式返回文件列表,还是显示在buffer中.

## Autoload<a id="sec-14-2" name="sec-14-2"></a>

autoload让你在一开始只是记录函数/宏所对应的加载文件路径. 当第一次用到该函数/宏(或查看其帮助文档)时才开始加载对应的文件.

有两种方法设置一个autoload函数:使用autoload函数和在源代码中使用特定的注释

-   (autoload function-or-macro filename &optional docstring interactive type)
    
    该函数指定function-or-macro为autoload函数/宏. 其源代码定义在filename中.
    
    若filename中不包含目录名称或.el/.elc的后缀,该函数会自动在加载时添加后缀,并且该函数不会加载不带后缀的文件.
    
    参数doc-string使得在不加载实际文件前,也能够查看function-or-macro的对应说明.
    
    参数interactive为非nil,则表示function-or-macro为命令. 这使得Emacs能够为M-x提供该命令的补全而不用加载function-or-macro的真实定义. 
    
    当参数function-or-macro为macro/keymap时,可以将type参数设置为'macro或'keymap
    
    若function-or-macro已经有一个非autoload的非空函数,则autoload什么也不做,只是返回nil

-   (autoloadp object)
    
    判断object是否为autoload类型的对象

-   使用特殊注释定义autoload对象
    
    在定义真实的函数定义前,加上注释\`;;;###autoload'(这种特殊的注释,被称为autoload cookie)
    
    随后执行M-x update-file-autoloads/update-directory-autoloads命令,会将autoload的调用命令写道生成的loaddefs.el中.

-   变量generate-autoload-cookie
    
    该变量指定了定义autoload对象的特殊注释格式,默认为\`;;;###autoload'

-   变量generate-autoload-file
    
    该变量定义了将生成的autoload语句放到哪个文件中,默认为\`loaddefs.el'

-   (autoload-do-load autoload-object &optional name macro-only)
    
    加载autoload-object所在的源代码文件. 
    
    参数name若为非nil则需要时一个表示autoload-function的symbol. 这时它的返回值为该symbol的实际定义函数.
    
    若参数macro-only为'macro,则autoload-do-load不加载函数,只加载macro

## Features<a id="sec-14-3" name="sec-14-3"></a>

features是除autoload外推迟加载的另一种方式.

一个feature是一个表示函数与变量的集合的symbol,可以在文件中用provide声明一个feature,同时使用require来加载一个feature

需要注意的是: 不要在let内使用require,否则可能会产生不可预知的后果.

Although top-level calls to \`require' are evaluated during byte compilation, \`provide' calls are not.  Therefore, you can ensure that a file of definitions is loaded before it is byte-compiled by including a \`provide' followed by a \`require' for the same feature, as in the following example.

    (provide 'my-feature)  ; Ignored by byte compiler,
                                            ;   evaluated by `load'.
    (require 'my-feature)  ; Evaluated by byte compiler.

-   (provide feature &optional subfeatures)
    
    该函数声明已经加载了feature,下次再require该feature时,不会去重新加载该feature所在的文件
    
    这里参数subfeatures应该而我一个由symbol组成的list,表示该版本的feature,提供了一系列的subfeatures

-   (require feature &optional filename noerror)
    
    该函数检查该Emacs Session是否已经加载了feature,若没有,则使用load加载filename. 
    
    若参数filename为nil,则使用feature的字符串表示作为load的参数. 但要注意的是,这种情况下,require只会加载带有.el/.elc为后缀的文件(auto comression mode也有效果). 一个名为feature而不带任何后缀的文件不会被加载.
    
    若noerror参数为非nil,则当load文件失败时,只返回nil,而不抛出error.否则返回参数feature.
    
    若加载filename成功,而该文件没有provide feature,则require抛出error:\`Required feature FEATURE was not provided'
    
    **require语句会在编译阶段得到执行.**

-   (featurep feature &optional subfeature)
    
    若feature已经加载到该Emacs Session(即feature是否为\`features'中的member)则返回t.
    
    若subfeature为非nil,则只有在subfeature也被provided了的情况下才返回t

-   变量features
    
    该变量为一个由symbol组成的list,每个symbol都是加载到该Emacs Session中的feature

## 查找定义所在的文件<a id="sec-14-4" name="sec-14-4"></a>

-   (symbol-file symbol &optional type)
    
    查找定义symbol的文件路径.
    
    参数type指定了symbol的类型,可以是nil,'defun,defvar或defface
    
    symbol-file实际是从\`load-history'变量中查找symbol所在的文件的.

## Unloading<a id="sec-14-5" name="sec-14-5"></a>

-   (unload-feature feature &optional force)
    
    回收feature所定义的函数/变量,恢复之前的symbol定义.
    
    若变量\`FEATURE-unload-function'的值为某个函数,则unload-feature会在执行清理前执行该函数. 若该函数返回nil,则unload-feature接着执行正常的清理过程,否则,unload-feature不再进行下一步的清理.
    
    默认情况下,unload-feature不会unload被其他库依赖的feature, 但若force参数为非nil,则unload-feature不会检查依赖关系.
    
    unload-feature函数也是根据变量\`load-history'的内容来行动的.

-   变量unload-feature-special-hooks
    
    该变量为一个hooks列表,在执行unload操作前,会先删除这些hooks中的定义在library中的函数.

## Hooks<a id="sec-14-6" name="sec-14-6"></a>

-   after-load-functions
    
    load完某个文件后,会执行该hook,每个hook函数会接收一个参数:刚加载文件的绝对路径

-   宏(with-eval-after-load library-or-feature bodys&#x2026;)
    
    若library-or-feature为library,则在每次加载完library文件后,都执行一次bodys代码
    
    若在执行该宏的时候,library已经被加载过了,则该宏会立刻执行一次bodys
    
        (with-eval-after-load "edebug" (def-edebug-spec c-point t)
    
    若library-or-feature为feature,则在执行(provide feature)之后才回执行bodys的内容
    
    若执行bodys时抛出error,不会unload已加载的文件,但是会阻止bodys中的下面语句的执行.
    
    一般该宏没什么用.

# Byte Compilation<a id="sec-15" name="sec-15"></a>

Elisp的Byte Compilation为伪编译,它将lisp编译为字节码格式,由特定的字节码解释器解释,而不是编译为与硬件相关的代码. 这使得它的速度会稍微慢点,但同时也保证了不同硬件平台之间的可移植性

若希望某个lisp file不被编译,设置file-local变量no-byte-compile的值为t
格式为:\`;; -\*-no-byte-compile: t; -\*-'

当编译的文件中包含宏时要特别注意,因为在编译阶段,宏会被展开,这时可能宏的定义还未加载到Emacs中. 为了应付这种情况,一般使用require语句指定包含所需宏的文件(require在编译阶段会被执行). 为了防止用户在执行编译后程序时依然执行require语句,可以使用\`eval-when-compile'包含\`require'语句

## 相关函数<a id="sec-15-1" name="sec-15-1"></a>

-   (byte-compile symbol)
    
    编译symbol的函数定义成字节码格式.
    
    参数symbol的函数定义必须是函数的真实代码,而不能是引用函数.
    
    参数symbol也可以是lambda表达式,但这种情况下,byte-compile只是返回对应的编译后代码,而并不存储它
    
    若symbol的函数定义是一个已经编译为字节码格式的函数,则该函数什么也不做,只是返回nil

-   命令(copmile-defun &optional arg)
    
    编译并执行当前top-level form,并将结果输出到echo area中.
    
    若参数arg为非nil,则将结果插入到当前buffer中,执行的form位置后

-   命令(byte-compile-file filename &optional load)
    
    该命令将lisp格式的filename编译为字节码格式的文件,生成的文件名称是原filename的.el后缀改为.elc后缀,若filename不带.el后缀,则生成的文件名为filename.elc
    
    若load参数为非nil,则在编译完filename后,还是加载编译后的文件.
    
    若byte-compile-file作为命令执行时,会提示输入要编译的文件,这时参数load额值为prefix argument

-   命令(byte-recompile-directory directory &optional flag force)
    
    该命令重新编译directory及其子目录中的所有需要重新编译的.el文件(存在.elc文件比.el文件旧的.el文件)
    
    若存在没有对应.elc文件的.el文件,则由参数flag来说明该如何处理,nil表示不编译这些文件,0表示编译他们,其他值表示询问用户
    
    若参数force为非nil,则命令在重编译所有有对应.elc文件的.el文件.

-   (batch-byte-compile &optional noforce)
    
    该函数调用\`byte-compile-file'编译命令行中指定的文件.
    
    该函数必须当Emacs处于batch状态时才能使用,因为当编译完成后,它会关闭Emacs.
    
        emacs -batch -f batch-byte-compile *.el
    
    编译一个文件出错,不会妨碍其编译下一个文件,但这时,Emacs退出时会设置非0的状态码.
    
    若参数noforce为非nil,则,该函数不会编译那些已经有更新版本的.elc文件的.el文件

-   配置项byte-compile-dynamic-docstrings
    
    默认情况下,Emacs从字节码文件中加载函数和变量时不会加载 他们的doc-string,当需要时才动态的从字节码文件中加载进来. 这就产生了一个后果:若此时字节码文件被更新了,那么原来的doc-string就被覆盖了.
    
    设置该配置项为nil,可以静止Emacs动态加载doc-string的行为.
    
    可以在lisp文件中添加一行"-\*-byte-compile-dynamic-docstrings: nil;-\*"

-   变量byte-compile-dynamic
    
    若为非nil,则表示开启"dynamic function loading"功能. 这时加载该文件并不会读取其中函数的真实定义,只有在正在调用该函数时采取临时读取该函数的定义.

-   (fetch-bytecode function)
    
    若function为byte-code function object,则立即从字节码文件中加载function的字节码.
    
    返回参数function

## 编译期执行语句<a id="sec-15-2" name="sec-15-2"></a>

-   (eval-and-compile bodys&#x2026;)
    
    在编译期间和执行期间都执行bodys
    
    想过类似于将bodys放入file中,然后(require file)
    
    autoload和require在编译期和执行期都会执行.

-   (eval-when-compile bodys&#x2026;)
    
    只在编译期才计算bodys的值. **这时bodys的值被作为常量存储起来,当正常执行该段代码时,直接返回该常量** 
    
        (defvar my-regexp
          (eval-when-compile (regexp-opt '("aaa" "aba" "abb"))))

## Compiler Errors<a id="sec-15-3" name="sec-15-3"></a>

-   (with-no-warning bodys&#x2026;)
    
    执行bodys时,不出现warnning警告

-   变量\`byte-compile-warnings'
    
    控制编译时什么样的警告会被抛出

## Disassembly<a id="sec-15-4" name="sec-15-4"></a>

-   (disassemble object &optional buffer-or-name)
    
    显示object的反编译代码

# Reading and Printing Lisp Objects<a id="sec-16" name="sec-16"></a>

Reading是将文本转换为lisp object的过程

Printing是将lisp object转换为文本的过程

## Input Stream<a id="sec-16-1" name="sec-16-1"></a>

输入流可以是以下几种类型

-   Buffer
    
    从buffer中光标所处位置开始读取

-   Maker
    
    从buffer中指定Maker处开始读取

-   string
    
    从string的第一个字母开始读取

-   function
    
    由function产生要读取的字符. 这种函数必须支持两种调用模式:
    
    1.  当无参数调用时,返回下一个要读取的字符
    
    2.  当带一个参数(通常是一个字符)调用时,保存该参数,并在下一次无参数调用时返回它,及实现unreading功能.

-   t
    
    表示从minibuffer中读取,若Emacs运行在batch mode状态下,则使用stdin

-   nil
    
    表示使用\`standard-input'的值作为输入流

-   symbol
    
    表示使用symbol的函数定义作为输入,类似function

### Input Functions<a id="sec-16-1-1" name="sec-16-1-1"></a>

-   (read &optional stream)
    
    从stream中读取一个S表达式,并转换为Lisp Object返回

-   (read-from-string string &optional start end)
    
    从string中读取一个S表达式,并返回'(lisp-object . postion)
    
    其中lisp-object为S读到的表达式,postion是string中剩余字符的位置(第一个未读字符的位置)
    
        (read-from-string "(setq x 55) (setq y 5)") ; => ((setq x 55) . 11)
        (read-from-string "\"A short string\"")     ; => ("A short string" . 16)
        
        ;; Read starting at the first character.
        (read-from-string "(list 112)" 0)       ; => ((list 112) . 10)
        ;; Read starting at the second character.
        (read-from-string "(list 112)" 1)       ; => (list . 5)
        ;; Read starting at the seventh character, and stopping at the ninth.
        (read-from-string "(list 112)" 6 8)     ; => (11 . 8)

-   变量standard-input
    
    当stream参数为nil时,使用该变量的值作为steam参数的实参

-   变量read-circle
    
    若为非nil,则允许读取循环结果的S表达式,默认为t

## Output Stream<a id="sec-16-2" name="sec-16-2"></a>

输出流参数可以是以下类型:

-   buffer
    
    输出字符插入到Buffer中的光标处,光标会随着字符的插入而向前移动.

-   Maker
    
    输出字符插入Buffer中Maker处

-   Function
    
    Elisp使用输出字符作为参数调用function,该function应该存储这些输出字符

-   t
    
    输出结果到echo area

-   nil
    
    使用\`standard-output'的变量值

-   symbol
    
    使用symbol的function定义

### Output Functions<a id="sec-16-2-1" name="sec-16-2-1"></a>

-   (print object &optional stream)
    
    输出object的文本表示到stream中.
    
    输出时,在object的前后都会增加一个回车. 并且会输出引用字符
    
        (progn (print 'The\ cat\ in)
               (print "the hat")
               (print " came back"))
        ;; -|
        ;; -| The\ cat\ in
        ;; -|
        ;; -| "the hat"
        ;; -|
        ;; -| " came back"
        ;; => " came back"
    
    该函数返回object的文本表示字符串

-   (prin1 object &optional stream)
    
    类似print,但是不会在object的文本表示前后添加回车
    
        (progn (prin1 'The\ cat\ in)
               (prin1 "the hat")
               (prin1 " came back"))
        ;; -| The\ cat\ in"the hat"" came back"
        ;; => " came back"

-   (princ object &optional stream)
    
    该函数输出object的文本表示到stream中,并返回参数object.
    
    该函数一般用来输出对人可读的信息(而不是对read函数可以读),因此该函数并不会插入引用字符,也不会在字符串两边加上双引号,更不会自动插入空格分隔两次调用间的内容
    
        (progn
          (princ 'The\ cat)
          (princ " in the \"hat\""))
        ;; -| The cat in the "hat"
        ;; => " in the \"hat\""

-   (terpri &optional stream) 
    
    输出newline到stream中

-   (write-char char &optional stream)
    
    输出char到stream中,返回参数char

-   (prin1-to-string object &optional noescape)
    
    该函数返回一个字符串,该字符串的内容就是(prin1 object)的输出
    
        (prin1-to-string 'foo) ;; => "foo"
        (prin1-to-string (mark-marker)) ;; => "#<marker at 2773 in strings.texi>"
    
    若参数noescape为非nil,则输出时不使用引用字符
    
        (prin1-to-string "foo")                 ; => "\"foo\""
        (prin1-to-string "foo" t)               ; => "foo"
    
    也可以使用format函数实现该功能

-   宏(with-output-to-string bodys&#x2026;)
    
    该宏在将\`standard-output'设置为一个字符串的环境下执行bodys,然后返回该字符串
    
        (with-output-to-string
          (princ "The buffer is ")
          (princ (buffer-name)))                ;=>"The buffer is foo"

-   (pp object &optional stream)
    
    类似prin1,但是输出的格式更方便阅读.

### Output Variables<a id="sec-16-2-2" name="sec-16-2-2"></a>

-   standard-output
    
    当参数stream为nil时,使用该变量的值

-   print-quoted
    
    若该值为非nil,表示使用简写形式输出quoted forms.例如
    (quote foo)输出为'foo, (function foo)输出为#'foo

-   print-escape-newlines
    
    若该值为非nil,则表示字符串中的newline字符,会被输出为\n,formfeed符会被输出为\f
    
    该参数影响prin1和print函数的输出方式,但是不能影响prnc的输出
    
        (prin1 "a\nb")
        -| "a
        -| b"
        => "a
           b"
        
        (let ((print-escape-newlines t))
          (prin1 "a\nb"))
        -| "a\nb"
        => "a
           b"

-   print-escape-nonascii
    
    若该变量值为非nil,则字符串中的unibyte格式非ascii字符输出为\\XXX的格式.
    
    该参数影响prin1和print函数

-   print-escape-multibyte
    
    若该变量值为非nil,则字符串中的mutibyte格式非ascii字符输出为\\XXX的格式.
    
    该参数影响prin1和print函数

-   print-length
    
    该变量指明了输出list,vector或bool-vector时,能输出最多多少个元素. 若超过这么多个元素,则使用引号缩写
    
        (setq print-length 2)                   ; => 2
        (print '(1 2 3 4 5))                    ; => (1 2 ...)
        -| (1 2 ...)
    
    nil表示无限制

-   print-level
    
    该变量值指明了输出时()和[]能够嵌套的最大深度,超过这个深度会用省略号代替,nil表示无限制

-   配置项eval-expression-print-length/eval-expression-print-level
    
    eval-expression中使用的print-length/print-level版本

-   print-circle
    
    若该值为非nil,则在输出时开启探测object是否有循环结构

-   print-gensym
    
    若该值为非nil,则输出时开启探测symbol是否是uninterned.
    
    这时,uninterned symbol输出时会带有前缀#:

-   print-continuous-numbering
    
    If non-\`nil', that means number continuously across print calls. 
    This affects the numbers printed for \`#N=' labels and \`#M#' references.  
    Don't set this variable with \`setq'; you should only bind it temporarily to \`t' with \`let'. 
    When you do that, you should also bind \`print-number-table' to \`nil'

-   print-number-table
    
    This variable holds a vector used internally by printing to implement the \`print-circle' feature.  
    You should not use it except to bind it to \`nil' when you bind \`print-continuous-numbering'.

-   float-output-format
    
    该变量指明了输出float类型数字时的格式. 默认为nil,表示在不丢失精度的情况下,使用最短的格式输出.

# Documentation<a id="sec-17" name="sec-17"></a>

## 获取doc-string<a id="sec-17-1" name="sec-17-1"></a>

-   (documentation-property symbol property &optional verbatim)
    
    查看symbol的property属性中存储的doc-string,它会自动从DOC文件中或编译的字节码代码中抽取出对应的doc-string
    
    若参数verbatim为nil,则,找到的doc-string会传入函数\`substitute-command-keys'进行键绑定说明的转换
    
        (documentation-property 'command-line-processed
                                'variable-documentation) ; => "Non-nil once command line has been processed"
        (symbol-plist 'command-line-processed)           ; => (variable-documentation 188902)
        (documentation-property 'emacs 'group-documentation) ; => "Customization of the One True Editor."

-   (documentation function &optional verbatim)
    
    该函数返回function的doc-string,其中function可以是macro,named keyboard macro,special forms,oridnary function
    
    若参数verbatim为nil,则,找到的doc-string会传入函数\`substitute-command-keys'进行键绑定说明的转换
    
    若function没有函数定义,则抛出\`void-function'错误,若函数定义没有doc-string,则返回nil

-   (face-documentation face)
    
    返回face的doc-string

-   doc-directory
    
    DOC文件的存放路径,Emacs可能要从DOC文件中读取doc-string

## 替换doc-string中的key binding<a id="sec-17-2" name="sec-17-2"></a>

当doc-string中要引用绑定的键序列时,使用特殊的引用形式可以通过函数\`substitute-command-keys'转换为指定命令真实的绑定键序列.

-   \`\\[COMMAND]'
    
    显示调用COMMAND时的键序列,若COMMAND没有绑定键序列,则显示为M-x COMMAND

-   \`\\{MAPVAR}'
    
    使用函数\`describe-bindings'显示MAPVAR所表示的keymap中的summary

-   \`\\<MAPVAR>'
    
    转换为空值,该形式的说明会产生一个副作用:it specifies MAPVAR's value as the keymap for any following \`\\[COMMAND]' sequences in this documentation string.

-   \`\\='
    
    引用接下来的那个字符;例如\`\\=\\['在显示时显示为\`\\[',而\`\\=\\='显示为\`\\='

## 将键序列输出为文本格式<a id="sec-17-3" name="sec-17-3"></a>

-   (key-description sequence &optional prefix)
    
    将sequence中的input event转换为文本格式
    
        (key-description [?\M-3 delete])        ; => "M-3 <delete>"
        (key-description [delete] "\M-3")       ; => "M-3 <delete>"

-   (single-key-description event &optinal no-angles)
    
    将input event转换为文本形式字符串. 
    
    若参数no-angle为非nil,则在包围在function keys和event symols的尖括号会被忽略,这是为了与旧版本的Emacs兼容.
    
        (single-key-description ?\C-x)          ; => "C-x"
        (key-description "\C-x \M-y \n \t \r \f123") ; => "C-x SPC M-y SPC C-j SPC TAB SPC RET SPC C-l 1 2 3"
        (single-key-description 'delete)             ; => "<delete>"
        (single-key-description 'C-mouse-1)          ; => "<C-mouse-1>"
        (single-key-description 'C-mouse-1 t)        ; => "C-mouse-1"

-   (text-char-description character)
    
    返回描述character的字符串,类似\`single-key-description'的作用
    
        (text-char-description ?\C-c)           ; => "^C"
        (text-char-description ?\M-m)           ; => "\xed"
        (text-char-description ?\C-\M-m)        ; => "\x8d"
        (text-char-description (+ 128 ?m))      ; => "M-m"
        (text-char-description (+ 128 ?\C-m))   ; => "M-^M"

-   命令(read-kbd-macro string &optional need-vector)
    
    \`key-description'的逆操作
    
    参数string中包含了用空格分隔的key descriptions,该函数会返回一个string或vector,包含了对应的events.
    
    若参数need-vector,则总是返回vector

# Elisp中的函数<a id="sec-18" name="sec-18"></a>

Elisp中的函数,是跟C++不同的. C++中的函数必须有一个函数名,然而Elisp中的函数没有函数名,只是你可以把它与一个symbol相连接,这样这个symbol的名字就暂时作为该函数的函数名了.

此外,Elisp中的函数可以通过与多个symbol相关连的方式而为同一个函数提供多个名称,而C++中的函数只有一个函数名称.

## Elisp中函数的分类<a id="sec-18-1" name="sec-18-1"></a>

函数的特性在与能够接收参数,然后返回计算结果,并可能产生一定的副作用. 在Elisp中符合这些特性的类函数对象有以下几种类型:

-   lambda expression
    匿名函数

-   primitive
    使用C语言编写的内置类函数对象,special form都认为是primitive的一种.

-   special form
    类似C语言中的固定语法的语句

-   macro
    宏,跟function类似,但它并不对参数进行预运算且返回的结果必须是一段S表达式.

-   command
    可以通过\`command-execute\`这个primitive调用的对象,通常是一个带了interactive声明的函数(也可能是keyboard macro).

-   closure
    闭包,带有静态作用域下变量的函数.

-   byte-code function
    编译为字节码的函数

-   autoload object
    它指向一个真实的函数的位置. 当真正调用到autoload object时,Emacs载入包含真正函数定义的那个文件,并且调用那个真正的函数.

## 获取函数信息<a id="sec-18-2" name="sec-18-2"></a>

-   (functionp object)
    
    判断object是否为函数. 若为函数则返回t,但macro和special form会返回nil
    
    object也可以为symbol类型,会自动判断它所指向的function.
    
        (functionp 'goto-line)                  ;=>t

-   (subrp object)
    
    判断object是否为primtive.
    
    **注意:** 与functionp不同.object为symbol的话,会返回nil.
    
        (subrp 'message)            ; `message' is a symbol,
        => nil                 ;   not a subr object.
        (subrp (symbol-function 'message))
        => t

-   (byte-code-function-p object)
    
    判断object是否为byte-code function. object为symbol类型则返回nil
    
        (byte-code-function-p 'next-line) ; => nil
        (byte-code-function-p (symbol-function 'next-line)) ; => t

-   (subr-arity subr)
    
    这里subr需要为一个primitive对象(不能为symbol),该函数返回subr的最少参数个数和最大参数个数. 
    
    返回格式为'(MIN . MAX). 
    
    若参数有&rest,则MAX为many.
    
    若subr为special form,则该函数返回'unevalled

-   (interactive-form function)
    
    获取function的interactive信息

## 匿名函数<a id="sec-18-3" name="sec-18-3"></a>

### 获取匿名函数<a id="sec-18-3-1" name="sec-18-3-1"></a>

获取匿名函数,主要有三种方法:

-   使用lambda宏
    
        (lambda (参数列表...)
            [函数描述字符串]
            [交互模式声明]
            函数体...)

-   使用function函数
    
    (function function-object)
    
    类似quote函数,它直接返回 **未计算** 的参数function-object. 
    
        (function 3)                            ;=>3,function的参数可以不为lambda表达式
        (function (lambda add-1(x) (1+ x)))     ;=>(lambda add-1(x) (1+ x)),但一般function的参数都是lambda表达式
    
    所不同的是,该函数告诉Emacs evaluator和byte-compiler,function-object为函数.
    
    具体来说,若function-object为lambda表达式,则有两个附加效果:
    
    1.  When the code is byte-compiled, FUNCTION-OBJECT is compiled into a byte-code function object
    
    2.  When lexical binding is enabled, FUNCTION-OBJECT is converted into a closure

-   使用\`#'\`标识
    
    \#'f是(function f)的缩写形式
    
        ;; 一下三种写法是等价的
        (lambda (x) (* x x))
        (function (lambda (x) (* x x)))
        #'(lambda (x) (* x x))

### 参数列表<a id="sec-18-3-2" name="sec-18-3-2"></a>

参数列表的格式为:(必须参数列表&#x2026;[&optional 可选参数列表] [&rest 剩余参数])

使用&optional表示之后的参数是可选的.

使用&rest表示之后的参数为不定参数. 它是实际参数的一个列表.

若在实际调用函数时,没有为可选参数和剩余参数提供实际参数值,则这些参数值为nil.

### 函数描述字符串(docstring)<a id="sec-18-3-3" name="sec-18-3-3"></a>

-   一般来说,函数描述字符串的第一行为对该函数作用的总结.
-   docstring的第一行最好独立的,因为apropos命令只显示第一行的文档
-   docstring中参数最好用大些字母
-   docstring以\*开头的defvar变量被认为是用户选项（user option）
    -   用户选项可以通过命令set-variable交互设置
    -   可以使用edit-options命令编辑\*scratch\*
-   \`符号名'生成一个链接
-   \\\\{major-mode-map}可以显示扩展成按键的说明
-   docstring最后那个的\\[ command ]会被command的绑定键所代替
-   如果不想要这种代替，需要用\\=转义，当然，在Emacs的docstring中，真正的写法应该是
    
        "\\=\\{major-mode-map}"
        "\\=\\[command]"
-   将\`\n(fn ARGLIST)\`放在最后一行,会自动扩展为该函数的实际参数列表.

### 交互模式声明<a id="sec-18-3-4" name="sec-18-3-4"></a>

若一个函数带了交互模式声明,则它也就是一个命令了,即可以通过M-x(execute-command)来调用了.

交互模式声明的格式为(interactive code-string),其中:
-   若interactive的参数以\*开头，则意义是，如果当前buffer是只读的，则不执行该函数

-   interactive可以后接字符串,表示获得参数的方式
    -   p 接收C-u的数字参数
        
        也可以不用P参数,直接在代码中判断current-prefix-arg的值
    -   r region的开始/结束位置
    -   n 提示用户输入数字参数,n后面可用接着提示符
    -   s 提示用户输入字符串参数
    -   若函数接收多个input,需要用\\n来分隔

-   interactive可以后接一个form,form的求值结果应该是一个list,这个list的值作为参数的实参
    
    在form中一般会用到如下几个函数用于获取用户输入
    
    -   read-string
    -   read-file-name
    -   read-directory-name
    -   read-regexp
    -   y-or-n-p
    -   read-from-minibuffer
    -   使用变量\`current-prefix-arg\`来判断是否有universal-argument

## 命名函数<a id="sec-18-4" name="sec-18-4"></a>

使用fset/defalias将匿名函数与一个symbol想结合,就为这个匿名函数分配了一个名称.

-   (fset symbol lambda函数)
    
        (fset 'plus-one (lambda (x) (+ x 1)))
        (plus-one 10)                           ;11

-   (defalias alias-name lambda-function-or-symbol &optional doc-string)
    
    为函数设定名字或别名,一般很少用到
    
        (defalias 'add-one '1+)
        (add-one 11)                            ;12
        (defalias 'add-two (lambda (x) (+ x 2)))
        (add-two 11)                            ;13

实际上,更常见的定义命名函数的方法是使用defun宏
-   (defun 函数名 (参数列表) [函数说明字符串] [declare-form] [交互模式声明] 函数体&#x2026;)
    
    定义一个带名字的函数.
    
        (defun add-one (x)
          "return value after plus one"
          (+ x 1))
        
        (add-one 10)                            ;11
    
    **注意:** 它可以比lambda函数多一个declare-form部分,这个declare-form通常用于提供Elisp编译器一些函数的信息,以便进行优化.

-   (fboundp symbol)
    
    判断symbol是否可以作为函数使用

-   (fmakeunbound symbol)
    
    使symbol不再作为函数使用.

### declare form<a id="sec-18-4-1" name="sec-18-4-1"></a>

declare form常用来为函数或宏添加一些关于属性的元标签. 它的语法是:

-   (declare specs&#x2026;)
    
    其中spec的格式为(PROPERTY ARGS&#x2026;),spec可以是以下几种说明
    
    -   (advertised-call-convention new-arg-list when)
        
        new-arg-list为正确的调用函数的方法,其他的调用方法都被认为是废弃的.
        
        when为一个表示什么时候废弃的字符串.
    
    -   (debug EDEBUG-FORM-SPEC)
        
        只能在定义宏时使用. 当用Edebug来调试该宏时,使用EDEBUG-FORM-SPEC
    
    -   (doc-string N)
        
        This is used when defining a function or macro which itself will be used to define entities like functions, macros, or variables 
        
        它表示,第N个参数作为doc-string来看待
    
    -   (ident indent-spec)
        
        Indent calls to this function or macro according to INDENT-SPEC.
        
        虽然可以用在函数上,但一般还是用在宏定义中
    
    -   (obsolete current-name when)
        
        类似(make-obsolete),表示该函数被废弃了
    
    -   (compiler-macro EXPANDER)
        
        只能用在函数定义时,告诉编译器在编译时,使用EXPANDER代替该函数.
        
        这样的话,所有的(function args&#x2026;)都实际上调用的是(EXPANDER args&#x2026;)
    
    -   (gv-expander EXPANDER)
        
        Declare EXPANDER to be the function to handle calls to the macro (or function) as a generalized variable, similarly to \`gv-define-expander'.  
        
        EXPANDER can be a symbol or it can be of the form \`(lambda (ARG) BODY)' in which case that function will additionally have access to the macro (or function)'s arguments.
    
    -   (gv-setter SETTER)
        
        Declare SETTER to be the function to handle calls to the macro (or function) as a generalized variable.  
        SETTER can be a symbol in which case it will be passed to \`gv-define-simple-setter', or it can be of the form \`(lambda (ARG) BODY)' in which case that function will additionally have access to the macro (or function)'s arguments and it will passed to \`gv-define-setter'.

## 调用函数<a id="sec-18-5" name="sec-18-5"></a>

最常用的调用函数的方式是将函数作为一个list的第一个参数. 这样当计算这个list时,会把地一个元素作为函数,其他作为参数来调用.

但是有的时候,需要在运行期间决定要执行的函数,这时候就需要使用以下函数的帮助:

-   (funcall function &rest arguments&#x2026;)
    
    使用参数arguments调用函数function.
    
        (setq f 'list)                          ; => list
        (funcall f 'x 'y 'z)                    ; => (x y z)
        (funcall f 'x 'y '(z))                  ; => (x y (z))
    
    参数function必须是一个lisp function或primitive function,而不能是macro或special form

-   (apply function &rest arguments&#x2026;)
    
    类似funcall函数,但apply的arguments中,最后一个参数 **必须** 是list. 而这个list中的元素会被打散为独立的参数来作为function的实参.
    
        (setq f 'list)                          ; => list
        (apply f 'x 'y 'z)                      ; error--> 最后一个参数z不是list类型
        (apply '+ 1 2 '(3 4))                   ; => 10
        (apply '+ '(1 2 3 4))                   ; => 10
        
        (apply 'append '((a b c) nil (x y z) nil)) ; => (a b c x y z)

-   (apply-partially func &rest args)
    
    apply-partially使用参数args绑定func中的前(length args)个参数,并由此产生一个新的函数.
    
    返回的新函数接受剩余的参数,并在内部调用原func函数.
    
        (defalias 'add-1 (apply-partially '+ 1)
          "Increment argument by one.")
        (add-1 10)                              ; => 11

-   (identity arg)
    
    该函数返回参数arg,没有任何其他处理

-   (ignore &rest args)
    
    该函数忽略args,直接返回nil

若要对某个集合(包括list)中的每个元素都调用某个函数(注意,不能是宏和special form),需要使用到map系列的函数.

**需要注意的是**,char-table比较特殊,只能用map-char-table函数调用.

-   (mapcar function sequence)
    
    mapcar将sequence中的每个元素都调用一次function方法,并将结果组成一个list返回.
    
        (mapcar 'car '((a b) (c d) (e f)))      ; => (a c e)
        (mapcar '1+ [1 2 3])                    ; => (2 3 4)
        (mapcar 'string "abc")                  ; => ("a" "b" "c")

-   (mapc function sequence)
    
    类似mapcar,但不收集个函数的运算结构. mapc的返回值为参数sequence

-   (mapconcat function sequence separator)
    
    对sequence中的每个元素都调用function方法,其function方法计算的结果必须为string类型. 然后将这个string类型的结果用separator结合起来.
    
        (mapconcat 'symbol-name
                   '(The cat in the hat)
                   " ")                         ; => "The cat in the hat"
        
        (mapconcat (function (lambda (x) (format "%c" (1+ x))))
                   "HAL-8000"
                   "")                          ; => "IBM.9111"

## 废弃函数<a id="sec-18-6" name="sec-18-6"></a>

类似变量一样,函数也可以被标注为废弃的.

-   (make-obsolete obsolete-name current-name &optional when)
    
    该函数标注obsolete-name为废弃的. 其中
    
    obsolete-name可以为表示函数或宏的symbol,也可以为函数或宏的别名.
    
    current-name可以是一个symbol,表示使用current-name代替obsolete-name. 也可以是一个字符串表示废弃的警告说明. 也可是nil.
    
    when应该是一个日期或版本号的字符串,用于表示什么时候开始废弃该函数.

-   (define-obsolete-function-alias obsolete-name current-name &optional when doc)
    
    该宏定义obsolete-name为函数current-name的别名,同时标注obsolet-name为废弃的函数.
    
    该宏等价于:
    
        (defalias OBSOLETE-NAME CURRENT-NAME DOC)
        (make-obsolete OBSOLETE-NAME CURRENT-NAME WHEN)

-   (set-advertised-calling-convention function new-arg-list when)
    
    该函数与上面两个函数不同点在于,它不是标注某个函数为废弃的,它只标注某个函数的某种用法为废弃的.
    
    任何不使用new-arg-list表示的实参调用function函数都会被警告为废弃的.
    
    when表示什么时候开始废弃function的原用法,一般为表示版本号的字符串.
    
        ;; 在老版本中sit-for函数可以接受三个参数
        (sit-for seconds milliseconds nodisp)
        
        ;; 然而用这种调用方法在Emacs22.1版本之后就被废弃掉了,因此可以这样设置
        (set-advertised-calling-convention
         'sit-for '(seconds &optional nodisp) "22.1") ;表示新的sit-for函数签名为(defun sit-for (seconds &optional nodisp))

## 内联函数<a id="sec-18-7" name="sec-18-7"></a>

要定义内联函数,只需要将定义函数的defun,换成defsubst即可

    (defsubst name (arg-list)
       [doc-string]
       [declare-form]
       [interactive]
       bodys)

注意:虽然内联函数会加快函数的执行速度,但它会增加文件和内存的消耗量,而且对debugging,tracing和asdising支持不够好,因此除非速度真的很重,否则不要用内联函数.

## 函数声明<a id="sec-18-8" name="sec-18-8"></a>

-   (declare-function function file &optional arglist fileonly)
    
    该宏告诉编译器,function函数在文件file中定义,且参数签名为arglist.
    
    编译器会检查文件file中是否包含了function函数,且参数签名是否为arglist,若想让编译器不检查函数的参数签名,需要将arglist设置为t
    
    若参数fileony为非nil,表示只检查file存在,而不检查文件中是否定义了function.

## 判断function是否安全<a id="sec-18-9" name="sec-18-9"></a>

使用unsafep来判断一个form是否是安全的

-   (unsafep form &optional unsafep-vars)
    
    若判断form为安全的可以执行,则返回nil. 否则返回一个list描述为什么form是不安全的.
    
    The argument UNSAFEP-VARS is a list of symbols known to have temporary bindings at this point;
    
    The current buffer is an implicit argument, which provides a list of buffer-local bindings.

# Advising Emacs Lisp Functions<a id="sec-19" name="sec-19"></a>

Emacs's advice system provides two sets of primitives for that: 
the core set, for function values held in variables and object fields (with the corresponding primitives being \`add-function' and \`remove-function') and 
another set layered on top of it for named functions (with the main primitives being \`advice-add' and \`advice-remove').

## Core Advising Primitives<a id="sec-19-1" name="sec-19-1"></a>

-   (add-function where function-place advise-function &optional props)
    
    为存储function的place(泛化变量)加上advise-function,使之称为一个组合了原始函数和advise函数的组合函数.
    
    -   where参数指明了advise-function与function-place处函数的整合方式. 
        -   :before
            
            在调用原function(function-place所存放的function)前调用advise-function.
            
            原function与advise-function接收同样的参数调用,并以原function的返回结果为组合函数的返回结果
            
                (add-function :before 'old-function 'advise-function) 
                ;; 等价于
                (lambda (r) (advise-function r) (old-function r))
        
        -   :after
            
            在原function调用之后调用advise-function. 
            
            原function与advise-function接收同样的参数调用,并以原function的返回结果为组合函数的返回结果
            
                (add-function :after 'old-function 'advise-function) 
                ;; 等价于
                (lambda (r) (prog1(advise-function r) (old-function r)))
        
        -   :override
            
            用advise-function代替原function
        
        -   :around
            
            使用advise-function代替原function,但原function会作为第一个参数传递給advise-function. 这样advise-function内可以调用原函数.
            
                (add-function :around 'old-function 'advise-function)
                ;; 等价于
                (lambda (r) (apply 'advise-function 'old-function r))
        
        -   :before-while
            
            先执行advise-function,若advise-function返回nil,则不再调用原function.
            
            advise-function与原function公用一样的参数,使用原function的结果作为组合函数的返回值
            
                (add-function :before-while 'old-function 'advise-function)
                ;; 等价于
                (lambda (r) (and (apply 'old-function r) (appy 'advise-function r)))
        
        -   :before-until
            
            先执行advise-function, 只有当advise-function返回nil,才调用原function.
            
            advise-function与原function共用一样的参数,使用原function的结果作为组合函数的返回值
            
                (add-function :before-while 'old-function 'advise-function)
                ;; 等价于
                (lambda (r) (or (apply 'old-function r) (appy 'advise-function r)))
        
        -   :after-while
            
            先调用原function,若function返回nil,则不调用advise-function.
            
            原function和advise-function共用同样的参数. 组合函数的返回结果为 **advise-function** 的返回结果
            
                (add-function :after-while 'old-function 'advise-function)
                ;; 等价于
                (lambda (rest r) (and (apply 'old-function r) (apply advise-function r)))
        
        -   :after-until
            
            先调用原function,只有当function返回nil时,才调用advise-function.
            
            原function和advise-function共用同样的参数. 组合函数的返回结果为 **advise-function** 的返回结果
            
                (add-function :after-while 'old-function 'advise-function)
                ;; 等价于
                (lambda (rest r) (or (apply 'old-function r) (apply advise-function r)))
        
        -   :filter-args
            
            先用原始参数调用advise-function,再将advise-function返回的结果(advise-function必须返回一个list)作为参数,来调用原function.
            
                (add-function :filter-args 'old-function 'advise-function)
                ;; 等价于
                (lambda (reset& r) (apply 'old-function (funcall 'advise-function r)))
        
        -   :filter-return
            
            先调用old-function,将结果作为参数调用advise-function.
            
                (add-function :filter-return 'old-function 'advise-function)
                ;; 等价于
                (lambda(rest& r) (funcall 'advise-function (apply 'old-function r)))
    
    -   function-place为被添加advise-function的函数位置. 它同时也决定了该advise是全局都有用,还是只在当前buffer生效.
        
        若function-place是一个symbol,则该advise全局生效
        
        若function-place为'(local SYMBOL-expression),这里SYMBOL-experssion表示一个expression,它的计算结果为一个表示变量的symbol. 则该advise只在当前buffer生效
        
        若要对静态作用域下的变量提出advise,则function-place的格式应为(var VARIABLE)
    
    -   props参数为一个代表属性的alist,目前只支持两个属性:
        
        name属性,表示该advice的名字,当remove-function时有用. 尤其是当advise-function为匿名函数时,特别有用.
        
        depth属性,表示优先级,用于决定多个advise-function的执行顺序. 
        他的取值范围从-100(表示最接近原始函数的执行顺序)到100(表示里原始函数的执行顺序最远). 默认为0
        当两个advise-function用了同一个优先级,则最后添加的advise-function会覆盖前面的.
    
    -   advise-function参数
        
        若advise-function没有interactive声明,则advise后的组合函数会继承原始函数的interactive声明.
        
        若advise-function有interactive声明,则advise后的组合函数使用advise-function的interactive声明.
        
        上述关于advised后的组合函数的interactive声明,在某一种情况下不成立: 
        if the interactive spec of FUNCTION is a function (rather than an expression or a string), then the interactive spec of the combined function will be a call to that function with as sole argument the interactive spec of the original function.  To interpret the spec received as argument, use \`advice-eval-interactive-spec'.

-   (remove-function function-place advise-function)
    
    删除通过add-function添加到function-place的advise-function

-   (advice-function-member-p advice-function function-def)
    
    判断advice-function是否已经function-def的advice

-   (advice-function-mapc f function-def)
    
    用添加到function-def的每个advicse-function和对应的propos作为参数,都调用一次f函数.

-   (advice-eval-interactive-spec interactive-spec)
    
    根据interactive-spec所声明的interactive方式,返回对应的获取值.

## Advising Named Functions<a id="sec-19-2" name="sec-19-2"></a>

advice的最常用法是給命名函数或宏添加advice

这种方法会引入一些问题,最好在没有办法的时候,使用下面的方法添加advice

-   (advice-add function-symbol where advice-function &optional props)
    
    为function-symbol添加名为advice-function的advice. where和props参数与add-function一致

-   (advice-remove function-symbol advise-function)
    
    删除function-symbol上的advise-function

-   (advice-member-p advise-function function-symbol)
    
    判断advise-function是否已经是function-symbol的advice了

-   (advice-mapc f function-symbol)
    
    使用function-symbol中的每个advise-function及其对应的props作为参数,用f来调用.

# 宏<a id="sec-20" name="sec-20"></a>

## 宏与函数的不同<a id="sec-20-1" name="sec-20-1"></a>

-   宏的参数在传递給宏前并不会作计算处理,也就是说宏看到的是传递给它的原始参数. 而函数参数传递給函数时是已经经过计算的结果,也就是说函数看到的是参数的计算结果.
-   宏的计算结果需要是一个S表达式(这个过程被称为宏扩展),Elisp会再计算这个返回的S表达式以算出最终结果.

## 定义宏<a id="sec-20-2" name="sec-20-2"></a>

定义宏的格式与定义函数的格式一样,只是用defmacro替代defun

    (defmacro macro-name (参数列表...)
            [函数描述字符串]
            [declare-form]   
            [交互模式声明]
            函数体...)

## 宏扩展<a id="sec-20-3" name="sec-20-3"></a>

调用宏会将传递給宏的参数扩展成一个S表达式,这个过程称为宏扩展过程.

-   (macroexpand macro-form &optional environment)
    
    递归扩展macro-form直到结果中不再为宏调用为止(不代表结果中就不包含宏了,只是第一个元素不为宏而已). 然后返回扩展结果.
    
        (defmacro inc (var)
          (list 'setq var (list '1+ var)))
        
        (macroexpand '(inc r))                  ; => (setq r (1+ r))
        
        (defmacro inc2 (var1 var2)
          (list 'progn (list 'inc var1) (list 'inc var2)))
        
        (macroexpand '(inc2 r s))               ; => (progn (inc r) (inc s))  ; `inc'并没有扩展
    
    environment参数为一个包含宏定义的alist. macroexpand在扩展宏时会使用environment中的宏定义替代当前环境下的宏定义.

-   (macroexpand-all macro-form &optional environment)
    
    类似macroexpand,但会递归扩展直到结果中不再包含宏为止.
    
        (defmacro inc (var)
          (list 'setq var (list '1+ var)))
        
        (macroexpand '(inc r))                  ; => (setq r (1+ r))
        
        (defmacro inc2 (var1 var2)
          (list 'progn (list 'inc var1) (list 'inc var2)))
        
        (macroexpand-all '(inc r s))           ; => (progn (setq r (1+ r)) (setq s (1+ s))) inc也扩展了

当对程序进行编译时,编译器在遇到宏调用时,会对宏进行扩展,因此:
-   要注意分清哪些操作应该放在宏扩展的过程中完成,哪些操作放在宏扩展后的结果中进行. 例如
    
        (defmacro my-set-buffer-multibyte (arg)
          (if (fboundp 'set-buffer-multibyte)
              (set-buffer-multibyte arg)))      ;在编译期执行该操作其实是没有意义的,应该改为`(set-buffer-multibyte ,arg)

-   不要在宏中对宏参数进行eval操作. 因为这时候宏参数还并未绑定任何实际参数.

-   由于编译器只对宏进行一次扩展,在其他使用宏的地方不再进行扩展动作,而在解释执行时会在每次宏调用时都对宏进行扩展. 因此宏扩展的过程,不能产生副作用,否则就会发生编译和解释执行结果不一致的情况. 例如:
    
        (defmacro empty-object ()
          (list 'quote (cons nil nil)))
        
        ;; 上面的宏在解释执行时,每次都会生成一个新的(nil).
        ;; 但在编译执行时,会在编译器生成一个(nil),然后每次都使用它

# 调试ELisp程序<a id="sec-21" name="sec-21"></a>

有以下几种调试Elisp程序的方法
-   若运行程序时抛出异常,可以使用Emacs内置的debugger或edebug
-   通过查看编译器定位问题.
-   使用ERT包来写回归测试
-   使用profile来定义性能关注点

## debugger<a id="sec-21-1" name="sec-21-1"></a>

### 配置何时进入debugger<a id="sec-21-1-1" name="sec-21-1-1"></a>

当Elisp程序运行时,若发生error,则根据配置项\`debug-on-error\`决定是否进入debugger.

-   配置项debug-on-error
    
    若值为t,则任何种类的error都会进入debugger.
    
    若值为nil,则任何种类的error都不会进入debugger
    
    若值为error conditon的列表,则只有指定种类的error会进入debugger

-   配置项debug-ignored-errors
    
    该变量在debug-on-error的基础上,屏蔽指定种类的error不触发debugger.
    
    该变量的值为一个由error condition和正则表达式组成的list. 任何符合error condtion的error,和error message匹配指定正则表达式的error,都不会触发debugger

-   配置项eval-expression-debug-on-error
    
    该配置项的值为t时,使用eval-expression命令时,会将debug-on-error的值临时改为t.
    
    若该配置项为nil,则不会修改debug-on-error的值.

-   变量debug-on-signal
    
    默认情况下,若error被condition-case所捕获,则不会进入debugger,但若该变量为非nil,则会先进入debugger,再被condition-case所捕获.
    
    当然,是否进入debugger,还要看debug-on-error和debug-ignored-errors的值
    
    一般不会使用该变量,而使用condition-case-unless-debug代替.

-   debug-on-event
    
    当Emacs捕获到指定event发生时,进入debugger

-   debug-on-message
    
    该变量为一个正则表达式,当在echo area显示了符合该正则的message时,进入debugger. 
    
    该变量常用于寻找引起特定message的原因.

-   配置项debug-on-quit
    
    当按下C-g时,会产生一个quit,quit和error不是一回事,因此quit默认是不进入debugger的.
    
    通过设置该值为非nil,则当quit发生时,进入debugger

-   命令(debug-on-entry function-symbol)
    
    该命令标注当指定的function被调用时,主动进入debugger(无论有没有error/quit发生)
    
        (defun fact (n)
          (if (zerop n) 1
            (* n (fact (1- n)))))               ; => fact
        (debug-on-entry 'fact)                  ; => fact
        (fact 3)                                ; => 进入debugger

-   命令(cancel-debug-on-entry &optional function-symbol)
    
    该函数取消debug-on-entry对指定function的操作.
    
    若function-symbol为nil,则表示debug-on-entry对所有函数的操作.

-   (debug &rest debugger-args)
    
    显式调用debugger. 程序执行到该语句,会立刻进入debugger.
    
    通常debugger只是把debugger-args的值显示在backtrace buffer的首部,以方便用户可以看到它.
    
    然而,有些debugger-arg有其特殊的意义:
    
    -   第一个参数为lambda
        
        当debugger是由于参数\`debug-on-next-call\`设置为非nil的情况下进入了函数而触发的,则该变量会显示为\`Debugger entered&#x2013;entering a function:\`
    
    -   第一个参数为debug
        
        当debugger是由于设置了参数\`debug-on-entry\`的情况下进入了函数而触发的,则该变量会显示为\`Debugger entered&#x2013;entering a function\`
    
    -   第一个参数为t
        
        当debugger是由于参数\`debug-on-next-call\`设置为非nil的情况下进入了函数而触发的,则该变量会显示为\`Debugger entered&#x2013;beginning evaluation of function call form\`
    
    -   第一个参数为exit,第二个参数为debug
        
        当debugger是由于之前被b标记过的stack frame退出而触发的情况下,会显示为\`Debugger entered&#x2013;returning value:\`加上返回的值
    
    -   第一个参数为error
        
        当debugger是由于error/quit未捕获而触发时,会显示为\`Debugger entered&#x2013;Lisp error:\`加上error的信息
    
    -   当第一个参数为nil
        
        TODO 不知道什么意思.

### debugger使用说明<a id="sec-21-1-2" name="sec-21-1-2"></a>

当进入debugger后,会有一个名为\*Backtrace\*的buffer出现. 

在该buffer的第一行显示了进入debugger的原因,下面是backtrace.

backtrace由一系列的stack frame组成,每行一个stack frame. 其中
-   光标所在的stack frame为当前frame,有些debugger命令会对当前frame进行操作
-   若某stack frame以\*开头,表示离开这个stack frame会再次调用debugger.
-   若stack frame中的函数名带了下划线,表示debugger可以找到该函数的源代码.

当进入debugger后,会根据\`eval-expression-debug-on-error\`的值来临时更改\`debug-on-error\`的值.若\`eval-expression-debug-on-error\`的值为t,则会设置debug-on-error的值为t. 这意味着在debug中触发的任意error都会产生一个backtrace. 若不想这样,可以设置\`eval-expression-debug-on-error\`为nil,或在\`debugger-mode-hook\`中设置\`debug-on-error\`为nil

Debugger中的命令:
-   c
    
    continue. 退出debugger,并且继续向下执行.

-   d
    
    步进一个S表达式,然后看步进的那个S表达式做了什么操作.

-   b
    
    为当前frame加上断点标记. 加了标志的frame,在行头会加上一个\*

-   u
    
    取消b命令为frame加上的断点标志.

-   j
    
    像b命令一样为当前frame加上标记,然后像命令c一样继续执行程序,但是在执行时会临时屏蔽\`debug-on-entry\`标记

-   e
    
    执行输入的S表达式. 通过该命令,可以修改debugger的变量.

-   R
    
    类似e,但是会把执行S表达式的结果,保存到一个名为\*Debugger-record\*的buffer中.

-   q
    
    退出debugger,退出程序的执行过程

-   r
    
    读取一个S表达式,并将其计算结果作为当前frame的返回值.
    
    当debugger是由于捕获到异常而触发时,无法使用该命令.

-   l
    
    列出会debug-on-entry的函数列表. 该列表根据\`debug-on-entry\`的值来过滤函数.

-   v
    
    显示/不现实当前stack frame中的局部变量

### debugger内部实现使用到的变量与函数<a id="sec-21-1-3" name="sec-21-1-3"></a>

-   debugger
    
    该变量的值需要是一个函数,当触发debugger时,实际上是通过调用该函数来实现的.
    
    该变量默认值为\`debug\`

-   (backtrace)
    
    This function prints a trace of Lisp function calls currently active.
    
        (defun show-back-trace()
          (backtrace))
        
        (show-back-trace)
        
        ;; ==================>
        backtrace()
        show-back-trace()
        eval((show-back-trace) nil)
        eval-last-sexp-1(nil)
        eval-last-sexp(nil)
        call-interactively(eval-last-sexp nil nil)
        command-execute(eval-last-sexp)

-   变量debug-on-next-call
    
    若该值为nil,则在执行下一个eval,apply或funcall之前,先会调用debugger.
    
    进入debugger后,会将该值设置为nil,但debugger中的d命令会将该变量设置为t

-   (backtrace-debug level flag)

-   变量command-debug-status
    
    该变量记录了当前interctive command的debug状态.

-   (backtrace-frame frame-number)

## edebug<a id="sec-21-2" name="sec-21-2"></a>

### 使用Edebug的一般步骤<a id="sec-21-2-1" name="sec-21-2-1"></a>

1.  引入函数/宏到edebug中来调试 
    
    将光标移动到要debug的函数/宏定义上,按下C-u C-M-x(eval-defun)
    
    一旦函数/宏被引入到edebug来调试,任何调用该函数/宏的操作都会触发edebug执行.

2.  Edebug跳转到定义Elisp源代码的buffer,且该buffer暂时变为只读的.

3.  使用Edebug命令开始调试,可以使用\`?\`来显示Edebug命令

4.  若不需要在用Edebug调试了,需要将函数/宏引出Edebug,方法是再执行一边函数/宏的定义即可.

### Edebug中的命令<a id="sec-21-2-2" name="sec-21-2-2"></a>

1.  Execution Mode

    Edebug在调试程序时,也支持各种execution modes. 但它并不是实际上的major-mode或minor-mode
    
    execution mode决定了Edebug下一次在哪里暂停,以及在暂停时显示多少执行的信息.
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="left">命令</th>
    <th scope="col" class="left">说明</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="left">S</td>
    <td class="left">Stop:不再往下执行程序,等待用户输入更多的Edebug命令(edebug-stop)</td>
    </tr>
    
    
    <tr>
    <td class="left"><SPC></td>
    <td class="left">Step:步进下一个语句(edebug-step-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">n</td>
    <td class="left">Next:跳到下一个Form(edebug-next-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">t</td>
    <td class="left">Trace:每执行一个语句(会在echo area显示每个语句执行的结果)就暂停一段时间(默认为1s,由参数\`edebug-sit-for-seconds\`确定)</td>
    </tr>
    
    
    <tr>
    <td class="left">T</td>
    <td class="left">Rapid trace:类似t,但并不暂停(edebug-Trace-fast-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">g</td>
    <td class="left">Go:继续执行直到下一个端口(edebug-go-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">c</td>
    <td class="left">Continue:继续执行,在每个断点处都停顿一下,然后继续执行(edebug-continue-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">C</td>
    <td class="left">Rapid continue:类似c,但在断点处并不停顿(edebug-continue-fast-mode)</td>
    </tr>
    
    
    <tr>
    <td class="left">G</td>
    <td class="left">Go non-stop:忽略断点的存在,继续执行程序.</td>
    </tr>
    </tbody>
    </table>
    
    在程序执行过程中,可以用S或其他命令暂停程序的执行

2.  Jumping命令

    Jumping系列命令告诉Edebug,让程序执行直到指定的位置
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="left">命令</th>
    <th scope="col" class="left">说明</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="left">h</td>
    <td class="left">执行到光标所在位置(edebug-goto-here)</td>
    </tr>
    
    
    <tr>
    <td class="left">f</td>
    <td class="left">执行一个sexp(edebug-forward-sexp)</td>
    </tr>
    
    
    <tr>
    <td class="left">o</td>
    <td class="left">执行完(跳出)当前的sexp(edebug-step-out)</td>
    </tr>
    
    
    <tr>
    <td class="left">i</td>
    <td class="left">进入form所调用的函数/宏定义(edebug-step-in)</td>
    </tr>
    
    
    <tr>
    <td class="left">&#xa0;</td>
    <td class="left">&#xa0;</td>
    </tr>
    </tbody>
    </table>

3.  Breaks

    在三种情况下,Edebug会暂停程序的执行:
    
    -   设置断点
        
        <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
        
        
        <colgroup>
        <col  class="left" />
        
        <col  class="left" />
        </colgroup>
        <thead>
        <tr>
        <th scope="col" class="left">命令</th>
        <th scope="col" class="left">说明</th>
        </tr>
        </thead>
        
        <tbody>
        <tr>
        <td class="left">b</td>
        <td class="left">设置断点(edebug-set-breakpoint),若带prefix argument,则该断点为临时断点</td>
        </tr>
        
        
        <tr>
        <td class="left">u</td>
        <td class="left">取消断点(edebug-unset-breakpoint)</td>
        </tr>
        
        
        <tr>
        <td class="left">x CONDITION-FORM <RET></td>
        <td class="left">设置条件断点,当运行CONDITION-FORM的结果为非nil时,断点生效(edebug-set-conditional-breakpoint). 若带prefix argument,则断点为零时断点</td>
        </tr>
        
        
        <tr>
        <td class="left">B</td>
        <td class="left">光标跳转到下一个断点处(edebug-next-breakpoint)</td>
        </tr>
        </tbody>
        </table>
        
        re-evaluting/reinstrumenting函数定义会移除之前的所有断点
        
        设置条件断点时,CONDITION-FORM抛出的error会被忽略,当成返回nil来看待.
        
        一般情况下,Edebug会在断点处暂停程序的执行. 然而,当Edebug处于Go-nonstop mode下时,会完全忽略断点.
    
    -   当某个条件(Global Condition)匹配时
        
        若变量\`edebug-global-break-condtion\`的计算结果为非nil则暂停程序的执行. 同样的,若计算过程中抛出error,则当返回nil处理.
        
        可以在edebug模式下使用X命令来设置该条件. 也可以在任何buffer的任何时候,通过C-x X X来调用(edebug-set-global-break-condition)设置该条件
    
    -   插入断点代码
        
        使用(edebug)主动调用edebug,进入断点模式.
        
        若执行(eedbug)时,该函数并未引入到edebug中,则该函数其实调用的是(debug)

4.  Evaluation

    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="left">命令</th>
    <th scope="col" class="left">说明</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="left">e EXP <RET></td>
    <td class="left">在Edebug的外部上下文环境中计算EXP(edebug-eval-expression)</td>
    </tr>
    
    
    <tr>
    <td class="left">M-: EXP <RET></td>
    <td class="left">在Edebug的上下文环境中计算EXP(eval-expression)</td>
    </tr>
    
    
    <tr>
    <td class="left">C-x C-e</td>
    <td class="left">在Edebug的外部上下文环境中计算光标前的expression(edebug-eval-last-sexp)</td>
    </tr>
    </tbody>
    </table>

5.  Evalution List Buffer

    在Edebug中可以按E命令,进入名为\*edebug\*的"evaluation list buffer".
    
    在该buffer中可以交互式的运行SEXP,且在该buffer中计算的SEXP,处于Edebug外部的上下文环境中.
    
    可以在该buffer中使用Lisp Interaction mode中的命令. 还可以执行以下命令:
    
    -   C-j (edebug-eval-print-last-sexp)
        
        在edebug的外部上下文环境中,计算光标前的expression,并将结果插入到当前buffer
    
    -   C-x C-e (edebug-eval-last-sexp)
        
        在edebug的外部上下文环境中,计算光标前的expression
    
    -   C-c C-u (edebug-update-eval-list)
        
        基于当前buffer的内容,创建新的evaluation list
        
        evalution list由多个evalutation list groups组成. 每个groups由多个Lisp expression组成,group之间使用注释行来区分.
        
        当edebug每次暂停程序执行时,每个evaluation list group中的地一个Lisp expression都会自动执行一遍.
        
            (current-buffer)
            #<buffer *scratch*>
            ;---------------------------------------------------------------
            (selected-window)
            #<window 16 on *scratch*>
            ;---------------------------------------------------------------
            (point)
            196
            ;---------------------------------------------------------------
            bad-var
            "Symbol's value as variable is void: bad-var"
            ;---------------------------------------------------------------
            (recursion-depth)
            0
            ;---------------------------------------------------------------
            this-command
            eval-last-sexp
            ;---------------------------------------------------------------
    
    -   C-c C-d (edebug-delete-eval-list)
        
        从evalution list中删除光标所在的group
    
    -   C-c C-w (edebug-where)
        
        切换回当前暂停点的原代码buffer处

6.  其他命令

    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="left" />
    
    <col  class="left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="left">命令</th>
    <th scope="col" class="left">说明</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="left">?</td>
    <td class="left">显示Edebug的帮助信息(edebug-help)</td>
    </tr>
    
    
    <tr>
    <td class="left">C-]</td>
    <td class="left">Abort one level back to the previous command level(\`abort-recursive-edit')</td>
    </tr>
    
    
    <tr>
    <td class="left">q</td>
    <td class="left">终止程序运行并退出edebug,但\`unwind-protect\`和\`condition-case\`中的代码还是会执行</td>
    </tr>
    
    
    <tr>
    <td class="left">Q</td>
    <td class="left">类似q,但\`unwind-protect\`和\`condition-case\`中的代码不会执行(edebug-top-level-nonstop)</td>
    </tr>
    
    
    <tr>
    <td class="left">r</td>
    <td class="left">重新在echo area中显示上次expression的运算结果(edebug-previous-result)</td>
    </tr>
    
    
    <tr>
    <td class="left">d</td>
    <td class="left">显示backtrace(但是不显示Edebug自己的function,并且此时处于标准debugger模式下),(edebug-backtrace)</td>
    </tr>
    
    
    <tr>
    <td class="left">&#xa0;</td>
    <td class="left">&#xa0;</td>
    </tr>
    </tbody>
    </table>

7.  捕获Errors

    默认情况下,若某函数被引入edebug中,则当该函数抛出error时,会自动激活edebug. 
    
    但可以通过配置变量\`edebug-on-error\`和\`edebug-on-quit\`来改变这一情况.

8.  Edebug Views

### Edebug中的输出格式<a id="sec-21-2-3" name="sec-21-2-3"></a>

当Edebug输出循环list结构时,可能会出错,这时需要设置一下几个变量

-   配置项edebug-print-length

-   配置项edebug-print-level

-   配置项edebug-print-circle

### Trace Buffer<a id="sec-21-2-4" name="sec-21-2-4"></a>

通过设置变量\`edebug-trace\`的值为非nil,可以使得Edebug将每次执行的过程都记录下来.

记录存储在名为\`\*edebug-trace\*\`的buffer中. 它记录了使用什么参数调用那个函数,返回值是什么.

## test coverage<a id="sec-21-3" name="sec-21-3"></a>

### 使用步骤<a id="sec-21-3-1" name="sec-21-3-1"></a>

通过testcover库,能够对代码进行铺盖面测试. 方法是:

1.  载入testcover库
    
    (require 'testcover)

2.  执行命令testcover-start
    
    M-x testcover-start <RET> FILE <RET>

3.  然后对你的代码进行测试

4.  测试完成后执行命令testcover-mark-all命令会高亮出覆盖面不完全的地方
    
    M-x testcover-mark-all

5.  使用命令testcover-next-mark跳转到下一个高亮点

### 高亮说明<a id="sec-21-3-2" name="sec-21-3-2"></a>

一般来说,红色的高亮表示这个地方从来没有测试过. 

棕色的高亮表示这个地方的计算结果每次都一样的,而这往往意味着测试得还不够充分.

### give advice to the test coverage too<a id="sec-21-3-3" name="sec-21-3-3"></a>

可以通过将代码包裹进一些宏(这些宏本身不会改变代码的执行结果)中,来告诉testcover一些信息.

-   (1value form)
    
    该宏告诉testcover,form的计算结果每次都应该一样的.

-   (noreturn form)
    
    该宏告诉testcover,form不应该返回. 若form返回了,会收到一个run-time error

## Profiling<a id="sec-21-4" name="sec-21-4"></a>

-   使用M-x profiler-start开启性能监控,然后选择监控cpu还是mem还是两者都监控.

-   执行操作,运行待测试的函数

-   执行M-x profiler-report显示性能检测结果.
    
    在报告中
    
    -   按j可以跳转到函数定义处.
    
    -   按d可以显示函数的documentation
    
    -   可以使用C-x C-w保存检测报告
    
    -   使用=比较两个检测结果

-   执行M-x profiler-stop结束监控过程

# Command Loop<a id="sec-22" name="sec-22"></a>

当进入Emacs后,Emacs会循环读取key sequences,读取对应的命令,并显示结果. 这个过程称为Command Loop.

## Command Loop概述<a id="sec-22-1" name="sec-22-1"></a>

1.  command loop第一步是调用函数\`read-key-sequence'来读取key sequence,并转换为一个command或keyboard macro.

2.  在执行command前,调用\`undo-boundary'来保存undo信息

3.  执行\`pre-command-hook'中的函数
    
    在执行command前,会触发\`pre-command-hook',这时变量\`this-command'的值为将要运行的command,而\`last-command'的值为上一次运行的command
    
    执行该hook参数时,不抛出quitting,也不抛出error,但会把抛出error的函数移除该hook

4.  Emacs通过调用\`command-execute'来读取传递給command的参数列表
    1.  若command为keyboard macro,则Emacs通过\`execute-kbd-macro'来执行command
    
    2.  若command为命令(interactively callable function),则通过\`call-interactively'来读取参数并执行command

5.  执行\`post-command-hook'中的函数
    
    在执行command后,会触发\`post-command-hook',这时变量\`this-command'的值为刚运行的command,而\`last-command'的值为再上一次运行的command
    
    执行该hook参数时,不抛出quitting,也不抛出error,但会把抛出error的函数移除该hook

## Command<a id="sec-22-2" name="sec-22-2"></a>

所谓Command,不仅仅指的带有top-level \`interactive' form的函数. 还可以是声明为interactive的autoload object,某些primitive functions,以及strings和vectors(被当成是keyboard macro来看待),

-   (commandp object &optional for-call-interactively)
    
    判断object是否为command
    
    若参数for-call-interactively为非nil,则只有在object能被\`call-interactively'调用时才返回t,这时keyboard macro返回nil

-   (command-execute command &optional record-flag keys special)
    
    执行command
    
    若command为string或vector,则被认为是keyboard macro,会使用\`execute-kbd-macro'执行command. 否则连同参数keys和record-flag一起传递給\`call-interactively'一起调用
    
    参数special,若为非nil,则表示忽略preifix argument但是不clear它. 常用来执行特殊event

-   命令(execute-extended-command prefix-argument)
    
    该命令使用\`completing-read'从minibuffer中读取命令,并用\`command-execute'执行该命令,并返回执行结果
    
    若读取的命令需要prefix argument,则会将参数prefix-argument传递給它.
    
    当用interactively的方式运行该命令时,参数prefix-argument的值就是传递給\`execute-extended-command'的prefix-argument
    
    默认情况下,M-x执行的就是该命令

## Disabling Commands<a id="sec-22-3" name="sec-22-3"></a>

"Disabling a Command"給一个command加上标记,运行command时实际上会调用\`disabled-command-function'所指向的函数,默认的行为是会要求用户确认是否执行该函数. 

被disable的command,其symbol的\`disabled'属性被设置为非nil,若\`disabled'属性为一个string,则警告信息中会包含该string

-   (enable-command command)
    
    允许command(symbol格式)不经确认就执行该command
    
    **该命令会同时修改init文件,使之在以后的session中也生效**

-   (disable-command command)
    
    使得command在之前,需要经过确认.
    
    **该命令会同时修改init文件,使之在以后的session中也生效**

-   变量disabled-command-function
    
    该变量的值为一个function. 当用户交互式的调用一个disabled command时,实际上调用的是该函数.
    
    在该function中可以使用\`this-command-keys'来探测用户实际的输入的key sequence,并以此来找到需要执行的函数.
    
    若值为nil,则disabled function跟普通function一样执行.

## Command History<a id="sec-22-4" name="sec-22-4"></a>

command loop会记录执行过的complex command的历史记录.

所谓complex command指的是其 **interactive argument** 会从minibuffer中读取参数值的command.(在执行command的过程中明确使用到minibuffer的,不算)

-   command-history
    
    记录了最近执行过的complex command的list

-   命令(repeat-complex-command N)
    
    编辑并重新执行最后执行过的/倒数第N个complex command

-   命令(list-command-history)
    
    列出在minibuffer中输入过的command的历史

## 如何分辨Command是否通过Interactive方式调用<a id="sec-22-5" name="sec-22-5"></a>

一个比较好的方法是在interactive form中设置某个标识为非nil. 例如

    (defun foo (&optional print-message)
      (interactive "p")
      (when print-message
        (message "foo")))

另一种方法是使用函数\`called-interactively-p'

-   (called-interactively-p kind)
    
    若正在执行的function是通过\`call-interactively'调用的,则返回t
    
    参数kind只能是'interactive或'any
    
    若参数kind为'interactive,则只有当function是直接由用户调用的情况下,才返回t(例如if the user typed a key sequence bound to the calling function, but <span class="underline">not</span> if the user ran a keyboard macro that called the function)
    
        (defun foo ()
          (interactive)
          (when (called-interactively-p 'any)
            (message "Interactive!")
            'foo-called-interactively))
        
        ;; Type `M-x foo'.
        -| Interactive!
        
        (foo)                                   
        => ni
    
    若参数kind为'any,则包括keyboard macro在内,也返回t
    
        (defun bar ()
          (interactive)
          (message "%s" (list (foo) (called-interactively-p 'any))))
        
        ;; Type `M-x bar'.
        -| (nil t)

## generic command<a id="sec-22-6" name="sec-22-6"></a>

第一次执行用M-x COMMAND<RET>来执行generic command,Emacs会提示你选择哪一种具体实现,并保存选择信息,下一次就不会询问了. 若执行时带了prefix argument,则又会重复该过程.

COMMAND的不同实现存储在变量\`COMMAND-alternatives'中,只有在该变量存在时,才能使用宏\`define-alternatives'定义COMMAND的另一个实现方式.

If CUSTOMIZATIONS is non-\`nil', it should consist of alternating \`defcustom' keywords (typically \`:group' and \`:version') and values to add to the declaration of \`COMMAND-alternatives'.

-   宏(define-alternatvies comand &rest customizations)
    
    定义新命令COMMAND,参数COMMAND为一个symbol

## 获取Command Loop中的信息<a id="sec-22-7" name="sec-22-7"></a>

-   last-command
    
    上次运行的command名称
    
    当一个command从command loop中退出时,会从\`this-command'中复制该值

-   real-last-command
    
    类似\`last-command',但不会被Lisp程序所修改

-   last-repeatable-command
    
    类似\`last-command'但不保存input event. 这里面保存的是\`repeat'命令会重复执行的command

-   this-command
    
    正在执行的命令名称,但有些命令会在执行时人工修改该值

-   this-original-command
    
    类似this-command,但当command remapping发生时,\`this-command'存储的是实际运行的command名称,而\`this-original-command'存储的是触发的原始command的名称

-   (this-command-keys)
    
    返回调用command的key sequence,返回类型为string或vector
    
    但若command调用了\`read-key-sequence',则返回的是最后读取到的key sequence
    
        (this-command-keys)
        ;; Now use `C-u C-x C-e' to evaluate that.
        => "^U^X^E"

-   (this-command-keys-vector)
    
    类似\`this-command-keys',只是返回的值总是vector

-   (clear-this-command-keys &optional keep-record)
    
    This function empties out the table of events for \`this-command-keys' to return.  
    
    Unless KEEP-RECORD is non-\`nil', it also empties the records that the function \`recent-keys' will subsequently return.
    
    一般常用于读取一个密码后

-   last-nomenu-event
    
    该变量斥候最后发生的input event(不包括mouse menu event)
    
    使用该变量的一个场景是用来告诉\`x-popup-menu'在哪里弹出一个menu. 在\`y-or-n-p'内也用到了该变量值

-   last-command-event
    
    This variable is set to the last input event that was read by the command loop as part of a command
    
    在\`self-insert-command'中用到该变量来决定插入哪个character
    
        last-command-event
        ;; Now use `C-u C-x C-e' to evaluate that.
        => 5
        
        ;; The value is 5 because that is the ASCII code for `C-e'.

-   last-event-frame
    
    该变量记录了最后的input event是在哪个frame中调用的.
    
    Usually this is the frame that was selected when the event was generated, but if that frame has redirected input focus to another frame, the value is the frame to which the event was redirected.

## Command的prefix argument<a id="sec-22-8" name="sec-22-8"></a>

prefix argument有两种表现形式:"raw"和"numeric". coomand loop内部,和lisp变量使用raw表现形式

Here are the possible values of a raw prefix argument:

-   \`nil', meaning there is no prefix argument.  
    Its numeric value is 1, but numerous commands make a distinction between \`nil' and the integer 1.

-   An integer, which stands for itself.

-   A list of one element, which is an integer.  
    This form of prefix argument results from one or a succession of \`C-u's with no digits.  
    The numeric value is the integer in the list, but some commands make a distinction between such a list and an integer alone.

-   The symbol \`-'.  
    This indicates that \`M&#x2013;' or \`C-u -' was typed, without following digits.  
    The equivalent numeric value is -1, but some commands make a distinction between the integer -1 and the symbol \`-'.

-   (prefix-numeric-value arg)
    
    这里的arg为raw格式的prefix argument. 该函数将arg转换为对应的numeric格式.
    
    若arg为nil,则返回1
    
    若arg为-,则返回-1
    
    若arg为数字,则返回该数字
    
    若arg为list,则返回(car arg)

-   current-prefix-arg
    
    该变量存储的是当前命令的raw prefix argument.
    
    command可以直接检查该变量的值,但大多数是使用\`(interactive "P")'来获取该参数的值

-   prefix-arg
    
    下一个命令使用的raw prefix argument.
    
    类似\`universal-argument'这样的函数,通过设置该变量来为接下来要执行的命令设置prefix argument

-   last-prefix-arg
    
    上一个command的raw prefix argument

-   (universal-argument)
    
    该命令读取用户的输入,并将用户的输入值设置为变量\`prefix-arg'的值,这样就为下一个待执行的command设置了prefix argument
    
    小心使用该函数

-   (digit-argument arg)
    
    This command adds to the prefix argument for the following command.  
    The argument ARG is the raw prefix argument as it was before this command; 
    it is used to compute the updated prefix argument.

-   (negative-argument arg)
    
    This command adds to the numeric argument for the next command.
    The argument ARG is the raw prefix argument as it was before this command; 
    its value is negated to form the new prefix argument

## Quitting<a id="sec-22-9" name="sec-22-9"></a>

当Lisp函数正在运行时,可以按下\`C-g',让Emacs退出当前的工作.

然而当command loop在等待keyboard input时,按下C-g并不会引发quitting,Emacs只是把它当成一个普通的input character.

when \`C-g' follows a prefix key, they combine to form an undefined key. The effect is to cancel the prefix key as well as any prefix argument.

而当在minibuffer中输入时,\`C-g'的意义又不一样,它中断并退出minibuffer

\`C-g'通过设置变量\`quit-flag'为t来表示要quit,Emacs检查该变量的值并产生quitting

若想在执行Lisp函数时阻止quitting的产生,只需要将变量\`inhibit-quit'绑定为非nil值即可.这时,即使\`quit-falg'设置为t,依然不会产生quitting

-   quit-flag
    
    该值为非nil,除非\`inhibit-quit'被设置为非nil,否则Emacs立即退出当前执行的任务.

-   inhibit-quit
    
    当\`quit-flag'设置为非nil时,该变量决定Emacs是否执行退出

-   宏(with-local-quit body&#x2026;)
    
    该宏执行body,执行过程中,即使\`inhibit-quit'设置为非nil,也运行产生quitting. 
    
    若body运行过程中,被quitting中断,则返回nil,否则返回最后语句的执行结果.
    
    若进入\`with-local-quit'时,\`inhibit-quit'为nil,则执行body时若产生quitting,则Emacs设置\`quit-flag'并产生一个普通quit.
    
    若进入\`with-local-quit'是,\`inhibit-quit'为非nil,这时普通的quitting被推迟. 非nil的\`quit-flag'会触发一种特殊的quit&#x2013;local quit. 它会终止body的执行并退出\`with-local-quit'. **退出\`with-local-quit'后的\`quit-flag'依然为非nil**.

-   (keyboard-quit)
    
    该函数设置产生quit的条件,默认绑定到C-g

## Keyboard Macro<a id="sec-22-10" name="sec-22-10"></a>

一个"keyboard macro"指的是一系列的input event,这一系列的input event可以认为是一个command.(A "keyboard macro" is a canned sequence of input events that can be considered a command and made the definition of a key)

keyboard macro的lisp表现形式为一个string或由event组成的vector

-   (execute-kbd-macro kbdmacro &optional count loopfunc)
    
    把kbdmacro当作一系列的event来执行. 
    
    若kbdmacro为string或vector,则就好像用户直接输入一样.  The sequence is <span class="underline">not</span> expected to be a single key sequence
    
    若kbdmacro为symbol,则执行该symbol的函数定义,若该symbol的函数定义还是一个symbol,则不断的递归下去. 最终,其函数定义应该是一个string或vector,否则会抛出error
    
    参数count表示重复执行多少次kdbmacro,若count为nil,则执行一次,若count为0,表示执行无穷多次
    
    若loopfunc为非nil,则配次循环都会不带参数调用该函数,或函数返回nil,则停止执行该macro

-   executing-kbd-macro
    
    当前正在执行的kbd-macro,nil表示没有在执行kbd-macro

-   defining-kbd-macro
    
    只有当正在定义的kbd-macro的情况下,该值才为非nil.
    
    该值为'append表示正在为现有的macro添加定义( The value is \`append' while appending to the definition of an existing macro)
    
    命令\`start-kbd-macro',\`kmacro-start-macro'和\`end-kbd-macro'会设置该值&#x2013;尽量不要自己去设置该值
    
    The variable is always local to the current terminal and cannot be buffer-local

-   last-kbd-macro
    
    最近所定义的kbd-macro

-   kbd-macro-termination-hook
    
    当keyboard macro执行完成后触发该hook(不管是正常结束还是异常结束都触发)

# InputEvent<a id="sec-23" name="sec-23"></a>

Emacs Command Loop读取一系列的"input event"来表示键盘/鼠标的动作,或发送给Emacs的系统事件.

表示键盘动作的event,用char或symbol的格式表示. 其他类型的event统一用list来表示.

-   (eventp object)
    
    若object为input event或event type,则返回非nil
    
    需要注意的是,任何symbol既可以用来作为event,也可以作为event type,因此eventp不能区分一个symbol是被用于作为event,还是event type.

## Keyboard Event<a id="sec-23-1" name="sec-23-1"></a>

键盘输入可以分为两类:普通的按键和功能键. 

### 普通按键事件<a id="sec-23-1-1" name="sec-23-1-1"></a>

普通按键产生的event,在lisp中用character来表示. 

The event type of a character event is the character itself (an integer)

一个input character event由"basic code"(取值范围从0到524287)加上"modifier bits"组成

modifier bits包括:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">说明</th>
<th scope="col" class="left">值</th>
<th scope="col" class="left">说明</th>
</tr>
</thead>

<tbody>
<tr>
<td class="left">meta</td>
<td class="left">2\*\*27</td>
<td class="left">&#xa0;</td>
</tr>


<tr>
<td class="left">control</td>
<td class="left">2\*\*26</td>
<td class="left">C-a这样的已经定义在ASCII中的控制字符,由于已经有了特定的basic code了,因此Emacs不需要使用special bit来指示它</td>
</tr>


<tr>
<td class="left">shift</td>
<td class="left">2\*\*25</td>
<td class="left">对于字符,数字和标点来说,basic code中已经定义相关的shift key按下后的对应键值,对于这些按键,Emacs不使用special bit</td>
</tr>


<tr>
<td class="left">hyper</td>
<td class="left">2\*\*24</td>
<td class="left">&#xa0;</td>
</tr>


<tr>
<td class="left">super</td>
<td class="left">2\*\*23</td>
<td class="left">&#xa0;</td>
</tr>


<tr>
<td class="left">alt</td>
<td class="left">2\*\*22</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
</table>

最好不要直接在程序中使用specific bit(因为这些bit的位置可能会改变)

应该使用\`event-modifiers'函数来测试specific bit是否被设置

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">简写形式</th>
<th scope="col" class="left">说明</th>
</tr>
</thead>

<tbody>
<tr>
<td class="left">A-</td>
<td class="left">alt</td>
</tr>


<tr>
<td class="left">C-</td>
<td class="left">control</td>
</tr>


<tr>
<td class="left">H</td>
<td class="left">hyper</td>
</tr>


<tr>
<td class="left">M-</td>
<td class="left">meta</td>
</tr>


<tr>
<td class="left">S-</td>
<td class="left">shift</td>
</tr>


<tr>
<td class="left">s-</td>
<td class="left">super</td>
</tr>
</tbody>
</table>

### 功能键事件<a id="sec-23-1-2" name="sec-23-1-2"></a>

功能键event在elisp中用symbol来表示. 一般来说,symbol的名称就是功能键的label(全小些形式). 例如<F1>产生的input event表示为符号'f1

The event type of a function key event is the event symbol itself

还有一些功能键event的表示与功能键的label不一致的情况:

-   \`backspace',\`tab',\`newline',\`return',\`delete'

-   \`left',\`up',\`right',\`down'
    
    光标箭头按键

-   \`kp-add',\`kp-decimal',\`kp-divide',&#x2026;
    
    右边小键盘的加减乘除

-   \`kp-0',\`kp-1',&#x2026;
    
    右边小键盘的数字键

-   \`kp-f1',\`kp-f2'&#x2026;
    
    右边小键盘的fn

-   \`kp-hoome',\`kp-left',\`kp-up',\`kp-right',\`kp-down'
    
    右边小键盘的对应功能键

-   \`kp-prior',\`kp-next',\`kp-end',\`kp-begin',\`kp-insert',\`kp-delete'
    
    右边小键盘的对应功能键

### 以字符串表示keyboard event<a id="sec-23-1-3" name="sec-23-1-3"></a>

现在一般不建议使用string来表示keyboard event,最好使用vector代替. 

可以使用函数\`listify-key-sequence'来讲string格式的keyboard event转换为list,方便解析出其中的内容.

需要注意:当使用字符串来表示keyboard event时,只有Meta modifier才能以'\M-'的格式表示在string中,其他modifier都无法表示.

下面是一些转换规则:

-   若keyboard character的值范围为0到127,则可以直接写进string
-   若上面的keyboard character同时按下了meta键(即2\*\*27 到 2\*\*27+127),则需要转换为(2\*\*7到2\*\*7+127)
-   若是大于256的非ASCII字符,可以包含进multibyte string中
-   其他字符(128-255范围的字符)无法用string表示.

## Mouse Events<a id="sec-23-2" name="sec-23-2"></a>

Emacs支持4种鼠标事件:click event,drag event,button-down event和motion event.

所有的鼠标事件都用list来表示,且(car list)为event type(提供了按下的是哪个鼠标按键,同时有哪个modifier key被按下了,这些信息). (cdr list)则提供了位置与时间的信息

需要注意的是,鼠标事件是由鼠标所在buffer的keymap来处理的,而不是光标所在的buffer的keymap来处理.

### 点击事件<a id="sec-23-2-1" name="sec-23-2-1"></a>

点击事件的结果为'(EVENT-TYPE PSITIION CLICK<sub>COUNT</sub>)

其中:

-   EVENT-TYPE
    
    该symbol标识鼠标的哪个按键被点击,可选值为'mouse-1,'mouse-2,'mouse-3
    
    当然,也可以通过添加前缀\`A-',\`C-',\`H-',\`M-',\`S-'和\`s-'来标识点击时同时按下了哪个modifier key
    
    该symbol同时也作来标识event的event type

-   POSTION
    
    POSTION具体的格式,根据点击的位置而不同. 
    
    当点击在text area,mode-line,header-line或area的边界时,POSTION的格式为:
    
        (WINDOW POS-OR-AREA (X . Y) TIMESTAMP
        OBJECT TEXT-POS (COL . ROW)
        IMAGE (DX . DY) (WIDTH . HEIGHT))
    
    其中:
    
    -   WINDOW
        
        表示点击的那个window
    
    -   POS-OR-AREA
        
        若点击的位置在text area内,则表示点击处的buffer postion
        
        否则,它的值为表示window area的symbol:'mode-line,'header-line,'vertical-line,'left-margin,'right-margin,'left-fringe,'right-fringe
    
    -   X,Y
        
        点击的位置相对text area左上角的坐标
    
    -   TIMESTAMP
        
        事件发生的时间
    
    -   OBJECT
        
        若点击的位置没有string类型的text property,则为nil.
        
        否则为'(点击位置的带属性string . string的位置)
    
    -   TEXT-POS
        
        对于点击在marginal area或fringe上时,该值为对应行第一个字符的buffer postion.
        
        其他情况下,则就是当前buffer position
    
    -   COL,ROW
        
        点击位置相对text area左上角的行列数
    
    -   IMAGE
        
        若点击的位置是一个IMAGE,则该值为\`find-image'返回的image object
        
        否则为nil
    
    -   DX,DY
        
        若OBJECT为nil,为点击的位置相对点击到的字符左上角的坐标
        
        否则,为点击的位置相对OBJECT左上角的坐标
    
    -   WIDTH,HEIGTH
        
        OBJECT的宽度与高度,若OBJECT为nil,则为点击处文本的宽度与高度
    
    若点击的地方为scroll bar,则POSTION的格式为
    
        (WINDOW AREA (PORTION . WHOLE) TIMESTAMP PART
    
    其中:
    
    -   WINDOW
        
        点击到的scroll bar所属的window
    
    -   AREA
        
        为'vertical-scroll-bar
    
    -   PORTION
        
        从scrollbar的最顶端到点击位置的长度,以像素为单位
        
        On some toolkits, including GTK+, Emacs cannot extract this data, so the value is always \`0'.
    
    -   WHOLE
        
        scrollbar的整个长度,以像素为单位
        
        On some toolkits, including GTK+, Emacs cannot extract this data, so the value is always \`0'.
    
    -   TIMESTAMP
        
        事件发生的时间
    
    -   PART
        
        点击在了scrollbar的哪个位置,可以为'handle,'above-handle,'below-handle,'up,'down

-   CLICK-COUNT
    
    快速点击的次数

### 拖拽事件<a id="sec-23-2-2" name="sec-23-2-2"></a>

拖拽事件的格式为:

    (EVENT-TYPE
     (WINDOW1 START-POSITION)
     (WINDOW2 END-POSITION))

EVENT-TYPE以\`drag-'为前缀,例如\`drag-mouse-1'表示按下mouse button 1来拖动

根据是否按下了Modifier Key,还可以在\`drag-'前添加\`C-',\`M-'&#x2026;等前缀.

WINDOW和POSTION的值,则跟点击事件定义一样

若\`read-key-sequence'接收到一个拖拽事件,但发现并没有相应的key binding绑定到这个事件上,而相应的点击事件有binding. 则会自动将拖拽事件转换为点击事件.

### Button-Down事件<a id="sec-23-2-3" name="sec-23-2-3"></a>

Button-Down事件的格式与Click事件格式一样,都是

    (EVENT-TYPE PSITIION CLICK_COUNT)

不同点在于EVENT-TYPE是以\`down-'作为前缀的,根据是否按下Modifier key,在\`down-'前还有\`C-'和\`M-'前缀

\`read-key-sequence'忽略任何没有command binding的buton-down event.

### Repeat Event<a id="sec-23-2-4" name="sec-23-2-4"></a>

若快速点击同一个mouse botton而不移动mouse位置的话,则Emacs产生"repeat event"

最常见的"repeat event"就是"double-click" event(双击事件)

双击事件的EVENT-TYPE以\`double-'为前缀,根据modifier key是否按下,可能在\`double-'前添加\`M-',\`S-'等前缀

当用户执行双击时,其实产生了两个事件,第一个是普通的单击事件,第二个为双击事件. 因此在处理双击事件前单击事件的相关命令已经执行了.

同理,若点击一次鼠标之后立即按下鼠标并拖动鼠标,则产生了\`double-drag' event.

而,在\`double-click' event和\`double-drag' event产生前,Emacs还会产生\`double-down' event.

**总结起来,一次双击动作会产生4个事件** :down event->click event->double-down event->double-click event.

**一次double-drag动作也会产生4个事件** :down event->click event->double-down event->double-drag event.

同理,还有\`triple-down',\`triple-click'和\`triple-drag'

**Emacs最多只产生triple-click event**. 

若想知道精确的点击几次button,使用函数\`event-click-count'

-   (event-click-count event)
    
    获取event中鼠标点击的次数

-   配置项double-click-fuzz
    
    定义了两次双击之间,位置不能超过的像素数

-   配置项double-click-time
    
    定义了两次双击之间,不超过的时间,以毫秒为单位
    
    nil表示直接不探测multi-click
    
    t表示无限时间.

### Motion Events<a id="sec-23-2-5" name="sec-23-2-5"></a>

在运行\`trace-mouse'的body时,不按mouse botton的情况下移动mouse,会产生"mouse motion" event,它的格式为:

    '(mouse-movement POSITION)

这里的POSITION跟点击事件中的POSITION一样

在trace-mouse之外的情况下,emacs不产生mouse motion event

### Focus Events<a id="sec-23-2-6" name="sec-23-2-6"></a>

当切换frame时,会产生Focus Event. 它的格式为:

    '(switch-frame NEW-FRAME)

这里NEW-FRAME为新切换到的frame

由于在一系列按键序列中间产生一个focus event会扰乱原按键序列的执行,因此Emacs不会在key sequence中间产生focus event.

若用户在key sequence中间更改了focus,则Emacs会重新排列event,将focus event放在multi-event key sequence的最前面或最后面.

### 其他System Event<a id="sec-23-2-7" name="sec-23-2-7"></a>

若用户在key sequence中间发生了下面的那些system event,则Emacs会重新排列event,将这些system event放在multi-event key sequence的最前面或最后面.

-   '(delete-frame (FRAME))
    
    表示用户对FRAME发送了关闭命令

-   '(iconify-frame (FRAME))
    
    iconify某个FRAME,默认的定义为\`ignore'

-   '(make-frame-visible (FRAME))
    
    表示用户deiconified FRAME,默认为\`ignore'

-   '(wheel-up POSITION) / '(wheel-down POSITION)
    
    滚动鼠标wheel时产生的event. 
    
    POSITION的结构跟Click Event的POSITION一样,标识了event发生时的鼠标位置
    
    这种event只在某些操作系统上会产生,有些操作系统上产生的是\`mouse-4'和\`mouse-5' event. 
    
    因此,为了可移植性,建议使用定义在\`mwheel.el'中的变量\`mouse-wheel-up-event'和\`mouse-wheel-down-event'来代替

-   '(drag-n-drop POSITION FILES)
    
    当从Emacs外选择了一些文件,并拖到Emacs frame中时产生\`drag-n-drop' event
    
    这里POSITION的格式跟click event中的POSITION一样.
    
    FILES为文件名称的列表.

-   '(help-echo FRAME HELP WINDOW OBJECT POS)
    
    但光标移动到buffer中带有\`help-echo' text property的文本时,产生该event

-   'sigusr1 / 'sigusr2
    
    当Emacs收到信号\`SIGUSR1'和\`SIGUSR2'时触发该event. 一般用于调试时使用
    
    要捕获user signal,绑定相应的event到\`special-event-map'中的命令. 这时会不带参数地执行该命令,而signal event可以通过变量\`last-input-event'来获得. 例如
    
        (defun sigusr-handler ()
          (interactive)
          (message "Caught signal %S" last-input-event))
        
        (define-key special-event-map [sigusr1] 'sigusr-handler)

-   '(language-change FRAME CODEPAGE LANGUAGE-ID)
    
    在MS-Windows下才更改input language会产生该event. 
    
    这里FRAME表示改变input language时的当前frame.
    
    CODEPAGE为更改为的新codepage number
    
    LANGUAGE-ID为新input language的数字id
    
    例如:
    
        ;; Get the abbreviated language name, such as "ENU" for English
        (w32-get-locale-info language-id)
        ;; Get the full English name of the language,
        ;; such as "English (United States)"
        (w32-get-locale-info language-id 4097)
        ;; Get the full localized name of the language
        (w32-get-locale-info language-id t)

## 特殊Events<a id="sec-23-3" name="sec-23-3"></a>

特殊Event在非常底层的地方被处理&#x2013;as soon as they are read.

\`read-event'函数内部就会消化掉这些event,而不会返回这种event. 事实上,\`read-event'会一直等待并返回地一个非特殊event

特殊event不会被显示出来,不会被纳入key sequence中,不会存入\`last-command-event'和\`(this-command-keys)'. 
特殊event They do not discard a numeric argument, they cannot be unread with \`unread-command-events', they may not appear in a keyboard macro, and they are not recorded in a keyboard macro while you are defining one.

然而在读取到特殊event时,会记录在\`last-input-event'中,and this is the way for the event's definition to find the actual event.

常见的特殊event type有\`iconify-frame',\`make-frame-visible',\`delete-frame',\`drag-n-drop',\`language-change'以及用户信号\`sigusr1',\`sigusr2'&#x2026;

定义如何处理特殊event的keymap为变量\`special-event-map'

## 区分Events<a id="sec-23-4" name="sec-23-4"></a>

每个event都有一个"event type",用于区分event.

对于keyboard event,event type就是event value

对于list格式的event,event type为(car list)

相同的event type运行相同的命令. 键序列与event type绑定

-   (event-modifiers event)
    
    返回一个list,包含了该event中所有的modifiers,modifier的类型为symbol,
    它的值可能是'shift,'control,'meta,'alt,'hyper和'super
    对于mouse event来说,还可能包括'click,'drag,'down,'double,'triple
    
    参数event可以是一个event对象,也可以是个event type.
    
    If EVENT is a symbol that has never been used in an event that has been read as input in the current Emacs session, then \`event-modifiers' can return \`nil', even when EVENT actually has modifiers.
    
        (event-modifiers ?a)                    ; => nil
        (event-modifiers ?A)                    ; => (shift)
        (event-modifiers ?\C-a)                 ; => (control)
        (event-modifiers ?\C-%)                 ; => (control)
        (event-modifiers ?\C-\S-a)              ; => (control shift)
        (event-modifiers 'f5)                   ; => nil
        (event-modifiers 's-f5)                 ; => (super)
        (event-modifiers 'M-S-f5)               ; => (meta shift)
        (event-modifiers 'mouse-1)              ; => (click)
        (event-modifiers 'down-mouse-1)         ; => (down)

-   (event-basic-type event)
    
    返回去掉modifier标志之后的event描述. 例如
    
        (event-basic-type ?a)                   ; => 97
        (event-basic-type ?A)                   ; => 97
        (event-basic-type ?\C-a)                ; => 97
        (event-basic-type ?\C-\S-a)             ; => 97
        (event-basic-type 'f5)                  ; => f5
        (event-basic-type 's-f5)                ; => f5
        (event-basic-type 'M-S-f5)              ; => f5
        (event-basic-type 'down-mouse-1)        ; => mouse-1
    
    -   (mouse-movement-p object)
        
        object是否为mouse movent event
    
    -   (event-convert-list list)
        
        This function converts a list of modifier names and a basic event type to an event type which specifies all of them.  
        The basic event type must be the last element of the list. 
        例如:
        
            (event-convert-list '(control ?a))      ; => 1,C-a
            (event-convert-list '(control meta ?a)) ; => -134217727
            (event-convert-list '(control super f1)) ; => C-s-f1

## 获取Mouse Events中的信息<a id="sec-23-5" name="sec-23-5"></a>

要想获得mouse event中的position list,可以使用以下两个函数

-   (event-start event)
    
    若为drag event,则返回start-postion
    
    若为click或button-down event,则返回唯一的那个postion

-   (event-end event)
    
    若为drag event,则返回end-postion
    
    若为click或button-down event,则返回唯一的那个postion

-   (posnp object)
    
    判断object是否为mouse position

下面的函数,一mouse postion list为参数,返回相应部分的值

-   (posn-window postion)
    
    返回postion list中的window

-   (posn-area position)
    
    返回position中的window area标志
    
    若event发生在text-area则返回nil,否则返回表示area的symbol

-   (posn-point position)
    
    返回position中的buffer位置信息.
    
    当event发生在text-area,marginal area或fringe上时,返回一个表示buffer位置的整数
    
    其他情况下,返回值意义不明确

-   (posn-x-y position)
    
    以'(X . Y)的形式返回相对(posn-window postion)的坐标,单位为像素.
    
    下面的例子,演示了如何将相对window的坐标转换为相对frame的坐标
    
        (defun frame-relative-coordinates (position)
          "Return frame-relative coordinates from POSITION.
                  POSITION is assumed to lie in a window text area."
          (let* ((x-y (posn-x-y position))
                 (window (posn-window position))
                 (edges (window-inside-pixel-edges window)))
            (cons (+ (car x-y) (car edges))
                  (+ (cdr x-y) (cadr edges)))))

-   (posn-col-row postion)
    
    以'(COL . ROW)的格式返回buffer postion在text area中的列与行
    
    它是根据(postion-x-y postion)的信息与frame的默认字符的宽度和默认行的高度,计算出来的.
    
    需要注意的是,ROW是从text area的最顶端开始计算的,也就是说,如果(position-window positon)拥有header line,则它不会计算如ROW中

-   (posn-actual-col-row postion)
    
    以'(COL . ROW)的形式返回真正的相对(posn-window postion)的列数与行数

-   (posn-string positiion)
    
    返回position中的string object,可能为nil或'(STRING . STRING-POS)

-   (posn-image position)
    
    获得position中的image object,可能为nil或'(image&#x2026;)

-   (posn-object position)
    
    返回position中的string object或image object,可能为nil或'(STRING . STRING-POS)或'(image&#x2026;)

-   (posn-object-x-y position)
    
    获取相对POSITION list中的'(DX . DY). 即位置相对(posn-object position)的坐标. 单位为像素
    
    若position为buffer position,则返回相对该处字符左上角的坐标.

-   (posn-object-width-height position)
    
    以'(WIDTH. HEIGHT)格式,返回(posn-object position)的宽度和高度,单位为像素
    
    若position为buffer position,则返回位置处字符的宽度和高度

-   (posn-timestamp position)
    
    返回position中的timestamp信息,表示事件发生的时间戳,以毫秒为单位

以下函数根据buffer position或screen position,计算出position list

-   (posn-at-point &optional pos window)
    
    该函数返回position list用于表示参数pos在参数window中的位置. 若pos在window中不可见,则返回nil
    
    参数pos默认为参数window中光标的位置
    
    参数window默认为选中的window

-   (posn-at-x-y x y &optional frame-or-window whole)
    
    该函数返回position list用于表示(x . y)在参数frame-or-window中的相对坐标,
    
    参数x,y是相对frame-or-window的以像素为单位的位置.
    
    参数frame-or-window,默认为当前window
    
    若参数为nil,则坐标是相当与window text area来计算的. 否则计算包括整个window area(text-rea+scroll bar+margin+fringe)

## 获取scroll bar event中的信息<a id="sec-23-6" name="sec-23-6"></a>

-   (scroll-bar-event-ratio event)
    
    以格式'(PORTION .WHOLE)返回event在scroll-bar中的位置.

-   (scroll-bar-scale ratio total)
    
    该函数事实上将参数ratio与total相乘,并将结果约为整数.
    
    这里参数ration不是数字,而是格式为'(NUM . DENOM)的cons ceil. 一般该值由函数scroll-bar-event-ration返回.
    
    该函数用于将scroll bar position转换为buffer postion是很方便:
    
        (+ (point-min)
           (scroll-bar-scale
            (posn-x-y (event-start event))
            (- (point-max) (point-min))))

## 捕获Input Event<a id="sec-23-7" name="sec-23-7"></a>

-   (read-key-sequence prompt &optional continue-echo dont-downcase-last switch-frame-ok command-loop)
    
    该函数读取key sequence并以string或vector的形式返回.
    
    该函数会一直读取key sequence直到获取到一个完整的key sequence为止(即在当前keymap下能定位到某个command)
    
    需要注意的是: **以mouse event开头的key sequence,是在mouse所在的window中keymap中查找对应command的**
    
    参数prompt为提示信息,nil表示没有提示
    
    参数continue-echo表示当key sequence不完整时,是否显示已经输入的key sequence
    
    默认情况下,任何upper case event在找不到对应command时,会转换为lower case event再去查找一遍(这是会设置变量\`this-command-keys-shift-translated'为t),参数dont-downcase-last禁止这种转换
    
    参数swith-frame-ok表示在输入key sequence的过程中,是否能切换frame
    
    参数command-loop若为非nil,则表示可以一次输入多个key sequence(一个key sequence与command想对应). nil表示只读取表示一个key sequence
    
    \`read-key-sequence'会压抑住quitting,也就是说,在输入\`C-g'时,就好像其他普通的字符一样,不会去设置quit-flag
    
    **当使用\`read-key-sequence'读取mouse event时,若mouse event发生在window的非text area中,则会添加prefix-key来表示该area**:'header-line,'horizontal-scroll-bar,'menu-bar,'mode-line,'vertical-line,'vertical-scroll-bar
    
        (read-key-sequence "Click on the mode line: ")
                  => [mode-line
                      (mouse-1
                       (#<window 6 on NEWS> mode-line
                        (40 . 63) 5959987))]

-   (read-key-sequence-vector prompt &optional continue-echo dont-downcase-last switch-frame-ok command-loop)
    
    与\`read-key-sequence'类似,只是肯定以vector类型返回

-   num-input-keys
    
    当前Emacs session目前为止处理过的key sequence的数量.

-   (read-event &optional prompt inherit-input-method seconds)
    
    该函数只读取一个event,而不像\`read-key-sequence'一样可能读取多个event.
    
    The returned event may come directly from the user, or from a keyboard macro.  
    It is not decoded by the keyboard's input coding system 
    
    参数prompt为提升信息
    
    若参数inherit-input-method为非nil,则支持用当前输入法输入non-ASCII字符. 否则会禁用输入法
    
    参数seconds表示等待输入的超时秒数,若超时还未有event发生,则返回nil. 
    若参数seconds为nil,则Emacs在等待用户输入时被认为处于idle状态,若设置了值,则等待期间不会认为处于idle状态.
    
    If \`read-event' gets an event that is defined as a help character, then in some cases \`read-event' processes the event directly without returning.
    
    Certain other events, called "special events", are also processed directly within \`read-event'

-   (read-char &optional prompt inherit-input-method seconds)
    
    读取并返回输入的character. 若用户产生的event不是character(例如点击事件或功能键事件),则\`read-char'会抛出一个错误

-   (read-char-exclusive &optional prompt inherit-input-method seconds)
    
    类似\`read-char',只是当读到的event不是character时,会忽略这个event,接着读取下一个event,而不是抛出错误

-   num-nonmacro-input-events
    
    该变量存储了到目前为止从terminal读取到的input events总数(那些由keyboard macro)产生的不算.

-   (read-key &optional prompt)
    
    该函数读取single key. 它处于\`read-key-sequence'和\`read-event'之间.
    
    跟\`read-key-sequence'不同之处在于,它读取single key而不是完整的key sequence
    
    跟\`read-event'不同之处在于,它会根据\`input-decode-map',\`local-function-key-map'和\`key-translation-map'解码并转换用户的输入.

-   (read-char-choice prompt chars &optional inhibit-quit)
    
    该函数使用\`read-key'读取并返回一个character. 它会忽略任何不是参数chars中的member的character.
    
    chars为一个由characters组成的list. 表示可接受的character范围.

-   (read-quoted-char &optional prompt)
    
    类似\`read-char',只是当读取的地一个character是一个8进制数时(0-7),它会读取接下来输入的所有8进制数,并返回由这些8进制numeric character code所表示的character.
    
        (read-quoted-char "What character")
        
        ---------- Echo Area ----------
        What character 1 7 7-
        ---------- Echo Area ----------
        
        => 127

## Modifying and Translating Input Events<a id="sec-23-8" name="sec-23-8"></a>

在使用\`read-event'时,Emacs会根据\`extra-keyboard-modifiers'的值对读取到到的event做改变(modify),然后根据\`keyboard-translate-table'的值做转换(translate)

-   extra-keyboard-modifiers
    
    该变量允许Lisp程序模拟按下键盘上的modifier key. 
    
    该变量的至必须为一个设置了modifier bit位的character(例如'?\C-\M-a'). 真正其作用的是其中的modifier bit(?\C-\M-).
    
    若变量的值为\`?\C-@',不会设置Ctrl被按下,相反, **这个值表示取消所有的modification**
    
    另外,需要注意的是, **该变量只会修改从keyboard读取到的event,而对mouse event或其他类型的event无效**

-   keyboard-translate-table
    
    该变量为terminal-local variable. 它允许你将一个keyboard event重新映射成另一个keyboard event
    
    一般情况下,它的值为一个char-table或nil. 
    
    Note that this translation is the first thing that happens to a character after it is read from the terminal.  
    Record-keeping features such as \`recent-keys' and dribble files record the characters after translation.

-   (keyboard-translate from to)
    
    该函数通过修改\`keyboard-translate-table'的值来达到将character code FROM转换为character code TO的目的.

## Event Input的其他特性<a id="sec-23-9" name="sec-23-9"></a>

-   unread-command-events
    
    该变量存储的值为一个由event组成的list,表示待读取的event.
    
    该list中的event,以显示的顺序(即最前面的最先被使用)被读取,并且在使用后被删除
    
    一般情况下,从该list中读取的event不会添加到当前命令的key sequence中(即不会被\`this-command-keys'),因为该event在第一次读取时已经添加过一次了.
    但若list中的element格式为'(t . EVENT)则表示强制将该event放入当前command的key sequence中

-   (listify-key-sequence key)
    
    该函数将key(string或vector)转换为由单独event组成的list,可以很容易的将这个list放入\`unread-command-events'中

-   (input-pending-p &optional check-timers)
    
    该函数检查是否有command input可以被读取了.
    
    若参数check-timers为非nil,则若没有input可以被读取时,运行Emacs运行已经ready的timers

-   last-input-event
    
    该变量存储最后的terminal input event. whether as part of a command or explicitly by a Lisp program.
    
    在下面的例子中,这段Lisp程序读取字符'1'(ASCII码为49). 假设我们用C-x C-e来执行这段代码,则会发现\`last-input-event'的值为'1'(49),而\`last-command-event'只为?\C-e(5)
    
        (progn (print (read-char))
                   (print last-command-event)
                   last-input-event)
                 -| 49
                 -| 5
                 => 49

-   宏(while-no-input body&#x2026;)
    
    当运行body的过程中没有输入时,正常执行body并返回body的值.
    
    但若执行body的过程中有输入到来,则会中断body的执行(类似quit),并返回t
    
    若执行body的过程中,被真正的quit所打断,则返回nil
    
    若BODY中某部分绑定\`inhibit-quit'为非nil,则即使有输入到来,也不会中断该部分代码的执行,直到该部分代码被执行完毕.

-   (discard-input)
    
    该函数丢弃terminal input buffer的内容并取消正在处理的keyboard macro,并返回nil
    
    例如:
    
        (progn (sleep-for 2)                    ;在等待期间,用户可能输入了一些东西
               (discard-input))                 ;会丢弃用户在等待期间所输入的东西
               => nil

# 关于输入法<a id="sec-24" name="sec-24"></a>

读取event的函数会调用当前使用的输入法. 但\`read-event'读取一个print character(包括<SPC>)时,会以该character作为参数,调用\`input-method-function'所表示的函数

-   input-method-function
    \`read-event'读取一个print character(包括<SPC>)时,会以该character作为参数,调用\`input-method-function'所表示的函数
    
    该input-method-function的返回值应该是一系列由event组成的list. 若返回nil表示没有输入,这样\`read-event'会等待下一个event产生.
    
    若input-method-function中又调用了\`read-event'或\`read-key-sequence',则需要记住把\`input-method-function'的值绑定为nil,否则会发生无限递归.
    
    The input method function is not called when reading the second and subsequent events of a key sequence.  
    Thus, these characters are not subject to input method processing.  
    The input method function should test the values of \`overriding-local-map' and \`overriding-terminal-local-map'; 
    if either of these variables is non-\`nil', the input method should put its argument into a list and return that list with no further processing.

# Keymaps<a id="sec-25" name="sec-25"></a>

input event与command的对应关系被记录在名为"keymaps"的结构体中. 每个event type对应一个command或另一个keymap. 

当一个event type绑定到另一个keymap时,这个keymap被用于查找下一个input event的对应关系.

若某个event sequence找到的是一个keymap,则我们称该key sequence为"prefix key". 否则则为"complete key". 

这个从event sequence一直找到某个command的过程,被成为"key lookup"

Emacs中有三类keymap:

-   global map
    
    由所有buffer所共享

-   local keymap
    
    由buffer指定的major mode所决定,会覆盖global map的key sequence

-   minor mode keymaps
    
    由buffer所开启的minor mode所决定,会覆盖global map和local keymap的key sequence

## Key Sequences<a id="sec-25-1" name="sec-25-1"></a>

"Key sequence",简称为"key",是指一个或多个input event做组成的序列集合. input event包括characters,function keys,mouse actions或system events

当用vector来表示key sequences时,每个vector的元素都是character,每个character表示一个input event. 例如\`[?\C-x ?l]'表示key sequence \`C-x l'

-   (kbd keyseq-text)
    
    将string类型的keyseq-text转换为key sequence.
    
        (kbd "C-x") => "\C-x"
        (kbd "C-x C-f") => "\C-x\C-f"
        (kbd "C-x 4 C-f") => "\C-x4\C-f"
        (kbd "X") => "X"
        (kbd "RET") => "\^M"
        (kbd "C-c SPC") => "\C-c "
        (kbd "<f1> SPC") => [f1 32]
        (kbd "C-M-<down>") => [C-M-down]

# Number相关函数<a id="sec-26" name="sec-26"></a>

-   判断是否为自然数(0+正整数)
    
    (natnump object)

-   判断是否为0
    
    (zerop number)

-   取余数
    
    (% dividend divisor)
    
    %的参数必须是整数,对于任何两个整数dividend和divisor都有(+(% DIVIDEND DIVISOR) (\* (/ DIVIDEND DIVISOR) DIVISOR)) == DIVIDEND
    
    (mod dividend divisor)
    
    mode的参数可以是Float型,它的返回值的正负号与DIVISOR一致,并且mod的商值使用floor进行截断到整数,然后再计算返回的余值.
    
    (+ (mod DIVIDEND DIVISOR) (\* (floor DIVIDEND DIVISOR) DIVISOR)) == DIVIDEND

-   三角函数
    -   (sin arg)
    
    -   (cos arg)
    
    -   (tan arg)
    
    -   (asin arg)
    
    -   (acos arg)
    
    -   (atan y &optional x)

-   指数计算
    -   (exp arg)
        e的arg次方
    
    -   (expt x y)
        x的y次方
    
    -   (log arg &optional base)
        base默认为e,取arg的指数
    
    -   (aqrt arg)
        取arg的平方根,若arg<0,则返回NaN
    
    -   常量float-e
    
    -   常量float-pi

-   获取随机值
    (random &optional limit)
    -   若limit为正整数，则返回0到limit的随意整数
    
    -   若limit为t，则表示使用当前时间和Emacs的进程号重新选择一个种子
    
    -   若limit为一个字符串，它表示使用string的内容作为种子

# 二进制函数<a id="sec-27" name="sec-27"></a>

二进制函数只能作用于Integer型参数.

-   逻辑位移
    (lsh Integer count)
    
    lsh是logical shift的缩写,它向左移动count位(若count为负数,则表示向右移动), 使用0填充

-   算术位移
    (ash Integer count)
    
    ash是arithmetic shift的缩写,它跟lsh类似,但当对负数进行右移时,使用符号位进行填充,即该函数不会改变Integer的正负号

-   and操作
    (logand &rest ints-or-markers)
    
    对所有Integer的所有位做and操作,若没有参数,则返回-1,即所有位都是1的Integer

-   or操作
    (logior &rest ints-or-markers)
    对所有Integer的所有位做or操作,若没有参数,则返回0,即所有位都是0的Integer

-   xor操作
    (logxor &rest ints-or-markers)
    对所有Integer的所有位做xor操作,若没有参数,则返回0,即所有位都是0的Integer
-   not操作
    (lognot integer)
    对Integer的所有位做not操作

# 字符串处理相关函数<a id="sec-28" name="sec-28"></a>

  Emacs has only very few functions that takes a string as argument. Any non-trivial string processing is done with a buffer. Use with-temp-buffer, then insert your string, process it, then use
buffer-string to get the whole buffer content.

## 判断函数<a id="sec-28-1" name="sec-28-1"></a>

-   (stringp object)
-   (string-or-null-p object)
-   (char-or-string-p object)
-   (string-prefix-p prefix str &optional ignore-case)
-   (string-suffix-p suffix str &optional ignore-case)
-   (compare-strings str1 start1 end1 str2 start2 end2 &optional ignore-case)
    
    比较的区间为[start end),start为nil则默认为0,end为nil则表示字符串的结尾.
    
    该函数会把unibyte string先转换为multibyte string再进行比较.
    
    若比较的区间,两个string是相等的,则返回t.
    若str1<str2,则返回负数,若str1>str2则返回正数. 
    该整数的绝对值指示了不同点开始的地方

## 获取字符串的函数<a id="sec-28-2" name="sec-28-2"></a>

-   (make-string count character)
    
    count必须为整数，返回由count个character组成的字符串

-   (string &rest characters)
    
    返回由characters组成的字符串

-   带text properties截取子字符串
    
    (substring myStr startIndex &optional endIndex)
    
    startIndex和endIndex若为负数,则表示从尾部开始往回数.
    
    因此(substring str 0)表示返回str的一个copy,但推荐用copy-sequence代替
    
    substring中的参数str也可以是一个vector,例如
    
        (substring [a b (c) "d"] 1 3)           ; => [b (c)]
    
    若string带有text properties,则新产生的string也会带有text properties

-   不带text properties截取字符串
    
    (substring-no-peroperties string &optional start end)

-   组合字符串
    
    (concat &rest sequences) 返回连接多个字符串的字符串
    
        (concat "abc" (list 120 121) [122])     ; => "abcxyz"
    
    (mapconcat function sequence separator)
    
    对sequence的每个元素都调用function,然后将结果用separator concat起来作为字符串返回.当function为'identity时则起到join的作用
    
        (mapconcat 'identity '("abc" "123" "one" "two" "three") " ") ;=>"abc 123 one two three"
-   从buffer获取字符串
    
    (buffer-substring myStartPos myEndPos)
    
    (buffer-substring-no-properties myStartPos myEndPos)

-   获取光标所在位置的内容
    
    (thing-at-point THING),这里THING指明了各种类型:
    
    (thing-at-point 'word) // 光标所在位置的单词
    
    (thing-at-point 'symbol) // 光标所在位置的单词(包括连字符和下划线)
    
    (thing-at-point 'line) // 光标所在位置的行, **一般情况下它获取一行及行结束符,然而若光标处于行的最后一个字符,则不获取行结束符**
    
    (thing-at-point 'sexp) // 光标所在位置的s表达式
    
    (thing-at-point 'sentence) // 光标所在位置的句子
    
    (thing-at-point 'defun) // 光标所在位置的函数
    
    (thing-at-point 'url) // 光标所在位置的url, **若url不以http开头,则会自动加上http**
    
    &#x2026;还有很多类型

-   获取光标所在THING的开始/结束位置
    
    (bounds-of-thing-at-point THING)

-   从报文中截取字符串
    
    (setq myStr (buffer-substring startPos endPos))

## 字符串操作<a id="sec-28-3" name="sec-28-3"></a>

-   获取字符串长度
    
    (string-width myStr)
    
    这里要注意的是，不能用(lenth myStr)来获取字符串长度
    
        (length "我的")                         ;=>2
        (string-width "我的")                   ;=>4

-   修改字符串内容
    
    由于字符串是character的数组,因此最基础的修改字符串内容的函数是使用(aset str idx char)来将str的地idx位置的内容替换为char. 
    由于字符串是数组,而数组的长度是不可变的,因此若替换的character和被替换的character的字节数不相同,则会报错
    
        (setq str "我的")
        (aset str 0 ?\m)                        ;str变为了"m的"
    
    (store-substring str idx string-or-char)
    
    使用string-or-char从idx开始替换str的内容,若替换的内容过长,则会报错
    
        (setq str "我的")
        (store-substring str 0 ?n)              ;str变为"n的"
        (store-substring str 1 "nm")            ;会raise args-out-of-range error

-   清空字符串
    
    (clear-string str)
    该函数会使得str变为二进制字符串,并且将内部结构清空为0
    
        (setq str "我的")
        (clear-string str)                      ;=>str现在为"      "

-   判断字符串是否匹配某正则表达式
    
    (string-match myRegex myStr)

-   获取捕获到的分组内容
    
    (match-string N myStr) ,这里myStr可以忽略,表示在buffer中作的查询. 但若上一次的匹配使用string-match函数作的,则需要该参数

-   对字符串进行正则替换
    
    (replace-regexp-in-string myRegex myReplacement myStr)  ;这里myReplacement可以是一个函数,该函数接收匹配的字符串,然后返回要替换的字符串

-   split字符串
    
    (split-string myStr &optiional mySepeartor omit-nulls)
    
    根据separator拆分myStr,默认值为变量\`split-string-default-separators\`的值(默认为"[ \f\t\n\r\v]+")
    
    若omit-nulls为t则在组成list时,会忽略空字符串.
    
    若希望把字符串分解为(split-string-and-unquote "cd 'abc edf'")

-   字符串正则替换
    
    (replace-regexp-in-string myRegxp myReplace myStr)

-   

## Format函数<a id="sec-28-4" name="sec-28-4"></a>

-   %s
    object的输出格式,但是不带引号. 若object为带text properties的string,则text properties也被复制进去了.
-   %S
    object的输出格式,带引号
-   %.Ns / %.NS
    截取字符串的前N位显示
-   %o
    8进制的Integer型
-   %d
    十进制的Integer型
-   %x
    十六进制的Integer型,字母用小些形式
-   %X
    十六进制的Integer型,字母用大写形式
-   %c
    输出Character
-   %e
    使用指数形式表示Float型
-   %f
    使用小数形式表示Float型
-   %g
    使用指数或小数形式表示Float型,使用哪种表示方式就看哪个更简短.
-   %%
    %

# list相关函数<a id="sec-29" name="sec-29"></a>

## 判断函数<a id="sec-29-1" name="sec-29-1"></a>

-   (consp object)
    object是否为cons cell. 一般情况下,list就是cons cell,但nil比较特殊,虽然它是list,但不是cons clell
-   (atom object)
    nil即是atom,也是list
-   (listp object)
    object是否为list
-   (nlistp object)
    object是否不是list
-   (null object)
-   (memq object list)
    判断list中是否包含object,它返回list中第一次出现object的位置.函数名中的q表示使用 **eq** 作为比较函数.
-   (memql object list)
    类似memq,但是函数名中的ql表示使用 **eql** 作为比较函数.
-   (member object list)
    类似memq,但是使用 **equal** 作为比较函数
-   (member-ignore-case str list)
    类似member,但参数str必须是string类型,并且比较时不区分大小写,单字节字符串也被转换为多字符串进行比较.

## 获取list中的元素<a id="sec-29-2" name="sec-29-2"></a>

-   (car-safe object)
    它与car不同点在于,若object不是cons ceil,则car会报错,而car-safe只是返回nil
-   (cdr-safe object)
    它与cdr不同点在于,若object不是cons ceil,则cdr会报错,而cdr-safe只是返回nil
-   (pop list)
    弹出list中的第一个元素
-   (nth n list)
    返回list中的第n个元素(从0开始计算), 若n为负数,则返回list中的第一个元素.
-   (nthcdr n list)
    返回第n个cdr后的list,若n为0或负数,则返回原list
    
        (nthcdr 2 '(1 2 3 4))                   ;=>(3 4)
        (nthcdr 10 '(1 2 3 4))                  ;=>nil
        (nthcdr -3 '(1 2 3 4))                  ;=>(1 2 3 4)
-   (last list &optional n)
    返回list中最后n个元素组成的list,默认n=1
    
        (last '(1 2 3 4 5) )                    ;=>(5)
        (last '(1 2 3 4 5) 3 )                  ;=>(3 4 5)
-   (safe-length list)
    对于circular list,只能表示list的长度最大不会超过safe-length返回的值,而不是实际值.
-   (butlast l &optional n)
    返回l去掉了后面n个元素后的列表,默认n为1
    
        (butlast '(1 2 3 4) 1)                  ;=>(1 2 3)
        (butlast '(1 2 3 4) 2)                  ;=>(1 2)
-   (nbutlast l &optional n)
    类似(butlast,但是会同时更改l的值

## 创建cons cell和list<a id="sec-29-3" name="sec-29-3"></a>

-   (cons obj1 obj2)
    cons一般用来将一个元素添加到某个list中的头部.
    
        (cons 1 '(2 3 4))                       ;=>(1 2 3 4)
-   (list &rest objects)
-   (make-list n object)
    返回由n个object组成的list
    
        (make-list 3 2)                         ;=>(2 2 2)
-   (append &rest sequences)
    将所有的sequences中的元素串在一起组成一个list, 需要注意的是,出了最后一个参数以外,其他的参数都被copy一份,用于与最后那个参数进行连接. 
    
        (setq trees '(pine oak))                ;=>(pine oak)
        (setq more-trees (append '(maple birch) trees)) ;=>(maple birch pine oak)
        (eq trees (last more-trees 2))                  ;=>t
    
    通过在最后的参数后添加nil,可以让所有的参数都强制copy
    
    最后的参数在处理上会有些特殊,最后一个参数只是单纯的被安置到前面参数组成list的cdr位置,例如
    
        (append '(x y) [z])                     ;=>(x y . [z]),最后的参数只是放在cdr的位置而已,因此最终结果不是(x y z)
-   (reverse list)
-   (copy-tree tree \*optional vecp)
-   (number-sequence from &optional to step)
    返回一个number list,值的范围为从from开始到to结束,步进为step(默认为1)
    
        (number-sequence 4 9)                   ;=>(4 5 6 7 8 9)
    
    若to为nil或与from相等,则返回单元素列表(from)
    
    若step为0,且to不为nil或与from的值相等,则elisp会报出错误,因为这会产生一个死循环
    
    若step不为0,而from累加step永远不会超过或到达to,则函数返回nil
    
        (number-sequence 8 5 1)                 ;nil
        (number-sequence 5 8 -1)                    ;nil

## 修改list变量<a id="sec-29-4" name="sec-29-4"></a>

### 会破坏原参数中的值<a id="sec-29-4-1" name="sec-29-4-1"></a>

这里的函数都会直接修改参数中的list
-   (push element list)
    把element放在list的第一位,作用类似cons
-   (add-to-list listname element &optional append compare-fn)
    类似push,但若list中已经有了element,则保持list不变
    
    若append为非nil,则将element放在list的最后位置
    
    compare-fn默认使用equal进行比较
-   (add-to-ordered-list listname element &optional order)
    这里的order需要是number类型,
    
    order的值决定了element的位置,若order为nil,则将element放在list中最后带order的元素后面
    
        (setq foo nil)
        (add-to-ordered-list 'foo 'a 1)         ;=>(a)
        (add-to-ordered-list 'foo 'c 3)         ;=>(a c)
        (add-to-ordered-list 'foo 'b 2)         ;=>(a b c)
        (add-to-ordered-list 'foo 'b 4)         ;=>(a c b)  若element已经存在,且设定了order,则使用新orde放置element的位置
        (add-to-ordered-list 'foo 'd)           ;=>(a c b d)
        (add-to-ordered-list 'foo 'e)           ;=>(a c b e d)
        (add-to-ordered-list 'foo 'f)           ;=>(a c b f e d)  若order为nil,则将element放在list中最后带order的元素后面
-   (setcar cons-ceil object) / (setcdr cons-ceil object)
    修改cons-ceil的car/cdr部分,并返回参数object作为返回值
    
    通过setcdr可以实现删除/添加list中element的目的
    
        (setq x1 '(a b c d))
        (setcdr x1 (cddr x1));=>'(a c d)
        (setcdr x1 (append '(1 2) (cdr x1)))    ;=> (a 1 2 c d)
-   (nconc &rest lists)
    类似append,所不同的是它直接修改所有参数的last element的cdr,而不会先做copy-sequence操作.
    
    由于除了最后一个参数不用被修改之外,其他参数的结构都会被修改,因此除了最后一个参数可以是const list外,其他参数必须是个变量.
    
    跟append一样的,最后一个参数可以不是list
    
        (setq x '(1 2 3))                       ; => (1 2 3)
        (nconc x 'z)                            ; => (1 2 3 . z)
        x                                       ; => (1 2 3 . z)
-   (nreverse list)
    翻转参数list
-   (sort list predicate-less)
    使用predicate-less进行从小到大的排序,若存在相等的值,则保持相等值的位置不变
    
        (setq x1 '(1 2 4 3 7 6 5));=>(1 2 4 3 7 6 5)
        (sort x1 '<)     ;=>(1 2 3 4 5 6 7)
    
    这里的predicate-less为比较函数,它接收两个参数,并判断第一个参数是否小于第二个参数.
    
    predicate-less函数必须有下面两个特性:
    
    1.  A<B,则B!<A
    
    2.  若A>B,B>C,则A>C
    
    **注意:**
    
    sort有一个很变态的特性:sort函数会让参数list依然指向原来的哪个cons-cell的位置,而不管这个cons-cell是否在sort后依然是处于第一个元素的位置. 例如
    
        (setq x1 '(9 8 7 2 3))
        (sort x1 '<)                            ;=>(2 3 7 8 9)
        x1                                      ;=>(9),注意,x1实际上依然指向了9这个cons cell的位置
    
    **因此一般情况下,都需要把sort的返回结果赋值回参数list**
-   (delq object list)
    移除list中所有与object相等的element,函数中的q表示使用eq作为比较函数.
    
    由于delq在删除list头部的element时,仅仅是返回跳过头部element的cdr位置,而不会改变list参数所指向的位置.
    
        (setq x1 '(a b c))
        (delq 'a x1)                            ;=>(b c)
        x1                                      ;=>(a b c)
    
    **因此使用delq,一般我们也需要将返回值赋值回参数list**
-   (delete object seq)
    delete函数比较特殊,它根据seq的类型不同而有不同的行为.
    
    当seq为list类型时,它跟delq一样会修改seq的值,所不同的是它使用equal作为比较函数.
    
    当seq为vector或string,则delete不会修改原seq的值
    
        (setq l '((2) (1) (2)))
        (delete '(2) l)                         ; => ((1))
        l                                       ; => ((2) (1))
        ;; If you want to change `l' reliably,
        ;; write `(setq l (delete '(2) l))'.
        (setq l '((2) (1) (2)))
        (delete '(1) l)                         ; => ((2) (2))
        l                                       ; => ((2) (2))
        ;; In this case, it makes no difference whether you set `l',
        ;; but you should do so for the sake of the other case.
        (setq v [(2) (1) (2)])
        (delete '(2) v)             ; => [(1)]
        v                           ; => [(2) (1) (2)]
-   (delete-dups list)
    删除list中所有重复的元素,使用equal作为比较函数. 
    
    当list中有多个重复元素时,delete-dups保留第一个元素.

### 不破坏原参数的值<a id="sec-29-4-2" name="sec-29-4-2"></a>

-   (remq object list)
    类似delq,但不改变原参数list的值. 这里的q也表示使用eq作为判断函数.
-   (remove object seq)
    类似函数delete,但它保证不修改参数seq的值
-   ()

## alist相关函数<a id="sec-29-5" name="sec-29-5"></a>

### 获取alist<a id="sec-29-5-1" name="sec-29-5-1"></a>

-   (copy-alist alist)
    拷贝alist的一个副本(two-level deep copy)

### 根据key取key-value键值对<a id="sec-29-5-2" name="sec-29-5-2"></a>

-   (assoc key alist)
    
    当使用assoc在alist中取键值对时,只会取发现的第一个符合条件的键值对. 因此可以直接用push命令将要修改为的新键值对放到alist的前面,以此来模拟对老键值对的修改,同时保留了老键值对的历史.
    
        (assoc 'garden *nodes*)
    
    assoc使用equal函数作为比较函数

-   (assq key alist)
    类似assoc,但函数名中的q表示使用eq作为比较函数. 一般用于key为symbol类似时,因为eq速度比equal快得多.

### 根据value查找key-value键值对<a id="sec-29-5-3" name="sec-29-5-3"></a>

-   (rassoc value alist)
    
    rassoc也使用equal作为比较函数.

-   (rassq value alist)
    
    类似rassoc,但是函数名中的q标识用eq作为比较函数

-   (assoc-default key alist &optional test default)
    
    assoc-default与其他assoc系列函数不同之处在于, **它直接返回key部分,而且它也比较不为cons cell的element**.
    
    若alist中某element为atom,则该element整个被用于与可以进行比较,且使用default作为返回值.
    否则若element为cons cell,则使用(car element)进行比较. 使用(cdr element)作为返回值.
    
        (setq x1 '(0 (1 "one") (2 "two")(3 "three" )))
        (assoc-default 1 x1);=>("one")
        (assoc-default 0 x1 'equal "zero") ;=>"four"
        (assoc-default 4 x1) ;=>nil
    
    test为比较函数,默认为equal

### 更新新值/添加新值<a id="sec-29-5-4" name="sec-29-5-4"></a>

使用push将新键值对放入alist中即可

    (push '(old-key new-value) *alist*)
    (push '(new-key new-value) *alist*)

### 删除键值对<a id="sec-29-5-5" name="sec-29-5-5"></a>

-   根据key删除
    (assq-delete-all key alist)
    
    类似delq的alist版,他可能会也可能不会修改原alist的结构,因此 **需要将返回值赋值回原参数alist**
    
    函数名中的q表示比较时使用eq函数

-   根据value删除
    (rassq-delete-all value alist)
    
    类似assq-delete-all,但是它比较value而不是key

## Property list相关函数<a id="sec-29-6" name="sec-29-6"></a>

-   判断plist中是否存在指定的property
    (plist-member plist property)
    
    返回plist中指向property的位置. 使用eq作为
    
        (plist-member '((1) "one" 2 two) 2)     ;=>(2 two)

-   返回plist中匹配参数property的value值
    (plist-get plist property)
    
    该函数使用eq作为比较函数
    
        (plist-get '(foo 4) 'foo)               ; => 4
        (plist-get '(foo 4 bad) 'foo)           ; => 4
        (plist-get '(foo 4 bad) 'bad)           ; => nil
        (plist-get '(foo 4 bad) 'bar)           ; => nil
    
    (lax-plist-get plist property)
    
    类似plist-get,但是该函数使用equal来作为比较函数

-   增加/修改plist中的键值对
    (plist-put plist peroperty value)
    
    该函数可能/可能不会修改原参数plist的结构.因此你需要把返回值重新赋值回原plist中
    
        (setq my-plist '(bar t foo 4))               ; => (bar t foo 4)
        (setq my-plist (plist-put my-plist 'foo 69)) ; => (bar t foo 69)
        (setq my-plist (plist-put my-plist 'quux '(a))) ; => (bar t foo 69 quux (a))
    
    (lax-plist-put plist property value)
    类似plist-put函数,但是使用equal作为比较函数来决定是添加还是更新值

# 环状结构体相关函数<a id="sec-30" name="sec-30"></a>

有时我们会使用一种环状结构体来存储数据,我们可以插入数据到环状结构体中,也可以删除,旋转环状结构中的数据,还可以遍历数据或者根据索引的模值访问数据(在这种环状结构体中,最新插入的数据索引为0,然后从新到就以此累加).

elisp提供了名为\`ring\`的package,供我们方便操作这种环状结构体. 

-   (make-ring size)
    创建一个大小为size的环状结构

-   (ring-p object)
    判断object是否为环状结构体

-   (ring-size ring)
    获取该ring上实际包含了多少数据

-   (ring-elements ring)
    把ring中的数据,从新到旧,以list的形式返回

-   (ring-emplty-p ring)
    判断ring是否为空

-   (ring-ref ring index)
    根据索引,查找ring中相应的值.
    
    最新插入的数据索引为0,然后从新到旧依次累加.
    
    索引也可以为负数,-1表示最旧插入的数据,-2表示第二旧的数据,以此类推.

-   (ring-insert ring object)
    往ring中插入object,该object作为最新插入的数据,它的索引为0.
    
    若ring中的数据已经满了,则该操作会同时删除最旧的那个数据
    
    该函数的返回值为object

-   (ring-insert-at-beginning ring object)
    往ring中插入数据,但该数据被作为最旧的数据项来处理.
    
    若ring中的数据已经满了,则该操作会删除最旧的那个数据.

-   (ring-remove ring &optional index)
    除并返回ring中的数据. index若为nil则表示最旧的数据

-   若能够保证不超出ring的容量,则可以使用ring结构体作为先进先出队列来使用.例如
    
        (let ((fifo (make-ring 5)))
          (mapc (lambda (obj) (ring-insert fifo obj))
                '(0 one "two"))
          (list (ring-remove fifo) t
                (ring-remove fifo) t
                (ring-remove fifo)))
        ;; => (0 t one t "two")

# Sequences相关函数<a id="sec-31" name="sec-31"></a>

-   (sequencep object)
    判断object是否为sequence

-   (length sequence)
    获取sequence中的element个数
    
    需要注意的是length不能对点列表和环形列表求长度,但是可以用safe-length代替

-   (elt sequence index)
    返回sequence中index所标示的element(index从0开始标示)
    
    若index的值不为0到(1- (length sequence)),则若参数sequence不是list,则elisp报\`args-out-of-range\`错误
    
        (string (elt "1234" 2))                 ; => "3"
        (elt [1 2 3 4] 4)                       ; error--> Args out of range: [1 2 3 4], 4
        (elt [1 2 3 4] -1)                      ; error--> Args out of range: [1 2 3 4], -1

-   (copy-sequence sequence)
    创建sequence的一个新的引用.
    
    这里引用的意思在于新的copy与原sequence共同指向一个结构,即:若对拷贝添加信新的元素,并不会对原sequence进行修改,但若对原element进行修改会同时影响原sequence,反之依然.
    
        (setq y (copy-sequence x))              ; => [foo (1 2)]
        (eq x y)                                ; => nil
        (equal x y)                             ; => t
        (eq (elt x 1) (elt y 1))                ; => t
        
        ;; Replacing an element of one sequence.
        (aset x 0 'quux)                        ; x => [quux (1 2)] ; y => [foo (1 2)]
        
        ;; Modifying the inside of a shared element.
        (setcar (aref x 1) 69)                  ; x => [quux (69 2)] ; y => [foo (69 2)]
    
    copy-sequence不能用于点列表和环形列表,可以用copy-tree函数拷贝点列表,但无法复制环形列表

-   (append aVector nil)
    append函数提供了一种将sequence转换为list的方法
    
        (setq avector [1 two (quote (three)) "four" [five]]) ; => [1 two (quote (three)) "four" [five]]
        (append avector nil)                                 ; => (1 two (quote (three)) "four" [five])

## Array相关函数<a id="sec-31-1" name="sec-31-1"></a>

-   (arrayp object)
    判断object是否为array
-   (aref array index)
    获取array中index所指的element的引用
-   (aset array index object)
    设置array中第index的元素为object,该函数返回object
-   (fillarray array object)
    将array中所有元素都填充为object
    
        (setq a [a b c d e f g])                ; => [a b c d e f g]
        (fillarray a 0)                         ; => [0 0 0 0 0 0 0]
        a                                       ; => [0 0 0 0 0 0 0]
        (setq s "When in the course")           ; => "When in the course"
        (fillarray s ?-)                        ; => "------------------"

### Vector相关函数<a id="sec-31-1-1" name="sec-31-1-1"></a>

-   (vectorp object)
    判断object是否为vector
-   (vector &rest objects)
    创建由objects组成的vector
-   (make-vector N object)
    创建由N个object组成的vector
-   (vconcat &rest sequences)
    将sequences中的element,转换到vector中
    
        (setq a (vconcat '(A B C) '(D E F)))    ; => [A B C D E F]
        (eq a (vconcat a))                      ; => nil
        (vconcat)                               ; => []
        (vconcat [A B C] "aa" '(foo (6 7)))     ; => [A B C 97 97 foo (6 7)]

### Char-Table相关函数<a id="sec-31-1-2" name="sec-31-1-2"></a>

-   (char-table-p object)
    判断object是否为char-table类型的

-   (make-char-table SUBTYPE &optional init)
    创建一个新char-table对象,该char-table的subtype为参数SUBTYPE(必须为symbol类型). 该char-table的所有element初始化为参数init(默认为nil).
    
    一旦创建了char-table,就不能再修改其subtype了.

-   (char-table-subtype char-type)
    返回char-table的subtype

-   (char-table-parent char-table)
    获得char-table的父级char-table对象,若没有,则返回nil
    
    char-table从父级char-table中继承值

-   (set-char-table-parent char-table new-parent-char-table)
    为char-table设置父级char-table

-   (char-table-extra-slot char-table n)
    返回char-table中第n个slot上的值
    
    一个char-table有多少个slot,由它的subtype的属性\`char-table-extra-slots\`决定

-   (set-char-table-extra-slot char-table n value)
    设置char-table的第n个slot的值为value

-   (char-table-range char-table range)
    该函数返回char-table中某个由参数range指定的范围内的值
    
    range参数可以是:
    
    -   nil
        获取默认值
    
    -   char
        获取char对应的值
    
    -   '(from . to)
        获取[from,to]这个范围内char的相应值

-   (set-char-table-range char-table range value)
    设置char-table中由range所指范围的对应值.
    
    这里的参数range可能是:
    
    -   nil
        设置char-table的默认值为value
    
    -   t
        设置整个char-table的值为value
    
    -   char
        设置char对应的值为value
    
    -   (from. to)
        设置范围[from,to]之间的值为value

-   (map-char-table function char-table)
    针对char-table中所有值非nil的键值对都作为参数调用function函数.
    
    该function函数必须接收两个参数(一个key,一个value).
    其中key的类型可以是某个char,或这类似'(from . to)这样的标示范围的cons ceil(不是很明白什么时候会用到(from.to)这样类型的参数呢??)
    而value的值为(char-table-range char-table key)的返回值
    
    map-char-table的返回值必定为nil,因此我们通常只使用function的副作用.
    
        (let (accumulator)
          (map-char-table
           #'(lambda (key value)
               (setq accumulator
                     (cons (list
                            (if (consp key)
                                (list (car key) (cdr key))
                              key)
                            value)
                           accumulator)))
           (syntax-table))
          accumulator)
        ;; =>
        ;; (((2597602 4194303) (2)) ((2597523 2597601) (3))
        ;;  ... (65379 (5 . 65378)) (65378 (4 . 65379)) (65377 (1))
        ;;  ... (12 (0)) (11 (3)) (10 (12)) (9 (0)) ((0 8) (3)))

### Bool-vector相关函数<a id="sec-31-1-3" name="sec-31-1-3"></a>

-   创建bool-vector
    (make-bool-vector length initial)
    
    创建长度为length的bool-vector,每个值初始化为initial
    
        (setq a (make-bool-vector 10 nil))      ;=>#&10"  "

-   类型判断
    
    (bool-vector-p object)
    
    object是否为为bool-vector类型

-   集合运算
    
    (bool-vector-exclusive-or a b &optional c)
    
    求a和b的异或计算结果,若有参数c,则将结果存入c中.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-union a b &optional c)
    
    求a&b的计算结果,若有参数c,则将结果存入c中.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-intersection a b &optional c)
    
    求a|b的运算结果,若有参数c,则将结果存入c中.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-set-difference a b &optional c)
    
    求a-b的运算结果,若有参数c,则将结果存入c中.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-not a &optional b)
    
    求!a的运算结果,若有参数b,则将结果存入b中.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-subsetp a b)
    
    判断a是否为b的子集, 所谓a是b的子集指的是所有a中值为t的位置,在b中也为t.
    所有参数都都必须为bool vector类型且具有相同的长度
    
    (bool-vector-count-consecutive bool-vector a index)
    
    统计bool-vector中从index开始,连续值等于a的个数
    
    (bool-vector-count-population bool-vector)
    
    统计bool-vector中值为t的个数
    
    (aref bool-vector index)
    
    要修改/获取bool-vector的值,需要使用array的相关函数来进行:
    
    获取bool-vector中index的值
    
    (aset bool-vecotr index value)
    
    设置bool-vector在index位置的value
    
    下面是一些例子
    
        (setq bv (make-bool-vector 5 t))        ; => #&5"^_"
        (aref bv 1)                             ; => t
        (aset bv 3 nil)                         ; => nil
        bv                                      ; => #&5"^W"

# HashTable相关函数<a id="sec-32" name="sec-32"></a>

## 判断函数<a id="sec-32-1" name="sec-32-1"></a>

-   (hash-table-p table)
    判断table是否为hash-table

## 创建hash-table<a id="sec-32-2" name="sec-32-2"></a>

(make-hash-table &rest keyword-args)

常用的keyword-args有:
-   :test TEST
    
    指定了用于测试相等的函数. 默认使用eq

-   :weakness WEAK
    
    指定了hash-table什么时候被垃圾回收机制回收. WEAK的可选参数为:
    
    -   nil(默认值)
        表示key和value都不是弱引用,hash-table会保证key和value不会被垃圾回收机制回收
    
    -   key
        表示key为弱引用,即若除了hash-table其他地方没有引用key的变量,则key变量所指的内存块被回收. 该key-value键值对从hash-table中被删除
    
    -   value
        表示value为弱引用,即若除了hash-table其他地方没有引用value的变量,则value变量所指的内存块被回收. 该key-value键值对从hash-table中被删除
    
    -   key-or-value
        表示若除了hash-table其他地方 **同时** 没有引用key或value的变量,则key和value变量所指的内存块被回收. 该key-value键值对从hash-table中被删除
    
    -   key-and-value / t
        表示key和value都为弱引用,即若除了hash-table其他地方没有引用key或value的变量,则key或value变量所指的内存块被回收. 该key-value键值对从hash-table中被删除

-   :size SIZE
    指示大致上会有SIZE个数据存入hash-table,用于优化初始容量,默认为65

-   :rehash-size REHASH-SIZE
    指示当hash-table容量爆满后,怎么进行扩容.
    
    若REHASH-SIZE为正整数,则每次扩容都增加REHASH-SIZE个容量
    
    若REHASH-SIZE为正浮点数,则每次扩容都按照REHASH-SIZE的倍数来调整容量(因此REHASH-SIZE需要>1)
    
    REHASH-SIZE默认为1.5

-   :rehash-threshold THRESHOLD
    该参数指明了什么时候hash-table进行扩容. 默认为0.8
    
    THRESHOLD是一个不大于1的浮点数, 当hash-table中的元素个数>THRESHOLD乘与hash-table容量时,进行扩容

(copy-hash-table table)

创建table的副本,但 **它的key和value与原table共享**

## 添加item / 修改item的值<a id="sec-32-3" name="sec-32-3"></a>

(puthash myKey myVal myHash)

## 删除item<a id="sec-32-4" name="sec-32-4"></a>

(remhash myKey myHash)

删除myHash中索引为myKey的键值对. 该函数总是返回nil

(clrhash myHash)

清空myHash中的所有内容,该函数总是返回nil

## 获取某item的值<a id="sec-32-5" name="sec-32-5"></a>

(gethash myKey myHash &optional default)  

若没key为myKey的item,则返回default,默认为nil

## 获取hash中的属性<a id="sec-32-6" name="sec-32-6"></a>

-   获取hash中的key-value键值对个数
    (hash-table-count myHash)

-   获取hash中的查询机制(即:test属性的值)
    (hash-table-test myHashTable)

-   获取hash-table中:weak属性的值
    (hash-table-weakness myHash)

-   获取hash-table中:rehash-size参数的值
    (hash-table-rehash-size table)

-   获取hash-table中:rehash-threshold参数的值
    (hash-table-rehash-threshold table)

-   获取hash-table中的:size参数的值
    (hash-table-size table)

## 为hash-map中的所有键值对调用函数处理<a id="sec-32-7" name="sec-32-7"></a>

(maphash myFunc myHash)  

myFunc接收两个参数,一个key,一个value.该函数总是返回nil

## 获取hash-map中的所有key值 / value值<a id="sec-32-8" name="sec-32-8"></a>

-   在emacs24.4之后,可以使用
    
        ;; get all keys
        (require 'subr-x)
        (hash-table-keys myHash) ; 
        (hash-table-values myHash) ;

-   在emacs24.3可以自定义函数
    
        (defun get-hash-keys (hashtable)
          "Return all keys in hashtable."
          (let (allkeys)
            (maphash (lambda (kk vv) (setq allkeys (cons kk allkeys))) hashtable)
            allkeys
          )
        )
        
        (defun get-hash-values (hashtable)
          "Return all values in HASHTABLE."
          (let (allvals)
            (maphash (lambda (kk vv) (setq allvals (cons vv allvals))) hashtable)
            allvals
          )
        )

## 修改Hash-table的比较方法<a id="sec-32-9" name="sec-32-9"></a>

要修改Hash-table中的查询机制,需要同时修改计算Hash Code的方法和比较key值的方法.

-   (define-hash-table-test name test-fn hash-fn)
    定义一个名为name的hash-table查询机制.
    
    当定义了查询机制后,该查询机制就可以传给make-hash-table中的:test参数用于新生成的hash-table了.
    
    test-fn需要接收两个key作为参数,并在认为两个key相等时返回非nil
    
    hash-fn则需要接收一个key作为参数,并返回一个整数(可以为负数)作为它的hash值.
    
    elisp提供了一个函数用于根据object的内容来生成hash值:sxhash
    
        (defun case-fold-string= (a b)
          (eq t (compare-strings a nil nil b nil nil t)))
        (defun case-fold-string-hash (a)
          (sxhash (upcase a)))
        
        (define-hash-table-test 'case-fold
          'case-fold-string= 'case-fold-string-hash)
        
        (make-hash-table :test 'case-fold)

-   (sxhash obj)
    
    根据obj的内容生成hash code,若两个obj是equal的,则该函数返回相等的hashcode
    
        (define-hash-table-test 'contents-hash 'equal 'sxhash)
        
        (make-hash-table :test 'contents-hash)

# Symbol相关函数<a id="sec-33" name="sec-33"></a>

## symbol组成部分<a id="sec-33-1" name="sec-33-1"></a>

-   (symbol-name symbol)
    获取symbol的名称
    
        (symbol-name 'foo)

-   (symbol-function symbol)
    获取symbol的函数cell

-   (indirect-function symbol-or-function &optional noerror)
    类似symbol-function,但若symbol的function cell为另一个symbol,则它会返回(indirect-function 另一个symbol)的值
    
    参数symbol-or-function表示它也可以是function类型的,若类型为function,则直接返回该function参数

-   

-   (fset symbol definition)
    设置symbol的函数cell为definition

## 获取symbol<a id="sec-33-2" name="sec-33-2"></a>

-   (make-symbol name)
    创建uninterned symbol
    
        (setq sym (make-symbol "foo"))          ; => foo
        (eq sym 'foo)                           ; => nil ,uninterned symbol和interned symbol是不一样的

-   (intern name &optoinal obarray)
    返回obarray中名为name的symbol,若obarray中不存在名为name的symbol,则新建一个symbol. 
    
    obarray默认为全局变量\`obarray\`
    
    参数name必须是字符串类型
    
        (setq sym (intern "foo"))               ; => foo
        (eq sym 'foo)                           ; => t
        (setq sym1 (intern "foo" other-obarray)) ; => foo
        (eq sym1 'foo)                           ; => nil

-   (intern-soft name &optional obarray)
    类似intern,但若obarray中不存在名为name的symbol,则返回nil
    
    且参数name可以为symbol类型和字符串类型
    
        (intern-soft "frazzle")                 ; No such symbol exists. => nil
        (make-symbol "frazzle")                 ; Create an uninterned one. => frazzle
        (intern-soft "frazzle")                 ; That one cannot be found. => nil
        (setq sym (intern "frazzle"))           ; Create an interned one. => frazzle
        (intern-soft "frazzle")                 ; That one can be found! => frazzle
        (eq sym 'frazzle)                       ; And it is the same one. => t

## 其他函数<a id="sec-33-3" name="sec-33-3"></a>

-   (mapatoms func &optional obarray)
    对obarray中包含的每个symbol,都调用func来处理,然后返回nil.
    
    obarray默认为全局的obrray变量
    
        (setq count 0)
        
        (defun count-syms (s)
          (setq count (1+ count)))
        
        (mapatoms 'count-syms)                  ; => nil
        count                                   ; => 54972

-   (unintern symbol-or-string obarray)
    从obarray中删除指定的symbol
    
    删除成功返回t,否则返回nil

## symbol中的property<a id="sec-33-4" name="sec-33-4"></a>

-   获取symbol的property
    
    (get symbol property)
    
    从symbol的property list中出去出与参数property eq的值,若没有找到,则返回nil
    
    (symbol-plist symbol)
    
    返回symbol相应的property list
    
    (function-get symbol property)
    该函数与get类似,但若参数symbol为另一个函数的别名时,该函数返回实际函数的property的值,而不是别名的property的值

-   设置symbol的property
    (put symbol property value)
    
    设置symbol中property list的相应property的值.
    
    若原property不存在则添加新property和value,否则更新其value
    
        (put 'fly 'verb 'transitive)            ; =>'transitive
        (put 'fly 'noun '(a buzzing little bug)) ; => (a buzzing little bug)
        (get 'fly 'verb)                         ; => transitive
        (symbol-plist 'fly)                      ; => (verb transitive noun (a buzzing little bug))
    
    (setplist symbol plist)
    
    覆盖symbol的原property list为参数plist
    
    该函数的返回值为参数plist
    
        (setplist 'foo '(a 1 b (2 3) c nil))    ; => (a 1 b (2 3) c nil)
        (symbol-plist 'foo)                     ; => (a 1 b (2 3) c nil)

## 标准symbol property说明<a id="sec-33-5" name="sec-33-5"></a>

-   :advertised-binding
    symbol所表示的函数的建议绑定键

-   char-table-extra-slots
    若symbol所表示的值为char-table类型,则该值指明了能有多少个额外slot

-   customized-face,face-defface-spc,saved-face,theme-face
    定义了face的方方面面的性质,不要去直接修改这些属性,而应该使用deffac及相关函数

-   customized-value,save-vlaue,standard-value,theme-value
    这些属性用来记录customizable variable的方方面面的属性,不要去直接修改这些属性,而应该使用defcustom及相关函数

-   disabled
    若为非nil,则表示该函数不为command

-   face-documentation
    指定face的说明,该属性由defface自动设置

-   history-length
    指明了minibuffer中,对指定的history list variable的最大历史存储数量

-   interactive-form
    symbol表示函数的interactive form. 不要直接修改该属性,使用定义函数时的interactive特殊form

-   menu-enable
    该属性是一个表达式,根据该表达式的值来决定是否在menu中显示该菜单项

-   mode-class
    若该属性为\`special\`,则指定的major mode是\`special\`的

-   permanent-local
    若该属性值为非nil,则表示symbol表示的变量是buffer-local的变量, 当更换major mode时,这种变量的值不会被重置

-   permanent-local-hook
    若该属性值为非nil,则表示当鞥该major mode时,该symbol表示的hook变量不被重置

-   pure
    该属性值为非nil告诉编译器,该symbol所表示的方法为纯函数方法(即没有副作用). 因此在使用const参数来调用该方法时,在编译期就能执行该方法. 这会让一些本该在运行期报的错误,在编译器就被检查出来.

-   risky-local-variable
    若该属性值为非nil,表示该symbol表示的变量,不建议设置为file-local variable

-   safe-function
    标示该symbol标示的函数,是否可以安全的执行

-   safe-local-eval-function
    标示该symbol标示的函数,是否可以安全的在file-local evaluation form中执行

-   safe-local-variable
    该属性值应该是一个函数,该函数用来决定该symbol表示的变量是否为safe file-local的

-   side-effect-free
    非nil表示symbol表示的函数无副作用,该属性用来决定函数的安全性和字节编译优化, **不要尝试手工修改它**

-   variable-documentation
    该属性为指定变量的说明

# Region/Mark相关函数<a id="sec-34" name="sec-34"></a>

-   设置mark
    
    (set-mark-command)

-   删除region
    
    (kill-region)

-   注释region
    
    (comment-region)

-   重新格式化region
    
    (fill-region)

-   缩进region
    
    (indent-region)

-   判断Region是否是active的
    
    (region-active-p) 该函数还要求Transient-mark-mode

# Evaluation<a id="sec-35" name="sec-35"></a>

## \`(反引号)<a id="sec-35-1" name="sec-35-1"></a>

\`\`\`类似\`'\`,
但当object前带了\`,\`,则会对该object进行求值,
当object前带了\`,@\`,则会将object的求值结果中的各个元素打散插入.

## 函数<a id="sec-35-2" name="sec-35-2"></a>

-   (eval form &optional lexical)
    在当前环境下执行form
    
    参数lexical决定了form中的本地变量采用的是静态作用域还是动态作用域.
    
    -   nil 表示使用动态作用域
    
    -   t 表示使用静态作用域
    
    -   某个非空的alist 表示alist中所指定变量采用静态作用域,其他变量为动态作用域

-   (eval-region start end &optional stream read-function)
    运行由start和end所标识的region
    
    默认情况下,eval-region并不产生任何输出,但通过传递一个非nil的stream参数,可以将期间产生的输出输出到stream中
    
    若read-function为非nil,则使用指定的read-function来取代read函数读取表达式. 该函数需要接收一个参数:读取输入的stream

-   (eval-buffer &optioanl buffer-or-name stream filename unibyte print)
    运行指定buffer的可见部分所组成的region.
    
    buffer-or-name可以为buffer或string,也可以为nil表示当前buffer
    
    stream的作用跟eval-region中的stream类似,但若stream为nil而print为非nil,则执行的结果依然会被丢弃,但执行的过程中所产生的哪些输出会被输出到echo area中.
    
    filename是給load-history使用的文件名称.
    
    若inibyte为非nil,则elisp reader尽可能的将string转换为unibyte格式.

## 选项<a id="sec-35-3" name="sec-35-3"></a>

-   max-lisp-eval-depth

-   max-specpdl-size

-   values
    该变量的值为一个list,每个list元素都是执行form的结果,最近的结果放到第一位.
    
        (setq x 1)                              ; => 1
        (list 'A (1+ 2) auto-save-default)      ; => (A 3 t)
        values                                  ; => ((A 3 t) 1 ...)

# 缓冲区<a id="sec-36" name="sec-36"></a>

## 获取buffer对象<a id="sec-36-1" name="sec-36-1"></a>

-   得到当前buffer对象
    
    current-buffer(**当前buffer不一定是在屏幕上显示的哪个缓冲区,另外,当命令执行完成后,光标所在的buffer自动成为当前buffer** )

-   若缓冲区存在则返回该缓冲区对象,否则新建缓冲池对象返回
    
    get-buffer-create

-   若有同名缓冲区存在,则新建的缓冲区后会加上后缀
    
    generate-new-buffer

-   获得所有buffer的列表
    
    buffer-list

-   获得窗口对应的buffer
    
    window-buffer

## buffer操作<a id="sec-36-2" name="sec-36-2"></a>

-   返回当前buffer的文件全路径
    
    buffer-file-name

-   获得指定/当前buffer的名字
    
    buffer-name
    
        (buffer-name [buffer对象])
-   重命名缓冲区
    
    rename-buffer

-   产生一个唯一的缓冲区名
    generate-new-buffer-name

-   设置指定buffer为当前buffer
    
    (set-buffer myBuffer)

-   保存当前buffer到文件
    
    save-buffer

-   在不改变当前状态下,临时用另一buffer的变量代替现有变量执行语句
    
    with-current-buffer
    
        (with-current-buffer buffer对象或buffer名称
          表达式)

-   关闭缓冲区
    
    (kill-buffer myBuffer) ;如果要用户确认是否要关闭缓冲区，可以加到kill-buffer-query-functions里。如果要作善后处理，可以用kill-buffer-hook

-   关闭当前buffer
    
    (kill-this-buffer)

-   确认缓冲区是否存在
    
    buffer-live-p

-   使用临时buffer执行相应代码
    
    with-temp-buffer
    
        ;; use a temp buffer to manipulate string
        (with-temp-buffer
          (insert myStr)
          ;; manipulate the string here
          (buffer-string) ; get result
        )

-   创建新的空标记
    
    make-marker
    
        (make-marker)

-   设置标记的位置和缓冲区
    
    set-marker
    
        (set-marker foo (point))

-   得到point处的标记
    
    point-marker
    
        (point-marker)
-   复制标记或直接用位置生成一个标记
    
    copy-marker
    
        (copy-marker 位置/marker对象)

-   得到一个marker的内容
    
    maker-position / marker-buffer
    
        (maker-position marker对象)
        (marker-buffer marker对象)

-   buffer大小
    
    buffer-size

-   mark-marker
    
     point /point-max /point-min
    返回当前缓冲区的mark(**注意mark与marker的区别,mark是用来与point一起定义一个region的,而marker是一个标记位置**)

-   设置mark的值,并激活mark
    
    set-mark

-   加入/删除mark-ring的元素
    
    push-mark / pop-mark

-   取得region的起点和终点
    
    region-beginning / region-end

-   让某个缓冲区可见
    
    display-buffer

-   判断buffer是否被修改
    
    (buffer-modified-p)

-   选中的window切换到上一个/下一个buffer
    
    (previous-buffer)
    
    (next-buffer)
-   

## 获取缓冲区内容<a id="sec-36-3" name="sec-36-3"></a>

-   得到整个缓冲区的文本
    
    buffer-string
-   得到buffer某个区间的文本
    
    buffer-substring
-   得到point附件的字符
    
    char-after / char-before
-   point处的词
    
    current-word
-   得到point处的其他类型的文本
    
    thing-at-point

## buffer内容处理相关函数<a id="sec-36-4" name="sec-36-4"></a>

### 删除操作<a id="sec-36-4-1" name="sec-36-4-1"></a>

-   删除从当前光标开始的N个字符
    
    (delete-char N)

-   删除光标前的N个字符
    
    (delete-backward-char N)

-   删除region
    
    (delete-region sartPos endPos)

-   清空整个buffer
    
    (erase-buffer)

### 插入操作<a id="sec-36-4-2" name="sec-36-4-2"></a>

-   在光标处插入文字
    
    (insert str)

-   在光标处插入某buffer的一部分文本
    
    (insert-buffer-substring-no-properties myBuffer myStartPos myEndPos)
    
    -   插入文件中某部分到当前缓冲区中
        
        (insert-file-contents myPath)
        
            (insert-file-contents filename &optional visit beg end replace)
        
        如果指定visit则会标记缓冲区的修改状态并关联缓冲区到文件，一般是不用的。
        replace是指是否要删除缓冲区里其它内容，这比先删除缓冲区其它内容后插入文件内容要快一些，但是一般也用不上。
        insert-file-contents会处理文件的编码，如果不需要解码文件的话，可以用insert-file-contents-literally。

### 查找/替换操作<a id="sec-36-4-3" name="sec-36-4-3"></a>

-   改变大小写
    
    (capitalize-region startPos endPos)

-   替换操作
    
    变量\`case-fold-search\`决定是否大小写敏感
    
    replace-match,需要与其他的search类函数配合,它替代上次search匹配的文本
    
    (replace-match 字符串) 表示用字符串替代上次search匹配的文本呢

-   获取上次正则查询的分组内容
    
    (match-string N) 返回上次正则查询的第N个分组的内容

-   获取上次正则查询分组的起始/结束电
    
    (match-beginning N)
    
    (match-end N)

-   

## 保存现场<a id="sec-36-5" name="sec-36-5"></a>

-   保存当前buffer,执行其中的表达式,然后回复为原来的buffer
    
    save-current-buffer
    
        (save-current-buffer
          表达式)

-   保存narrow-to-region
    
    (save-restriction
       (narrow-to-region pos1 pos2)
       lisp代码)

-   保存buffer状态
    (save-excursion
        reset body
        )

# 窗口<a id="sec-37" name="sec-37"></a>

## 获得窗口对象<a id="sec-37-1" name="sec-37-1"></a>

-   得到当前光标所在的窗口对象
    
    selected-window
-   得到当前frame里的所有窗口
    
    window-list
-   window-lists里排在某个window之后/之前的窗口对象
    
    next-window / previous-window
-   查找符合某个条件的窗口
    
    get-window-with-predicate
-   根据buffer获得window(如果有多个窗口显示同一个缓冲区,那么函数由window-list决定返回哪个).
    
    get-buffer-window
-   根据buffer获得全部的相应window
    
    get-buffer-window-list
-   根据给定的文件名,返回缓冲区
    
    find-buffer-visiting

## 窗口操作<a id="sec-37-2" name="sec-37-2"></a>

-   分割window
    
    split-window
-   删除当前选中的窗口
    
    delete-window
-   删除其他窗口
    
    delete-other-windows
-   得到当前窗口配置信息,可以用setq保存起来
    
    current-window-configuration
-   设置当前窗口配置信息
    
    set-window-configuration
-   使某个窗口对象变成选中的窗口
    
    select-window
-   执行的语句结束后,选择的窗口仍留在执行语句之前的窗口
    
    save-selected-window / with-selected-window
-   遍历窗口操作
    
    walk-windows
-   让某个窗口显示某个缓冲区
    
    set-window-buffer
-   让选中的窗口显示某个缓冲区
    
    switch-to-buffer

## 窗口信息<a id="sec-37-3" name="sec-37-3"></a>

-   得到当前窗口的结构
    
    window-tree
-   判断窗口对象是否存在
    
    window-live-p
-   获得窗口的高度(包括了mode line和 header line)
    
    window-height
-   获得窗口的高度(排除了mode line和 header line)
    
    window-body-height
-   窗口的宽度,不包括滚动条和边缘
    
    window-width
-   返回各顶点的坐标信息(包括滚动条,边缘,mode line ,header line)
    
    window-edges
-   返回窗口的文本区域的坐标信息
    
    window-inside-edges
-   用像素表示的window位置
    
    window-pixel-edges / window-inside-pixel-edges

# 文件<a id="sec-38" name="sec-38"></a>

## 文件读写<a id="sec-38-1" name="sec-38-1"></a>

-   打开一个文件
    
    (find-file myPath)

-   改变缓冲区关联的文件
    
    set-visited-file-name

-   保存当前文件
    
    (save-buffer)

-   另存为文件
    
    (write-file myPath)

-   把文本块追加到文件后
    
    (append-to-file startPos endPos filePath)

-   把缓冲区当中的一部分写入到指定文件中
    
    wirte-region
    
        (write-region start end filename &optional append visit lockname mustbenew)
    
    如果指定append则是添加到文件末尾。
    visit参数也会把缓冲区和文件关联，
    lockname 则是文件锁定的名字
    mustbenew(保文件存在时会要求用户确认操作。

## 文件信息<a id="sec-38-2" name="sec-38-2"></a>

-   判断文件是否存在,对于目录和一般文件都能用这个函数进行判断,但是符号链接只有当目标文件存在时才返回t
    
    file-exists-p
-   文件属性判断
    
    file-readable-p / file-writable-p / file-executable-p / file-modes
-   判断文件类型是普通文件/目录/符号链接,其中file-symlink-p返回目标文件名
    
    file-regular-p / file-directory-p / file-symlink-p
-   文件的详细信息
    
    file-attributes
-   设置文件修改时间
    
    set-file-times
-   设置文件位模式
    
    set-file-modes

-   除去链接后的真实文件名
    
    file-truename

## 文件名相关函数<a id="sec-38-3" name="sec-38-3"></a>

-   分解文件路径各部分
    
    file-name-directory / file-name-nodirectory / file-name-sans-extension / file-name-extension / file-name-sans-versions
    
        (file-name-directory "~/temp/test.txt") ; => "~/temp/"
        (file-name-nondirectory "~/temp/test.txt") ; => "test.txt"
        (file-name-sans-extension "~/temp/test.txt") ; => "~/temp/test"
        (file-name-extension "~/temp/test.txt") ; => "txt"
        (file-name-sans-versions "~/temp/test.txt~") ; => "~/temp/test.txt"
        (file-name-sans-versions "~/temp/test.txt.~1~") ; => "~/temp/test.txt"

-   测试一个路径是否是绝对路径
    
    file-name-absolute-p

-   得到绝对路径
    
    (expand-file-name myFilePath)

-   把绝对路径转换成相对路径
    
    (file-relative-name myFilePath dirPath)

-   把路径转换为目录形式,也就是确保它是以路径分隔符结束的
    
    file-name-as-directory
    
        (file-name-as-directory "~rms/lewis") ; => "~rms/lewis/"

-   获得目录名
    
    directory-file-name
    
        (directory-file-name "~lewis/") ; => "~lewis"
-   得到所在系统使用的文件名
    
    convert-standard-filename
    
        (convert-standard-filename "c:/windows") ;=> "c:\\windows"
-   得到某个目录的全部或者符合某个正则表达式的文件名,directory-files-attributes返回的列表包含了file-attributes得到的信息
    
    directory-files / directory-files-attributes
-   得到某个文件在目录中的所有版本
    
    file-name-all-versions
-   得到通配符扩展厚的文件列表
    
    file-expand-wildcards

## 文件操作<a id="sec-38-4" name="sec-38-4"></a>

-   重命名 拷贝 删除文件
    
    (rename-file fileName newName)
    
    (copy-file sourcName desName)
    
    (delete-file fileName)
    
    (copy-directory dirPath newDirPath)

-   删除目录
    
    (delete-directory dirPath 是否循环删除子目录的标记 是否放入Trash的标记)

-   设置文件MODE
    
    (set-file-mode FILE MODE)

-   获取目录中的文件列表
    
    (directory-files DIR &optional FULL MATCH NOSORT)

-   创建目录
    
    (make-dirctory DIR &optional PARENTS)

-   

## 临时文件<a id="sec-38-5" name="sec-38-5"></a>

-   这个函数按给定前缀产生一个不和现有文件冲突的文件，并返回它的文件名。如果给定的名字是一个相对文件名，则产生的文件名会用temporary-file-directory 进行扩展。也可以用这个函数产生一个临时文件夹。
    
    make-temp-file
    
        (make-temp-file "foo") ; => "/tmp/foo5611dxf"
-   产生一个不存在的文件名
    
    make-temp-name
    
        (make-temp-name "foo") ; => "foo5611q7l"

## 神奇的handler<a id="sec-38-6" name="sec-38-6"></a>

-   在Emacs里，底层的文件操作函数都可以托管给elisp中的函数，这样只要用elisp实现了某种类型文件的基本操作，就能像编辑本地文件一样编辑其它类型文件了

# Dired-mode相关函数<a id="sec-39" name="sec-39"></a>

-   获取dired中marked file
    
    使用函数\`dired-get-marked-files\`

# 执行命令<a id="sec-40" name="sec-40"></a>

-   执行shell命令并等待shell命令结束
    
    (shell-command "shell命令")

-   执行shell命令,等待shell命令结束,并获得命令的输出
    
    (shell-command-to-string "shell命令")

-   使用外部命令对所选择Region进行处理
    
    shell-command-on-region

-   执行shell命令,但是不等待shell命令结束
    
    start-process
    
    start-process-shell-command
    
    call-process-region

# Register函数<a id="sec-41" name="sec-41"></a>

-   将内容复制到Register中
    
    (copy-to-register ?1 startPos endPos)

-   从Register中取出内容
    
    (insert-register ?1 t)

# Org相关函数<a id="sec-42" name="sec-42"></a>

## 取entry属性<a id="sec-42-1" name="sec-42-1"></a>

(org-entry-get nil "属性名" 是否继承属性)

## 取entry的tag list<a id="sec-42-2" name="sec-42-2"></a>

(org-get-tags)

## 取entry的TODO state<a id="sec-42-3" name="sec-42-3"></a>

变量\`org-get-tags\`

## 判断哪些state是完成状态<a id="sec-42-4" name="sec-42-4"></a>

变量\`org-done-keywords\`

# 版本信息<a id="sec-43" name="sec-43"></a>

-   变量emacs-version
-   变量emacs-major-version
-   变量emacs-minor-version

# wait function<a id="sec-44" name="sec-44"></a>

wait function用于等待一段时间或等待input.

-   (sit-for seconds &optional nodisp)
    
    sit-for等待一段时间或直到收到某个input event. 在这段时间内Emacs会实时更新屏幕显示.
    
    若等待不是由收到input而中断的,则返回t,否则返回nil
    
    参数seconds可以是浮点数. (sit-for 0)等价于(redisplay),它只是立即更新屏幕显示.
    
    若参数nodisp为非nil,则sit-for在等价期间不会更新屏幕显示.
    
    在Emacs处于batch mode时,\`sit-for'不能被interrupt event中断,这时等价于\`sleep-for'

-   (sleep-for seconds &optional millisec)
    
    该函数等价seconds秒,等待期间不会被input event打断,也不会更新屏幕显示. 它总是返回nil
    
    参数seconds可以为浮点数.
    
    参数millisec表示在等待seconds秒后,再等待millisec毫秒
