# Quickstart

1. **Copy files only** to a fresh story folder or repository; do not transplant another story's Git history.
2. Edit `project.json`: set unique ID/title, story language, repository/branch, approval mode and storage mode.
3. Write approved initial character, world and style rules in `canon/`. Set future intentions in `planning/`, not `state/`.
4. If using Google Docs, configure two folders (working and approved) and set `storage.mode` to `GITHUB_AND_GOOGLE_DRIVE`. Every chapter has one Google Doc that moves between folders when approved.
5. Create one chat per role, or manually instruct one assistant to perform the roles sequentially. These are **prompts, not autonomous workers**.
6. Each role loads `START.md`, its own role/ SafeState file and relevant authoritative context.
7. Ask Writer to draft Chapter 001. It saves the full working manuscript and updates only its own checkpoint.
8. Curator-Editor directly edits that working chapter and forwards the verified full revision.
9. Archivist independently checks continuity and either returns specific fix requests or promotes the chapter according to `chapter_approval`.
10. Read the links to the approved chapter. Repeat.

## Prefer guided setup?

You can ask **any AI assistant** to guide you instead of studying the instructions. Open [AI_SETUP_GUIDE.md](../AI_SETUP_GUIDE.md) and copy its starter prompt. The AI should explain one action at a time, help prepare files, and be clear about which files it can actually read or save. A specific AI provider is **not required**.

## Important
Under the default policy **you do not approve each chapter**. You approve fundamental canon changes; Archivist handles normal chapter approval. To require chapter sign-off set `workflow.chapter_approval` to `HUMAN_EACH_CHAPTER`.

No files or Google Docs are automatically created just because these prompts exist. An AI needs the necessary connected tools and explicit access, or you must manually transfer the files.
