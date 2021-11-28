####  git 提交代码的三种情况
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211107095719474-1517924223.png)

```js
// 一. 先创建分支 在做页面写功能, 功能做好后推送到暂存区 开始合并， 合并后将 master 先推送到云端，再推送分支
// 查看当前状态  和  拉取更新的代码  及 初始化一个 git 仓库
git status       git pull                 git init

// 创建分支
git checkout -b login

// 查看分支
git branch

// 将代码提交到 暂存区  合并分支步骤
git status
git add .
git status
git commit -m '完成了登录功能'
// 合并分支  先要切换到主分支上
git branch
git checkout master
git branch
git merge login
git push
// 将 分支提交到 远端仓库中  login 是分支名
git branch
git checkout login
git branch
git push -u origin login

// 注意： 第一次提交分支到远端仓库， git push -u origin login  （login 是分支名）

// 二. 完成了功能后， 创建分支 （提交到远端仓库）
// 页面 功能完成后（发现没有创建分支）
// 先创建 分支并切换到分支上（所有的代码都会跟着切换到 分支上）
git checkout -b user

// 添加到 暂存区
git add .

// 提交代码  并注释
git commit -m '添加完成用户列表功能'

// 提交代码到远端 并且将分支也提交到远端仓库
git push -u origin user

// 切换到主分支
git checkout master

// 合并分支
git merge user

// 推送到 远端仓库
git push

// 三. 先创建分支，并将分支提交到云端， 再写代码完成页面的功能，功能完成后将代码提交到云端，最后和master合并，再将master分支的代码提交到云端

// 写页面代码之前，将分支提交到云端
git checkout -b order
git push -u origin order

// 查看分支
git branch

// 将分支代码提交到暂存区 并且提交到云端
git status
git add .
git status
git commit -m '完成了订单页面的功能'
git push

// 最后将分支代码合并，再将master合并的代码提交到云端
git checkout master
git merge order
git push
```