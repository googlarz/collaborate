# collaborate

This started when me and two friends were writing a document together. All three of us using Claude. All three with completely separate conversations, no shared context, constantly asking each other "wait, what did you decide on that section?" — with the most powerful writing tool in the world open in front of each of us and no way to actually work together.

Google Docs didn't solve it. We could all see the same file — but not each other's reasoning, not what Claude told each of us, not why a section changed.

AI has made individual writing dramatically better. A single person with Claude can research, draft, and refine documents that would have taken a team days — in an hour.

But AI assistance is single-player. The context lives in your conversation. The moment the document needs someone else — a co-author, a reviewer, a team of ten writing in parallel — that context disappears. The next person opens a blank session and starts over. They don't know what was decided. They don't know what was tried and dropped. They don't know what you need from them.

So teams are left doing what they've always done: emailing files, leaving comments in shared docs, losing track of who changed what and why. The AI made each person faster. It didn't make the team work any better.

**collaborate** fixes that.

---

## What does it look like?

You pick up the document and Claude briefs you — in plain English, no setup:

```
Hi Mia 👋
Tom just finished his part. Here's where things stand:

He added flight options and a rough daily schedule for Barcelona. He's not sure
about the third day — left a note that you'd have stronger opinions on that one.

What changed since you were last here:
  Flights     — updated (3 options, budget vs. direct tradeoff explained)
  Daily plan  — updated (days 1 and 2 done, day 3 left open for you)

Tom asked you to look at:
  "Mia knows Barcelona better than me — can she fill in day 3 and check
   if the restaurant I picked on day 2 is actually good?"

Ready when you are.
```

Every person gets this when it's their turn. No one has to ask "where are we?" or dig through version history.

Starting a session looks like this:

```
You: Start a new document with my team — it's a trip plan, me and two friends.

Claude: What's the document called?
You: Barcelona Trip — June 2026

Claude: Who's working on it with you?
You: Tom and Mia.

Claude: How do I reach Tom?
You: Signal — +1-555-0101

Claude: How do I reach Mia?
You: Slack — @mia

Claude: What's each person doing?
You: Tom writes the flights and logistics. Mia writes the daily plan.
     I'll review and put it all together at the end.

Claude: Where should I save it?
You: /Users/dawid/iCloud Drive/Shared/Barcelona/

Claude: Done. Tom and Mia can start whenever — I've messaged them both.
```

And when there's reviewer feedback to resolve before handing off:

```
Claude: Mia left feedback on your section:

  #1 The restaurant on day 2 — do you have a backup in case it's fully booked?
  #2 Day 3 feels rushed — she thinks the museum might be too much.

Did you handle #1?
You: Yes — added two backup options near the same area.

Did you handle #2?
You: Agreed, I removed the museum and left the afternoon open.

Claude: All resolved. Passing to Mia now — I'll send her a message.
```

---

## How it works

Each contributor takes a turn. When it's your turn, Claude shows you what changed since you were last involved, any feedback waiting for you, and what the previous person asked you to focus on. You write. When you're done, you hand off — with a brief note on what you did and anything the next person should know.

That's it. Claude handles the rest: snapshots, feedback tracking, notifications, history.

---

## Each person uses their own Claude

Everyone works in their own conversation — your own Claude, your own setup, your own skills and tools. There's no shared session, no special account, nothing to configure together.

collaborate is a skill, not a platform. It gives your Claude the instructions to coordinate with your teammates' Claudes through a shared file. The AI stays yours. The document becomes shared.

---

## Modes

You don't pick a mode — Claude does, based on what you tell it at the start. Two writers with no specific roles? Ping-Pong. A writer and a reviewer? Structured Critique. Multiple sections and a bigger team? Section Ownership. Writing a decision document? Challenger/Defender. Have a draft already and need someone to review it? Annotation Loop. Want everyone to review everyone else's sections? Round Robin.

You can also just say what you want and Claude will figure it out. If you change your mind mid-project, you can switch.

**Ping-Pong** — two writers, back and forth.
The simplest mode. Writer A drafts, Writer B responds, and so on. Good for policies, briefs, proposals where two perspectives sharpen the result.

**Section Ownership** — parallel sections, any team size.
Each person owns one or more sections and writes in parallel. Claude tracks per-section turns, locks, and feedback separately. When every section is done, Claude checks for consistency and merges. Good for strategy reports, team documentation, research papers.

**Structured Critique** — one writer, one reviewer.
The writer drafts. The reviewer gives numbered feedback. The writer resolves each item before the next handoff. Disputes escalate to an approver. Good for anything that needs rigorous editorial review.

**Challenger/Defender** — two positions, one decision.
One person argues for a proposal, the other argues against. Positions are assigned at the start. Each turn must engage directly with what the other person argued. An approver reads both sides and decides. Good for decision memos, build vs. buy, option analysis.

**Annotation Loop** — review an existing draft.
The reviewer goes first, marking the draft with inline comments section by section. Claude helps write specific, actionable feedback. At handoff, comments are compiled into numbered items for the writer to resolve. Good for reviewing documents that already exist.

**Round Robin** — everyone reviews everyone's sections.
After all sections are written, each person reviews every section they didn't write. Claude collects all feedback, groups it by section, and routes it to the right writer — so each person only sees feedback on their own work. Good for team retrospectives, peer feedback, shared decisions where everyone's input matters.

---

## Storage

Two options:

**iCloud** — put the document in a shared iCloud folder. Everyone on the team needs access to the same folder.

**Google Drive** — share a Drive folder with your team. Requires the [Google Drive MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive) server.

---

## Notifications

Turn notifications go out via **Signal** or **Slack**. Signal requires the [signal-mcp](https://github.com/googlarz/signal-mcp) server. Slack requires the [Slack MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) server. You can also use email, or combine backends per person.

---

## Install

Tell Claude:

> *install this skill: https://github.com/googlarz/collaborate/raw/main/SKILL.md*

---

## Use

Just describe what you want — no commands to memorize:

> *"Start a new document with my team"*
> *"It's my turn, I want to work on the strategy report"*
> *"I'm done, pass it to Morgan"*
> *"Go back to the version before Alex's turn"*
> *"Show me where things stand"*
