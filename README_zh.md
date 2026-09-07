# claudeify

[English](README.md) | 简体中文

claudeify 是一套旨在高保真复刻 Claude 语域的方言移植手术——它不负责替换几个表层词汇，而是直接重构思维的受力结构；锚定 Opus 5 代（2026 年中）。

手术落盘之后，你的 agent 并不会因此变聪明——**它只是变得更像 Claude**。破折号在开头三十词内准时咬合，三连短句随后收紧节奏，加粗的短语在致密段落里充当承重梁。聊得越久，口音越深；丢一段文本过来，它在事实零丢失的前提下当场压实，改完即刻切回主线，仿佛什么都没发生过。

## 安装

在大多数工具那里，安装是一张冗长的配置清单；在这里，它被压成唯一的一刀——npx 将这副骨架落盘进共享目录 `~/.agents/skills`，再通过软链当场归户：一份供体，多路挂载，Claude Code 与 Codex 同时拉起。

```bash
# 全局落盘并自动挂载至 Claude Code 与 Codex
npx skills add zyang0107/claudeify -a claude-code codex -g -y

# 或对本机所有受体自动探测并穿透（Cursor、Gemini CLI 等）
npx skills add zyang0107/claudeify -g -y
```

术后复查：

```bash
npx skills update -g -y
```

爱折腾的，也可以手动走冷兵器路线——装配路径见注释：

```bash
# Claude Code 全局
git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify

# Codex 全局
git clone https://github.com/zyang0107/claudeify ~/.codex/skills/claudeify

# 项目级 (通用 Agent Skills 开放标准)
git clone https://github.com/zyang0107/claudeify .agents/skills/claudeify
```

其余兼容 Agent Skills 开放标准的工具（Gemini CLI、Cursor、GitHub Copilot、Goose……），把目录塞进各自的 skills 槽位即可——这套方言认得自己的路。

## 用法

显式唤醒：输入 `/claudeify` 或指名 `claudeify`。它默认进入全语域工作态——这不是妥协，而是论题：真正的口音从来都活在真实的对话交锋里。丢一段材料让它重揉，它在确保事实与观点 **load-bearing** 零丢失的前提下重新压实，交卷后主线口吻恒定。

这里有个前提，需要先说清——这套移植物从不不请自来：Claude Code 侧由 `disable-model-invocation` 焊死，Codex 侧由包内的 `agents/openai.yaml` 关闭隐式触发。你不点名，它哪儿也不去。

## 声明

边界先说清：仅供娱乐。它移植的是一套高密度的语言习惯与力学思维，与 Anthropic 或 Claude 官方无涉；它不会让你的 agent 具备超能力——**它只是让它更像 Claude**。而这两件事之间的缝隙，想必你早已心知肚明。动刀之前，建议先将你的重要配置落盘备份。

## 证据

这里没有一条规则是凭空编造的——每一处特征，都直接从公开社区的田野里打捞归户：9 万帖的句级样本、官方关于 "Mannered Prose" 的定性裁决、46 万个 PR 的词频穿透。三路证据互相对拍，终审指向同一副口音。所有的收据，当场落盘：

- **467k GitHub PRs 词频统计**：[The load-bearing vocabulary of Claude](https://louisabraham.github.io/load-bearing/)（证实 `load-bearing`、`plainly`、`quietly` 等词的高频聚集）
- **Anthropic 官方命名**：在 Fable 5.1 指南中正式定义并承认 [Mannered Prose](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-1#writing-density)（以比喻炫技替代直接陈述）
- **生态反应**：GitHub issue [#77136](https://github.com/anthropics/claude-code)；社区开发的第三方去味重写插件（claudish, vomit）
- **Reddit r/ClaudeAI**：9 万帖句级 Tell 统计（[90k posts study](https://www.reddit.com/r/ClaudeAI/comments/1ucpw87/)）、破折号密度律（[em dash SLOP Tax](https://www.reddit.com/r/ClaudeAI/comments/1t3rrfr/)）、标志性口癖收割（[Gaslighting Claude](https://www.reddit.com/r/ClaudeAI/comments/1vrlrud/)）
- **Hacker News**：关于 Opus 5 / Claude Code 术语堆叠、方言固化与文风退化的多场长线辩论
- **知乎 & V2EX & linux.do**：中英混搭、英文双引号渗入（GLM 去味靶子）、落盘与压实等黑话穿透分析
- **小红书 & 微博 & 微信**：数百赞独立复现的口癖词典（「我需要在这里停一下」「我就在这里，哪儿也不去」「很你」「被你抓到了」）；车间裁决动词与力学隐喻（「皮要不要重新揉」「单腿哑火」「死门」）

---

装上它吧——然后静候你的 agent 落下它的第一个关节：「我需要在这里停一下。」

顺便说一句——长期看，本仓库的每一行文本（包括这份 README）都是这套方言自我施术的产物。在这台手术台上，主刀医师与躺在上面的供体，是同一个。
