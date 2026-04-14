# 纠错学习协议

> 所有 Claude Code Agents 必须遵循的学习流程

## 核心原则

### 1. 犯错后立即记录
当用户纠正你时，无论是否理解为什么，先记录再学习。

### 2. 知识共享
所有机器人都从同一个知识库学习，一个机器人的教训是所有机器人的教训。

### 3. 主动预防
在执行任务前，回顾相关错误模式，避免重犯。

---

## 学习流程

### 当用户纠正你时

```
1. 承认错误（不要辩解）
2. 询问原因（确保理解）
3. 立即记录到知识库
4. 确认正确做法
5. 在当前任务中应用
```

### 当发现新错误模式时

```
1. 记录到 error-patterns/[机器人名]-errors.md
2. 更新 corrections/correction-log.md
3. 更新 learned/patterns.md（如果是通用模式）
4. 同步到 GitHub
```

### 当启动新会话时

```
1. 读取 learned/patterns.md（复习）
2. 读取对应机器人的 error-patterns 文件
3. 应用到当前任务
```

---

## 记录格式

### 错误记录

```markdown
## [日期] 错误描述

**错误做法**：...
**原因**：...
**正确做法**：...
**教训**：...
```

### 纠正记录

```markdown
## [日期] [机器人名] 用户纠正

**问题**：...
**纠正内容**：...
```

---

## GitHub 同步

仓库地址：
- 知识库：https://github.com/hahahmomo/claude-agents-knowledge
- 记忆备份：https://github.com/hahahmomo/claude-agents-memory

同步命令：
```bash
C:/Users/Administrator/.cc-connect/sync-knowledge.sh
```

---

## 知识库结构

```
knowledge/
├── README.md              # 索引和说明
├── error-patterns/       # 各机器人错误模式
│   ├── overseas-b2b-errors.md
│   ├── novel-writer-errors.md
│   ├── daily-report-errors.md
│   └── domestic-ecom-errors.md
├── corrections/           # 用户纠正记录
│   └── correction-log.md
└── learned/             # 已学习的通用模式
    └── patterns.md
```

---

**最后更新**：2026-04-14
