# 升级 Android 17 后 Shizuku 无法启动

Date: 2026-11-10 | Category: 手机

## 问题
升级 Android 17 后，thedjchi 分支的 Shizuku 13.7.0 无法启动运行。官方 Shizuku 13.6.0 在 Android 17 上也有已知问题 (GitHub Issue #2180)：能启动但显示 0 个已授权应用，无法新授权，所以新装 Canta 很可能授权失败。

## 解决
用 Termux，通过本地无线调试 (ADB Loopback) 拉起定制修改版 Shizuku：
- Termux 里安装 android-tools 和 nmap
- 首次分屏做一次无线调试配对
- 日常使用只需要在 Termux 里输入 `shizuku`，它会自动扫描 32768-65535 端口、连接无线调试并拉起 Shizuku

## 备注
- Canta 官方仓库：samolego/Canta，用 Shizuku 免 root 卸载系统应用，卸载前先确认应用说明，别批量全选。
- 不要从第三方网站下载 Shizuku；分支版本报告未经核实，仅作记录。
