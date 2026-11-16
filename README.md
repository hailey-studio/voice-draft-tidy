# voice-draft-tidy · 语音稿整理

一个给内容创作者用的 Agent Skill：把你对着手机语音输入的乱稿，整理成你自己的稿子。

**它不替你写。** 市面上很多写作 Skill 是“按某种风格帮你写一篇”。这个 Skill 反过来：稿子、观点和语气都是你的，它只帮你看清楚自己想说什么，再用你的原句帮你排好。

## 它解决什么问题

灵感来了就语音输入，出来的稿子通常是这样的：

- 识别错别字一堆（“生物钟”变成“生物中”，“靠谱”变成“靠普”）
- 同一个意思绕着说三遍
- 最想说的那句话，藏在某个顺口带过的地方
- 顺序跟着思绪跳，中间突然冒出一段不相关的

直接丢给 AI 润色，结果往往是逻辑顺了，但读起来不像你了。

## 两步流程

**第一步：提炼和讨论（不改稿）**
找出一句话中心、画出逻辑线、列出车轱辘话和断层、列出所有拿不准的识别错误，然后问你 1 到 3 个问题。等你拍板。

**第二步：重新整理**
按定下的框架重排，尽量保留原句，只修识别错误、合并重复。缺内容的地方标【】提示你自己写，最后附改动说明。

完整示例（虚构原稿 → 第一步讨论 → 第二步成稿）见 [references/examples.md](references/examples.md)。

## 安装

把整个文件夹放进你的 skills 目录，例如：

```
~/.claude/skills/voice-draft-tidy/
```

然后填写 [references/voice-profile.md](references/voice-profile.md)，告诉它你说话的习惯、风格参考和不能公开的信息。不填也能用，只是没那么像你。

## 使用

直接把语音稿发过去，说“帮我整理一下”就行。也可以点名加选模式：

- “压缩一下，没价值的删掉”
- “用资深观众的角度挑挑刺”
- “给我几个标题”
- “这是商单，品牌要求 15 秒内提到产品”

## 文件结构

```
voice-draft-tidy/
├── SKILL.md                      主流程
└── references/
    ├── examples.md               完整示例
    ├── ai-tone-checklist.md      交付前的 AI 腔检查
    ├── sponsored.md              商单稿规则
    └── voice-profile.md          你的声音档案（使用前填写）
```

## 致谢

设计时参考了这些项目：

- [obra/superpowers](https://github.com/obra/superpowers) 的 brainstorming：先问为什么，一次只问一个问题
- [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh)：不改变原文信息和确定程度，中文 AI 腔分类
- [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) 的 khazix-writer：选题自检，AI 和人的分工边界
- [anthropics/skills](https://github.com/anthropics/skills) 的 skill-creator：Skill 结构和触发描述

## License

MIT
