# Tool-Fn

> 函数式编程风格的工具函数

### 快速开始

我该如何给仓库贡献代码？

``` bash
#首先打开终端输入命令 克隆仓库
$ git clone https://github.com/unjust-life/Tool-Fn.git

#安装依赖
$ npm install

#接下来你就可以给仓库贡献代码啦

#首先在src/modules文件下新建一个文件夹 以英文驼峰格式命名
$ cd src/modules    #进入modules目录  新建一个log文件夹
$ cd log            #新建log.js  开始编写你的代码吧(使用es6模块语法)

#写完代码觉得没问题了 请执行检查命令(在提交代码的时候我也会帮你检查一遍 有问题的话将被打回)

#因此建议你自己先检查一遍(如果你使用vscode配置插件将获得实时的错误提示)

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
