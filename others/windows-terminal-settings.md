---
layout: note
title: Windows terminal设置
permalink: /others/windows-terminal-settings/
---

# 问题背景

因为现在公司使用的都是 ssh 登录到服务器那边使用 AI CLI agent 工具，例如 codex、copilot 等。但是在 Windows 平台上使用 ssh 登录的工具，在使用这些 AI CLI agent 的时候，总是有各种各样的问题。例如 xshell 和 tabby 存在乱码和错乱的问题，这些问题很难找到合适的解决方式，因为涉及到多个系统之间的适配，AI CLI agent 和终端登录工具，Windows 和 Ubuntu 系统。所以我决定采用 Windows Terminal 加上 PowerShell 7 来进行，这样能确保尽量少因为第三方系统引入问题。

# 配置修改

## 安装 PowerShell 7

Windows 上面内置有 Windows PowerShell，这个和 PowerShell 7 有比较大的区别。PowerShell 7 相当于是 Windows PowerShell 的一个开源跨平台版本，功能更多，处于活跃开发期。例如历史命令提示补全。

## 修改字体

因为我在 Ubuntu 那边使用了 `lsd`，直接 ssh 后发现 `lsd` 显示前面的图标会乱码，所以需要安装字体，然后在 Windows Terminal 中设置对应配置文件中的字体。

我现在使用的字体是：`CaskaydiaMono Nerd Font Mono`

## 修改配色方案

我现在使用的配置方案是：

https://github.com/mbadolato/iTerm2-Color-Schemes/blob/master/windowsterminal/Nord.json

## 默认打开 ssh 登录的 pwsh.exe

![Windows Terminal 默认打开 ssh 登录的 pwsh.exe](/assets/others/windows-terminal-settings/image-1.png)

![Windows Terminal 默认打开 ssh 登录的 pwsh.exe 配置细节](/assets/others/windows-terminal-settings/image-2.png)

## 新增 gitbash 选项

因为 gitbash 在 Windows 可以使用 `grep` 和 `find` 命令，有时候会有一些用处。

# 最终结果

![最终结果](/assets/others/windows-terminal-settings/image-3.png)

https://chat.deepseek.com/share/o1g6ug0moaosueuljz

[settings.json 配置文件](/assets/others/windows-terminal-settings/settings.json)
