# Life Plan 插件分发指南

## 分发方式概览

| 方式 | 适用场景 | 复杂度 |
|-----|---------|-------|
| GitHub Marketplace | 公开分享给所有人 | ⭐⭐ |
| 私有 Git 仓库 | 团队内部使用 | ⭐⭐ |
| 直接分享文件 | 快速分享给个人 | ⭐ |

---

## 方式一：通过 GitHub Marketplace 分发（推荐）

### 步骤 1：创建 GitHub 仓库

```bash
cd /Users/charliec/Projects/life-plan/life-plan-plugin

# 初始化 Git
git init
git add .
git commit -m "Initial commit: life-plan plugin v1.0.0"

# 创建 GitHub 仓库后推送
git remote add origin https://github.com/YOUR_USERNAME/life-plan-plugin.git
git branch -M main
git push -u origin main
```

### 步骤 2：更新 plugin.json 中的仓库地址

编辑 `.claude-plugin/plugin.json`，将 `repository` 改为你的实际仓库地址：

```json
{
  "repository": "https://github.com/YOUR_USERNAME/life-plan-plugin"
}
```

### 步骤 3：其他用户安装

用户执行以下命令即可安装：

```bash
# 1. 添加你的仓库作为 marketplace
/plugin marketplace add YOUR_USERNAME/life-plan-plugin

# 2. 安装插件
/plugin install life-plan@YOUR_USERNAME
```

或者一步到位：

```bash
/plugin install github:YOUR_USERNAME/life-plan-plugin
```

---

## 方式二：私有 Git 仓库分发

适用于公司内部或团队使用。

### 步骤 1：推送到私有仓库

```bash
# GitLab 示例
git remote add origin https://gitlab.com/your-team/life-plan-plugin.git
git push -u origin main

# 或者私有 GitHub
git remote add origin https://github.com/your-org/life-plan-plugin.git
git push -u origin main
```

### 步骤 2：团队成员安装

```bash
# 通过 URL 添加
/plugin marketplace add https://gitlab.com/your-team/life-plan-plugin.git

# 安装
/plugin install life-plan@your-team
```

### 步骤 3：团队配置（可选）

在团队的 `.claude/settings.json` 中预配置：

```json
{
  "extraKnownMarketplaces": {
    "team-tools": {
      "source": {
        "source": "url",
        "url": "https://gitlab.com/your-team/life-plan-plugin.git"
      }
    }
  },
  "enabledPlugins": {
    "life-plan@team-tools": true
  }
}
```

---

## 方式三：直接分享文件

最简单的方式，适合一次性分享。

### 打包插件

```bash
cd /Users/charliec/Projects/life-plan
zip -r life-plan-plugin.zip life-plan-plugin/
```

### 接收方安装

1. 解压 `life-plan-plugin.zip`
2. 将文件夹放到任意位置
3. 启动 Claude Code 时加载：

```bash
claude --plugin-dir /path/to/life-plan-plugin
```

或者复制到全局插件目录：

```bash
# macOS/Linux
cp -r life-plan-plugin ~/.claude/plugins/

# 然后在 Claude Code 中启用
/plugin enable life-plan
```

---

## 验证安装

安装后，可以通过以下方式验证：

```bash
# 查看已安装的插件
/plugin list

# 查看可用的 skills
What skills are available?

# 测试触发
我想做年度规划
```

---

## 版本更新

### 发布新版本

1. 更新 `plugin.json` 中的 `version`
2. 提交并推送到 Git：

```bash
git add .
git commit -m "Release v1.1.0: added new features"
git tag v1.1.0
git push origin main --tags
```

### 用户更新

```bash
/plugin update life-plan@YOUR_USERNAME
```

---

## 常见问题

### Q: 插件没有被识别？

检查目录结构是否正确：
- `.claude-plugin/plugin.json` 必须存在
- `skills/` 目录必须在插件根目录

### Q: Skill 没有触发？

检查 `SKILL.md` 的 `description` 字段是否包含足够的触发关键词。

### Q: 如何调试？

```bash
# 以调试模式启动
claude --debug --plugin-dir ./life-plan-plugin

# 验证插件配置
/plugin validate ./life-plan-plugin
```

---

## 联系方式

如有问题，请在 GitHub 仓库提交 Issue。
