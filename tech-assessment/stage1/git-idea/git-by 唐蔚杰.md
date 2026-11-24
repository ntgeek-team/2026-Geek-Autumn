# 学习笔记
---
## 学习背景
本次学习Git、GitHub基础操作与Markdown语法，掌握仓库创建、文件提交、推送、PR协作等基础流程。

## 学习内容的目录
- Git基础命令：clone、add、commit、push、pull
- GitHub协作：Fork、分支、PR（Pull Request）
- Markdown基础语法，在GitHub和VS Code中使用
- VS Code图形化Git操作，对比Git Bash命令行

## 学习内容
### 1. Git基础命令
clone、add、commit、push、pull
我理解了本地仓库和远程仓库是分开的。
- clone：把网上仓库下载到电脑
- add：把文件标记为待提交
- commit：保存这次改动
- push：把本地改动传到网上
- pull：把网上最新的改动拉回本地

一开始很容易搞混 push 和 pull，记反方向，多操作几次才慢慢分清。

### 2. GitHub协作
Fork、分支、PR（Pull Request）
- Fork是复制一份别人的仓库到自己账号里，自己可以修改。
- 正式提交任务不能直接在 main 分支改，要新建分支，改完之后发起PR，等待管理员审核合并。
这个规范是为了保护主仓库，避免大量直接修改把内容弄坏。

### 3. Markdown基础语法
在GitHub和VS Code中使用
Markdown用来写文档，用简单符号实现标题、列表、加粗、插入图片，不用复杂排版。
在VS Code里可以实时预览，上传到GitHub也能正常渲染。
上手很简单，写笔记、写README都很合适，以后可以多用它记录学习。

### 4. VS Code图形化操作，对比Git Bash命令行
Git Bash敲命令，功能全但是要记很多指令；VS Code有可视化面板，能直接看到哪些文件改动了，对新手更友好。
可视化适合入门，但是命令也要了解，很多场景只能用命令操作。
### 5. PR完整流程与Pull同步代码的意义
- 完整的Fork模式PR流程：先Fork目标仓库，再Clone到本地，新建分支修改文件，本地add、commit保存改动，push推送到个人远程分支，在GitHub发起PR并填写信息，等待评审修改，最后由管理员合并代码。
- 发起PR之前建议先pull同步远程代码。因为公共主仓库一直在被其他人更新，如果本地代码版本太旧，直接提交PR会产生代码冲突。提前pull可以同步最新代码，提前解决冲突，保证PR可以顺利合并。
 ## 参考资料
 [抖音fork教程](https://v.douyin.com/G-RgVtOF3dE/)
 
 [B站Git教程](https://b23.tv/TsdhnMo)

 [vs code入门教程](https://b23.tv/x8HftAR)

 [git与vs code结合使用](https://b23.tv/DGLbVBS)
## 遇到的问题与收获
1. 网页端修改和本地仓库不会自动同步，忘记pull会出现版本不一致
2. 图片粘贴上传GitHub时，网络慢容易上传卡住
收获：明白了版本控制的意义，多人协作不能直接在main主分支修改。
