# Chief of Staff Logbook

Optional: attach this as a agent file if you want a durable,
readable log to seed memory from, or to reference alongside memory.

**Important limitation:** Copilot agents can't write back to their own
attached files. This file is a snapshot, not a live database. The real
day-to-day tracking should happen through memory (see
`custom-instructions.md` → "Logbook — Tracking Commitments"). Periodically
re-export your memory into an updated version of this file if you want a
backup outside of memory.

This starter file is empty — below is the format your entries should
follow once you start using memory and want to snapshot it here.

## Active — Committed

_None yet. Example format:_
```
[ID]: [what you promised]
To: [who]
Created: [date] · Due: [date] · Status: open
Context: [1-2 lines of background]
Source: [email/Teams/meeting]
```

## Active — Delegated

_None yet. Example format:_
```
[ID]: [what you asked someone to do]
To: [who]
Assigned: [date] · Due: [date] · Status: open
Source: [email/Teams/meeting]
```

## Active — Decisions

_None yet. Example format:_
```
[ID]: [what was decided]
Date: [date] · Who: [names]
Context: [why this decision was made]
Source: [email/Teams/meeting]
```

## Active — Follow-ups

_None yet. Example format:_
```
[ID]: [what needs a follow-up]
Owner: [you, or whoever owns it]
Created: [date] · Status: open
Source: [where this came from]
```

## Archived — Completed

_None yet. When you mark something done, move it here with a completed
date and a one-line resolution:_
```
[ID]: [what it was]
Assigned/Created: [date] · Completed: [date]
Type: delegated / committed / decision / followup
Resolution: [how it was resolved, or why it was closed]
```
