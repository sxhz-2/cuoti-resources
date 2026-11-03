# 智能错题本 · 资源与发布仓库

本仓库同时承担两件事：

1. **错题本网页版（在线可打开）** —— 根目录 `index.html`，单文件应用，打开即用，无需构建。
2. **资料清单与镜像** —— `manifest.json` 记录高考真题 / 电子课本 / 知识点资料的分包信息，
   大文件本身放在 **GitHub Releases**，通过 `https://res.sxhzxy.ccwu.cc/` 代理下载。

## 在线地址

- 网页版：<https://sxhz-2.github.io/cuoti-resources/>
- 安装包：<https://sxhz-2.github.io/cuoti-resources/apk/>（手机打开后自动开始下载）

## 目录

```
index.html         错题本网页版（单文件，含全部逻辑与数据）
apk/cuoti-10.60.apk  安卓安装包（当前版本）
apk/index.html     安装包下载页（手机访问自动跳转）
manifest.json      资料清单（schema: cuoti-res/1）
.nojekyll          关闭 Jekyll 处理，纯静态站必须有
```

## 更新流程

1. 用新版 `index.html` 覆盖根目录同名文件（网页版直接拖拽上传即可，约 30 秒生效）；
2. 新安装包放进 `apk/`，文件名带版本号（如 `cuoti-10.61.apk`），同时把 `apk/index.html`
   里的链接和版本号改掉；
3. 旧版本安装包**不要一直留在仓库里**（每版 21 MB，会把仓库撑大）。归档到
   Releases → 打 tag（如 `v10.60`）→ 上传 `cuoti-10.60.apk`。

## 数据与隐私

- 本仓库是 **public**，只放程序、安装包、资料清单。
- **不要**把个人错题、答题记录、成绩截图放进来。
- 多设备同步数据走独立的私有通道（GitHub secret Gist，文件名 `ctb650-sync.json`），
  与本站互不相干。

## 关于访问速度

`github.io` 在国内网络下不稳定，首次打开 18 MB 的单文件页面可能很慢。
如果需要更快的入口，把同一个目录部署到 Cloudflare Pages（免费、无需备案），
再绑自有域名即可；本目录可直接拖拽上传，无需任何构建命令。
