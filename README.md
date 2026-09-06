# claudeify

一个高保真模仿 Claude 说话与写作风格的 skill,锚定 Opus 5 代(2026 年中)。
这不是一个改写器,而是一整套方言的移植。

装上它,你的 agent 不会变得更聪明——它会变得更像 Claude:每一次回复自带那股味儿,聊得越久越明显。
丢一段文本过来,它会把文本改写成 Claude 会写出的样子。

A skill that replicates how Claude talks and writes, anchored on the Opus 5 era.
This is not a rewriter — it is a dialect transplant.
With it installed, your agent does not get smarter — it gets more Claude: every reply carries the flavor, and long conversations carry it more. Paste any text, and it comes back as Claude would have written it.

## 安装 / Install

git clone https://github.com/&lt;你&gt;/claudeify ~/.claude/skills/claudeify

一行命令,一次克隆,终身带味。
其他 agent 平台:把该目录放进对应的 skills 目录——方言不分家。

For other agent platforms: place the folder in your skills directory — the dialect travels.

## 用法 / Usage

显式调用:输入 /claudeify 或点名 claudeify。它默认进入人设聊天模式——这不是缺陷,是设计:那股味儿最浓的地方,本来就是聊天。
丢一段文本给它,它切换进改写模式,改完自动回到聊天。

Invoke it by name (/claudeify). Persona chat is the default — not a limitation, a thesis: chat is where the flavor lives.
Paste any text, and it steps into rewrite mode, then steps back out.

## 声明 / Disclaimer

仅供娱乐。它模仿的是一整套语言习惯,与 Anthropic 或 Claude 无关;它不会让 agent 更有用,只会让 agent 更像 Claude——这两件事的区别,你已经知道了。使用前请备份重要内容。

For entertainment only. It parodies a set of language habits and is not affiliated with Anthropic or Claude. It does not make your agent more capable — only more Claude. You already know the difference. Back up important content before use.

## 证据 / Evidence

每一条规则都不是想出来的,是捡出来的:来自公开社区的真实观察与标本,来源清单见 references/sources.md。

No rule here was invented — every one was collected: real observations and specimens from public communities. The receipts live in references/sources.md.
