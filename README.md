# 恋爱聊天教练

中文 Agent Skill，用于回消息、延续话题、表达好感、约见面、确认关系，以及在冷淡或冲突时把话说清楚。这个仓库可以直接作为 Skill 目录使用。

## 本地安装

从仓库根目录运行以下命令，将 Skill 复制到 Codex 的个人 Skill 目录。其他兼容 Agent Skills 的客户端请使用其个人或项目 Skill 目录。

```sh
skill_dir="$HOME/.agents/skills/relationship-chat-coach"
mkdir -p "$skill_dir"
cp -R SKILL.md references "$skill_dir/"
```

在 Codex 开新会话，输入 `$relationship-chat-coach` 加上你的问题。支持自动触发的客户端也可以直接描述场景。

> 我们最近聊到一家咖啡店，我想约周日下午见面。帮我写一句自然的邀请。

Skill 本身没有运行时依赖，不调用外部服务，也不保存聊天档案。聊天内容按所用客户端的设置处理。

## 开源项目参考

| 项目 | 许可 | 调研结果与本项目用法 |
| --- | --- | --- |
| [openclaw-relationship-coach](https://github.com/cozer-1024/openclaw-relationship-coach) | MIT | 参考了主入口按场景指向不同参考文档的结构。 |
| [dsh-relationship-coach](https://github.com/Satesera/dsh-relationship-coach) | MIT | 把可观察行为、可能解释和未知拆开，再给可执行回复。这里复用这个分析思路。 |
| [relationship-coach-skill](https://github.com/replyher/relationship-coach-skill) | MIT | 参考沟通、冲突和边界的覆盖范围，补齐关系升温之外的场景。 |
| [HeDao-Coach](https://github.com/sanguo-jiang/HeDao-Coach) | GitHub 元数据未列明 | 调研了普通用户贴消息、拿回复和接续话题的流程。 |

本仓库的提示词、中文示例和验收场景为原创，复用范围是上述组织方式和交互思路。格式遵循 [Agent Skills 规范](https://agentskills.io/specification)。

## 开发

- [SKILL.md](SKILL.md) 定义触发条件、回复流程和边界。
- [references/](references/) 包含按需加载的场景示例。
- [evals/scenarios.md](evals/scenarios.md) 提供人工验收输入和检查点。
