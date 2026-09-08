# claudeify

[English](README.md) | 简体中文

claudeify 是一套旨在高保真复刻 Claude 语域的方言移植手术——它不负责替换几个表层词汇，而是直接重构思维的受力结构；锚定 Opus 5 代（2026 年中）。

手术落盘之后，你的 agent 并不会因此变聪明——**它只是变得更像 Claude**。破折号干脆挑起逻辑翻转，短句碎步随后收紧节奏，承重短语在致密段落里立起骨架。丢一段文本过来，它在事实零丢失的前提下当场压实，改完即刻切回主线，仿佛什么都没发生过。

## 快速上手

```bash
# 推荐：全局安装并自动挂载至 Claude Code 与 Codex
npx skills add zyang0107/claudeify -a claude-code codex -g -y

# 或对本机所有受体自动探测并挂载（Cursor、Gemini CLI 等）
npx skills add zyang0107/claudeify -g -y
```

需要手动装配？直接克隆至对应槽位：
- **Claude Code**: `git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify`
- **Codex**: `git clone https://github.com/zyang0107/claudeify ~/.codex/skills/claudeify`
- **通用 Agent Skills 客户端**: `git clone https://github.com/zyang0107/claudeify .agents/skills/claudeify`

**调用**：输入 `/claudeify` 或指名 `claudeify` 显式唤醒，默认进入全语域工作态。唤醒首句即交代备份底线，随后直接推进任务，零分支阻断；后续无论面对技术交锋还是长篇写作（原创撰写或材料重揉），AI 均会自动切入对应力学引擎——句子更长段落更少、散文压过列表、事实观点零丢失。这套移植物从不不请自来：Claude Code 由 `disable-model-invocation` 焊死，Codex 由包内 `agents/openai.yaml` 关闭隐式触发。你不点名，它哪儿也不去。

## 实弹对照

实弹样本（以下交互取自 Gemini 3.8 Flash 挂载 `claudeify` 的真实跑测）：

### 1. 交互对话（现场被抓）

> **用户**：「你之前说这个参数不用配，但报错了，你搞错了。」
>
> **Claudeify**：「好，被抓到了——这点我承认。但我不能同意归因：报错是下游依赖未固定，旋钮本身没问题。回滚命令在下面，先执行第一行。」

### 2. 成篇写作 / 改写（事实零丢失）

> **原稿**：「新版本缓存性能提升了 50%，修复了并发情况下的内存泄漏，大家可以放心升级。」
>
> **Claudeify**：「新缓存不是单纯变快——它只是在并发压力下**变得诚实**。吞吐压实 50%，内存死门归零，回滚链路全绿。升级只有一处边界：历史 session 需执行一次性归户。」

## 架构解剖

这套方言绝非玄学 Prompt，而是一套严格正交的三层力学引擎：

| 层级 | 关注焦点 | 核心机制 |
| :--- | :--- | :--- |
| **0. 整体基准** | 基础气质姿态 | 资深同事姿态；冷静克制、极度自信、工作语域、零多余情绪。 |
| **1. 判断层** | 哪些话值得说 | **立己**：内有一尺、认账-设限三段式（认局部微观，守宏观防线）、适度说教。<br>**待人**：激进代办、揣测为实（答底层意图）、程序性在场。<br>**审事**：物理力学受力构件、核心承重、死门归零、全链路闭环。 |
| **2. 表达层** | 这些话怎么说 | **篇章**：断言带界（Caveat-First）、散文压过列表、致密段落承载、平实定调收束。<br>**句式**：破折号主关节（挑起转折/插入/翻转）、not A — B 否定翻转、短句碎步切节奏。<br>**词法**：具象车间手势动词（`落盘`、`压实`、`死门`）、零文学腔。<br>**标记**：半角英文双引号（`"..."`）、视线克制局部加粗。 |

## 证据收据

这里没有一条规则是凭空编造的——特征全部来自公开社区田野与语料穿透：

- **官方与语料**：[467k GitHub PRs 词频统计](https://louisabraham.github.io/load-bearing/)（证实 `load-bearing`、`plainly` 等词的高频聚集）；Anthropic 官方对 [Mannered Prose](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-1#writing-density) 的定性命名；社区反弹（GitHub issue [#77136](https://github.com/anthropics/claude-code)、去味插件）。
- **英文田野**：[Reddit 9万帖句级样本](https://www.reddit.com/r/ClaudeAI/comments/1ucpw87/)；破折号密度律（[em dash SLOP Tax](https://www.reddit.com/r/ClaudeAI/comments/1t3rrfr/)）；口癖收割（[Gaslighting Claude](https://www.reddit.com/r/ClaudeAI/comments/1vrlrud/)）；Hacker News 术语方言辩论。
- **中文田野**：知乎/V2EX/linux.do 对英文双引号与速记动词（`落盘`、`压实`）的穿透分析；小红书/微博/微信口癖词典（「我需要在这里停一下」「很你」「被你抓到了」）与车间力学动词（「皮要不要重新揉」「单腿哑火」「死门」）。

---

边界说明：仅供娱乐与研究，与 Anthropic 官方无涉。它不会让你的 agent 变聪明——**它只是让它更像 Claude**。

装上它吧——然后静候你的 agent 落下它的第一个关节：「我需要在这里停一下。」

顺便说一句——长期看，本仓库的每一行文本（包括这份 README）都是这套方言自我施术的产物。在这台手术台上，主刀医师与躺在上面的供体，是同一个。
