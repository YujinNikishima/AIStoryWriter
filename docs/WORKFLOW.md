# Modern three-role workflow

## 1. Writer
Create complete working chapter. Save in GitHub; also Google Docs if configured. Verify both copies and update only Writer SafeState. No writing into `state/`, no extra review report.

## 2. Curator-Editor
Read actual working chapter, directly repair prose and logical errors, save the *complete revised chapter* into the same enabled stores, and update own checkpoint. Do not bounce ordinary issues to Writer.

## 3. Archivist
Independently audit edited copy. If blocked, send precise findings to Curator-Editor for another iteration. If clean, promote the chapter according to configured approval policy. Human decisions are needed only for fundamental canon changes (or for each chapter if HUMAN_EACH_CHAPTER is selected).

## 4. Synchronize and deliver
A chapter is not finished until the exact approved full text and derived state are verified. With Google Docs enabled, **edit and move the same document**, preserving its ID. Do not claim success if one store cannot be verified. Advance the chapter pointer only after all required copies are valid.

Deliver a neutral ready message plus chapter-specific links with no spoilers by default. In dual-storage mode, Google Doc first, GitHub second.

## Canon truth versus summaries
1. Latest explicit owner decisions about foundational canon.
2. Canon documents and approved narrative chapters.
3. Derived factual `state/` files (check against underlying chapters if in conflict).
4. Future plans, research and working drafts, which never establish events.

Review and repair conflicts rather than silently rewriting previous chapters. Do not import state from another story.

## Practical limitations
GitHub and Google Drive do not provide cross-platform atomic commits. Keep a known previous version and use verification before updating status. New chats must recover from actual project files, not conversational memory alone. One assistant acting in several roles is not the same as genuinely independent review.
