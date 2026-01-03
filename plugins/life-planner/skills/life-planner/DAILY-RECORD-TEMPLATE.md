# Daily Record Template

Use this template when creating or updating daily record files.

**IMPORTANT: For file operations, use Bash heredoc method (see SKILL.md Method 1)**
- All sections should be generated in ONE Bash call using { } braces
- This ensures only ONE user confirmation is needed

## File Naming Convention

```
plans/{year}/daily-records-{year}-{month}.md
```

Example: `plans/2026/daily-records-2026-01.md`

## Document Structure

```markdown
# {Year}年{Month}月 每日记录

> 创建日期：{first_record_date}
> 最后更新：{last_update_date}
> 本月记录数：{total_count}

---

## 记录汇总

| 分类 | 记录数 | 说明 |
|-----|-------|-----|
| 运动健身 | {count} | 跑步、健身、游泳等 |
| 社交见面 | {count} | 聚会、约会、见面等 |
| 消费支出 | {count} | 购物、消费等 |
| 自由记录 | {count} | 其他记录 |

---

## 详细记录

### 运动健身

| 日期 | 内容 | 备注 |
|-----|-----|-----|
| {date} | {content} | {note} |

### 社交见面

| 日期 | 内容 | 备注 |
|-----|-----|-----|
| {date} | {content} | {note} |

### 消费支出

| 日期 | 内容 | 金额 | 备注 |
|-----|-----|-----|-----|
| {date} | {content} | {amount} | {note} |

### 自由记录

| 日期 | 内容 | 备注 |
|-----|-----|-----|
| {date} | {content} | {note} |

---

*本文件由每日记录功能自动维护*
```

## Category Keywords

Use these keywords to automatically classify records:

| 分类 | 关键词 |
|-----|-------|
| 运动健身 | 跑步, 健身, 游泳, 锻炼, 运动, 瑜伽, 骑行, 篮球, 足球, 羽毛球, 网球, 乒乓, 徒步, 爬山, 健走, 举重, 深蹲, 俯卧撑, 仰卧起坐, 普拉提, 拉伸, 有氧, 无氧, gym, workout |
| 社交见面 | 见面, 约会, 聚会, 聚餐, 饭局, 派对, 聚一聚, 叙旧, 相亲, 会面, 拜访, 串门, 团建, 联谊, meeting, party |
| 消费支出 | 买了, 花了, 消费, 购买, 支出, 付款, 下单, 充值, 订购, 购物, 采购, 开销, 报销, spent, bought, paid |
| 自由记录 | (默认，不匹配以上任何关键词时) |

## Amount Extraction Patterns

For expense records, extract amounts using these patterns:
- `花了100元` → 100元
- `花费100` → 100元
- `100元` / `100块` → 100元
- `￥100` / `¥100` → 100元

## Generation Guidelines

1. **New file creation** - Use `cat >` to create the initial file
2. **Appending records** - Use `cat >>` or direct table row insertion
3. **Update summary counts** - After adding records, update the summary table
4. **Maintain chronological order** - Sort records by date within each category
5. **Date format** - Use YYYY-MM-DD format for all dates
