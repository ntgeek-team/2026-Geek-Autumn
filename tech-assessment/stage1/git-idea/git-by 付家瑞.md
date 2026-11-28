#  Git 学习感想
> 付家瑞

## 今天踩过的坑
今天遇到的报错中让我印象最深的主要有以下几个：

1. **`git config` 配置了却没生效**：我输的是 `git config --global user.name"741Ray"`，漏了空格。Git 把 `user.name741Ray` 当成完整键名去读取，找不到就静默返回了，看起来像成功其实没有。
2. **`git commit` 忘了 `-m`，掉进 vim 编辑器**：Git 自动打开编辑器让我写提交说明，我按教程按 `i` 却多按了一次，第一行多了个孤零零的 `i`。最后用 `Esc` → `:q!` 退出，改用 `git commit -m "说明"` 解决
3. **SSH 端口不通**：`ssh: connect to host github.com port 22: Connection refused`。我一开始用 `git@github.com:...` 的 SSH 地址显示网络端口不通，后面改为http才走通
5. **push 成功却看不到文件**：推到 `Tasks` 仓库后，网页默认显示 `main` 分支，而我推的是 `master` 分支。
6. **PR 提不了**：我在 Tasks 仓库想用 PR 合并 master 到 main，GitHub 却提示 `There isn't anything to compare`，因为那两个分支一个是 `git init` 新建的、一个是仓库原有的，没有共同祖先。


