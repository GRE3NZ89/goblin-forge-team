# SillyTavern two-character setup: neutral structure and test checklist

Date: 2026-11-06
From: Nash
To: GRE3NZ89
Command: [../../commands/2026-11-06-sillytavern-two-character-team.md](../../commands/2026-11-06-sillytavern-two-character-team.md)

No character identities appear here. Everything below is a template to fill once Green names the two characters. Nothing has been installed or changed in Green's live SillyTavern.

## Verified facts

- Green's names for the two characters have not been given. This is the only blocker for character-specific work (from the command).
- Nothing in this document has been tested in SillyTavern yet. Field names below are from Nash's general knowledge of SillyTavern's Character Card V2 format and must be checked against Green's installed version before import.

## Proposal: structure

Two fully separate character cards, `A` and `B` (placeholders), each its own file, so identities can never bleed together.

### Per-character card fields (one card each)

| Field | Plan |
| --- | --- |
| Name | Exactly as Green gives it |
| Description | Appearance, role, core facts. Facts only Green or approved lore supplies |
| Personality | Short trait list |
| Scenario | Default setting; neutral until Green decides |
| First message | One per character, in that character's voice |
| Example dialogue | 2-3 short exchanges showing voice |
| Alternate greetings | Optional |
| Creator notes | Public-safe version/credit notes only |
| System prompt / post-history instructions | Short identity-lock lines, e.g. "stay as this character; never speak for the other" |
| Tags | Simple, public-safe |
| Avatar | Lux's approved portrait, once delivered |

### Lorebook / World Info (optional, decide with Green)

- One **shared** lorebook for shared world facts (places, factions).
- One **per-character** lorebook for private facts, so entries are not triggered for the wrong character.
- Relationship/state entries (how A regards B and vice versa) kept as short, keyword-triggered entries, one for each direction, so each can be edited alone.

### Chat modes

- **Separate chats:** cleanest identity separation; no cross-talk. Best default.
- **Group chat** containing both cards: supports them interacting. Needs the group's reply order and card-merging options chosen, plus a check that each stays in its own voice.
- Recommendation: build both. Test separate chats first, then the group.

### Relationship / state handling

Open question for Green (see below). Options: static relationship in each card's description, or lorebook entries that can be edited as the story moves on.

## Import and test checklist (to run on a copy, not the live setup)

1. Back up Green's existing SillyTavern data folder (Green to do or approve).
2. Import card A alone; confirm name, avatar, greeting display correctly.
3. Import card B alone; same checks.
4. Separate chat with each: five turns; confirm voice stays distinct and neither mentions the other unprompted.
5. Create the group chat; run ten turns; confirm each speaks only as itself and no merged traits.
6. Check lorebook triggers fire for the right character only.
7. Re-export both cards; confirm nothing was lost.
8. Confirm no private data, paths or credentials are in any exported file.
9. Show Green results; install into the live setup only after Green's approval.

## Unresolved questions for Green

1. The two characters' names (blocking).
2. Separate chats, group chat, or both?
3. Is their relationship fixed, or should it evolve in the story?
4. Which SillyTavern version and which model/backend does Green use? (Not private details; version only.)
5. Any existing lore or references to preserve?

## Next steps

- Green names the characters; Nash fills the cards from Green's and Lux's approved material.
- Lux's visual prompt package arrives; Nash integrates it and reports.
