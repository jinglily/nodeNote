## Git 本地工作

本地工作流程：

```
  git init
  git add README.md
  git commit -m "first commit"
  git remote add origin git@github.com:jinglily/node-note.git
  git push -u origin master

```
  - `git init` 将普通项目变成 **Git仓库**
  - `git add .` 添加修改内容到Git
  -  `git commit -m "first commit"` 制作版本并版本留言
  - `git push` 把本地仓库中有，而远端对应仓库中没有的版本推送到远端
  - `git pull` 把远端仓库中有，而本地对应仓库中没有的版本拉到本地
  - `git clone` 把远端仓库，克隆到本地
  - `git log -p` 本地查看版本历史
