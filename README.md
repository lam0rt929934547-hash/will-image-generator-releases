# Will Image Generator

Windows 上的 YouTube 缩略图创作工具：AI 生图、参考图编辑、本地水印与调色、批量导出。

本仓库仅用于发布安装包、使用说明和版本记录，不提供开发源码。运行时请使用你自己的 OpenAI 项目 API Key，安装包不附带 Key。

## 下载与安装

- [下载最新版 Windows 64 位安装包](https://github.com/lam0rt929934547-hash/will-image-generator-releases/releases/latest/download/WillImageGenerator-Setup-x64.exe)
- [查看版本说明与全部附件](https://github.com/lam0rt929934547-hash/will-image-generator-releases/releases/latest)
- [下载 SHA-256 校验文件](https://github.com/lam0rt929934547-hash/will-image-generator-releases/releases/latest/download/WillImageGenerator-Setup-x64.exe.sha256.txt)

支持 Windows 10 / 11，64 位 x64。下载 EXE 后双击安装，无需手动解压。安装到当前用户目录，不要求管理员权限。当前安装包未做商业代码签名，系统可能显示未知发布者。

## 开始使用

1. 在「设置」填写自己的 OpenAI API Key，设置原图与无水印导出文件夹。
2. 粘贴完整提示词，选择生成参数并生成。每次可生成 1–3 张。
3. 在左侧画布切换「原图 / 渲染预览」，预览当前水印、调色和尺寸效果。
4. 在导出面板选择水印预设、位置、调色、尺寸、格式和命名。可导入原 WatermarkStudio 的 studio_config.json。
5. 勾选、Ctrl / Shift 点击或从空白处拖动框选多张图片，也可「全选已完成」，然后「导出所选」。拖动缩略图可以调整左右顺序。

「尺寸参数优先」默认开启：按生成尺寸控件提交，原始提示词保留，不再弹出尺寸冲突提醒。提交成功后提示词框自动清空。

生图请求与更新下载跟随 Windows 系统代理。API 用量、模型权限与额度由 OpenAI 项目控制；本地导入、水印和导出不消耗生图额度。

## 0.1.6 交互更新

- 任务卡片的「编辑提示词」直接填入输入框，可恢复上一份草稿；点击已完成卡片的非按钮位置直接查看图片。
- 渲染模式下，拖动调色和水印滑块即时显示效果，松开后校准。滑块旁支持精确整数输入。
- 从文件管理器直接拖入 PNG、JPG、WebP，支持一次导入多张图片。
- 历史记录可调整缩略图大小与每页数量，记住偏好，支持拖动框选、Ctrl / Shift 多选和跨页选择。
- 创作台图片可拖动排序，重启后保留顺序。
- 按住「手机预览」显示手机外框与 YouTube 首页示意背景，松开恢复。背景不会写入导出图片。
- 按钮、弹窗、面板与排序采用柔和过渡，并遵循系统减少动态效果设置。

## 更新

0.1.4 起，点击软件右上角「检测更新」。默认在检测到新版后自动下载，可关闭此选项。下载完成并校验后点击「退出并安装」，按安装程序完成更新。

生成、保存或导出任务未完成时，软件会阻止安装更新。等待中的队列会暂停；更新后可继续。Key、历史记录、水印设置、原图与导出文件保留。较旧版本首次使用更新功能，需要手动安装一次新版。

## 本机数据

配置与历史记录位于 `%APPDATA%\Will Image Generator`，原图与水印导出目录由用户选择。Key 通过 Windows 加密保存在本机，迁移电脑后需要重新填写。不要把本机配置或 API Key 上传到此仓库。

## 下载校验

发布附件包含 SHA-256 校验文件。PowerShell 中可运行：

```powershell
Get-FileHash -LiteralPath '.\WillImageGenerator-Setup-x64.exe' -Algorithm SHA256
```

将结果与同一版本的校验文件比较。校验不一致时请重新下载，不要继续安装。
