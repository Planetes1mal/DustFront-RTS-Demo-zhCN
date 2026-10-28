# Dust Front RTS Demo 简体中文补丁

非官方简体中文补丁，当前版本 **v1.1.0**，适用于 **Demo D-35-1 / Steam Build 26104922**。请先通过 Steam 安装对应的游戏 Demo。

## 下载

在 [Releases](https://github.com/Planetes1mal/DustFront-RTS-Demo-zhCN/releases/latest) 下载 `DustFront-RTS-Demo-zhCN-v1.1.0.zip`。各版本的变化见 [CHANGELOG.md](CHANGELOG.md)。

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

安装器会核对游戏版本，并把原文件备份到游戏根目录的 `.dustfront-zhcn-backup-26104922`。

## 恢复原版

退出游戏，运行安装器并点击“恢复原版”。恢复需要补丁文件夹和 `.dustfront-zhcn-backup-26104922`。

Steam 更新游戏后，旧版补丁无法安装，请使用对应的新版本补丁。

## 问题反馈

在 [Issues](https://github.com/Planetes1mal/DustFront-RTS-Demo-zhCN/issues) 反馈，请附游戏版本、补丁版本、截图和复现步骤。

## 字体与声明

中文字体为 [Noto Sans SC](https://github.com/google/fonts/tree/main/ofl/notosanssc) 的子集，采用 SIL Open Font License 1.1，许可见 [licenses/OFL.txt](licenses/OFL.txt)。

这是玩家制作的非官方补丁，与游戏开发者无关。
