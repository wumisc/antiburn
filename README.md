# 防烧屏 · Antiburn

LSPosed / Xposed 模块，包名 `io.github.wumisc.antiburn`。给 OLED 屏做常驻防烧屏：像素位移、状态栏与导航栏兜底、应用内固定区域遮盖，并对抖音 / 红果短剧 / 快手 / B 站的常驻 UI 做分区隐藏。

## 反馈

- **问题反馈、功能建议**：直接开 issue 👉 https://github.com/wumisc/antiburn/issues
- 开 issue 请附：机型、ROM 版本、Android 版本、LSPosed 版本、模块版本号，以及「诊断日志」导出（App 首页 › 功能设置 › 诊断日志 › 导出）。有日志和没日志，定位速度差一个数量级。
- 这里是**主仓库**：issue 在这里收，源码也在这里跟进。
- 安装入口是 LSPosed 平台镜像 `Xposed-Modules-Repo/io.github.wumisc.antiburn`，那个仓库的 issues 被平台统一禁用，请不要在那里留言（写了没人能看到）。

## 安装

1. LSPosed 里启用模块，作用域勾选 **系统框架（com.android.systemui）**；要让 App 内隐藏生效，再勾选目标视频 App。
2. 安装包用独立正式签名（`CN=Antiburn, O=wumisc, OU=Release, C=CN`）。**3.4.0 起签名与 3.3.x 不同**，覆盖安装会失败，请先卸载旧版再装。
3. 像素位移 / 遮盖按首页提示开对应开关；无障碍兜底通道可选。

## 目录

```
antiburn-lite/   模块源码（Android，Java + 少量 Compose/Kotlin）
tests/           本地验证套件（javac 直跑，不需要模拟器）
cf/              日志上传后端（Cloudflare Pages Functions + D1）
docs/            版本说明与设计记录
```

## 版本

当前 `3.4.0`（vc142）。历史版本与安装包见镜像仓库 Releases：
https://github.com/Xposed-Modules-Repo/io.github.wumisc.antiburn/releases

## License

MIT
