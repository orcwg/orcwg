# Agent instructions: agendas and minutes

How an AI agent helps SIG, task force (TF), and committee facilitators manage meeting agendas and minutes in this repository. The facilitator stays in charge: the agent drafts, the facilitator reviews, sends, and merges.

The rules themselves live elsewhere. Read them before you start, and don't restate them in the files you write:

- [`working-mode.md`](working-mode.md#meetings): what meetings and minutes must do, and the meeting notes lifecycle (`🗓️ Proposed agenda` → `📝 Draft` → `✅ Approved`).
- [`document-metadata.md`](document-metadata.md#minutes): frontmatter fields, file naming, and where minutes live.
- [`templates/meeting-notes.md`](templates/meeting-notes.md): the generic structure.
- [`MEETINGS.md`](MEETINGS.md): each group's cadence, time, conf-call link, and minutes folder.

## What the facilitator can ask for

| Request | What you produce |
| --- | --- |
| "Agenda for the next call: …" | A new agenda file ([Draft the next agenda](#draft-the-next-agenda)) |
| "Announce the next call" | An email draft ([Call announcement](#call-announcement-email)) |
| "Notes doc for the call" | Markdown to paste into Google Docs ([Live notes skeleton](#live-notes-skeleton)) |
| "Here are the notes from the call" | Draft minutes ([Turn notes into minutes](#turn-notes-into-minutes)) |
| "Announce the minutes" | An email draft ([Minutes announcement](#minutes-announcement-email)) |

Emails and the notes skeleton are text for the facilitator to copy: give them in your reply, in a fenced block, and don't commit them. You never send email.

## Conventions

- **Follow the group, not the generic template.** Groups differ in file names, section headings ("Participants" or "Attendees", "Minutes" or "Notes"), and agenda table layout. Copy the group's own `yyyy-mm-dd-mom-*.md` template if its `minutes/` folder has one, and match the group's most recent minutes file. Use `templates/meeting-notes.md` only when the group has neither.
- **Link with absolute URLs** (`https://github.com/orcwg/orcwg/blob/main/…`) to other minutes, so the links work from email, calendar invites, and Google Docs.
- **Participants** are written `Name (Affiliation)`, one per line, in the order given. Leave the affiliation out when none was given; don't guess one.
- **Don't invent.** Record only what the facilitator's notes say. When an agenda topic has no notes, or the notes point to something you don't have ("see links"), ask, or leave it out and say so in your reply. Look links up at their source and check they resolve before adding them.
- **Tidy, don't rewrite.** Fix typos and grammar and turn fragments into sentences. Keep the substance and the level of detail. Don't attribute comments to individuals; naming who presented a topic or owns an action item is fine.
- **Numbers you add** (issues closed, PRs merged, and the like) come from the tracker, not from the call. Say in your reply where each one comes from and how it was counted, so the facilitator can check it.
- **Tell the facilitator what you assumed**: the date of the next call, time slots, moderators, any line that isn't in their notes.

## Draft the next agenda

1. Work out the date from the group's cadence in `MEETINGS.md` and the date of the last call. Say which date you picked; calls get skipped or moved.
2. Create `YYYY-MM-DD-mom-[group].md` in the group's `minutes/` folder with `Status: 🗓️ Proposed agenda`.
3. Fill the agenda table with:
   - the group's standing items (for example: welcome and approve agenda, approve minutes, pending action items, AOB);
   - an "Approve minutes" item linking to every minutes file of the group still in `📝 Draft`;
   - topics the previous minutes say were carried over;
   - the topics the facilitator gave you, in their order and in their words.
4. Copy the unchecked action items of the previous minutes under "Pending action items". Write "None" when there are none.
5. Spread the time slots over the length of the call and name the facilitator as moderator unless told otherwise.

## Turn notes into minutes

The facilitator pastes or attaches the notes taken during the call, usually a Google Docs export with attendees, notes, and action items.

1. Edit the agenda file of that call: set `Status: 📝 Draft`, and keep the agenda table as it was.
2. Add the participants.
3. Write the minutes under one heading per agenda topic, in agenda order, reusing the agenda wording. Put topics raised outside the agenda under "AOB".
4. For an agenda topic that wasn't addressed, write "Not addressed. Carried over to next call." and add the topic to the next agenda. Confirm with the facilitator first if the notes don't say what happened.
5. List the action items with their owner (`- [ ] Owner to do something.`). Write "None recorded." when there are none. Commitments made in the notes ("X hopes to ship this week") are action items: propose them.
6. Tick the pending action items the notes report as done.
7. If the notes record that earlier minutes were approved, set those files to `Status: ✅ Approved` and add `Approved: YYYY-MM-DD` with the date of the call that approved them.
8. Create or update the next agenda so that it holds the carried-over topics and open action items ([Draft the next agenda](#draft-the-next-agenda)).

Put the minutes, the approvals, and the next agenda in one pull request titled `[Group]: YYYY-MM-DD minutes and YYYY-MM-DD agenda`. Open it when the facilitator asks. Minutes are merged as drafts; they are approved at the next call.

## Call announcement email

Draft it once the agenda is on `main` (or in an open pull request, if the facilitator wants to announce early). Take the time, time zones, and conf-call link from `MEETINGS.md`, and the topics from the agenda table, leaving out the standing items. Plain text, full URLs, no Markdown: it goes to a mailing list.

```text
Subject: [Group] call on [Weekday D Month YYYY], [time] CET

Hi all,

The next [Group] call is on [Weekday D Month YYYY] at [time] CET ([other time zones from MEETINGS.md]).

On the agenda:

- [Topic]
- [Topic]

Full agenda: [URL of the agenda file on main]
Join the call: [conf-call URL]

To add a topic, reply to this email or open a pull request against the agenda.

[Facilitator's first name]
```

## Live notes skeleton

Markdown the facilitator copies and pastes into the meeting's Google Doc with Edit → Paste from Markdown (turn it on under Tools → Preferences → Enable Markdown). Use one heading per agenda topic so that the notes come back already organised; write the headings without links or time slots. Prefill the pending action items, and the participants if the facilitator names them.

```markdown
## [Mon D, YYYY] | [Group]

Agenda: [URL of the agenda file on main]

### Attendees

* Name (Affiliation)

### Welcome & approve agenda

*

### Approve minutes

*

### Pending action items

* [ ] [Action item carried over from the last call]

### [Topic]

*

### AOB

*

### Action items

* [ ] Owner to do something.
```

## Minutes announcement email

Draft it once the pull request with the draft minutes is merged, not before: the link must point to the file on `main`. Summarise the call in a few bullets taken from the minutes, list the action items with their owners, and give the date of the call at which the minutes will be approved. Plain text, full URLs.

```text
Subject: [Group] minutes of [D Month YYYY] (draft)

Hi all,

The draft minutes of the [Group] call of [D Month YYYY] are published:
[URL of the minutes file on main]

In short:

- [Outcome]
- [Outcome]

Action items:

- [Owner] to [do something]

Corrections are welcome: reply to this email or open a pull request. The minutes will be proposed for approval at the next call, on [D Month YYYY].

[Facilitator's first name]
```
