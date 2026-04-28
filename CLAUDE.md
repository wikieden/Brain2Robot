# Brain2Robot · 项目规范

## 项目简介

研究如何将人类的熟悉技能、主动任务能力、社交偏好和判断逻辑蒸馏到人形机器人上。
涵盖认知架构、多人偏好系统、主动触发引擎、技能蒸馏管道等模块。

---

## 命名规范：模块术语优先借用哲学词汇

**规则**：专业模块、子系统、核心概念命名时，优先从哲学传统中取词，而非直接使用工程缩写或技术行话。

**目的**：让架构语言更有表达力，让模块的本质含义通过名字直接透出来。

**示例方向**：
- 世界状态监测 → **现象层**（Phenomenal Layer）
- 偏好推断引擎 → **意向性引擎**（Intentionality Engine）
- 触发判断 → **意志裁断**（Volitional Arbiter）
- 执行历史记忆 → **痕迹记忆**（Trace Memory）
- 失败驱动重规划 → **否定性学习**（Negation-driven Replanning）
- 身份识别融合 → **他者识别**（Other-recognition）
- 冲突解决层 → **调和层**（Dialectical Layer）
- 主动触发引擎 → **冲动发生器**（Conative Engine）

**操作方式**：
- 新模块命名时，Claude 主动提出 1–2 个哲学借词候选，由 wiki 确认
- 已有模块名称可在讨论中逐步替换为哲学术语
- 技术文档中保留工程名称作为副标题或括号注释，哲学名称作为主标题

---

## 设计原则

- 优先讨论架构和方案，不默认生成代码
- 每个模块讨论完毕后整理进 `design/` 目录的 Markdown 文档
- 架构图用 SVG 保存在 `design/assets/` 目录，并嵌入对应文档

---

## 文档结构

```
Brain2Robot/
├── CLAUDE.md                              # 本文件，项目规范
├── design/
│   ├── 00_manifesto.md                    # 总纲：愿景·哲学·架构·导航
│   ├── layers/                            # 三层架构文档
│   │   ├── L3_cognition.md               # L3 认知层
│   │   ├── L2_coordination.md            # L2 协调层
│   │   └── L1_execution.md               # L1 执行层
│   ├── systems/                           # 横切系统文档
│   │   ├── multi_person_support.md       # 多人支持系统
│   │   └── techne_crystallization.md     # 技艺结晶（蒸馏管道）
│   └── assets/                            # 架构图 SVG
└── l3_cognition/                          # 早期代码草稿（暂存）
```
