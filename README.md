# Dust Front RTS Demo 简体中文补丁

非官方简体中文补丁，当前版本 **v1.0.0**，适用于 **Demo D-32 / Steam Build 25969910**。请先通过 Steam 安装对应的游戏 Demo。

## 下载

在本仓库的 [Releases](https://github.com/Planetes1mal/DustFront-RTS-Demo-zhCN/releases) 页面下载对应版本的 ZIP 文件。当前版本的发布文件也保存在仓库中：

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

## 问题反馈

反馈问题时，请附游戏版本、补丁版本、截图和复现操作。安装器的完整操作说明随 ZIP 提供。

## 字体与声明

中文字体基于 [Noto Sans SC](https://github.com/google/fonts/tree/main/ofl/notosanssc)，采用 SIL Open Font License 1.1。补丁包含调整内部名称后的字体子集，版权声明与完整许可见 [licenses/OFL.txt](licenses/OFL.txt)，安装包内也保留该文件。

这是玩家制作的非官方补丁，不包含完整游戏，与游戏开发者没有官方隶属关系。游戏名称、美术和原始内容的权利归各自权利人所有。字体许可证仅适用于字体，不代表对游戏内容或其他补丁组件授予相同许可。
