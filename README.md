# Tool-Fn

> 函数式编程风格的工具函数

## 快速开始

``` bash

#(MAC)打开终端输入命令 克隆仓库
git clone https://github.com/unjust-life/Tool-Fn.git

#安装依赖
npm install

#代码检查 对src目录下所有文件执行styleLint检测
npm run lint

#代码检查 对src目录下所有文件执行styleLint检测并尝试自动修复
npm run fix

```



## 文件目录
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

提交规范
---
>提交代码前请确认代码通过lint检查 没有任何error

>单次提交一个模块文件/函数

>尽可能的避免兼容性问题 如使用了有兼容性问题的语法请注明

``` bash
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
