# 知识库索引

> 所有机器人的共享学习知识库

## 目录结构

```
knowledge/
├── README.md                      ← 本文件
├── INDEX.md                       ← 知识库索引
├── error-patterns/               ← 错误模式记录
│   ├── overseas-b2b-errors.md
│   ├── novel-writer-errors.md
│   ├── daily-report-errors.md
│   └── domestic-ecom-errors.md
├── corrections/                  ← 用户纠正记录
│   └── correction-log.md
├── learned/                      ← 已学习的正确做法
│   └── patterns.md
└── feedback.log                  ← 反馈日志
```

## 使用方法

### 当用户纠正你时
1. 将纠正记录到 `corrections/correction-log.md`
2. 将正确做法更新到对应的 `error-patterns/` 文件
3. 将通用模式更新到 `learned/patterns.md`

### 当启动新会话时
1. 读取 `knowledge/learned/patterns.md`
2. 读取对应机器人的 `error-patterns/` 文件
3. 避免重犯相同错误

## 原则

- **不重复犯错**：相同错误不会犯第二次
- **主动学习**：从每次交互中学习
- **知识共享**：所有机器人都从知识库中学习
- **结构化记录**：错误、原因、正确做法分开记录

## 最后更新

- 创建时间：2026-04-14
- 维护者：Claude Code Agents
