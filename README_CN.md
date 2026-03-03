# Claude Skill Architect (中文版)

**构建严格遵循 Anthropic 官方《Claude Skill 构建完整指南》的高质量 Claude Skills。**

[English Version](README.md) | [中文版](README_CN.md)

这个 Meta-Skill 将 Claude 转变为一位专业的 Skill 架构师。它不仅仅是写 Prompt，而是工程化地构建健壮、模块化、节省 Token 的 **Skill 软件包**。

## 🚀 特性

*   **官方最佳实践:** 直接基于 Anthropic 的 [Complete Guide to Building Skills for Claude](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf) 构建。
*   **渐进式披露架构 (Progressive Disclosure):** 自动将 Skill 结构化为：
    *   **路由层:** 简洁的 YAML frontmatter，用于高效的工具选择。
    *   **控制层:** 具有清晰逻辑流的 `SKILL.md` 正文。
    *   **知识层:** `references/` 和 `scripts/` 用于处理繁重任务，保持上下文窗口整洁。
*   **思维链 (CoT) 集成:** 在生成的 Skill 中强制使用 `<thinking>` 块，以提高推理能力并减少幻觉。
*   **结构化输入模式:** 为每个 Skill 定义清晰的基于 XML 的输入参数。

## 📂 仓库结构

由本架构师生成的标准 Skill 如下所示：

```text
my-new-skill/
├── SKILL.md          # 大脑: 元数据 + 逻辑 + 指令
├── references/       # 图书馆: 静态知识, 模板, API 文档
│   ├── template.md
│   └── glossary.md
└── scripts/          # 双手: 用于确定性任务的 Python/Bash 脚本
    └── utils.py
```

## 📦 安装

1.  将本仓库中的 `SKILL_CN.md` 文件复制到你的 Claude/OpenClaw skills 目录，并重命名为 `SKILL.md` (或者保持原名并在配置中指定)：
    ```bash
    mkdir -p /path/to/your/skills/claude-skill-architect
    cp SKILL_CN.md /path/to/your/skills/claude-skill-architect/SKILL.md
    ```
2.  重载你的 Agent 或重启会话以注册新 Skill。

## 💡 使用方法

安装完成后，只需让 Claude 为你构建 Skill。请明确说明 **触发器** (何时运行) 和 **预期结果**。

### 提示词示例

**基础:**
> "创建一个遵循 Google 风格指南编写 Python 文档字符串的 Skill。"

**进阶:**
> "构建一个 '周报生成器' Skill。它应该接受一系列要点作为输入。它需要一个 `references/template.md` 文件来存储报告格式。该 Skill 在生成报告之前应严格检查是否缺少关键指标。"

## 🛡️ 许可证

MIT License. 详见 [LICENSE](LICENSE)。

## 🔗 参考资料

*   [Anthropic: The Complete Guide to Building Skills for Claude](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf)
