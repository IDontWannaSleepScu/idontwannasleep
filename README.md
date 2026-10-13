# 本项目仅供网络安全测试、学术研究及个人学习交流使用，严禁用于任何商业目的或非法用途。请于下载后 2 小时内彻底删除相关程序及成果。使用者因违反相关法律法规或滥用本项目而引发的一切后果与法律责任，均由使用者自行承担，原作者不承担任何直接或间接的法律责任。如原厂商认为本项目侵权，请联系我们及时下架删除。

# Release 页面下载程序

# 本仓库说明

本仓库提供 GitHub Actions 自动打卡服务，并附带示例 `information.json` 配置文件。你可以通过 **Use this template** 或 **Fork** 创建自己的仓库，并上传个人的 `information.json` 文件。

本仓库已设置定时打卡任务，但由于 GitHub 服务器的稳定性问题，任务可能延迟执行甚至被取消，建议每天手动进入仓库的 **Actions** 页面运行任务（可使用 GitHub App）。

本仓库仅提供 Linux 版本的打卡程序 `checkin`，Action 运行环境为 Ubuntu。

**抓包用户码及自部署所需的最新构建版本，请前往 Releases 页面下载。后续更新也将发布于该页面。**

# 使用说明

## 解压安装包

## 一、抓取信息（cap）

- Windows：双击 `cap.exe`, 点击 "是" 自动设系统代理 + 装证书，退出自动还原。
- Linux：`sudo ./cap`, 输入密码自动设系统代理 + 装证书，退出自动还原。

完全退出微信再重开

进入成电智慧学工**小程序**中的晚安成电界面

回到终端查看你的用户码, 此字段也会同步保存在 `information.json`

高级功能见 `-h`

## 二、打卡（checkin）

- Windows：双击 `checkin.exe`
- Linux：`./checkin`

默认直接用即可, 会自动读取上一步存储的 `information.json`，不需要配置文件。

高级功能见 `-h`

## 提供 github actions

支持通过 GitHub Actions 定时自动打卡，也可在 GitHub 平台手动触发任务，实现远程打卡。

## 注意

- 获取到的用户码时效不确定, 过期请重新获取

- Windows 缺 `VCRUNTIME140.dll`：装 [VC++ 运行库](https://aka.ms/vs/17/release/vc_redist.x64.exe)。
