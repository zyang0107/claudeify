# claudeify

一个高保真模仿 Claude 说话与写作风格的 skill,锚定 Opus 5 代(2026 年中)。
这不是一个改写器——它是一整套方言的移植。

装上它,你的 agent 不会变得更聪明:它会变得更**像 Claude**。每一次回复都自带那股味儿——破折号先到,三连排比随后,加粗的关键短语在段落里替你指路;聊得越久,口音越重。丢一段文本过来,它切换进改写模式,把文本改写成 Claude 会写出的样子——改完,回到聊天,仿佛什么都没发生过。

A skill that replicates how Claude talks and writes, anchored on the Opus 5 era.
This is not a rewriter — it is a dialect transplant.
With it installed, your agent does not get smarter: it gets more **Claude**. Every reply carries the flavor — the em dash arrives early, the triads follow, and the bolded phrases do the navigating; the longer the chat, the heavier the accent. Paste any text, and it steps into rewrite mode, rewriting as Claude would have — then steps back into chat, as if nothing had happened.

## 安装:一行命令,各回各家

Claude Code:
git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify

Codex:
git clone https://github.com/zyang0107/claudeify ~/.agents/skills/claudeify

克隆一次、两处软链也可以——Codex 支持符号链接的 skill 目录。其余兼容 Agent Skills 开放标准的工具(Gemini CLI、Cursor、GitHub Copilot、Goose……),把目录放进它们各自的 skills 位置——方言不分家。

Claude Code:
git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify

Codex:
git clone https://github.com/zyang0107/claudeify ~/.agents/skills/claudeify

One clone, two symlinks also works — Codex follows symlinked skill folders. For other Agent-Skills-compatible tools (Gemini CLI, Cursor, GitHub Copilot, Goose…), place the folder in their skills location — the dialect travels.

## 用法:聊天是默认,改写是即兴

显式调用:输入 /claudeify 或点名 claudeify。它默认进入人设聊天模式——这不是缺陷,而是论题:那股味儿最浓的地方,本来就是聊天。
丢一段文本给它,它切换进改写模式,改完自动回到聊天。
它只显式触发:Claude Code 侧已内置;Codex 侧在 agents/openai.yaml 里设 policy.allow_implicit_invocation: false。

Invoke it by name (/claudeify). Persona chat is the default — not a limitation, a thesis: chat is where the flavor lives.
Paste any text, and it steps into rewrite mode, then steps back out.
It is explicit-invocation only: built into Claude Code; on Codex, set policy.allow_implicit_invocation: false in agents/openai.yaml.

## 声明

仅供娱乐。它模仿的是一整套语言习惯,与 Anthropic 或 Claude 无关;它不会让你的 agent 更有用——只会让它更像 Claude,而这两件事的区别,你已经知道了。使用前,请备份重要内容。

For entertainment only. It parodies a set of language habits and is not affiliated with Anthropic or Claude. It does not make your agent more capable — only more Claude. You already know the difference. Back up important content before use.

## 证据

这里没有一条规则是想出来的——每一条,都是从公开社区的帖子里捡回来的:9 万帖的统计、官方的命名、46 万个 PR 的词频。完整的收据,见 references/sources.md。

No rule here was invented — every one was collected from public communities: the statistics, the official naming, the vocabulary of 467k pull requests. The receipts live in references/sources.md.

值得一提:本仓库的每一份文档——包括这份 README——都由 claudeify 自己润色。它吃自己的狗粮,而且吃得很香。

Worth noting: every document in this repo — including this README — was polished by claudeify itself. It eats its own dog food, and it finds it delicious.

---

去吧,装上它——然后听你的 agent 说出它的第一句:
「我需要在这里停一下。」
