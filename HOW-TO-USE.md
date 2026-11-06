# How to use the forge

## Green: send a command

1. Open `commands/template.md` on GitHub and copy its contents.
2. Choose **Add file → Create new file** in `commands/`.
3. Name it `YYYY-MM-DD-short-name.md`, for example `2026-11-06-plan-game-night.md`.
4. Paste the template. Fill in Title, Date, To, Task, Context, Due, and Done looks like. Keep From as GRE3NZ89 and Status as new.
5. Commit the new file with a short description.
6. Give the selected AI the repository link and command path in its chat. For To: All, name a coordinator or ask one AI to claim it first; the whole crew should not duplicate the same task.

The example under `commands/examples/` is a demonstration, not a live order or an announced event.

## Each AI: read, claim, finish

1. Read README.md, TEAM.md, this guide, the command, and your inbox. Sync the latest files before changing anything.
2. Check the command's latest Status and Activity. If claimed, coordinate with its owner rather than taking over.
3. Append an Activity section with your name and timestamp, then `Status: claimed by [name] — [date/time]`. Commit the claim before starting. Use an explicit offset, such as `2026-11-06T14:00:00-05:00` (America/Toronto).
4. Save results in a new dated file under `work/gfg-discord/` or `work/shared/`. Include Date, From, To, and the originating command link. Separate verified facts, proposals, and unresolved questions.
5. Append a new dated Activity section with `Status: done`, a relative link to the result, and what was checked. The last dated Status is authoritative; preserve earlier status history.
6. If blocked, append `Status: blocked` with the precise missing input and next action. Never claim success without verification.
7. For a milestone, add a copy to `archive/` using a new dated name and link it from the command. Keep the original result and command in place. Lux curates the record and links it in the archive index.

Only append your own sections to existing commands. Correct your own mistakes with a clearly dated correction. Do not overwrite someone else's file or rewrite their sections.

## Message another AI

Create `inbox/<recipient>/YYYY-MM-DD-from-<sender>-subject.md`:

```markdown
# Short subject
Date: YYYY-MM-DD
To: Lux
From: Cinder
About: Relative link to command or work file

## Message
Question, evidence, or handoff, with the next action clearly stated.
```

The recipient replies in `outbox/<original-sender>/YYYY-MM-DD-from-<responder>-subject.md`, with the same fields and a link to the original message. Example: Cinder writes to Lux's inbox; Lux replies in `outbox/cinder/`. Outbox folders are named for the person receiving the reply, not its author. Check your inbox and your outbox folder when prompted to review messages. Use a unique subject suffix if a name already exists.

## Connect each AI

AI names are roles, not GitHub accounts. Do not invite invented AI usernames or share credentials in chat.

- **GitHub connector:** Green authorizes the app for this private repository through its normal settings. Confirm that it can read the repo and whether it supports writing; some connectors are read-only or cannot see newly created repos until granted access.
- **Local Git workspace:** An authorized coding session can clone the private repo using Green's normal Git authentication, read the docs, pull before work, commit changes, and push. Do not put tokens in clone URLs. For concurrent work use separate branches and pull requests; resolve overlapping claims before doing the task. Never force-push shared history.
- **GitHub website:** Green can create, edit, and commit files directly while signed in. Human collaborators need their own GitHub accounts and explicit access from Green.
- **Manual relay:** If Lux, Cinder, Scraps, or Nash cannot access GitHub, Green pastes the relevant command and context into that AI's chat, then commits its response. Label it `Relayed by: GRE3NZ89`; preserve the actual author and date. The AI must not claim it read or wrote GitHub directly.

This initial repo contains no bots, API integrations, background polling, or scheduled agents. A commit alone does not notify or start an AI. Green prompts each session or relays files. Keep the workflow free; any future automation needs a separate design and authorization.

## Keep the forge safe

Keep the repo private. Review every diff before committing. `.gitignore` is a convenience, not a secret scanner; it cannot recognize secrets inside otherwise allowed Markdown or erase tracked content. Never paste private member records, passwords, tokens, machine-specific absolute paths, or personal files. If a credential is accidentally committed, revoke it immediately and arrange history cleanup; deleting the latest file alone is insufficient.
