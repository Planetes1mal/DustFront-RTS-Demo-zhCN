# Dust Front RTS Demo 简体中文补丁

非官方简体中文补丁，当前版本 **v1.0.0**，适用于 **Demo D-32 / Steam Build 25969910**。请先通过 Steam 安装对应的游戏 Demo。

## 下载

在本仓库的 [Releases](https://github.com/Planetes1mal/DustFront-RTS-Demo-zhCN/releases) 页面下载对应版本的 ZIP 和 SHA-256 校验文件。当前版本的发布文件也保存在仓库中：

- [DustFront-RTS-Demo-zhCN-v1.0.0.zip](dist/DustFront-RTS-Demo-zhCN-v1.0.0.zip)（约 2.9 MB）
- [SHA-256 校验文件](dist/DustFront-RTS-Demo-zhCN-v1.0.0.zip.sha256)
- [版本记录](CHANGELOG.md)

请下载补丁 ZIP；GitHub 自动生成的 `Source code (zip)` 和 `Source code (tar.gz)` 是仓库快照，不是安装包。

## 安装

1. 退出游戏。在 Steam 中右键游戏，选择“管理 → 浏览本地文件”。
2. 解压补丁，把整个 `DustFront-zhCN` 文件夹放进游戏根目录，与 `Dust Front RTS.exe` 并列。
3. 运行 `DustFront-zhCN/PatchInstaller.exe`，确认游戏目录，点击“安装汉化”。
4. 从 Steam 正常启动游戏，语言选择 **English**，即可显示中文。

```text
Dust Front RTS Demo/
├── Dust Front RTS.exe
├── Dust Front RTS_Data/
└── DustFront-zhCN/
    ├── PatchInstaller.exe
    ├── manifest.json
    ├── payload/
    ├── OFL.txt
    └── 使用说明.txt
```

安装器会校验文件版本，并把原文件备份到游戏根目录的 `.dustfront-zhcn-backup`。现有的 `.bak` 文件不会被覆盖。游戏版本或文件不匹配时，安装器会停止操作。

## 恢复原版

退出游戏，再运行安装器并点击“恢复原版”。恢复前请保留补丁文件夹及 `.dustfront-zhcn-backup`。若 Steam 已更新游戏，不要用旧版补丁或旧备份覆盖新版文件。

## 翻译范围

主语言表 633 条、教程语言表 70 条已全部翻译，并补充处理额外界面文字和中文字体。已实机检查菜单、教程、部署、战斗界面、单位属性和结算，安装与还原也已验证。

- 使用 English 语言槽位，未新增独立的“简体中文”选项。
- 视频及美术中固有文字、配音不在本版翻译范围内。
- 帧率上限的 `None`（不限）、FPS、VSync、MCV、快捷键、型号和署名等保留原样。
- 尚未逐一触发全部战斗事件或测试所有分辨率，可能仍有漏译和排版问题。

反馈问题时，请附游戏版本、补丁版本、截图和复现操作。安装器的完整操作说明随 ZIP 提供。

## 仓库收录范围

这是补丁发布仓库。`.gitignore` 采用严格白名单，当前仅允许以下 **7 个文件**进入 Git：

```text
.gitattributes
.gitignore
README.md
CHANGELOG.md
licenses/OFL.txt
dist/DustFront-RTS-Demo-zhCN-v1.0.0.zip
dist/DustFront-RTS-Demo-zhCN-v1.0.0.zip.sha256
```

**允许的内容：** 面向玩家的使用说明、版本说明、字体许可、Git 文件规则，以及逐个列入白名单的补丁 ZIP 和对应校验文件。发布 GitHub Release 时，将 ZIP 和校验文件作为附件上传。

**不收录的内容：** 开发工具与依赖、构建脚本、分析及反编译结果、过程文档、测试报告与截图、原始导出表、翻译工作文件、推广草稿、游戏完整副本、原文件和备份。`dist` 中展开的安装包目录同样不进入 Git。

本地工作资料可以保留在同一工作区，但不属于公开仓库。新增版本时，应核对安装包内容，并在 `.gitignore` 中显式放行该版本的 ZIP 和校验文件；不要整体放行 `dist` 或其他工作目录。

## 字体与声明

中文字体基于 [Noto Sans SC](https://github.com/google/fonts/tree/main/ofl/notosanssc)，采用 SIL Open Font License 1.1。补丁包含调整内部名称后的字体子集，版权声明与完整许可见 [licenses/OFL.txt](licenses/OFL.txt)，安装包内也保留该文件。

这是玩家制作的非官方补丁，不包含完整游戏，与游戏开发者没有官方隶属关系。游戏名称、美术和原始内容的权利归各自权利人所有。字体许可证仅适用于字体，不代表对游戏内容或其他补丁组件授予相同许可。
