# Annual Plan Template

Use this template when generating annual planning documents.

**IMPORTANT: For document generation, use Bash heredoc method (see SKILL.md Method 1)**
- This template is ~200 lines, which is too long for Write tool
- **Generate ALL sections in ONE Bash call using { } braces**
- **This ensures only ONE user confirmation is needed (not 7 confirmations)**
- See SKILL.md "Document Generation Process" for detailed instructions

**Batch Execution Format:**
```bash
{
  cat > file.md << 'EOF'
Section 0
EOF

  cat >> file.md << 'EOF'
Section 1
EOF

  # ... all sections
} && echo "✓ Done"
```

## Document Structure & Section Boundaries

The document should be generated in these sections:

### Section 0: Header (lines 1-10)
- Title, date, theme word

### Section 1: Reality Check (lines 11-40)
- 一、现实约束与角色确认

### Section 2: Life Wheel (lines 41-70)
- 二、生命之轮结构判断

### Section 3: Strategic Focus (lines 71-100)
- 三、年度战略定位

### Section 4: OKR (lines 101-130)
- 四、年度 OKR

### Section 5: Action System & Routine (lines 131-200)
- 五、行动系统设计
- 五(附)、日常Routine时间表
- 六、恢复与输入配额

### Section 6: 12-Week Rhythm & Calendar (lines 201-end)
- 七、12周节奏规划
- 附录：年度日历视图

---

## Full Template Content

```markdown
# {Year} 年度战略地图

> 生成日期：{date}
> 年度主题词：{theme_word}

---

## 一、现实约束与角色确认

### 当前主要人生角色
- {role_1}
- {role_2}
- ...

### 最硬的现实约束
| 约束类型 | 具体描述 | 影响程度 |
|---------|---------|---------|
| {type} | {description} | 高/中/低 |

### 年度减法清单（必须减少/停止的事项）
1. {item_1}
2. {item_2}
3. {item_3}

> 今年的关键不是更努力，而是更少犯错。

---

## 二、生命之轮结构判断

### 八维度评分（1-10分）

| 维度 | 得分 | 状态标记 | 备注 |
|-----|-----|---------|-----|
| 健康 | {score} | {normal/危险短板/透支高分} | {note} |
| 事业/学业 | {score} | | |
| 财富/财务安全 | {score} | | |
| 家庭 | {score} | | |
| 亲密关系 | {score} | | |
| 社交/朋友圈 | {score} | | |
| 个人成长 | {score} | | |
| 休闲/恢复 | {score} | | |

### 结构性风险判断
- **危险短板**：{dimension} - {reason}
- **透支高分项**：{dimension} - {reason}
- **系统性风险**：{risk_description}

---

## 三、年度战略定位

### 年度定位陈述
> {1-3 sentences positioning statement}

### 战场划分

| 类型 | 维度 | 策略说明 |
|-----|-----|---------|
| 主战场 | {dimension_1} | {strategy} |
| 主战场 | {dimension_2} | {strategy} |
| 60分策略 | {dimension} | {approach} |
| 不优化 | {dimension} | {reason} |

### 年度成功判定（至少2条达成即视为成功）
1. {criterion_1} - 验收证据：{evidence}
2. {criterion_2} - 验收证据：{evidence}
3. {criterion_3} - 验收证据：{evidence}

---

## 四、年度 OKR（按主战场维度）

### 主战场 1：{dimension_name}

**Objective**: {state_change_description}

| Key Result | 验收证据 | 12周里程碑 |
|-----------|---------|-----------|
| KR1: {measurable_result} | {evidence} | Q1: / Q2: / Q3: / Q4: |
| KR2: {measurable_result} | {evidence} | Q1: / Q2: / Q3: / Q4: |
| KR3: {measurable_result} | {evidence} | Q1: / Q2: / Q3: / Q4: |

### 主战场 2：{dimension_name}

**Objective**: {state_change_description}

| Key Result | 验收证据 | 12周里程碑 |
|-----------|---------|-----------|
| KR1: {measurable_result} | {evidence} | |
| KR2: {measurable_result} | {evidence} | |

---

## 五、行动系统设计

### KR: {kr_name}

| 要素 | 内容 |
|-----|-----|
| **最小行动** | {5-20分钟可完成的低门槛动作} |
| **环境/系统调整** | {让正确行为更容易发生的改造} |
| **失败预演** | 风险1: {risk} → 兜底: {fallback} |
| | 风险2: {risk} → 兜底: {fallback} |

(Repeat for each KR)

---

## 五(附)、日常Routine时间表

> 基于行动系统设计,提取可固定化的日常routine,便于日程管理和自动化

### 每日Routine

| 时间段 | Routine名称 | 关联KR | 时长 | 备注 |
|-------|-----------|-------|-----|-----|
| 06:00-06:30 | {routine} | {kr_ref} | 30min | {note} |
| 07:00-07:30 | {routine} | {kr_ref} | 30min | {note} |
| ... | | | | |

### 每周Routine

| 星期 | 时间段 | Routine名称 | 关联KR | 时长 | 备注 |
|-----|-------|-----------|-------|-----|-----|
| 周一 | 19:00-20:00 | {routine} | {kr_ref} | 1h | {note} |
| 周三 | 20:00-21:00 | {routine} | {kr_ref} | 1h | {note} |
| ... | | | | | |

### 每月Routine

| 日期 | 时间段 | Routine名称 | 关联KR | 时长 | 备注 |
|-----|-------|-----------|-------|-----|-----|
| 每月1日 | 09:00-10:00 | {routine} | {kr_ref} | 1h | {note} |
| 每月15日 | 14:00-15:00 | {routine} | {kr_ref} | 1h | {note} |
| ... | | | | | |

### Routine设计原则

- **时间具体化**: 明确开始和结束时间,便于日历添加
- **关联KR**: 每个routine都应对齐具体的Key Result
- **时长合理**: 考虑实际可执行性,避免过度安排
- **灵活性**: 标注哪些可调整,哪些必须固定

---

## 六、恢复与输入配额

### 恢复活动池
| 活动 | 补能效果 | 占位方式 |
|-----|---------|---------|
| {activity} | {effect} | {reservation_method} |

### 输入活动池
| 方向 | 期望认知更新 | 占位方式 |
|-----|-------------|---------|
| {direction} | {expected_insight} | {reservation_method} |

### 防挤占策略
- 最容易被挤掉的：{item}
- 防挤占措施：{measure}

> 不设置次数/频率 KPI，只要求"价值清晰 + 有意识预留"

---

## 七、12周节奏规划

| 周期 | 主题词 | 对齐KR | 里程碑（可验收） | 主要风险与兜底 |
|-----|-------|-------|----------------|---------------|
| Q1 (W1-12) | {theme} | {kr} | {milestone} | {risk_fallback} |
| Q2 (W13-24) | {theme} | {kr} | {milestone} | {risk_fallback} |
| Q3 (W25-36) | {theme} | {kr} | {milestone} | {risk_fallback} |
| Q4 (W37-48+) | {theme} | {kr} | {milestone} | {risk_fallback} |

---

## 附录：年度日历视图

| 月份 | 季度 | 重点KR | 关键节点 |
|-----|-----|-------|---------|
| 1月 | Q1 | | |
| 2月 | Q1 | | |
| ... | | | |
| 12月 | Q4 | | |

---

*本文档为年度战略参考，建议每季度复盘时回顾调整*
```

## Generation Guidelines

1. **Always ask user for input** at each phase, don't assume
2. **Use specific, measurable language** - avoid vague words like "improve", "enhance"
3. **Include verification evidence** for every KR
4. **Keep trade-offs explicit** - what NOT to do is as important as what to do
5. **Validate against Life Wheel** - ensure main battlefields address real imbalances
