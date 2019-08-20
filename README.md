# Tool-Fn

> 函数式编程风格的工具函数

### 这是什么仓库？干嘛用的？

> 提供常用的JavaScript函数 例如随机排序、快速排序、数据清洗、分片、克隆、柯里化、面试常见函数实现等等

> 学习 or 工作时Copy代码

> 如果你有一个能实现某个功能的函数，不论它是什么，请提交你的code参与这个项目

> 如果你有一个想实现的功能确不知道怎么写(例如面试题)，可以提交Issues来进行讨论

### 快速开始

我该如何给仓库贡献代码？

``` bash
#首先打开终端输入命令 克隆仓库
$ git clone https://github.com/unjust-life/Tool-Fn.git

#安装依赖
$ npm install

#接下来你就可以给仓库贡献代码啦 例如你想提交一个十分好用的clone方法用于深拷贝对象

#首先在src/modules文件下新建一个文件夹 以英文驼峰格式命名
$ cd src/modules    #进入modules目录  新建一个clone文件夹
$ cd log            #新建clone.js    开始编写你的代码吧(使用es6模块语法)

#写完代码觉得没问题了 请执行检查命令(在提交代码的时候我也会帮你检查一遍 有问题的话将被打回)

#因此建议你自己先检查一遍(如果你使用vscode配置插件将获得实时的错误提示)

请务必按照函数式编程方式提交你的函数!
请务必写注释！

$ npm run lint  #对src目录下所有文件执行styleLint检测 提示目前存在的错误

$ npm run fix   #对src目录下所有文件执行styleLint检测 尝试自动修复错误(可以直接用这个)

检查通过后就可以提交你的代码啦 注意提交信息是有格式要求的 参照了开源社区的主流方案 具体格式在下面

```



### 文件目录
``` bash

src 开发目录
  -modules  模块 新增函数请在这在这个目录新建文件夹
    --fn    函数模块文件夹
  -index.js 入口
pages 页面目录
  -doc 文档页面

```



``` bash
```

### 提交规范

``` bash
提交代码前请确认代码通过lint检查 没有任何error

单次提交一个模块文件/函数

尽可能的避免兼容性问题 如使用了有兼容性问题的语法请注明

commit 提交信息格式 'type(scope): subject'

type: 本次改动类型
-feat()      提交新的代码
-fix()       修复bug
-docs()      文档修改
-chore()     辅助工具或配置的变更
-refactor()  重构
-test()      测试代码

scope 改动范围 不允许为空 使用英文小写字母

subject 改动内容 结尾禁止加标点符号

```

### 函数式编程概念

- 没有"副作用"

所谓"副作用"(side effect)，指的是函数内部与外部互动（最典型的情况，就是修改全局变量的值），产生函数运算以外的其他结果。

函数式编程强调没有"副作用"，意味着函数要保持独立，所有功能就是返回一个新的值，没有其他行为，尤其是不得修改外部变量的值。

比如 slice 和 splice，这两个函数的作用并无二致——但是注意，它们各自的方式却大不同。我们说 slice 符合纯函数的定义是因为对相同的输入它保证能返回相同的输出。而 splice 却会嚼烂调用它的那个数组，然后再吐出来。这就会产生可观察到的副作用，即这个数组永久地改变了。

- 引用透明性

函数程序通常还加强引用透明性，即如果提供同样的输入，那么函数总是返回同样的结果。就是说，函数不依赖于外部的全局状态。

- 只用"表达式"，不用"语句"

"表达式"（expression）是一个单纯的运算过程，总是有返回值；"语句"（statement）是执行某种操作，没有返回值。函数式编程要求，只使用表达式，不使用语句。也就是说，每一步都是单纯的运算，而且都有返回值。

- DRY（不要重复自己，don't repeat yourself）

- 最小意外原则（Principle of least surprise）

- 单一责任（single responsibility）


### 函数列表
``` bash

-chunk(arr, size)
#arr 需要处理的数组 #size 数组块长度
将数组（array）拆分成多个 size 长度的区块，并将这些区块组成一个新数组。 
如果array 无法被分割成全部等长的区块，那么最后剩余的元素将组成一个区块。

-clone(data)
#data 原对象
深拷贝一个对象或数组  返回值拷贝后的结果


```
