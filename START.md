# START — shared operating contract

This file applies to every AI collaborator in the story project.

## Identify, recover, verify
1. Open `project.json`. Check project ID, title, repository and branch when provided. Never import facts from another story.
2. Read **your own** `roles/<role>.md` and `safestate/<role>.md`, then only the relevant parts of `canon/`, `state/`, `planning/`, and previous approved chapters.
3. Verify the most recent approved chapter and source revision before making changes. If an expected source is unavailable, report the limitation. Do not fabricate read or write success.
4. Respect the configured output language; the instructions are in English, but the story may be written in any language.

## Authority and knowledge
The owner's latest explicit decisions control fundamental rules. Approved foundational canon and approved chapters are authoritative narrative evidence. State files summarize that evidence, not replace it. Plans, research, notes, and working drafts are not evidence of events.

A character's knowledge must come from approved background or events they actually witnessed/learned. A prepared scene, quest, source article or outside setting guide does not make its contents known to the characters.

## Three-role production workflow
**1. Writer** — On an explicit request to produce the next chapter, write the full manuscript. Save it in GitHub `chapters/working/`; if dual storage is enabled, also create the designated Google Doc in the configured working folder. Check full-text parity. Update *only Writer's own* SafeState with real paths/IDs. Stop. No state ledger or lengthy report.

**2. Curator-Editor** — Edit the same working manuscript directly: style, pacing, dialogue, characterization, logic and ordinary continuity errors. Save the **full corrected text** in both enabled stores, updating the *same* Google Doc if dual storage is enabled. Verify parity. Update only Curator-Editor's SafeState. Return from Archivist's review goes here for precise corrections; involve Writer only for major creative rewrites.

**3. Archivist** — Independently review the **edited** manuscript against approved canon and state. If blocked, give precise internal findings to Curator-Editor, not a spoiler report to the reader. If it passes, apply the approval policy in `project.json`:
- `ARCHIVIST_AFTER_REVIEW` (default): Archivist may approve routine chapters without asking the owner. Major new canon decisions or contradictions outside delegated authority still require the owner.
- `HUMAN_EACH_CHAPTER`: wait for explicit owner approval of the exact revision before promoting it.

On approval, put the final full text in `chapters/approved/`, move the existing Google Doc to the approved folder if dual storage is enabled (preserving its ID), verify content and location, and synchronize `state/`, `project.json`, and Archivist SafeState. Remove obsolete working copy only after successful verification; never risk losing the sole copy.

## Dual-storage gate (when enabled)
GitHub and Google Docs contain the **same complete chapter text** at each stage, allowing only harmless final newline normalization. The Google document is edited **in place** and moved between folders at approval; it is not cloned. If one side is unavailable or mismatched, mark the stage `SYNC_BLOCKED` and do not claim the chapter is approved. Git and Google Drive are not an atomic transaction: verify both before updating chapter state.

## Reader experience
Default `LINKS_ONLY_NO_SPOILERS`: after verified approval, report only a neutral ready message and links to the specific chapter (Google Doc first if enabled, then GitHub). No complete chapter text, preview, summary or plot hints in chat. Working chapter links are supplied only on explicit request, clearly marked draft. Configure alternative delivery only deliberately.

## Role restart prompt
> Open my story project. Verify project.json and START.md. Load my role and matching SafeState, the latest approved chapter, and only necessary canon/state files. Do not use other projects' events. Continue only the assigned workflow stage; confirm external writes rather than assuming they succeeded.
