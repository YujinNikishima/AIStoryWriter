# Story Engine Template

A story-agnostic English template for writing long-form fiction with AI roles, consistent canon, and repeatable chapter production.

**This is a reusable workflow and a collection of instructions and files—not an app or an automated AI runtime.** You can run the steps in connected AI chats, or later build your own orchestration.

## What it does
- Keeps established canon separate from future ideas and working drafts.
- Splits work among **Writer → Curator-Editor → Archivist**.
- Lets the Archivist approve routine chapters after independent continuity review; the owner retains authority over foundational canon.
- Supports an optional per-chapter owner-approval mode.
- Supports GitHub alone, or synchronized GitHub + Google Docs for readers who prefer documents.
- Gives assistants their own restart checkpoints (SafeState) without confusing role responsibilities.
- By default, readers receive **verified chapter links without excerpts or spoilers**.

## Quick start
1. Copy this template into an empty story folder or repo. Never mix story identities.
2. Set the project identity and workflow options in [project.json](project.json).
3. Fill the files under [canon/](canon/brief.md).
4. Read [START.md](START.md) and [docs/QUICKSTART.md](docs/QUICKSTART.md).
5. Assign AI assistants the prompts in [roles/](roles/writer.md) and their matching files in `safestate/`.
6. Request a chapter. Roles complete the cycle; you read the approved result.

## Directory guide
```text
project.json                 identity, current chapter and options
START.md                     common rules and recovery instructions
canon/                       approved premise, cast, world and style
planning/                    future route and unresolved questions
roles/                       writer, curator-editor, archivist instructions
safestate/                   independent restart checkpoints for each role
chapters/working/            not-yet-approved full chapter manuscripts
chapters/approved/           approved complete chapters
state/                       events, character knowledge and story threads
reviews/                     internal continuity/editorial notes
docs/                        quickstart, workflow and publication notes
```

## Non-negotiable principles
**A plan is not an event. A draft is not an approved chapter. Source research is not character knowledge.**
No role may silently rewrite an approved fact. Do not claim a write, synchronization, or approval happened until its result has been checked.

## What is intentionally not included
No fictional franchise or specific characters, no imported game databases, no previous story's chapters, no secret tokens, no ChatGPT subscription integration.

## Publication
This clean repository has fresh Git history without earlier story archives. Review its contents, test the workflow, and choose a license before making it public. See [docs/PUBLISHING.md](docs/PUBLISHING.md).

Licensing has intentionally not been selected yet. Add a license of your choice before public distribution.
