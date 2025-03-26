<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="logo.png" width="256" height="256" />
</p>

<div align="center">

# MAA_Punish

基于全新架构的 战双帕弥什 小助手。图像技术 + 模拟控制，解放双手！  
由 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 强力驱动！

</div>

<p align="center">
  <img alt="license" src="https://img.shields.io/github/license/overflow65537/MAA_Punish">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
  <img alt="platform" src="https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-blueviolet">
  <img alt="commit" src="https://img.shields.io/github/commit-activity/m/overflow65537/MAA_Punish">
  <img alt="mirrorchyan_rid" src="https://img.shields.io/badge/mirrorchyan_rid-MAA__Punish-orange">
</p>

## 主要功能

- 启动/关闭游戏
- 指挥局抽签
- 宿舍委托
- 宿舍任务
- 指挥局签到
- 拟真围剿
- 纷争战区自动首通
- 诺曼矿区自动首通
- 幻痛囚笼自动首通
- 维系者行动
- 领取邮件
- 商店自动购买逆元碎片
- 领取体力
- 自动刷拟战场域
- 领取凭证和任务奖励
- 自动肉鸽-矩阵循生
- 自动肉鸽-寒境曙光
  
## 注意事项

- 打开无法运行首先尝试安装运行库 <https://learn.microsoft.com/zh-cn/cpp/windows/latest-supported-vc-redist?view=msvc-170>
- 如有其他问题可以提交issue或者加群反馈965061066

## 图形化界面

### [MFW-PyQt6](https://github.com/overflow65537/MFW-PyQt6)

 一个基于PyQt6的MAAFramework图形化操作界面

- 下载对应系统架构,后缀带有MFW-PyQt的压缩包,比如`MPA-win-x86_64-MFW-PyQt-vXXX.zip`
- 解压后运行MFW.exe
  
## 使用说明

下载地址：<https://github.com/overflow65537/MAA_Punish/releases>

### Windows

- 对于绝大部分用户，请下载 `MPA-win-x86_64-vXXX.zip`
- 若确定自己的电脑是 arm 架构，请下载 `MPA-win-aarch64-vXXX.zip`
- 解压后以***管理员权限***运行 `MaaPiCli.exe` 即可

### macOS

- 若使用 Intel 处理器，请下载 `MPA-macos-x86_64-vXXX.zip`
- 若使用 M1, M2 等 arm 处理器，请下载 `MPA-macos-aarch64-vXXX.zip`
- 使用方式：

  ```bash
  chmod a+x MaaPiCli
  ./MaaPiCli
  ```

### Linux

~~用 Linux 的大佬应该不需要我教~~

## MaaPiCli使用说明

### A

- 启动后会出现:

```bash
Welcome to use Maa Project Interface CLI!

Version: v0.0.1

### Select ADB ###

        1. Auto detect
        2. Manual input

Please input [1-2]:
```

- 如无必要，请选择1.Auto detect

```bash
### Select ADB ###

        1. Auto detect
        2. Manual input

Please input [1-2]: 1

Finding device...

## Select Device ##

        1. MuMuPlayer12
                H:/Program Files/Netease/MuMuPlayer-12.0/shell/adb.exe
                127.0.0.1:16672

Please input [1-1]: 1
```

- 选择 1 后会像上面这样，列出若干个模拟器实例，之后选择你需要进行操控的即可。
- 如果没有出现选项，请检查模拟器是否正常启动。以及管理员权限启动MaaPiCli。

### B

- 选择完模拟器后就会进入到选择资源界面

```bash
### Select resource ###

        1. 官服
        2. B 服

Please input [1-2]:
```

- 请按照自己的服务器类型选择

### C

- 在初次启动后，会让你输入启动的任务：

```bash
### Add task ###

        1. 进入游戏
        2. 指挥局
        3. 领取体力
        4. 领取邮件
        5. 购买碎片
        6. 宿舍委托
        7. 拟战场域
        8. 守护者行动
        9. 领取任务
        10. 战令
        11. 结束游戏

Please input [1-11]:
```

- 选择你要执行的任务即可。

### D

- 之后会反复出现：

```bash
Tasks:

<这里会列出你已经增加，等待执行的任务>

### Select custom_actions ###

        1. Switch controller
        2. Switch resource
        3. Add task
        4. Move task
        5. Delete task
        6. Run tasks
        7. Exit
```

- 其中分别代表：

1. 调整控制器（也就是adb地址等）
2. 调整资源（切换官服或者b服）
3. 新增任务，像**C**中那样
4. 移动任务
5. 删除任务
6. 开始执行任务，在这之后就会自动开始操控。
7. 退出程序

## 其他说明

- 添加 `-d` 参数可跳过交互直接运行任务，如 `./MaaPiCli.exe -d`，配合Windows计划任务可以实现自动开启任务
- 反馈问题请附上日志文件 `debug/maa.log`，谢谢！

## How to build

**如果你要编译源码才看这节，否则直接 [下载](https://github.com/overflow65537/MAA_Punish/releases) 即可**

0. 完整克隆本项目及子项目

    ```bash
    git clone --recursive https://github.com/overflow65537/MAA_Punish.git
    ```

1. 下载 MaaFramework 的 [Release 包](https://github.com/MaaXYZ/MaaFramework/releases)，解压到 `deps` 文件夹中
2. 安装

    ```python
    python ./install.py
    ```

生成的二进制及相关资源文件在 `install` 目录下

## 开发相关

- [MaaFramework 快速开始](https://github.com/MaaAssistantArknights/MaaFramework/blob/main/docs/zh_cn/1.1-%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B.md)

## 鸣谢

### 开源库

- [MaaFramework](https://github.com/MaaXYZ/MaaFramework)
  
  基于图像识别的自动化黑盒测试框架 | An automation black-box testing framework based on image recognition
- ~~[MFAWPF](https://github.com/SweetSmellFox/MFAWPF)~~
  
  ~~本项目是一个基于WPF框架开发的用户界面，旨在提供类似于MaaPiCli的功能~~

### 开发者

感谢以下开发者对 MAA_Punish 作出的贡献：

<a href="https://github.com/overflow65537/MAA_Punish/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=overflow65537/MAA_Punish&max=1000" alt="Contributors to MAA_Punish"/>
</a>
