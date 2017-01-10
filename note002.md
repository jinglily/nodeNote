## 安装Node

安装 nvm

 > curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash

接下来就可以用 nvm 安装nodejs了
```
    nvm ls-remote  # 查看可以选择安装的 node 版本
    nvm install v7.4.0 # 安装 7.4.0 的 nodejs
```
node 安装完成之后 npm 也一样安装完成，查看是否安装完成

```
  node -v
  npm -v
```
用 npm 初始化一个 node 项目
- node init  生成 package.json 文件
- npm install <package name> --save  安装的包会记录到package.json 文件中的 dependencies 中
- npm install <package name> --save-dev 安装的包会记录到 package.json 文件中 devdependencise 中
- npm install <package name> -g 安装到本地电脑上

node 的模块分为 3 类 ，核心模块 ，第三方模块以及自定义的模块
```
// 通过 module.exports 导出模块 ，require 导入模块

// 导入核心模块
var fs = require ('fs')

// 导入第三方模块
var $ = require('jquery')

// 导入自定义模块
var test = require('./test')

// 导出模块

module.exports.test = 'test'

```
前端开发会用到es6的模板，这就需要 webpack 来给我们打包。
