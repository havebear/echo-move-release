# Echo Move

Echo Move 是一个面向个人运动数据的桌面应用，支持导入、整理、修复、可视化与分析 `FIT` / `GPX` / `TCX` 文件。应用采用 local-first 设计，活动数据默认保存在本地，不依赖账号体系或云端同步。

当前公开版本为 `0.0.10`。

## 0.0.10 版本亮点

- 活动详情新增自定义点位，可在二维/三维视图中标注备注、观景、补水、风险点与检查点，并直接关联到轨迹位置。
- 地图显示控制更细，照片点位、自定义点位、关键点与标记大小都可以单独调节。
- 二维/三维轨迹回放补充实时数据面板、多指标着色与自动全屏选项，回看活动过程更连贯。
- 三维地形新增 `ultra` 精细度与 DEM 缓存管理，复杂路线下的地形细节与重访体验更稳定。
- 相册预览性能、苹果健康导入识别，以及部分“运动时间 / 全程时间”口径问题已在本版修复。

## 核心能力

### 活动管理

- 支持文件选择、拖拽和批量导入
- 支持 `FIT`、`GPX`、`TCX` 三类主流运动文件
- 提供活动列表视图与轨迹墙视图，便于整理和回看
- 支持按关键词、运动类型、时间范围等条件快速筛选
- 支持批量导出、数据修复与轨迹修复
- 兼容不同坐标系统，活动数据默认仅保存在本地

### 地图可视化

- 基于 MapLibre GL 的高性能轨迹渲染
- 支持独立地图筛选、图例、统计卡片和最近活动高亮
- 支持轨迹颜色、线宽、透明度与底图样式切换
- 支持隐私模式、截图导出和海报导出
- 可在大批量活动数据下保持流畅浏览体验

### 统计与 AI Lab

- 提供生涯总览、趋势统计、年度汇总和热力图视图
- 统计页参考 Running-Page，并结合运动回看需求做了本地化调整
- AI Lab 已支持归纳整理统计数据
- AI Lab 已支持根据运动数据直接生成图表

### 工具与存储

- 提供格式转换与数据修复工具
- 支持多用户本地档案、主题、语言和存储管理
- AI 功能需要先在应用设置中配置可用模型

## AI 配置

AI Lab 需要先在 `设置 > AI 设置` 中添加可用模型配置。

当前版本内置支持：

- Anthropic Claude
- DeepSeek
- 通义千问
- 智谱 GLM
- Kimi
- 豆包（火山方舟）
- OpenAI 兼容服务

各平台 `API Key` 的申请入口、配置方式和常见注意事项见：

- [AI_API_KEY_GUIDE.md](./AI_API_KEY_GUIDE.md)

## 截图

### 地图页

![地图页](./screenshot-map.png)

### 活动列表

![活动列表](./screenshot-activity-list.png)

### 轨迹墙

![轨迹墙](./screenshot-trajectory-wall.png)

### 统计页

![统计页](./screenshot-stats.png)

### AI Lab

![AI Lab 统计归纳](./screenshot-ai-lab.png)

![AI Lab 图表生成](./screenshot-ai-chart.png)

### 微信群

<img src="./screenshot-wechat-group.jpg" alt="微信群" width="240" />

## 大模型 API Key 获取教程

如果你准备使用 Echo Move 的 AI 功能，可以先查看：

- [大模型 API Key 获取教程](./AI_API_KEY_GUIDE.md)

## 下载

前往 [Releases](https://github.com/havebear/echo-move-release/releases) 页面下载最新版。

更新日志与版本说明：

- [CHANGELOG.md](./CHANGELOG.md)
- [RELEASE_NOTES_0.0.10.md](./RELEASE_NOTES_0.0.10.md)
- [RELEASE_NOTES_0.0.3.md](./RELEASE_NOTES_0.0.3.md)
- [RELEASE_NOTES_0.0.1.md](./RELEASE_NOTES_0.0.1.md)

`0.0.10` 当前建议关注的安装包形态如下：

| 平台 | 文件 |
| --- | --- |
| macOS (Apple Silicon) | `Echo-Move-0.0.10-arm64.dmg` |
| macOS (Intel) | `Echo-Move-0.0.10-x64.dmg` |
| Windows (64-bit) | `Echo-Move-0.0.10-setup.exe` |
| Linux (64-bit) | `Echo-Move-0.0.10-x64.AppImage` / 对应 `.deb` 安装包 |

补充说明：

- macOS 当前仍以“检测更新后打开发布页，手动下载安装”为主；Apple Silicon 设备请选择 `arm64`，Intel 设备请选择 `x64`。
- 版本 `0.0.10` 的完整更新说明见 [RELEASE_NOTES_0.0.10.md](./RELEASE_NOTES_0.0.10.md)。

## 数据存储

活动、用户和大部分配置默认存储在本地：

- macOS: `~/Library/Application Support/echo-move/`
- Windows: `%APPDATA%/echo-move/`
- Linux: `~/.config/echo-move/`

## 相关链接

- 发布仓库: [havebear/echo-move-release](https://github.com/havebear/echo-move-release)
- 下载页面: [Releases](https://github.com/havebear/echo-move-release/releases)
- 更新日志: [CHANGELOG.md](./CHANGELOG.md)
- AI 配置说明: [AI_API_KEY_GUIDE.md](./AI_API_KEY_GUIDE.md)
