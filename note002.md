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
