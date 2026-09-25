# k3screenctrl-apk

适用于斐讯 K3、OpenWrt 25.12+（apk 包管理器）的屏幕控制 APK 包。

## 说明
- 适用硬件：斐讯 K3（5屏版）
- 适用系统：OpenWrt / ImmortalWrt 25.12 及以上（使用 apk 包管理器）
- 源码来源：https://github.com/MSquach/k3screenctrl （5P 分支）
- 编译 SDK：https://mirrors.ustc.edu.cn/openwrt/releases/25.12.5/targets/bcm53xx/generic/openwrt-sdk-25.12.5-bcm53xx-generic_gcc-14.3.0_musl_eabi.Linux-x86_64.tar.zst
- 编译协助：DeepSeek

## 包含文件
- `k3screenctrl-5-r1.apk`：屏幕控制主程序
- `luci-app-k3screenctrl-5-r1.apk`：LuCI 网页控制界面

## 安装方法
将两个 apk 文件上传到路由器 `/tmp` 目录，然后 SSH 登录执行：

```bash
cd /tmp
apk add --allow-untrusted ./k3screenctrl-5-r1.apk
apk add --allow-untrusted ./luci-app-k3screenctrl-5-r1.apk
/etc/init.d/k3screenctrl enable
/etc/init.d/k3screenctrl start
```

## 免责声明与 6 屏版指引

> 本包是作者为了救活自己的 5 屏版 K3，在 Arch Linux 下硬着头皮编译出来的，能用就行，没怎么测试。
>
> 由于手头没有 6 屏设备，**没有编译 6 屏版**。
>
> 如果你是 6 屏版，请去原作者 [MSquach/k3screenctrl](https://github.com/MSquach/k3screenctrl) 仓库拉取 `6P` 分支自行编译。编译流程可以找蓝色大肥鱼(Deepseek)问问。

## 特别感谢

- 编译协助：[DeepSeek](https://www.deepseek.com)
- 源码作者：[MSquach](https://github.com/MSquach/k3screenctrl)
