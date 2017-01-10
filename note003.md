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
