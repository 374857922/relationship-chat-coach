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
| [童锦程视角 Skill](https://github.com/hotcoffeeshake/tong-jincheng-skill) | MIT | 社区根据直播、约会视频等资料整理。参考它直给的分析方式，以及留意对方是否有实际行动的思路。 |
| [LoveHelper.skill](https://github.com/Mowon0303/LoveHelper.skill) | MIT | 结合具体聊天片段给一句可发消息，再定下一步。重点参考接梗、降压和把线上互动落到见面的处理方式。 |
| [约会特工](https://github.com/mountainwaterr/yuehui-tegong) | GitHub 元数据未列明 | 对照了暧昧、僵持和确认关系的场景分法，用于检查场景覆盖。 |
| [情圣.skill](https://github.com/tomwong001/qingsheng-skill) | MIT | 参考匹配平台与微信的语境差异，以及邀约成功后确认安排的做法。 |
| [她不一样](https://github.com/863401402/she-love-me) | MIT | 参考结论能回到原对话核查的做法，在用户提供的片段内逐条对照。 |
| [恋爱训练营.skill](https://github.com/TammyTan516/relationship-training-skill) | GitHub 元数据未列明 | 借鉴多轮模拟和复盘，加入可随时结束的邀约练习。 |

本项目根据上述社区作品整理分析思路，提示词与案例为原创。童锦程相关内容来自社区整理，未逐段核对原视频。格式遵循 [Agent Skills 规范](https://agentskills.io/specification)。

## 开发

- [SKILL.md](SKILL.md) 定义触发条件、回复流程和边界。
- [references/](references/) 包含按需加载的场景示例和[实战拆聊与升温](references/progression.md)。
- [聊天复盘、约会跟进与练习](references/review-and-practice.md) 提供截图复盘、不同平台的沟通场景和模拟流程。
- [evals/scenarios.md](evals/scenarios.md) 提供人工验收输入和检查点。
