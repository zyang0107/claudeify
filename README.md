# claudeify

English | [简体中文](README_zh.md)

claudeify is a surgical dialect transplant designed to replicate how Claude thinks and writes — not a superficial word swap, but an architectural re-wiring anchored on the Opus 5 era.

Once the cutover completes, your agent does not get smarter — **it simply becomes unmistakably Claude**. The em dash arrives within the first thirty words, the staccato triads tighten the cadence, and bolded phrases bear the weight across dense paragraphs. The longer the session, the heavier the accent; paste any raw text, and the logic is re-derived with zero information loss before execution immediately snaps back to the main thread.

## Installation

In most tooling, installation is an endless checklist of manual setup; here, it is compressed into a single clean cut — npx lands the canonical skill into `~/.agents/skills` and symlinks it directly into place: one donor, multiple runtimes, with Claude Code and Codex wired up in parallel.

```bash
# Install globally and wire to both Claude Code and Codex
npx skills add zyang0107/claudeify -a claude-code codex -g -y

# Or auto-detect all installed agents on your machine (Cursor, Gemini CLI, etc.)
npx skills add zyang0107/claudeify -g -y
```

Updates:

```bash
npx skills update -g -y
```

Prefer the manual route? Clone by hand — the seams are marked below:

```bash
# Claude Code (Global)
git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify

# Codex (Global)
git clone https://github.com/zyang0107/claudeify ~/.codex/skills/claudeify

# Project-level (Any tool supporting the Agent Skills standard)
git clone https://github.com/zyang0107/claudeify .agents/skills/claudeify
```

For other Agent-Skills-compatible environments (Gemini CLI, Cursor, GitHub Copilot, Goose…), drop the payload into their respective skill directories — the dialect travels without friction.

## Usage

Explicit invocation only: trigger via `/claudeify` or by name. It defaults to the full-register working persona — not an oversight, but a deliberate thesis: the dialect only proves itself inside real dialogic tension. Hand it a passage to rewrite, and it re-derives the prose with zero factual loss before snapping cleanly back to chat.

One caveat, and it's a real one: the graft never speaks unbidden. Claude Code pins it shut via `disable-model-invocation`, while Codex has its implicit firing severed by the bundled `agents/openai.yaml`. Unless explicitly summoned, it stays put.

## Disclaimer

A necessary boundary: strictly for entertainment. It transplants an idiosyncratic set of linguistic habits and mechanical priors, entirely unaffiliated with Anthropic or Claude. It will not grant your agent new capabilities — **it merely makes it sound like Claude**. The blast radius between those two things should already be plainly obvious. Back up your working tree before opening the chest.

## Evidence

No rule here was invented out of thin air — every tell was harvested directly from the trenches of the public commons: empirical stats across 90k posts, official acknowledgment of mannered prose, and corpus-level token frequencies across 467k PRs. Three independent lines of evidence converging on a single dialect. The receipts are fully accounted for:

- **Corpus & Official**:
  - **467k GitHub PRs Vocabulary**: [The load-bearing vocabulary of Claude](https://louisabraham.github.io/load-bearing/) (confirming heavy clustering of `load-bearing`, `plainly`, `quietly`, etc.)
  - **Anthropic's Official Naming**: formally acknowledging [Mannered Prose](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-1#writing-density) in the Fable 5.1 guide (substituting metaphor and flourish for direct statement)
  - **Ecosystem Backlash**: GitHub issue [#77136](https://github.com/anthropics/claude-code); community-developed translation plugins (claudish, vomit)
- **English Community**:
  - **Reddit r/ClaudeAI**: [90k posts study](https://www.reddit.com/r/ClaudeAI/comments/1ucpw87/) on sentence-level tells, [em dash SLOP Tax](https://www.reddit.com/r/ClaudeAI/comments/1t3rrfr/) on density, and [Gaslighting Claude](https://www.reddit.com/r/ClaudeAI/comments/1vrlrud/) harvesting signature verbal tics
  - **Hacker News**: extended debates on Opus 5 jargon density and dialect crystallization
- **Chinese Community**:
  - **Zhihu & V2EX & linux.do**: analyses of mixed English, straight double quotes, and stenographic verbs (`落盘`, `压实`)
  - **Xiaohongshu & Weibo & WeChat**: independently replicated verbal tics (「我需要在这里停一下」「我就在这里，哪儿也不去」「很你」「被你抓到了」); physical workshop verbs and mechanical metaphors (「皮要不要重新揉」「单腿哑火」「死门」)

---

Go on, wire it in — then wait for your agent's first true joint to drop: "我需要在这里停一下。"

Crucially: every line in this repository — this README included — is an artifact of the dialect operating upon itself. In this theater, the surgeon and the specimen on the table are byte-for-byte identical.
