---
{"dg-publish":true,"permalink":"/030/steam-deck/"}
---

# 1 快捷键

- 音量减 + 开机键 boot

# 2 双系统

## 2.1 进入恢复模式进行分区

使用kde的分区工具

## 2.2 安装windows

安装驱动

时间同步

使用easyuefi禁用windows boot manager

## 2.3 安装引导

进入steam os，检查一下 **EFI** 分区以下内容是否存在，正常情况下都会存在以下目录的：

- esp/efi/steamOS
- esp/efi/Microsoft

检查完成后，我们执行以下命令进行 **rEFInd** 的安装：

```text-plain
# 拉取 jlobue10 开发的一键安装脚本
git clone https://github.com/jlobue10/SteamDeck_rEFInd/
# 进入脚本目录
cd SteamDeck_rEFInd
# 设置脚本权限
chmod +x SteamDeck_rEFInd_install.sh
# 执行脚本
./SteamDeck_rEFInd_install.sh
```
# 3 插件

先使用 `passwd` 设置用户密码

## 3.1 Decky Loader

插件商店 [https://github.com/SteamDeckHomebrew/decky-loader](https://github.com/SteamDeckHomebrew/decky-loader)

安装  
`curl -L https://github.com/SteamDeckHomebrew/decky-installer/releases/latest/download/install_release.sh | sh`

卸载  
`curl -L https://github.com/SteamDeckHomebrew/decky-installer/releases/latest/download/uninstall.sh | sh`

- Bluetooth 显示最近连接过的蓝牙设置
- vibrantDeck 屏幕色彩饱和度调整及RGB三色调整
- CSS Loader 主题
- ProtonDB Badges 游戏运行兼容程度的评测
- SteamGridDB 自定义游戏封面、logo等
- Animation Changer 自定义开机动画
- To moon 翻墙[https://ohmydeck.net/d/4](https://ohmydeck.net/d/4)

# 4 设置软件商店源

```text-plain
# 禁止只读权限
sudo steamos-readonly disable
# 将商店源改成镜像源
sudo flatpak remote-modify flathub --url=https://mirror.sjtu.edu.cn/flathub
# 将商店源换回官方源
sudo flatpak remote-modify flathub --url=https://flathub.org/repo/flathub.flatpakrepo+
```

# 5 Greenlight

Xbox串流

[https://blog.muffn.io/posts/using-greenlight-to-stream-your-xbox-and-xcloud-to-steamdeck/](https://blog.muffn.io/posts/using-greenlight-to-stream-your-xbox-and-xcloud-to-steamdeck/)

```text-plain
wget https://github.com/TheAssassin/AppImageLauncher/releases/download/v2.2.0/appimagelauncher-lite-2.2.0-travis995-0f91801-x86_64.AppImage

chmod +x ~/Downloads/appimagelauncher-lite-2.2.0-travis995-0f91801-x86_64.AppImage

~/Downloads/./appimagelauncher-lite-2.2.0-travis995-0f91801-x86_64.AppImage install

cd ~/Downloads/
wget https://github.com/unknownskl/xbox-xCloud-client/releases/download/v2.0.0-beta2/Greenlight-2.0.0-beta2.AppImage
```

# 6 NonSteamLaunchers

https://github.com/moraroy/NonSteamLaunchers-On-Steam-Deck



