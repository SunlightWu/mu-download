# 工具箱

基于 uni-app x 开发的 Android 实用工具集合应用。

## 已实现功能

### M3U8 下载
- 支持标准 HLS 流媒体视频下载
- 自动识别并解密 AES-128 加密分片
- 支持自定义并发线程数（1-10）
- 支持暂停/继续下载
- 下载完成后自动合并为 MP4 文件
- 保存下载历史，支持任务恢复

## 规划中功能

- 直链下载
- 格式转换
- 音频提取
- 二维码扫描/生成
- JSON 格式化
- Base64 编解码
- ...

## 项目结构

```
mu-download/
├── pages/
│   ├── index/          # 首页（工具箱入口）
│   ├── m3u8/           # M3U8 下载功能
│   └── history/        # 下载历史
├── utils/              # 工具函数
├── static/             # 静态资源
├── manifest.json       # 应用配置
└── pages.json          # 页面配置
```

## 开发环境

- HBuilderX 4.x+
- uni-app x
- Android SDK 21+

## 编译运行

1. 使用 HBuilderX 打开项目
2. 运行 → 运行到手机或模拟器 → 运行到 Android App 基座

## License

MIT
