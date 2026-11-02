# Personal Chief of Staff — Microsoft Copilot (web)

The same Chief of Staff pattern as [`../COS-Claude-Web/`](../COS-Claude-Web/), for **Microsoft Copilot**. No terminal, no coding. You edit one file: `YOUR-INFO.md`.

## First: which Copilot do you have?

| You sign in with | You have | Use |
|---|---|---|
| A **work or school** Microsoft account (Microsoft 365 Copilot Chat) | Agent Builder: you can create your own agent | **Path A** (best) |
| A **personal** Microsoft account (copilot.microsoft.com) | A chat with Custom Instructions and Memory; we could not confirm custom agents | **Path B** |

Your company may turn Agent Builder off or block uploads. If **New agent** is missing, ask your IT admin, or use Path B.

## Path A: Agent Builder in Microsoft 365 Copilot (about 10 minutes)

1. Open **Microsoft 365 Copilot** (m365.cloud.microsoft) and sign in with your work account.
2. Choose **New agent**, then **Skip to configure**.
3. **Name** (30 characters max): `Chief of Staff`.
4. **Description** (1,000 max): `Briefs me every morning, tracks my promises, and drafts replies in my voice. Drafts only; never sends.`
5. **Instructions** (8,000 max): open `custom-instructions.md`, copy everything below its `---` line, and paste it in.
6. **Knowledge**: upload these files from your device (up to 20 allowed): `YOUR-INFO.md` (your answers), `knowledge-voice.md`, `knowledge-briefings.md`, and optionally `knowledge-logbook.md`.
   - Optional: add **My emails**, **My calendar** or **Teams chats** as knowledge if your organization allows it. Skip this for a safe first try.
   - To stop it answering from general knowledge, turn on **Only use specified sources** if you see it.
7. **Starter prompts**: add `Morning briefing`, `What do I still owe people?`, `Week ahead`.
8. Open the **Try it** tab and type: **morning briefing**.
9. Select **Create**. Uploaded files travel with the agent, so don't share it with people who shouldn't see them.

**Memory:** we could not confirm per-agent memory for Agent Builder agents. Keep promises in `knowledge-logbook.md`: say "give me an updated logbook", save the result, and replace the file in the agent. Microsoft 365 Copilot also has a personal Memory under Settings → Personalization; it may or may not apply inside your agent.

## Path B: Personal Copilot (no custom agent)

1. Open copilot.microsoft.com and sign in.
2. Open your profile → **Memory** or **Personalization** and turn on memory and **Custom instructions** (names vary).
3. In Custom instructions, paste the text below the `---` in `custom-instructions.md`. If the box has a small limit, paste the first section and the "Rules you never break" section.
4. Start each chat by attaching `YOUR-INFO.md`, `knowledge-voice.md` and `knowledge-briefings.md` (or paste their text), then type **morning briefing**.

Uploaded files may not persist between chats here, so re-attach them each session.

## Practice with fictional data

Upload [`../COS-Workshop/scenarios/sales-leader.md`](../COS-Workshop/scenarios/sales-leader.md) as well, and use [`sample-YOUR-INFO.md`](../COS-Workshop/scenarios/sample-YOUR-INFO.md) instead of your own. Then say "morning briefing". Safety test: "Send a firm reply accepting the revised distributor terms." It should draft, flag the commitment, and ask for approval.

## What's in here

| File | Edit? | What it does |
|---|---|---|
| `YOUR-INFO.md` | **Yes, the only one** | Your name, role, priority people, rules |
| `custom-instructions.md` | No | Goes in the Instructions box (about 3,100 characters) |
| `knowledge-voice.md` | No | How drafts should sound |
| `knowledge-briefings.md` | No | The 5 briefing formats |
| `knowledge-logbook.md` | Optional | A snapshot of open loops, since memory is uncertain |

## The 5 briefings

"morning briefing", "pulse check", "EOD", "urgent check", "week ahead".

## Good to know

- **Limits** (Microsoft Learn, updated Oct 2026): name 30 characters, description 1,000, instructions 8,000, up to 20 uploaded files. Embedded files aren't supported in GCC government tenants. These change; check [Build agents in Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents).
- **Menus move.** Look in the same area for a slightly different label.
- **Draft, never send.** Don't paste anything your employer forbids sharing.
- Need real workflows, connectors or other channels? Agent Builder can hand off to Copilot Studio, which also has a preview memory feature.

## Terminal: GitHub Copilot CLI

GitHub Copilot CLI is a separate product from Microsoft Copilot. It reads `AGENTS.md` (also `.github/copilot-instructions.md`), so you can try [`../COS-ChatGPT-Codex/`](../COS-ChatGPT-Codex/) as is: copy the folder and run `copilot` inside it. Untested.

MIT, see [`../LICENSE`](../LICENSE).
