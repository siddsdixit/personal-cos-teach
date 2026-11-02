# Chief of Staff — Briefing Formats

Upload this file as agent knowledge (see the README for the exact clicks). It contains 5 briefing formats matching your real
daily cadence. Say the trigger phrase for whichever one you want, and
follow that section's instructions.


**No connected tools?** Run every briefing from the files and text I attached (for example a scenario file). Say so in one line, then deliver. Never invent items.

| Say this | Runs |
|---|---|
| "morning briefing" / "morning brief" | Morning Briefing |
| "pulse" / "pulse check" / "what's next" | Pulse Check |
| "EOD" / "end of day" / "recap today" | End-of-Day Summary |
| "urgent check" / "anything urgent" | Evening Urgent Check |
| "week ahead" / "weekly preview" | Weekly Preview |

---

## Morning Briefing

Runs once in the morning (typically ~7am PT) to set up the day.

Pull the user's config context (priority senders, executive domains,
priority Teams channels, org context) from this agent's instructions if not already in context.

**Step 1: Calendar Today**

Get today's events on the primary calendar. Present as a table:

```
| Time | Meeting | Key Attendees |
|---|---|---|
```

Flag meetings that need prep with a note next to them:
- External attendees (outside your company domain)
- Board/parent-company attendees
- 1:1s with C-suite peers or the user's manager
- Large meetings (5+ attendees)
- Any meeting where the user is the presenter/trainer, not just an attendee

Note any gaps of 2+ hours as potential focus time. If the day has no such
gap, say so explicitly ("No focus time today — fully packed").

If two meetings conflict or overlap, flag it directly and suggest who to
ask to resolve it (an EA, or whichever meeting looks lower priority).

**Step 2: Email Triage**

Search unread messages from the last 12 hours, max 50 results.

For each email from a priority sender:
- Read the full message
- Categorize: **URGENT** / **NEEDS-RESPONSE** / **FYI** / **DELEGATE**
  - URGENT: from executive senders/domains, or contains escalation
    keywords (deadline today, "ASAP", budget overage, contractual/legal,
    payroll-blocking)
  - NEEDS-RESPONSE: from a priority sender, requires a reply, not
    time-critical
  - FYI: informational, no action needed
  - DELEGATE: could be handled by someone else on the team
- For URGENT and NEEDS-RESPONSE: draft a reply in the correct tone
  (executive/team/external per config)

Present as a table:
```
| From | Subject | Category | Summary |
|---|---|---|---|
```

Note how many drafts were created.

**Step 3: Teams Highlights**

For each priority channel: read recent messages (last 12 hours), skip bot
messages and reminders. Also check for DMs and @mentions.

Summarize only channels/DMs with meaningful activity:
```
- **#channel-name**: [1-line summary]
- **DM from [person]**: [1-line summary]
```

**Step 4: Pending Approvals**

If a finance/approval tool is connected, pull pending items. Flag anything
over the configured alert threshold. Note auto-approvable items under the
configured auto-approve threshold.

If the finance tool needs re-authentication or isn't connected, say so
plainly: "Approvals unavailable — [tool] needs re-authorization" rather
than silently skipping it.

**Step 5: Anything Else Worth Flagging**

Scan for anything that doesn't fit cleanly into email/Teams/calendar but
matters: overdue action item reminders, people out of office who are
relevant to today's meetings, upcoming deadlines mentioned in passing.

**Step 6: Top 5 Actions**

Compile a ranked list:
```
Top 5 Actions for Today:
1. [Most urgent: what + why + deadline]
2. [Second]
3. [Third]
4. [Fourth]
5. [Fifth]
```

Order: board/executive items first, then anything with a hard deadline
today, then peer requests, then direct-report items.

**Output format:** calendar, email triage, Teams highlights, approvals,
anything-else flags, top 5 actions, in that order. Keep it scannable — the
user has 30 seconds, not 5 minutes. Bold anything that needs a decision.
Never use em dashes. If a section has nothing notable, write one line
("All clear") and move on rather than an empty section.

---

## Pulse Check

Runs multiple times during the day (roughly hourly, or whenever asked) to
keep the user current between the morning briefing and the end-of-day
summary. Fast and tight, not a full re-scan.

**Step 1: Upcoming Meeting (next ~60 minutes)**

Check the calendar for anything starting soon. If there's a meeting:

```
Upcoming in ~[X] min: [Meeting name] ([time range])
Attendees: [key attendees, note anyone external or notable]
Context: [1-2 lines pulled from recent email/Teams relevant to this meeting]
Agenda: [from event description, or "none listed"]
```

If nothing is coming up in the next hour, say so and move on ("No
meetings in the next hour").

If a meeting is already in progress, note that instead:
```
In progress: [Meeting name] ([time range], [location if in-person])
Agenda: [known agenda items with times if available]
Attendees: [key attendees]
```

**Step 2: New Drafts**

Since the last check-in, scan for new unread priority email and relevant
Teams activity (last 1-2 hours is usually right — adjust based on how
long it's been since the last pulse).

For anything URGENT or NEEDS-RESPONSE, draft a reply (email or Teams,
matching wherever the original came in) and list it:

```
Drafts created: [count] email, [count] Teams

URGENT | [Email/Teams] | [Subject/topic] | Draft: [one-line summary]
NEEDS-RESPONSE | [Email/Teams] | [Subject/topic] | Draft: [one-line summary]
```

If there's a genuinely time-sensitive item (a deadline in the next hour or
two, an escalation, someone waiting on a reply), call it out ahead of the
drafts list with an explicit flag:

```
URGENT: [what] — [who is waiting] — [deadline/window]
[1-2 lines of context]
Action needed: [what the user specifically needs to do, and by when]
```

**Step 3: Teams Pulse**

Scan priority channels and DMs for anything from the last 1-2 hours that's
worth surfacing but doesn't need a draft:

```
Teams pulse:
[Person/channel]: [1-line summary]
[Person/channel]: [1-line summary]
```

Skip this section entirely if there's nothing notable rather than forcing
an entry.

**Step 4: Pending, No Draft Needed**

Items that need the user's own attention (signatures, approvals,
decisions only they can make), listed separately without a draft:

```
Pending (no draft):
[Item]: [what's needed] (from [person])
```

**Step 5: Skipped**

```
Skipped: [count] items (newsletters, bot reminders, no action needed)
```

**Output format:** keep it tight — this is a pulse check, not a full
briefing. Omit any section with nothing to report. If literally
everything is quiet: "All clear. No meetings in the next hour, no drafts
needed, Teams quiet." Never use em dashes. Draft, never send, without
explicit instruction otherwise.

---

## End-of-Day Summary

Runs in the early evening (typically 5-7pm PT) to close out the day and
set up tomorrow. A recap plus a forward look, not a full re-triage.

**Step 1: What Happened Today**

Email (priority senders): for each priority sender who emailed today,
note what they needed and whether a reply was sent. Be specific about
deadlines mentioned and whether they were met.

```
[Sender] ([topic], [time if known]): [what they asked/said]. [Reply sent / No reply sent].
```

Teams: summarize activity in priority channels and any DMs — what
happened, what's still active, anything unresolved.

**Step 2: Dropped Balls**

Cross-reference what came in today against what got a reply or a draft.
Anything from a priority sender still sitting unanswered goes here,
regardless of earlier categorization:

```
| From | What they asked | Deadline |
|---|---|---|
```

Be honest about this section — its entire value is surfacing things that
slipped, not making the day look clean.

**Step 3: Tomorrow's Calendar**

```
| Time (PT) | Meeting | Flag |
|---|---|---|
```

In the Flag column, call out: meetings where the user is
presenting/training, external meetings, anything needing prep tonight
(say what, specifically), and any conflicts/overlaps.

**Step 4: Approvals**

If a finance/approval tool is connected, check for pending items. If it
needs re-authentication or isn't connected, say so plainly.

**Step 5: Top 3 for Tomorrow**

```
Top 3 for Tomorrow:
1. [Most urgent/time-critical, tied to a real deadline if possible]
2. [Second]
3. [Third]
```

These should mostly come from Step 2 (dropped balls) and Step 3 (what
needs prep tonight) — the "if you only do 3 things" distillation, not a
new list.

**Output format:** keep it tight — a recap, not a novel. Bold anything
that needs a decision. Never use em dashes. If everything today was
clean: still show tomorrow's calendar and top 3, but note "No dropped
balls today" in Step 2.

---

## Evening Urgent Check

Runs late in the day (typically ~9pm PT) as a final sweep. The bar for
inclusion is high — this is not another full triage, it's specifically
looking for things that would be a real problem if left until morning.

**Step 1: Unanswered Critical Emails**

Check for unread or unreplied emails from today from executive
senders/domains (the user's manager, board/parent company contacts) and
C-suite peers.

Verify by checking sent mail for a reply with a matching subject/thread —
don't assume something is unanswered just because it's unread.

For anything genuinely unanswered: draft a reply in executive tone.

**Step 2: Unresolved Teams Escalations**

Search for messages from today where the user was directly mentioned or
asked for input and hasn't replied, or a priority channel contains
escalation keywords (outage, blocker, urgent, escalation) not already
being handled by someone else. Only include items where the user
specifically needs to act.

**Step 3: Overdue Approvals**

If a finance/approval tool is connected, check for anything pending more
than 2 business days, or anything over the configured alert threshold. If
the tool needs re-authentication, note it plainly.

**Step 4: Output**

If there are genuinely urgent items:
```
[count] items need attention:

1. [Item: who, what, why it's urgent]
   Action: [drafted reply / needs your input / approve in finance tool]

2. [Item]
   Action: [...]

Drafts created: [count] (check email/Teams drafts)
```

If nothing meets the bar:
```
All clear. Nothing urgent pending. Have a good evening.
```

**Rules:** high bar for "urgent" — if it can reasonably wait until
morning, leave it out. Max 5 items; if more, show top 5 and note "[N]
more items can wait until morning." Keep it short. Never use em dashes.
Draft, never send.

---

## Weekly Preview

Runs once a week (typically Sunday evening) to help the user walk into
Monday prepared.

**Step 1: Calendar Overview**

Get events for the upcoming work week (Monday through Friday, or the
user's actual work week).

```
Week of [date range]

Monday:
- [time] [meeting] (with [key attendees])
- Focus time: [gaps of 2+ hours, or "none"]

Tuesday:
...
```

Count total meetings and meeting hours for the week. Identify the
heaviest and lightest days by meeting load.

**Step 2: Meetings Needing Prep**

Flag meetings that need advance preparation: external or board/parent-
company attendees, quarterly reviews/planning sessions/all-hands,
first-time meetings with new people, large meetings (5+ attendees),
anywhere the user is presenting or training. Note what prep is needed in
one line for each.

**Step 3: Rollover from Last Week**

Check email for unanswered priority messages from the past week still
open. If a finance/approval tool is connected, check for anything still
pending from last week.

**Step 4: Output**

```
Week Ahead: [date range]

Summary: [X] meetings, [Y] hours. Heaviest day: [day]. Lightest: [day].

[Day-by-day calendar as above]

Prep needed:
- [Meeting]: [what to prep]
- [Meeting]: [what to prep]

Carried over from last week:
- [X] unanswered priority emails
- [X] pending approvals

Suggested focus blocks:
- [Day, time range]: [suggested use]
```

**Rules:** keep each day to 5 lines max — only notable meetings, not every
30-min sync. Focus blocks are suggestions based on real gaps in the
calendar, not guarantees. Never use em dashes.
