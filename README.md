# Echo Move

Echo Move 是一个面向个人运动数据的桌面应用，支持导入、整理、修复、可视化与分析 `FIT` / `GPX` / `TCX` 文件。应用采用 local-first 设计，活动数据默认保存在本地，不依赖账号体系或云端同步。

当前公开版本为 `0.0.19`。

## 0.0.19 版本亮点

- 三维地形沙盘新增高精度 DEM 预设，可围绕路线范围生成更细的高程网格，并在生成前展示网格规模、DEM 来源和预计成本。
- 高精度沙盘支持 IndexedDB 持久化保存，完整高度网格、DEM 元信息和场景配置可长期复看。
- 活动对比支持使用原始轨迹活动参与，更多从原始文件解析出的活动现在可以进入对比视图。
- AI 路书保存后会自动补齐海拔采样；路书和赛段缺少海拔时会显示更清晰的提示。
- 地图、路书详情和赛段详情减少首次交互与拖拽过程中的重渲染，高密度路线拖动更跟手。

## 当前能力概览

### 活动与文件管理

- 支持文件选择、拖拽和批量导入 `FIT` / `GPX` / `TCX` 活动文件。
- 提供活动列表、活动详情与轨迹墙视图，适合日常整理、筛选、复盘和浏览历史轨迹。
- 支持按关键词、运动类型、时间范围、年份等条件筛选，并可批量删除、批量导出或重新计算活动派生数据。
- 支持活动原始文件导出、格式转换、数据修复、轨迹修复和隐私处理，便于迁移、备份和二次整理。
- 支持 Strava、迈金 / OnelapFit 等第三方来源同步到本地活动库，优先保留可用的原始运动文件。

### 地图可视化

- 基于 MapLibre GL 渲染活动轨迹，支持独立地图筛选、图例、统计卡片、最近活动高亮和全屏查看。
- 活动详情支持 `2D / 3D` 轨迹视图，可查看速度 / 坡度着色、轨迹回放、图表联动、修复前后对比和自定义点位。
- 支持截图导出、透明轨迹 PNG 导出、当前视窗轨迹素材导出和隐私模式，方便继续制作海报或分享图。
- 支持应用瓦片本地底图、地图包资源库、自定义瓦片样式和地名标注控制，弱网或离线场景下也能浏览已导入区域。
- 支持多轨迹 3D 场景和三维地形沙盘，可围绕活动或路书生成 DEM 地形、调整视角、控制播放点并保存作品化场景。

### 路书、赛段与对比

- 路书模块支持 `FIT` / `GPX` / `TCX` / `KML` / `KMZ` 单个或批量导入，并提供拖拽覆盖层、批次面板和导入进度反馈。
- 路书列表支持关键词、运动类型、收藏筛选，以及收藏、信息编辑、重新计算和删除等操作。
- 路书详情支持 `2D / 3D` 地图、海拔概览、坡度着色、点位、附件和赛段联动查看。
- 路书对比支持最多 8 条同运动类型路线，对比距离、爬升、坡度、评分、海拔、路面类型和预计时长，并可拖动排序与全屏查看图表。
- 活动对比支持更多从原始文件解析出的活动，便于把真实活动和规划路线放在同一视角下判断难度与差异。

### 统计分析与 AI

- 提供生涯总览、趋势统计、年度汇总、热力图和 AI 骑行画像等统计视图。
- AI Lab 支持模型配置、助手切换、流式回复、会话历史、统计归纳和运动数据图表生成。
- AI 能力已扩展到活动复盘、路书分析、路书对比摘要、赛段信息和出行准备等场景。
- 当前内置支持 Anthropic Claude、DeepSeek、通义千问、智谱 GLM、Kimi、豆包和 OpenAI 兼容服务。

### 本地存储、备份与扩展

- 采用 local-first 设计，多用户档案、活动数据和大部分配置默认保存在本地。
- 支持主题、语言、偏好设置、存储空间查看、备份与恢复。
- MCP Server 可通过 stdio 将只读运动数据工具暴露给 Claude Code、Cursor 等 MCP Client，方便在外部 AI 工具中查询本地运动数据。
- 备份恢复会尽量把历史数据库和配置路径重映射到当前用户数据目录，降低跨设备或跨系统恢复成本。

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
- [RELEASE_NOTES_0.0.19.md](./RELEASE_NOTES_0.0.19.md)
- [RELEASE_NOTES_0.0.10.md](./RELEASE_NOTES_0.0.10.md)
- [RELEASE_NOTES_0.0.3.md](./RELEASE_NOTES_0.0.3.md)
- [RELEASE_NOTES_0.0.1.md](./RELEASE_NOTES_0.0.1.md)

`0.0.19` 当前已确认的安装包形态如下：

| 平台 | 文件 |
| --- | --- |
| macOS (Apple Silicon) | `Echo-Move-0.0.19-arm64.dmg` |
| macOS (Intel) | `Echo-Move-0.0.19-x64.dmg` |
| Windows (64-bit) | `Echo-Move-0.0.19-setup.exe` |

补充说明：

- macOS 当前仍以“检测更新后打开发布页，手动下载安装”为主；Apple Silicon 设备请选择 `arm64`，Intel 设备请选择 `x64`。
- Linux 安装包以 Releases 页面实际显示为准。
- 版本 `0.0.19` 的完整更新说明见 [RELEASE_NOTES_0.0.19.md](./RELEASE_NOTES_0.0.19.md)。

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
