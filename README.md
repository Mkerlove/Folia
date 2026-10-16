# Folia for Android · 安装包分发

本仓库用于存放 **Folia Android 版**的安装包（APK），方便直接下载安装。

## 什么是 Folia

[Folia](https://github.com/chthollyphile/folia-major) 是一款主打**全屏沉浸式歌词动画**的跨平台音乐播放器，支持网易云、QQ 音乐、酷狗、酷我、Navidrome 及本地音乐库等音源，歌词以文字逐帧动效、色彩渐变等形式呈现，兼顾响应式布局。

## 关于本仓库的安装包

上游项目 **官方并未提供 Android 版本**，其 Releases 仅包含 Windows / macOS / Linux 桌面端安装包。

这里的 APK 来自社区的非官方 Android 移植：[**whycfawa/folia-android**](https://github.com/whycfawa/folia-android)。

该移植版基于上游原版修改，新增了：

- Capacitor Android 容器
- 内置平台桥（原生层代理网络请求与 Cookie）
- 后台播放前台服务
- 锁屏媒体控制
- 本地音乐导入

改动说明与构建步骤详见该仓库的 `ANDROID_PORT.md`。

## 下载

前往本仓库的 [Releases](../../releases) 页面，下载最新版本的 APK。

### 当前版本

| 项目 | 值 |
| --- | --- |
| 应用名 | Folia |
| 包名 | `top.izuna.foliamajor` |
| 版本 | `0.7.18-android.155` |
| versionCode | 193 |
| 文件大小 | 35,836,147 字节 (约 34.2 MiB) |
| 最低系统 | Android 7.0 (API 24) |
| 目标系统 | Android 16 (API 36) |

### 校验值

下载后建议核对 SHA-256，确认文件完整、未被篡改：

```
9df6a940568ded51fb62ee3d6a00a9109540ea5b11dfebe3052e8f84fbd2f1d5
```

Windows 可用 `certutil -hashfile 文件名 SHA256`，macOS / Linux 可用 `shasum -a 256 文件名` 校验。

## 安装说明

1. 下载对应版本的 APK 文件
2. 在手机上点击安装；系统可能提示「未知来源应用」，需在设置中允许当前来源安装应用
3. 首次启动按提示授予通知、媒体音频读取等权限（用于后台播放和导入本地音乐）

> **升级提示**：该 APK 使用 Android 调试签名（debug keystore），无法通过应用商店更新。后续升级请回到本仓库 Releases 下载新版本覆盖安装。

## 权限说明

该应用仅申请播放器必需的权限：

| 权限 | 用途 |
| --- | --- |
| `INTERNET` | 在线搜索、加载歌曲与歌词 |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | 后台播放 |
| `POST_NOTIFICATIONS` | 播放通知与锁屏控制 |
| `READ_MEDIA_AUDIO` / `READ_EXTERNAL_STORAGE` | 导入本地音乐 |
| `WAKE_LOCK` | 息屏继续播放 |
| `CHANGE_WIFI_STATE` | 局域网音源（如 Navidrome） |

不包含定位、通讯录、短信、相机、麦克风等敏感权限。

## 免责声明

- 本仓库**仅为安装包的分发镜像**，不包含源代码，与 Folia 上游作者及移植作者均无隶属关系。
- 所有版权归原作者所有。Folia 上游项目以 **AGPL-3.0** 许可证发布，本仓库不修改、不附加任何许可限制。
- 安装包按「原样」提供，不对可用性、安全性作任何担保，请自行评估后使用。
- 仅供个人学习、技术交流与非营利测试使用，**请勿用于任何商业盈利用途**。
- 若权利人认为本仓库内容不妥，请联系删除。

## 相关链接

- 上游项目：https://github.com/chthollyphile/folia-major
- Android 移植：https://github.com/whycfawa/folia-android
- 官方在线版：https://folia-site.cielaniska.top
