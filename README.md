# 家庭记账本 PWA

这是可直接部署到 GitHub Pages 的 PWA 版本。

## 文件结构

```text
family-ledger-pwa/
├── index.html
├── manifest.webmanifest
├── service-worker.js
└── icons/
    ├── icon-192.png
    ├── icon-512.png
    └── apple-touch-icon.png
```

## 部署到 GitHub Pages

1. 新建一个 GitHub 仓库，例如 `family-ledger`。
2. 上传本目录里的所有文件，而不是只上传 zip。
3. 进入仓库 Settings → Pages。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main` / `/root`，保存。
6. 等 GitHub 生成链接后，用手机打开该链接。

## 手机安装

- iPhone：用 Safari 打开链接 → 分享 → 添加到主屏幕。
- Android：用 Chrome 打开链接 → 菜单 → 添加到主屏幕 / 安装应用。
- 鸿蒙：用系统浏览器打开链接 → 添加到桌面/主屏幕；具体文字因浏览器版本而异。

## 重要说明

- 数据保存在每台手机自己的浏览器 `localStorage` 中，不会自动同步到其他家人手机。
- 第一次打开需要联网；之后核心页面可以离线打开。
- Chart.js、Tesseract.js 和汇率接口仍来自线上资源。联网成功加载过后，Service Worker 会尽量缓存它们；但 OCR/汇率离线时可能不可用或使用旧数据。
- 如果清理浏览器数据、换浏览器、卸载 Web App，记账数据可能丢失。正式家庭长期使用前，建议下一步添加「导出/导入备份」。
