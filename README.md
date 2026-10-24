# BA-OS — Business Analysis Operating System (V1)

BA-OS helps you take a client request from "I have a brief" to an approved, scoped and estimated product, without losing the reasoning in between. Every project lives in one folder. AI drafts and checks; **you** decide, and every decision is written down.

V1 is the manual core: the method, templates, one items register and six commands. AI helpers, research and estimation commands come in V2 and V3.

---

## 1. First-time setup (Windows, about 10 minutes)

### Step 1 — Unzip into your Documents folder

Open a PowerShell window (or a terminal in Cursor) and paste this line. It assumes the zip is in your Downloads folder:

```powershell
Expand-Archive -Path "$HOME\Downloads\BA-OS-v1.zip" -DestinationPath "$HOME\Documents"
```

You should now have `Documents\BA-OS\CLAUDE.md`. (If you see `Documents\BA-OS\BA-OS\…`, move the inner folder up one level.)

### Step 2 — Open the folder in Cursor

In Cursor: **File → Open Folder…** → choose `Documents\BA-OS`.

### Step 3 — Turn on history (Git), once

Open a terminal in Cursor (**Terminal → New Terminal**) and paste these lines one at a time.

If you have never used Git on this computer, first tell Git your name and email (use your own):

```powershell
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Then save the first snapshot of BA-OS:

```powershell
git init -b main
git add -A
git commit -m "BA-OS V1"
```

A warning like *"LF will be replaced by CRLF"* is harmless.

### Step 4 — Start Claude Code

In the same terminal:

```powershell
claude
```

The first time, Claude Code asks whether you trust this folder. Choose **Yes** — the `/ba-` commands only load in a trusted folder.

Type `/ba` and you should see the six commands appear. You are ready.

---

## 2. The six commands

Type these **inside Claude Code** (after running `claude`), not in plain PowerShell.

| Command | What it does | Example |
| --- | --- | --- |
| `/ba-start <name>` | Creates a new project, saves the client input, drafts the profile (size and depth) | `/ba-start hotel booking` |
| `/ba-extract` | Reads new files in `inputs/` and adds items (requirements, questions, assumptions…) as drafts with sources | `/ba-extract` |
| `/ba-check` | Critic review + gate readiness. Writes a report to `checks/` | `/ba-check` |
| `/ba-approve …` | Records your decision: review, confirm, approve, reject, answer a question, pass a gate | `/ba-approve REQ-003 REQ-004 reviewed` |
| `/ba-status` | Rebuilds `control.md` and tells you the next action | `/ba-status` |
| `/ba-learn` | Turns a project (or a project done outside BA-OS) into lessons in `knowledge/lessons.md` and proposes improvements to BA-OS. Works at any gate | `/ba-learn` |

More `/ba-approve` examples:

```
/ba-approve Q-002 confirmed "Three branches: Mirpur, Uttara, Dhanmondi"
/ba-approve REQ-009 rejected "Client dropped online payments"
/ba-approve profile
/ba-approve section 03-define "Problem statement" reviewed
/ba-approve gate 1 pass "Worth doing; owner is the decision maker"
/ba-approve lesson L-001 L-002 approved
```

You can also just talk to Claude Code normally, for example: *"Draft the stakeholders section of 02-discover"* or *"Research what competitors in this market offer"*. It follows the house rules in `CLAUDE.md`.

---

## 3. Try it once (15 minutes, with a made-up clinic)

1. In Claude Code: `/ba-start smile point dental`
2. Choose privacy `internal`. When asked for the input, say the files are ready.
3. Copy `samples\sample-brief.md` and `samples\sample-call-notes.md` into the new project's `inputs\` folder (Claude will show you the path). Tell Claude "done".
4. Open `profile.md`, read the suggested size and depth, then run `/ba-approve profile`.
5. Run `/ba-extract`. Open `items.md` and look at the drafts.
6. Run `/ba-check`. Open the report in `checks\`.
7. Run `/ba-status` to see the next action.

The samples hide a few problems on purpose (a wrong branch count, a disagreement about choosing a dentist, a vague "staff" role, "we need an app"). See whether BA-OS finds them.

---

## 4. A normal working day on a project

```
New client files → put them in inputs\ → /ba-extract
Look at the new drafts → /ba-check → fix or answer the findings
Accept what is good → /ba-approve <IDs> reviewed
Send open questions to the client → record answers with /ba-approve Q-… confirmed "…"
Work on the stage file for the current phase (ask Claude to draft sections)
When the phase feels done → /ba-check gate → /ba-approve gate <n> <result>
Project finished, paused or lost? → /ba-learn → /ba-approve lesson <IDs> approved
Lost? → /ba-status
```

**Making BA-OS smarter after every project:** run `/ba-learn`. It drafts lessons (wrong assumptions, questions asked too late, problems that kept coming back) and proposes exact changes to the checklists, templates and commands. You choose which changes to apply, then approve the lessons. The next `/ba-start` and `/ba-check` use them automatically.

**Seeing exactly what the AI changed:** click the **Source Control** icon in Cursor's left sidebar (or press `Ctrl+Shift+G`). Every changed line is highlighted. `/ba-approve` saves a history snapshot each time you record a decision.

---

## 5. What is in this folder

| Folder / file | What it is | Do you edit it? |
| --- | --- | --- |
| `CLAUDE.md` | House rules Claude reads every session | Yes, to change rules for all projects |
| `method/` | The BA method: phases, gates, labels, requirement standard, depth by size, glossary | Yes, to improve the method |
| `templates/` | Blank project files | Yes, to change what new projects start with |
| `knowledge/` | Lessons and checklists that improve over time | Yes, after each project (`/ba-learn` drafts the changes) |
| `projects/` | Your projects (`_confidential/` is never backed up online) | Through the commands, and by hand |
| `.claude/skills/` | The six commands, one folder each | Yes, to change how a command works |
| `.claude/settings.json` | What Claude may do without asking (it can never push online or delete files) | Rarely |
| `samples/` | Made-up inputs to practise with | No |

---

## 6. Changing how BA-OS works

Everything is plain text. Change a file, save it, and the change applies the next time the command runs.

| You want to change | Edit this |
| --- | --- |
| How a command works | `.claude/skills/<command>/SKILL.md` |
| Rules for every project | `CLAUDE.md` or a file in `method/` |
| Behaviour for one project | That project's `profile.md` (Domain notes, Extra checks) |
| Questions BA-OS always checks | `knowledge/patterns/common-gaps.md` |
| Questions for one industry | a file in `knowledge/patterns/` (for example `hospitality.md`) |
| Lessons from a finished project | run `/ba-learn` |
| What a new project starts with | `templates/` (the client-facing proposal is `templates/exports/rfp-response.md`) |

Easiest way: ask Claude Code, for example *"Change /ba-extract so every REQ also gets a user role"*. Review the change in Source Control before keeping it. Git lets you undo any change.

---

## 7. Optional: private backup on GitHub

1. On github.com, create a new **private** repository named `ba-os` (do not add a README).
2. In the Cursor terminal (outside Claude Code), paste, replacing `<your-username>`:

```powershell
git remote add origin https://github.com/<your-username>/ba-os.git
git push -u origin main
```

After that, run `git push` whenever you want to back up. Claude Code is not allowed to push — only you can. Projects in `projects\_confidential\` are never uploaded.

---

## 8. If something goes wrong

| Problem | Fix |
| --- | --- |
| `/ba-` commands do not appear | Make sure Cursor opened the `BA-OS` folder itself, then type `/exit` and run `claude` again |
| Claude cannot read a Word file | Save it as PDF, or paste the text into a `.md` file in `inputs\` |
| An AI change looks wrong | Discard it in Source Control, or ask Claude to undo it |
| A long session feels confused | Type `/exit`, run `claude` again, then `/ba-status`. The project folder is the memory, not the chat |
| Not sure what to do next | `/ba-status` |
