# gitskills
This is a test for remote git clone
---
### 实现多人协作开发
首先创建一个仓库，勾选Initialize this repository with a README

这样会自动创建一个README.md文件

创建好该远程库之后，就可以使用命令
```
git clone git@github.com:username/repository.git
```
克隆到本地，进入文件夹之后就可以进行开发和git管理了


测试
---
### 添加分支

(1)创建一个新的分支dev。同时切换到该分支
```
git checkout -b dev
```
---
### 分支
现在已经在dev分支下了，对工作区进行修改和提交的内容都在dev分支下，master分支的内容不会发生改变
之后对README 的内容进行修改，之后add commit 提交
这时如果切换到主分支　ｍａｓｔｅｒ
```
git checkout master
```
会发现master中的README没有发生改变
使用命令
```
git merge dev
```
合并之后在master分支下的README更新了


之后可以通过
```
git branch -d dev
```
删除分支
---
### 分支冲突
分支冲突解决：
>>>>>>> feature1
出现的原因：在ｍｅｒｇｅ前修改了ｍａｓｔｅｒ的内容，之后在ｍｅｒｇｅ就会出现冲突的问题
![conflict](/images/conflict.png)

所以在分支的需求修改完毕之后，尽量在ｍｅｒｇｅ了之后再去修改ｍａｓｔｅｒ的内容，否则发生冲突之后就需要人工手工去修改
---

