# 自我纠错与自学习能力体系

> 来源：GitHub API + AI Agent最佳实践
> 整理时间：2026-04-14

---

## 一、GitHub明星仓库（通过curl获取）

### AI Agent框架

| Stars | 仓库 | 用途 |
|-------|------|------|
| 151k | obra/superpowers | Agentic skills framework & 方法论 |
| 143k | anomalyco/opencode | 开源编程Agent |
| 138k | langgenius/dify | Agentic workflow开发平台 |
| 134k | langchain-ai/langchain | Agent工程平台 |
| 118k | anthropics/skills | Claude Skills官方库 |
| 114k | anthropics/claude-code | Claude Code最佳实践 |
| 88k | browser-use/browser-use | AI Agent网页自动化 |
| 83k | NousResearch/hermes-agent | 自成长Agent |
| 78k | infiniflow/ragflow | RAG工作流 |

### 记忆与自学习系统

| Stars | 仓库 | 用途 |
|-------|------|------|
| 198 | zksha/alma | 自动元学习记忆设计 |
| 76 | GustyCube/membrane | Agent选择性学习记忆 |
| 70 | ldclabs/KIP | 知识记忆交互协议 |
| 16 | mhndayesh/Easy-agentic-memory-system | 轻量级记忆工具 |
| 9 | Youhai020616/Agentmind | 自学忆忆系统 |

### 自我反思与纠错

| Stars | 仓库 | 用途 |
|-------|------|------|
| 高评价 | ramakay/claude-self-reflect | AI自我反思机制 |
| 5 | cathydou/reflection-agent-maze | 强化学习反思能力 |

---

## 二、GitHub API调用方法

```bash
curl -s "https://api.github.com/search/repositories?q=关键词&sort=stars&per_page=20" | python3 -c "
import sys, json
data = json.load(sys.stdin)
for r in data.get('items', [])[:20]:
    print(f\"{r['stargazers_count']:>7} | {r['full_name']:<45} | {r['description'][:55]}\")
"
```

---

## 三、自我纠错核心机制

### 纠错流程

```
1. 错误发生
2. 立即分析（为什么出错）
3. 记录到overseas-b2b-errors.md
4. 制定正确做法
5. 更新patterns.md
6. 下次执行前检查错误清单
```

### 关键规则

- 工具执行失败 → 立即分析原因 → 记录
- 不重蹈覆辙 → 下次执行前先检查错误清单
- 保持记忆同步 → 每次会话结束更新

---

## 四、自学习核心机制

### 学习来源

| 来源 | 说明 |
|------|------|
| GitHub API | curl搜索AI/Agent类项目趋势 |
| 官方文档 | Anthropic Skills最佳实践 |
| 错误记录 | 从失败中学习 |
| 用户反馈 | 偏好和行为 |

### 知识积累流程

```
学习新内容 → 提炼要点 → 写入patterns.md → 定期回顾
```

---

## 五、记忆分层结构

| 层级 | 内容 | 更新频率 |
|------|------|----------|
| 项目记忆 | 当前项目配置、进度、文件 | 每次会话 |
| 用户偏好 | 沟通风格、授权要求、静默模式 | 首次+变化时 |
| 错误模式 | 所有历史错误 | 每次出错 |
| 学习积累 | patterns.md + GitHub新发现 | 每次新学习 |

---

## 六、执行清单

### 每次会话开始
- [ ] 读取MEMORY.md
- [ ] 检查是否有新错误需要处理
- [ ] 确认用户最新偏好

### 每次会话结束
- [ ] 更新yixiuworld_workspace.md（如有变化）
- [ ] 检查patterns.md是否有新内容
- [ ] 同步MEMORY.md索引

### 每次出错时
- [ ] 分析错误原因
- [ ] 记录到overseas-b2b-errors.md
- [ ] 更新patterns.md中的正确做法

### 每周
- [ ] GitHub API搜索新项目
- [ ] 检查MEMORY.md完整性
- [ ] 清理重复/过时信息

---

## 七、核心原则

1. **不重复犯错** - 每次错误都要记录，下次避免
2. **持续积累** - 每次新学习及时写入patterns.md
3. **记忆同步** - 保持记忆文件与项目状态一致
4. **用户优先** - 用户偏好一旦知道，立即写入user_preferences.md
5. **GitHub学习** - 定期用curl搜索AI/Agent趋势，持续进化
