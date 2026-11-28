# Git 学习笔记
> 参考文献：
 > [Git+Github核心概念大串讲](https://www.bilibili.com/video/BV1ySLc6QEcB?vd_source=eb8cf482f11927ebcf85fbab806d25b3)
 > [VS Code中使用Markdown书写](https://b23.tv/R6lGIDx)
## 任务一
生成 SSH 密钥，用 SSH 连上 GitHub，把我电脑上写好的文件传到网上的仓库里。

## 一、配置 SSH Key
1. 打开 Git Bash
2. 敲命令：ssh-keygen -t ed25519 -C "我的github邮箱"
3. 后面全部直接回车，不用设置密码
4. 找到公钥文件 id_ed25519.pub，把里面所有文字复制
5. 去 GitHub 设置里找到 SSH and GPG keys，点新增，粘贴进去保存
6. 测试能不能连上：ssh -T git@github.com，出现成功提示就是弄好了

## 二、把仓库下载到自己电脑
1. 在 GitHub 复制仓库的 SSH 地址
2. git clone 粘贴的地址
3. cd 仓库名字，进到这个仓库文件夹里面

## 三、新建文件、保存、上传（hello.md 的流程）
1. 新建 hello.md 文件
2. git add hello.md：告诉 Git，这个文件我要提交上传
3. git commit -m "add hello.md"：打包这次改动，写一句备注，方便以后看
4. git pull --no-edit：先拉取网上最新内容，不然上传的时候容易被拒绝
5. git push：把我这边改好的东西传到 GitHub 网上仓库

 - 具体操作{创建git学习笔记的流程)
  > 1. 创建文件
echo "# Git 学习笔记" > git笔记.md

  > 2. 打开 nano 编辑器写内容（可选，如果直接在命令行写好就不用写了）
nano git笔记.md

  > 3. 把这个文件加入暂存区，告诉 Git 要跟踪这个改动
git add git笔记.md.

  > 4. 生成本地提交，-m 后面写这次改动的备注
git commit -m "新增git学习笔记"

  > 5. 先拉取远程最新内容，防止推送被拒绝
git pull --no-edit

  > 6. 上传（推送）到 GitHub
git push

### 用vscode代替nano的流程
1. 先在VScode中下载markdown相关的插件
2. 书写：在桌面新建文件夹，通过code打开
3. 打开新建文件，注意后缀为“.md”
4. 上传：打开gitbash，进入桌面存放的文件夹
 - cd /c/Users/用户名/Desktop/Note
 - git status:查看当前状态
 - 若不是git仓库，先初始化+绑定远程仓库：git init;git remote add origin git@github.com:你的用户名/仓库名.git 
5. 加入暂存区：git add
6. git commit -m“上传Markdown笔记”
7. git pull --no-edit
8. 首次推送：git push -u origin main
   
## 踩过的坑
- push 上传被拒绝：网上仓库有别人/别的地方更新过内容，我这边不是最新的，要先 pull 拉一下再上传
- 突然弹出 nano 编辑页面：合并的时候跳出来的，很容易卡住，有时候可能Ctrl+x也退不出来，后面加 --no-edit 就可以自动处理，不弹出这个窗口
- 提示不是 git 仓库：我没进到正确的文件夹，要用 cd 切到仓库目录再敲 git 命令
- 注意标点的中英文，不然容易出错
