# AGENTS.md

这是 Dust Front RTS Demo 简体中文补丁的发布仓库：只放补丁 ZIP 和给玩家看的文档。补丁在维护者的 Windows 上构建，构建工具、翻译源文件和工作记录都留在本地。本地命令用 PowerShell 7 写。

## 仓库文件

`.gitignore` 是白名单，公开文件只有：

- `README.md`、`CHANGELOG.md`、`AGENTS.md`
- `licenses/OFL.txt`
- `dist/DustFront-RTS-Demo-zhCN-vX.Y.Z.zip`：只放当前版本，发新版时 `git rm` 旧 ZIP。旧版本从 Releases 下载。
- `.github/`：Release workflow 和 Dependabot 配置

要公开其他文件，先征得用户同意，再在 `.gitignore` 中逐个放行。

## 文档写法

读者是玩家。每句话都要帮玩家完成一件事：下载、安装、使用、恢复、反馈。写事实和步骤，用短句。

- README 写长期不变的内容：适用版本、下载、安装、恢复、反馈、字体许可。每次发版只改版本号和适用的游戏版本。
- 每个版本的变化写在 `CHANGELOG.md`，这一节原样成为 Release 正文。
- 已知范围只写玩家在游戏里能看到的差异，例如“语言菜单仍显示 English”。
- 用户删掉的内容就是不要的内容，保持删掉。

以下都是**防御性语句**，删掉整句，不要换个说法保留：

| 例子 | 原因 |
| --- | --- |
| “已检查菜单、教程……未穷尽所有战斗事件、单位组合和分辨率。” | 测试过程和覆盖范围不是玩家要做的事 |
| “可能仍有漏译和排版问题。” | 空泛的保留意见；有具体问题就写进已知范围 |
| “字体许可证仅适用于字体，不代表对游戏内容……授予相同许可。” | 法律式免责 |
| “GitHub 自动生成的 Source code 是仓库快照，不是安装包。” | 解释 GitHub 界面 |
| “现有的 `.bak` 文件不会被覆盖。” | 实现细节 |
| SHA-256 校验文件、校验值、校验方法 | GitHub Release 页面已为每个附件显示 SHA-256 |
| 仓库收录范围、白名单、发布流程、构建工具 | 维护信息，只写在本文件 |

“非官方补丁，与游戏开发者无关”这类声明在 README 中写一句即可。

## 发布

Release 由 `.github/workflows/release.yml` 在推送 `vX.Y.Z` tag 时创建。附件只有补丁 ZIP，正文是 CHANGELOG 对应一节加一行安装说明链接。发布只走这个 workflow。

1. 拿到用户提供的新 ZIP。用 `tar -tf <ZIP>` 确认顶层只有 `DustFront-zhCN/`，并包含 `PatchInstaller.exe`、`manifest.json`、`OFL.txt` 和 `payload/`。
2. `git rm` 旧 ZIP，把新 ZIP 放到 `dist/DustFront-RTS-Demo-zhCN-vX.Y.Z.zip`。`dist/` 里只有这一个文件。
3. 在 `CHANGELOG.md` 顶部加一节，标题严格为 `## vX.Y.Z — YYYY-MM-DD`（破折号是 `—`）。第一行写适用的游戏版本，然后列出变化和已知范围，按上面的写法。
4. 更新 README 的版本号和适用的游戏版本。
5. 提交 `release: vX.Y.Z` 并推送 `main`。可在 Actions 页面手动运行 Release workflow 预检，手动运行只校验、不发布。
6. 得到用户确认后，推送 tag：`git tag vX.Y.Z && git push origin vX.Y.Z`。

完成标准：workflow 成功；Release 页面只有一个 ZIP 附件，正文与 CHANGELOG 一致。

推送、打 tag、编辑已发布的 Release 都先问用户。

## 提交

提交信息使用 Conventional Commits 前缀：`docs:`、`ci:`、`release:`、`chore:`。作者只写维护者本人：提交信息、PR、Release 和文档中不加任何 AI 署名或 `Co-Authored-By` 行。
