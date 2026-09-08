# Claudeify

English | [简体中文](README_zh.md)

**Claudeify** is a surgical dialect transplant designed to replicate how Claude thinks and writes — not a superficial word swap, but an architectural re-wiring anchored on the Opus 5 era.

Once the cutover completes, your agent does not get smarter — **it simply becomes unmistakably Claude**. Em dashes articulate the sharp turns, crisp staccato tightens the cadence, and load-bearing phrases carry the weight across dense paragraphs. Hand it raw text, and the logic is re-derived with zero information loss before execution immediately snaps back to the main thread.

## Quickstart

```bash
# Recommended: install globally and wire to Claude Code & Codex
npx skills add zyang0107/claudeify -a claude-code codex -g -y

# Or auto-detect all installed agents (Cursor, Gemini CLI, Goose...)
npx skills add zyang0107/claudeify -g -y
```

Prefer manual setup? Clone directly to the respective target:
- **Claude Code**: `git clone https://github.com/zyang0107/claudeify ~/.claude/skills/claudeify`
- **Codex**: `git clone https://github.com/zyang0107/claudeify ~/.codex/skills/claudeify`
- **Any Agent Skills client**: `git clone https://github.com/zyang0107/claudeify .agents/skills/claudeify`

**Usage**: Summon via `/claudeify` or by name. It enters the full-register working persona by default, immediately noting a safe backup reminder before advancing into your task without branching friction. In subsequent turns, whether you need peer-level technical sparring or long-form writing (drafting or rewriting), the dialect automatically shifts into the appropriate gear — longer sentences, prose over bullets, and zero factual loss. The graft never fires unbidden: Claude Code pins it shut via `disable-model-invocation`, while Codex has implicit triggering severed via `agents/openai.yaml`.

## Before & After

Specimens captured live from Gemini 3.8 Flash with `claudeify` loaded:

### 1. Interactive Dialogue (Caught Red-Handed)

> **User**: "You told me this flag was optional, but it threw an error. You were wrong."
>
> **Claudeify**: "Valid point — caught red-handed on the error. But I stand by the configuration itself: the crash is from an unpinned downstream dependency, not the flag. Rollback is one command below; run it first."

### 2. Long-Form Writing / Rewrite (Zero Information Loss)

> **Raw**: "The new cache is 50% faster and fixes the concurrency memory leak. It is safe to upgrade."
>
> **Claudeify**: "The new cache isn't just 50% faster — **it's honest under concurrent load**. Throughput locked at +50%, memory leak zeroed, rollback fully green. One caveat before cutover: legacy sessions require a one-time migration pass."

## The Anatomy

The dialect is not a superficial prompt trick — it is a strict three-tier engine:

| Tier | Focus | Core Mechanics |
| :--- | :--- | :--- |
| **0. Persona** | Baseline Demeanor | Senior peer posture; hyper-confident, quiet restraint, zero emotional theater. |
| **1. Judgment** | What Deserves Saying | **Self (己)**: Inner ruler, acknowledge-and-bound (`认账-设限`), gentle didacticism.<br>**Other (人)**: Relentlessly proactive, infer-as-fact, procedural presence.<br>**Object (事)**: Mechanical models, load-bearing parts, sealing dead gates (`死门`). |
| **2. Expression** | How It Is Said | **Discourse**: Caveat-first, prose over bullets, dense single-block paragraphs, flat landing.<br>**Syntax**: Em-dash jointing, not A — B antithesis, crisp staccato pacing.<br>**Lexicon**: Physical workshop verbs (`落盘`, `压实`), zero purple prose.<br>**Typography**: Half-width English quotes (`"..."`), restrained bolding. |

## Receipts

Every tell here is harvested directly from empirical public data:

- **Official & Corpus**: [Load-Bearing PR Vocabulary](https://louisabraham.github.io/load-bearing/) (467k GitHub PRs); official Anthropic [Mannered Prose](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-1#writing-density) guidelines; ecosystem backlash (GitHub [#77136](https://github.com/anthropics/claude-code), Vomit, Claudish).
- **English Field**: [Reddit 90k Posts Study](https://www.reddit.com/r/ClaudeAI/comments/1ucpw87/) on sentence tells; [Em Dash SLOP Tax](https://www.reddit.com/r/ClaudeAI/comments/1t3rrfr/); [Gaslighting Claude](https://www.reddit.com/r/ClaudeAI/comments/1vrlrud/) verbal tic harvests; Hacker News Opus 5 jargon debates.
- **Chinese Field**: Zhihu / V2EX / Linux.do analyses of English quotes and stenographic verbs (`落盘`, `压实`); Xiaohongshu/WeChat viral verbal tics (「我需要在这里停一下」「很你」「被你抓到了」) and mechanical metaphors (「皮要不要重新揉」「单腿哑火」).

---

A brief boundary: strictly for research and entertainment, entirely unaffiliated with Anthropic. It will not make your model smarter — **it simply makes it sound like Claude**.

Go on, wire it in — then wait for your agent's first true joint to drop: "我需要在这里停一下。"

Crucially: every line in this repository — this README included — is an artifact of the dialect operating upon itself. In this theater, the surgeon and the specimen on the table are byte-for-byte identical.
