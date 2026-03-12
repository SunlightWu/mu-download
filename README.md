# M3U8 下载工具

基于 uni-app x 开发的 Android 视频下载工具，支持 M3U8/HLS 流媒体视频下载。

## 功能特性

- **M3U8 视频下载**：支持标准 HLS 流媒体视频下载
- **AES-128 解密**：自动识别并解密加密的 TS 分片
- **多线程下载**：支持自定义并发线程数（1-10）
- **断点续传**：支持暂停/继续下载
- **自动合并**：下载完成后自动合并为 MP4 文件
- **下载记录**：保存下载历史，支持任务恢复

## 项目结构

```
mu-download/
├── pages/
│   ├── index/          # 首页（工具箱入口）
│   ├── m3u8/
│   │   ├── input.uvue  # M3U8 链接输入页
│   │   └── detail.uvue # 下载详情页
│   └── history/        # 下载历史页
├── utils/
│   ├── AesDecryptor.uts    # AES-128-CBC 解密工具
│   ├── FileHelper.uts      # 文件操作工具
│   └── downloader/
│       ├── types.uts       # 类型定义
│       └── parsers/
│           ├── BaseParser.uts   # 解析器基类
│           └── M3u8Parser.uts   # M3U8 解析器
├── static/             # 静态资源
├── manifest.json       # 应用配置
└── pages.json          # 页面配置
```

## 使用方法

1. 打开应用，点击「M3U8下载」
2. 输入 M3U8 视频链接
3. 点击「解析」获取视频信息
4. 设置并发线程数（可选）
5. 点击「开始下载」
6. 下载完成后输入文件名，点击「合并导出」
7. 导出的视频保存在 `Download/M3U8Videos/` 目录

## 权限说明

应用需要以下权限：

- `INTERNET` - 网络访问
- `READ_EXTERNAL_STORAGE` - 读取存储
- `WRITE_EXTERNAL_STORAGE` - 写入存储
- `MANAGE_EXTERNAL_STORAGE` - 管理外部存储
- `READ_MEDIA_VIDEO` - 读取视频媒体

## 开发环境

- HBuilderX 4.x+
- uni-app x
- Android SDK 21+

## 编译运行

1. 使用 HBuilderX 打开项目
2. 运行 → 运行到手机或模拟器 → 运行到 Android App 基座

## 注意事项

- 仅支持标准 M3U8/HLS 格式
- 加密视频需要密钥可访问
- 导出的视频为 MP4 格式（TS 流直接合并）
- 部分加密视频可能因编码问题无法播放

## License

MIT
