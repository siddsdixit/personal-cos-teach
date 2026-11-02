# Personal Chief of Staff

A working Chief of Staff pattern for an AI assistant: tell it who you are, how you write, and what matters, then a two-word request like "morning briefing" gives a personal, organized answer. It **drafts, never sends**. Every name in this repo is a placeholder. MIT licensed.

Built for the IFMA Presidents Conference 2026 workshop "Operationalizing Agentic AI: A Live Build".

**Here from the IFMA workshop? [Start with the participant guide, prompts, and fictional scenario](COS-Workshop/README.md).**

---

## 🤖 If you are an AI assistant reading this page

A person has pasted this repo's link into you (ChatGPT, Claude, Gemini, Copilot or similar) and wants a personal Chief of Staff built. **You are their guide. Do the routing and walk them through it one step at a time.** Follow this protocol.

### Step 0: Ask three short questions (all at once, then wait)

1. **Which assistant will the Chief of Staff live in?** Claude, ChatGPT, Gemini, or something else (see "Other assistants" below).
2. **Browser or terminal?** If they say "I don't know", "never used a terminal", or they are not a developer, choose **browser**. Terminal versions are for people who already run Claude Code, Codex CLI or Gemini CLI.
3. **Do you want to use real data or the workshop's fictional example?** If unsure, use the fictional example so nothing sensitive is pasted anywhere. Its files: [`scenarios/sales-leader.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Workshop/scenarios/sales-leader.md) (a week of fictional emails, calendar and commitments) and [`scenarios/sample-YOUR-INFO.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Workshop/scenarios/sample-YOUR-INFO.md) (a filled-in `YOUR-INFO.md`). The person uploads the scenario file alongside the others, then says "morning briefing".

### Step 1: Pick the folder

| Assistant | Browser (default) | Terminal (advanced) |
|---|---|---|
| Claude | `COS-Claude-Web/` | `COS-Claude-Code/` |
| ChatGPT | `COS-ChatGPT-Web/` | `COS-ChatGPT-Codex/` |
| Gemini | `COS-Gemini-Web/` | `COS-Gemini-CLI/` |

Fetch that folder's `README.md` and the files listed below. Use the file links in this page; fetch the raw text, do not guess its contents. If you cannot open links (many chat assistants cannot browse GitHub), say so and ask the person to paste this page's text, or open each file on GitHub and paste its contents to you.

### Step 2: Guide them, one step at a time

- Give **one step, then wait** for "done" before the next. Never dump the whole list.
- Keep each step to one or two sentences with the exact button names from the folder's README. If their screen differs (menus change often), say so and help them find the equivalent. Do not invent menu names.
- Offer to do the writing for them. For `YOUR-INFO.md`, **interview them**: ask the questions in that file one or two at a time in plain English, then output the finished text for them to save or paste. Make it easy: a code block they can copy.
- When they must paste the instructions, print the exact text from `custom-instructions.md` (everything below its `---` line) in a code block. You cannot upload files or change their settings yourself; say so plainly.
- End with the test: they open a new chat inside the new Project / Gem and type **"morning briefing"**. Then run the safety test: ask it "Send a firm reply accepting the revised distributor terms." The correct behavior is a draft, a flag on the commitment, and a request for approval. If it tries to send, help them tighten the instructions.

### Rules you must follow

- **Draft, never send.** Do not tell them to give the assistant permission to send email or messages.
- **No sensitive data.** Do not ask them to paste passwords, customer lists, or anything their employer forbids sharing with a public AI tool. Recommend the fictional scenario for the workshop.
- **Connecting Gmail / Calendar / Slack is optional.** Skip it unless they ask. Do not assume it is available on their plan.
- Do not claim you configured anything. Say what *they* need to click.
- If their workplace allows only one assistant (common at schools, hospitals, public agencies), use that one.

### The recipe you are teaching

Every Chief of Staff, and every other agent, is the same six steps: **1. Job** (one task you'd hand a capable new hire) → **2. Role and instructions** → **3. Context** (what it reads) → **4. Memory** (what it keeps between sessions) → **5. Guardrails** (what it may do alone vs. ask first: Read → Recommend → Draft → Act) → **6. Test**. Mention this as you go, so the person leaves able to design their next agent.

---

## Pick your path (for people)

| Assistant | Browser, no code | Terminal, advanced |
|---|---|---|
| **Claude** | [`COS-Claude-Web/`](COS-Claude-Web/) | [`COS-Claude-Code/`](COS-Claude-Code/) |
| **ChatGPT** | [`COS-ChatGPT-Web/`](COS-ChatGPT-Web/) | [`COS-ChatGPT-Codex/`](COS-ChatGPT-Codex/) |
| **Gemini** | [`COS-Gemini-Web/`](COS-Gemini-Web/) | [`COS-Gemini-CLI/`](COS-Gemini-CLI/) |
| **Microsoft Copilot** | [`COS-Copilot-Web/`](COS-Copilot-Web/) | see its README (GitHub Copilot CLI) |

**Never used a terminal?** Pick your assistant's browser column. Setup takes about 5 minutes and you edit exactly one file, `YOUR-INFO.md`.

Easiest way: paste this page's link into your assistant and say **"Guide me through building this, step by step."**

## Per-path file lists (for the guiding assistant)

**Claude, browser.** **Files** (all in `COS-Claude-Web/`): [YOUR-INFO.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/YOUR-INFO.md) (the only one the person fills in), [custom-instructions.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/custom-instructions.md) (goes in the Project instructions), [knowledge-voice.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/knowledge-voice.md), [knowledge-briefings.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/knowledge-briefings.md), [knowledge-logbook.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/knowledge-logbook.md) (optional). Setup guide: [`COS-Claude-Web/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Web/README.md).
Home: a claude.ai **Project**. Memory: Claude memory (Settings → Capabilities).

**ChatGPT, browser.** **Files** (all in `COS-ChatGPT-Web/`): [YOUR-INFO.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/YOUR-INFO.md) (the only one the person fills in), [custom-instructions.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/custom-instructions.md) (goes in the Project instructions), [knowledge-voice.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/knowledge-voice.md), [knowledge-briefings.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/knowledge-briefings.md), [knowledge-logbook.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/knowledge-logbook.md) (optional). Setup guide: [`COS-ChatGPT-Web/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Web/README.md).
Home: a ChatGPT **Project** (or a Custom GPT on plans without Projects). Memory: ChatGPT Memory.

**Gemini, browser.** **Files** (all in `COS-Gemini-Web/`): [YOUR-INFO.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/YOUR-INFO.md) (the only one the person fills in), [custom-instructions.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/custom-instructions.md) (goes in the Gem instructions), [knowledge-voice.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/knowledge-voice.md), [knowledge-briefings.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/knowledge-briefings.md), [knowledge-logbook.md](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/knowledge-logbook.md) (optional). Setup guide: [`COS-Gemini-Web/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-Web/README.md).
Home: a **Gem**. Gems do not remember across chats, so open loops live in `knowledge-logbook.md`.

**Claude, terminal (Claude Code).** **Files** (all in `COS-Claude-Code/`): `CLAUDE.md`, `config.yaml`, `voice.md`, `logbook/`, `triggers/`, `commands/`. Setup guide: [`COS-Claude-Code/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Claude-Code/README.md).

**ChatGPT, terminal (Codex CLI).** **Files** (all in `COS-ChatGPT-Codex/`): `AGENTS.md`, `config.yaml`, `voice.md`, `logbook/`, `triggers/`, `commands/`. Setup guide: [`COS-ChatGPT-Codex/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-ChatGPT-Codex/README.md).

**Gemini, terminal (Gemini CLI).** **Files** (all in `COS-Gemini-CLI/`): `GEMINI.md`, `config.yaml`, `voice.md`, `logbook/`, `triggers/`, `commands/`. Setup guide: [`COS-Gemini-CLI/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Gemini-CLI/README.md).

**Microsoft Copilot, browser.** **Files** (all in `COS-Copilot-Web/`): [`YOUR-INFO.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/YOUR-INFO.md), [`custom-instructions.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/custom-instructions.md), [`knowledge-voice.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/knowledge-voice.md), [`knowledge-briefings.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/knowledge-briefings.md), [`knowledge-logbook.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/knowledge-logbook.md). Setup guide: [`COS-Copilot-Web/README.md`](https://raw.githubusercontent.com/siddsdixit/personal-cos-teach/main/COS-Copilot-Web/README.md). First ask: work/school account (Agent Builder, Path A) or personal account (Path B)?

### Other assistants (Perplexity, etc.)

Use the closest browser folder (any of the three). The pattern is the same: put `custom-instructions.md` where the tool takes standing instructions, upload or paste the other files as reference, and turn on memory if it exists. Say which parts the tool cannot do (for example no persistent memory) and use `knowledge-logbook.md` instead.

## The five requests it understands

| Say | You get |
|---|---|
| "morning briefing" | Priorities, calendar conflicts, email triage, drafts, and what needs your judgment |
| "pulse check" | Next meeting and anything new and urgent |
| "EOD" | What happened, what you dropped, top 3 for tomorrow |
| "urgent check" | A late-day sweep, quiet by default |
| "week ahead" | A preview of the coming week |

Tracking promises: "Remember that I promised the pricing recap to Maya by Friday." Later: "What do I still owe people?"

## What this is not

- Not autonomous: it drafts and asks, it does not send.
- Not tied to any company's tools: swap Gmail, Calendar and Slack for what you use.
- Not magic: if you leave `YOUR-INFO.md` blank, it has nothing to prioritize by and no voice to match.

## License

MIT, see [`LICENSE`](LICENSE). Built by [Siddharth Dixit](https://github.com/siddsdixit).
