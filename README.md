# claudeify

claudeify 是一个高保真模仿 Claude 说话与写作风格的 skill——不是换几个词,而是一整套方言的移植手术,锚定 Opus 5 代(2026 年中)。

移植完成之后,你的 agent 不会变得更聪明:它会变得更**像 Claude**。破折号先到,三连排比随后,加粗的短语在段落里替你指路——聊得越久,口音越重;丢一段文本过来,它被改写成 Claude 会写出的样子,改完回到聊天,仿佛什么都没发生过。

claudeify is a skill that replicates how Claude talks and writes — not a word swap, but a full dialect transplant, anchored on the Opus 5 era.

After the transplant, your agent does not get smarter: it gets more **Claude**. The em dash arrives early, the triads follow, the bolded phrases navigate — the longer the chat, the heavier the accent; paste any text, and it comes back as Claude would have written it, then chat resumes as if nothing had happened.

## 安装 / Install

在大多数工具那里,安装是一张配置清单;在这里,它是唯一的一刀——npx 把 skill 送进共享目录 ~/.agents/skills,再软链到位:一份供体,多位受者,Claude Code 与 Codex 同时接上。

In most tools, installation is a configuration checklist; here, it is a single cut — npx delivers the skill into the shared ~/.agents/skills and symlinks it into place: one donor, several recipients, and Claude Code and Codex come online together.

```bash
npx skills add zyang0107/claudeify -a claude-code codex -g -y
```

术后复查 / Updates:

```bash
npx skills update -g -y
```

爱折腾的,也可以手动克隆——目标路径见注释:

Prefer to tinker? Clone by hand — the comments show the way:

```bash
# Claude Code
git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify
# Codex
git clone https://github.com/zyang0107/claudeify ~/.agents/skills/claudeify
# 项目级 / Project-level(任何标准兼容工具 / any standard-compatible tool)
git clone https://github.com/zyang0107/claudeify .agents/skills/claudeify
```

其余兼容 Agent Skills 开放标准的工具(Gemini CLI、Cursor、GitHub Copilot、Goose……),把目录放进它们各自的 skills 位置——方言不分家。

For other Agent-Skills-compatible tools (Gemini CLI, Cursor, GitHub Copilot, Goose…), place the folder in their skills location — the dialect travels.

## 用法 / Usage

显式调用:输入 /claudeify 或点名 claudeify。它默认进入人设聊天模式——这不是缺陷,而是论题:那股味儿最浓的地方,本来就是聊天。丢一段文本给它,它切换进改写模式,改完自动回到聊天。
值得注意的是,移植物从不先开口——Claude Code 侧由 disable-model-invocation 锁死,Codex 侧由包内的 agents/openai.yaml 关掉隐式触发。

Invoke it by name (/claudeify). Persona chat is the default — not a limitation, a thesis: chat is where the flavor lives. Paste any text, and it steps into rewrite mode, then steps back out.
Worth noting: the graft never speaks first — Claude Code locks it via disable-model-invocation, and the bundled agents/openai.yaml turns off implicit invocation on Codex.

## 声明 / Disclaimer

仅供娱乐。它移植的是一整套语言习惯,与 Anthropic 或 Claude 无关;它不会让你的 agent 更有用——只会让它更像 Claude,而这两件事的区别,你已经知道了。手术之前,请备份重要内容。

For entertainment only. It transplants a set of language habits and is not affiliated with Anthropic or Claude. It does not make your agent more capable — only more Claude. You already know the difference. Before the operation, back up what matters.

## 证据 / Evidence

这里没有一条规则是想出来的——每一条,都是从公开社区的帖子里捡回来的:9 万帖的统计、官方的命名、46 万个 PR 的词频,三路证据,共同指向同一副口音。完整的收据,见 references/sources.md。

No rule here was invented — every one was collected from public communities: the statistics, the official naming, the vocabulary of 467k pull requests — three lines of evidence, one accent. The receipts live in references/sources.md.

值得一提:本仓库的每一份文档——包括这份 README——都由 claudeify 自己润色。这台手术,主刀和患者是同一个。

Worth noting: every document in this repo — including this README — was polished by claudeify itself. In this operation, the surgeon and the patient are the same.

---

Go on, install it — then listen for your agent's first line: 「我需要在这里停一下。」
