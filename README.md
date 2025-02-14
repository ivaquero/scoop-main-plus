# 🍨 Scoop Main Plus 🍨

[![Excavator](https://github.com/ivaquero/scoop-main-plus/actions/workflows/ci.yml/badge.svg)](https://github.com/ivaquero/scoop-main-plus/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/ivaquero/scoop-main-plus)](https://github.com/ivaquero/scoop-main-plus/blob/master/LICENSE)
[![code size](https://img.shields.io/github/languages/code-size/ivaquero/scoop-main-plus.svg)](https://img.shields.io/github/languages/code-size/ivaquero/scoop-main-plus.svg)
[![repo size](https://img.shields.io/github/repo-size/ivaquero/scoop-main-plus.svg)](https://img.shields.io/github/repo-size/ivaquero/scoop-main-plus.svg)

A Bucket for the Best Windows Package Manager [Scoop](https://github.com/ScoopInstaller/Scoop): An Enhancement for the Official CLI Bucket.

> If you would like to be a co-maintainer, feel free to tell me in the Discussion.

For ones familiar with Scoop:

```powershell
scoop bucket add main-plus https://github.com/ivaquero/scoop-main-plus
```

Enjoy the fun of command line!

# 🏃 To Start

## 🚲 Install Scoop

### 💻 Step 1: Enable remote policy in PowerShell

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

### ⚙️ Step 2: Download and install Scoop

```powershell
irm get.scoop.sh -outfile 'install.ps1'
.\install.ps1 -ScoopDir ['Scoop_Path'] -ScoopGlobalDir ['GlobalScoopApps_Path'] -NoProxy
# for example
.\install.ps1 -ScoopDir 'C:\Scoop' -ScoopGlobalDir 'C:\Program Files' -NoProxy
```

> If you skip this step, all user installed Apps and Scoop itself will live in `c:/users/user_name/scoop`.

### 📖 Step 3: Glance at quick-start by `scoop help`

For more information, please visit Scoop official site at 👉 https://scoop.sh/ 👈

## 🚗 Install Apps from this bucket

### 🚋 Step 1: Install Aria2 to accelerate downloading

```powershell
scoop install aria2
```

### 🎫 Step 2: Install Git to add new repositories

```powershell
scoop install git
```

if you are using VPN, you need to turn off aria2 before installing Apps

```powershell
scoop config aria2-enabled false
```

### ✈️ Step 3: Add this wonderful bucket and update, mua~ 💋

```powershell
scoop bucket add main-plus https://github.com/ivaquero/scoop-main-plus
scoop update
```

### 🚀 Step 4: Install Apps

#### Check the exact name of App by `scoop search`

```powershell
scoop search <app_name>
```

#### Install Apps with assistance of plugin `scoop-completion`

```powershell
scoop install scoop-completion
scoop install <app_name>
```

> to use `scoop-completion`, just to hit `tab` after initial letters of App names

## 📝 Trivial

### Tweak with Parameters in Aria2

```powershell
scoop config aria2-enabled true
scoop config aria2-retry-wait 4
scoop config aria2-split 16
scoop config aria2-max-connection-per-server 16
scoop config aria2-min-split-size 4M
```

## ⭐️ Summary

### CLI

|                            App                            | Auto-Update ? | Original ? |
| :-------------------------------------------------------: | :-----------: | :--------: |
| [LTeX-ls-Plus](https://github.com/ltex-plus/ltex-ls-plus) |       ✓       |     ✓      |
|     [MicroMamba](https://github.com/mamba-org/mamba)      |       ✓       |     ✓      |
|   [N-m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE)   |       ✓       |     ✓      |
|        [pixi](https://github.com/prefix-dev/pixi)         |       ✓       |     ✓      |
|      [sendme](https://github.com/n0-computer/sendme)      |       ✓       |     ✓      |
|      [serpl](https://github.com/yassinebridi/serpl)       |       ✓       |     ✓      |
|  [wthrr](https://github.com/ttytm/wthrr-the-weathercrab)  |       ✓       |     ✓      |

## Notes

Due to the complexity of Win to permission management, for some common applications that do not provide portable installation packages and require administrator application permissions, it is recommended to use WinGet for installation

```powershell
scoop install winget
winget install Rakuten.Viber
```
