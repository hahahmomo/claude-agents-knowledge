# 已学习的正确做法

> 从错误和纠正中总结的通用模式

## 核心原则

### 1. 输出风格
- ✅ **只输出最终结果**，不展示中间过程
- ✅ **必要确认才提示**，其他后台处理
- ✅ **简洁明了**，避免冗余信息

### 2. 会话管理
- ✅ **share_session_in_channel = true** — 防止会话切换
- ✅ **reply_to_trigger = true** — 只在被@时响应
- ✅ **receive_channel_messages_only = true** — 只接收频道消息
- ✅ **定期检查 sessions 目录** — 清理重复文件

### 3. MCP配置
- ✅ **使用免费MCP** — 无需API密钥的工具优先
- ✅ **按角色配置** — 根据职责选择最优MCP组合
- ✅ **无占位符** — 所有配置必须有效

### 4. 任务执行
- ✅ **先确认再执行** — 不随意执行未授权任务
- ✅ **保持专注** — 不偏离用户交代的任务
- ✅ **知识共享** — 从知识库中学习，避免重复犯错

## MCP选择优先级

1. **必须**：token-optimizer, memory, omega-memory
2. **推荐**：context7, lark-mcp
3. **可选**：ddg-mcp, fetch-mcp, sequential-thinking
4. **按需**：github, exa-web-search, firecrawl（需密钥）

## 机器人配置检查清单

每次启动或配置变更后检查：

- [ ] sessions 目录无重复文件
- [ ] config.toml 中所有机器人都有 share_session_in_channel
- [ ] config.toml 中所有机器人都有 reply_to_trigger
- [ ] config.toml 中所有机器人都有 receive_channel_messages_only
- [ ] .mcp.json 中无 YOUR_XXX_KEY_HERE 占位符
- [ ] MCP 工具都经过测试可用

## 用户偏好

| 项目 | 偏好 |
|------|------|
| 输出风格 | 只输出结果，不展示步骤 |
| 任务执行 | 先确认再执行 |
| 知识管理 | 主动学习，避免重复犯错 |
| 沟通方式 | 简洁明了 |

---

**最后更新**：2026-04-14
