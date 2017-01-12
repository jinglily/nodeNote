## webpack

webpack 是一款强大的模块加载器兼打包工具，他能把各种资源，例如 JS（含 JSX）, coffee ,样式 (含less/sass)，图片等作为模块来处理。[官网](http://webpack.github.io/)

### 初始化项目
---

创建一个项目

```
$ mkdir webpack-domes && cd webpack-domes
$ git init
$ touch README.md .gitignore
$ npm init
```

编辑 .gitignore

```
node_moduules
*.log*
.idea
```

建立src和build两个目录

```
// src 目录存放源码，build 目录存放编译打包之后的资源
$ mkdir src build
$ cd src && touch index.js component.js
$ cd ../ && touch index.html

```
```
/* src/index.js */
var component = require('./component.js');

component();
/* src/component.js */
module.exports = function(){
  alert('component');
}
/*index.html */
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Webpack demos</title>
</head>
<body>
  <div id="app"></div>
  <script src="./build/bundle.js"></script>
</body>
</html>

```

下载webpack和webpack-dev-server
```
# 安装并保存在项目依赖中
$ npm install --save-dev webpack webpack-dev-server
# 如果想直接在命令行使用webpack或webpack-dev-server命令，全局安装
```
创建webpack的配置文件
```
$ touch wenpack.config.js
```
`#请注意webpack.config.js这个文件名，默认情况下需要严格按照这个明明，不然会报Output filename not configured的错误；另外，如果不按这个命名，那么webpack运行的时候通过--conf这个参数指定配置文件，例如：webpack --config conf.js`

进行基本配置
```
var path = require('path');
module.exports = {
  entry: path.resolve(_dirname, 'src/index.js'),
  output: {
    path: path.resolve(_dirname, 'build'),
    filename: 'bundle.js'
  },
};
```
执行webpack命令，这里我们用的是项目内暗黄的webpack
```
$ ./node_moduules/.bin/webpack
```
可以在控制台看到如下信息
```
Hash: cf7cc9272c664f542fcb
Version: webpack 1.13.0
Time: 80ms
    Asset     Size  Chunks             Chunk Names
bundle.js  2.04 kB       0  [emitted]  main
   [0] ./src/index.js 60 bytes {0} [built]
   [1] ./src/component.js 57 bytes {0} [built]
```
