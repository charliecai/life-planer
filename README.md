# Life Plan - Personal Strategic Planning System

基于「生命之轮」方法论的个人年度战略规划与执行系统。

## 项目结构

```
life-plan/
├── .claude/
│   └── skills/
│       └── life-plan/          # Claude Code Skill
│           ├── SKILL.md                    # 主技能文件
│           ├── ANNUAL-PLAN-TEMPLATE.md     # 年度计划模板
│           ├── MONTHLY-PLAN-TEMPLATE.md    # 月度计划模板
│           └── MONTHLY-REVIEW-TEMPLATE.md  # 月度回顾模板
├── plans/
│   ├── 2024/                   # 2024年度文档
│   │   ├── annual-plan-2024.md
│   │   ├── monthly-plan-2024-01.md
│   │   ├── monthly-review-2024-01.md
│   │   └── ...
│   └── 2025/                   # 2025年度文档
│       ├── annual-plan-2025.md
│       └── ...
└── README.md
```

## 使用方法

### 触发 Skill

在 Claude Code 中，当你提到以下关键词时，会自动触发 life-plan skill：

- 年度计划、年度规划
- 年度复盘、年度回顾
- 月度计划、月度规划
- 月度复盘、月度回顾
- 生命之轮、人生规划

### 常用场景

**开始年度规划**
```
我想开始做2025年的年度规划
```

**进行年度复盘**
```
帮我做一下2024年的年度复盘
```

**制定月度计划**
```
帮我制定1月份的月度计划
```

**月度回顾**
```
我要做12月的月度回顾
```

## 方法论概述

### 核心理念

1. **生命之轮 8 维度**：健康、事业、财富、家庭、亲密关系、社交、个人成长、休闲恢复
2. **反幻想 OKR**：可验证、可观察的目标与关键结果
3. **12 周节奏**：按季度设定里程碑
4. **月度滚动**：持续复盘与计划调整

### 工作流程

```
Phase 0: 现实约束与角色确认
    ↓
Phase 1: 生命之轮冷静扫描
    ↓
Phase 2: 年度复盘（模式识别）
    ↓
Phase 3: 年度战略取舍
    ↓
Phase 4: 目标与结果拆解（OKR）
    ↓
Phase 5: 行动系统设计
    ↓
Phase 6: 恢复与输入配额
    ↓
Phase 7: 年度作战地图输出
    ↓
Phase 8: 12周节奏规划
    ↓
Phase 9: 月度计划拆分 ←──┐
    ↓                    │
Phase 10: 月度回顾与调整 ─┘
```

### 关键原则

- 先诊断结构，再谈目标
- 年度最多 2-3 个主战场
- 先做减法，再做加法
- 恢复与输入必须被保护
- 所有目标必须可验证

## 文档命名规范

- 年度计划：`annual-plan-{year}.md`
- 月度计划：`monthly-plan-{year}-{month}.md`
- 月度回顾：`monthly-review-{year}-{month}.md`

## 分享插件

本项目包含一个可分发的 Claude Code 插件，位于 `life-plan-plugin/` 目录。

### 插件结构

```
life-plan-plugin/
├── .claude-plugin/
│   ├── plugin.json         # 插件清单
│   └── marketplace.json    # 市场配置
├── skills/
│   └── life-plan/
│       ├── SKILL.md
│       ├── ANNUAL-PLAN-TEMPLATE.md
│       ├── MONTHLY-PLAN-TEMPLATE.md
│       └── MONTHLY-REVIEW-TEMPLATE.md
└── README.md
```

### 分发方式

详见 [插件分发指南](DISTRIBUTION.md)

## 参考资料

本系统基于「全息人生战略官 v2.2」方法论设计。
