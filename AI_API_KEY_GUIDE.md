# Echo Move 大模型 API Key 获取教程

本文面向 Echo Move 用户，说明常见大模型提供商的 API Key 获取入口，以及在 Echo Move 中的填写方式。

## 在 Echo Move 中的使用位置

进入：

- 设置
- AI 设置
- 添加配置

通常需要填写：

- 提供商
- API Key
- 模型
- Base URL

## 提供商获取入口

### OpenAI

- API Keys: https://platform.openai.com/api-keys
- 官方说明: https://help.openai.com/en/articles/4936850-where-do-i-find-my-api-key

### Anthropic Claude

- API 入门: https://docs.anthropic.com/en/api/getting-started
- Console: https://console.anthropic.com/

### DeepSeek

- API 文档: https://api-docs.deepseek.com/zh-cn/
- 开放平台: https://platform.deepseek.com/

### 通义千问

- 获取 API Key: https://help.aliyun.com/zh/model-studio/get-api-key
- 首次调用: https://help.aliyun.com/zh/model-studio/first-api-call-to-qwen

### 智谱 GLM

- API 使用概述: https://docs.bigmodel.cn/cn/api/introduction
- HTTP API 入门: https://docs.bigmodel.cn/cn/guide/develop/http/introduction

### Kimi

- 快速入门: https://platform.moonshot.cn/blog/posts/kimi-api-quick-start-guide
- 开放平台: https://platform.moonshot.cn/

### 豆包

- 获取 API Key 并配置: https://www.volcengine.com/docs/82379/1263279

### OpenAI 兼容

这一项通常用于本地模型服务或第三方兼容网关，例如：

- Ollama
- 自建 OpenAI 兼容代理
- 云厂商 OpenAI 兼容接口

这类服务不一定有统一的官方 API Key 页面，请按你实际使用的服务文档填写：

- Base URL
- Model
- API Key

## Echo Move 默认端点说明

Echo Move 当前内置的大模型配置默认端点如下：

- Anthropic: `https://api.anthropic.com`
- DeepSeek: `https://api.deepseek.com/v1`
- 通义千问: `https://dashscope.aliyuncs.com/compatible-mode/v1`
- 智谱 GLM: `https://open.bigmodel.cn/api/paas/v4`
- Kimi: `https://api.moonshot.cn/v1`
- 豆包: `https://ark.cn-beijing.volces.com/api/v3`
- OpenAI 兼容: `http://localhost:11434/v1`

如果你不清楚 Base URL，建议优先使用 Echo Move 默认值，不要手动改写。

## 安全建议

- 不要把 API Key 截图发到群里
- 不要把 API Key 提交到 Git 仓库
- 建议为 Echo Move 单独创建一个 API Key
- 如果怀疑泄露，请立刻在提供商控制台轮换或删除
