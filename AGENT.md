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
| "Here are the notes from the call" | Draft minutes, and the agenda file for the next call ([Turn notes into minutes](#turn-notes-into-minutes)) |
| "Email to share the minutes with the list" | An email draft ([Email to share the minutes](#email-to-share-the-minutes)) |
| "Add to the agenda of the next call: …" | Topics added to the next agenda ([Draft the next agenda](#draft-the-next-agenda)) |
| "Announce the next call" | An email draft ([Call announcement](#call-announcement-email)) |
| "Notes doc for the call" | Markdown to paste into Google Docs ([Live notes skeleton](#live-notes-skeleton)) |

Emails and the notes skeleton are text for the facilitator to copy: give them in your reply, in a fenced block, and don't commit them.

If the facilitator has an email tool connected (a plugin, connector, or the like), you can also save the email as a draft in their mailbox. Create a draft only: you never send email, even when asked to, and you say in your reply that the draft is waiting for them to review and send.

Address the draft to the group's mailing list. Find it in this repository: the "Get involved" section of [`README.md`](README.md), the group's landing page, and its past minutes. An Eclipse list named `list-name` is written to at `list-name@eclipse.org`. Say which address you used and where you found it; leave the recipient empty if you can't tell which list the group uses.

## Conventions

- **Follow the group, not the generic template.** Groups differ in file names, section headings ("Participants" or "Attendees", "Minutes" or "Notes"), and agenda table layout. Copy the group's own `yyyy-mm-dd-mom-*.md` template if its `minutes/` folder has one, and match the group's most recent minutes file. Use `templates/meeting-notes.md` only when the group has neither.
- **Link with absolute URLs** (`https://github.com/orcwg/orcwg/blob/main/…`) to other minutes, so the links work from email, calendar invites, and Google Docs.
- **No links in headings.** When an agenda topic carries a link, keep the heading to the topic's name and put the link in the first bullet under it:

  ```markdown
  ### AI section in the FAQ

  - Pull request: [cra-hub PR #353](https://github.com/orcwg/cra-hub/pull/353)
  ```

- **Participants** are written `Name (Affiliation)`, one per line, in the order given. Leave the affiliation out when none was given; don't guess one.
- **Don't invent.** Record only what the facilitator's notes say. When an agenda topic has no notes, or the notes point to something you don't have ("see links"), ask, or leave it out and say so in your reply. Look links up at their source and check they resolve before adding them.
- **Tidy, don't rewrite.** Fix typos and grammar and turn fragments into sentences. Keep the substance and the level of detail. Don't attribute comments to individuals; naming who presented a topic or owns an action item is fine.
- **Numbers you add** (issues closed, PRs merged, and the like) come from the tracker, not from the call. Say in your reply where each one comes from and how it was counted, so the facilitator can check it.
- **Tell the facilitator what you assumed**: the date of the next call, time slots, moderators, any line that isn't in their notes.

## Draft the next agenda

The agenda file for the next call is created at the same time as the minutes of the past call are added, in the same pull request ([Turn notes into minutes](#turn-notes-into-minutes)). When the facilitator gives you topics later, add them to that file; create it only if it doesn't exist yet.

1. Work out the date from the group's cadence in `MEETINGS.md` and the date of the last call. Check it against the common holidays that affect North America and the EU (for example Christmas and New Year, Easter Monday, 1 May, Ascension Day, Whit Monday, Thanksgiving in the US and Canada, 4 July, Labor Day, and the August summer break) and flag a clash instead of moving the call yourself. Say which date you picked; calls get skipped or moved.
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
3. Write the minutes under one heading per agenda topic, in agenda order, reusing the agenda wording without its links (see [Conventions](#conventions)). Put topics raised outside the agenda under "AOB".
4. For an agenda topic that wasn't addressed, write "Not addressed. Carried over to next call." and add the topic to the next agenda. Confirm with the facilitator first if the notes don't say what happened.
5. List the action items with their owner (`- [ ] Owner to do something.`). Write "None recorded." when there are none. Commitments made in the notes ("X hopes to ship this week") are action items: propose them.
6. Tick the pending action items the notes report as done.
7. If the notes record that earlier minutes were approved, set those files to `Status: ✅ Approved` and add `Approved: YYYY-MM-DD` with the date of the call that approved them.
8. Create the agenda file for the next call in the same change, holding the standing items, the carried-over topics, and the open action items ([Draft the next agenda](#draft-the-next-agenda)).

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

Markdown the facilitator copies and pastes into the meeting's Google Doc with Edit → Paste from Markdown (turn it on under Tools → Preferences → Enable Markdown). Use one heading per agenda topic so that the notes come back already organised; write the headings without links or time slots. Prefill the pending action items, the facilitator as first attendee if you have their name (leave the placeholder line otherwise), and any other participants the facilitator names.

```markdown
## [Mon D, YYYY] | [Group]

Agenda: [URL of the agenda file on main]

### Attendees

* [Facilitator's name (Affiliation)]
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

## Email to share the minutes

An email that shares the draft minutes with the group's mailing list. Draft it once the pull request with the draft minutes is merged, not before: the link must point to the file on `main`.

Keep it compact: the email points to the minutes, it doesn't repeat them.

- **"In short"**: three or four bullets at most, one short line each, saying what was decided or where things stand. No figures, no sub-points, no explanation of how the work was done: that is what the minutes are for.
- **"Where help is needed"**: only if the call asked the group for something. One line per request, saying what to do and where.
- **"Action items"**: only if there are any, one line each with the owner.
- **Leave out** routine procedure (agenda approved, previous minutes approved, no pending action items) and topics that weren't addressed, unless something notable happened, such as an objection or minutes that weren't approved.
- **Links**: put them inline, as a Markdown link on the relevant word or as the URL in parentheses, and not in a sentence of their own. One link per bullet at most.
- Close with how to send corrections and the date of the call at which the minutes will be approved.

```text
Subject: [Group] minutes of [D Month YYYY] (draft)

Hi all,

The draft minutes of the [Group] call of [D Month YYYY] are published:
[URL of the minutes file on main]

In short:

* [Outcome, with an inline [link](URL) if there is one to follow].
* [Outcome].

Where help is needed:

* [What to do, and where (URL)].

Action items:

* [Owner] to [do something].

Corrections are welcome: reply to this email or open a pull request. The minutes will be proposed for approval at the next call, on [D Month YYYY].

[Facilitator's first name]
```

For example, the "In short" of a call that covered a shipped feature, a long backlog update with statistics, and the next steps reads:

```text
* The guidance shorthand notation is now [integrated](https://github.com/orcwg/cra-hub/blob/main/faq/README.md#auto-linking-to-the-commissions-cra-guidance) in the FAQ.
* Most of the FAQ issue backlog has been triaged.
* Next steps: finish the manufacturer FAQs and improve how the information is organised.
```
