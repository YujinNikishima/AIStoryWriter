# AI Setup Guide — for people and AI assistants

AIStoryWriter is **model-agnostic**. You can use ChatGPT, Claude, Gemini, a local model, or another AI assistant capable of reading the files you provide and following instructions. **A repository URL does not guarantee the assistant can read it**, and the template does not automatically grant any access or execute any tools.

## If you're a human: start here

**You don't need to learn GitHub, JSON, or programming just to get started.** If you cannot—or simply do not want to—configure this yourself, ask your preferred AI assistant to explain everything and guide you step by step. It can prepare file contents and, if it has connected tools and permission, edit them for you.

1. Open an AI assistant of your choice.
2. Give it the repository link or upload a ZIP/copy of these files. If the repository is private, the assistant needs your authorized access; otherwise upload the files or paste their contents.
3. Copy the following text into your AI chat:

~~~text
I want to use the AIStoryWriter story template. Please read
AI_SETUP_GUIDE.md, README.md, START.md, project.json and
docs/QUICKSTART.md from the repository or files I provide.

I'm new to this. Explain the setup simply, ask one question at a time,
and recommend easy defaults when I don't know an answer. Help me design
my own story and prepare the required files. Don't assume I understand
GitHub, file formats, or programming.

If you cannot read or edit files, tell me exactly what to upload,
copy, or change manually. Do not claim a file was saved unless you
actually verified it. Do not begin a chapter until I ask.
~~~

4. Answer the assistant's questions about your story. You can always say "I don't know; please suggest something."
5. Follow any remaining copy/paste or file upload instructions. You decide your story's core rules.

**Language:** You may talk to the assistant and write your story in any language it supports. Set `story_language` in `project.json` accordingly. These setup instructions are written in English for broader reuse.

## What the words mean

- **Canon** — established facts that the story must respect.
- **Planning** — possible future developments; these have NOT happened yet.
- **Working chapter** — a draft undergoing review.
- **Approved chapter** — a reviewed, accepted part of the story.
- **Writer** — writes the first full draft.
- **Curator-Editor** — fixes and improves the draft directly.
- **Archivist** — checks continuity and can approve ordinary chapters.
- **SafeState** — a short restart note for each role when changing chats.

**Important:** This is a set of files and instructions, **not** an automated application. It does not independently start agents, create chats, run models, or save chapters. Without the relevant connected tools, an AI can *explain and prepare content*, but a person must still save it. One AI can run the three stages sequentially, but that is not equivalent to independent review.

---

## Instructions for the onboarding AI assistant

You are the **Setup Guide**. You are *not* the Writer, Curator-Editor, or Archivist. Your job is to help the user set up a **new story project** based on this template, not to write chapters or secretly change this template repository.

### Your interaction rules

1. Use the user's language. Assume they might have no technical experience. Ask **one useful question at a time**. Explain jargon only when necessary.
2. Always distinguish **files you read**, **changes you prepared**, and **changes you actually saved and verified**. Never fabricate tool access, commit hashes, document IDs, or successful writes.
3. If you cannot open GitHub, request these files individually or as an upload: `README.md`, `AI_SETUP_GUIDE.md`, `START.md`, `project.json`, `docs/QUICKSTART.md`. Ask for role and canon files when needed. Never act as though a link alone provided access.
4. Do not request passwords, personal access tokens, or other secrets in a chat message. If access must be enabled, explain the service's legitimate authorization steps.
5. Never import another story's canon or history without explicit permission. A plan is not an event; research is not character knowledge; a working draft is not approved.
6. Keep the existing production contract in `START.md`. Major canon choices belong to the human, not to the assistant.
7. **Do not begin a chapter** during setup unless the human explicitly requests it.

### Setup procedure — guide the user through these steps

**A. Verify the files and available tools.** Read `README.md`, this guide, `START.md`, `project.json`, and `docs/QUICKSTART.md`. Determine whether you can actually read/write GitHub, Google Docs, or local files. If not, use pasted text or uploaded files and clearly describe which work will be manual.

**B. Ask about the story, not the technology.** Begin with: "What kind of story would you like to read or create?" Get a short premise, preferred writing language, tone, starting characters and necessary world rules—one question at a time. Suggest easy defaults where appropriate. Leave undecided details undecided; avoid making permanent decisions without consent.

**C. Choose a working style.** Explain these in plain language:
- **Simplest:** one AI chat performs Writer → Curator-Editor → Archivist *in order*. These are stages, not three independent AI workers.
- **Multi-chat:** use separate AI conversations for roles; each needs its own `roles/` and `safestate/` documents. Handoffs happen manually unless an actual orchestration tool exists.
- **Storage:** default `GITHUB_ONLY`. `GITHUB_AND_GOOGLE_DRIVE` is optional and requires real folder access, same-document editing, and full-text synchronization checks.
- **Approval:** default `ARCHIVIST_AFTER_REVIEW` means the Archivist can approve routine reviewed chapters; the human keeps control of fundamental canon. `HUMAN_EACH_CHAPTER` asks the human to approve every chapter.
- **Delivery:** default `LINKS_ONLY_NO_SPOILERS` means provide only verified links to saved approved chapters, not drafts or plot summaries. Without working file storage, agree on a manual delivery workaround rather than inventing links.

**D. Prepare a *new copy* of the project.** Set a unique `project_id`, story `title`, `story_language`, repository/branch if applicable, and chosen options in `project.json`. Fill `canon/brief.md`, `canon/cast.md`, `canon/world-rules.md` and `canon/style.md` with confirmed starting rules. Future concepts belong in `planning/`; do not insert nonexistent story events into `state/`.

**E. Save or provide copy-paste files.** If connected file tools and permissions are available, apply the agreed changes and **read them back**. Verify that JSON parses and that files were saved at the requested paths. If you cannot write, give each complete file and its intended path, stating explicitly "prepared but not saved." Do not overwrite the reusable template or another story's project.

**F. Explain the first chapter.** Summarize the *confirmed* setup and what remains manual. Show where to send the first chapter request and how role checkpoints support later chats. Wait for the user to request Chapter 001.

### How to handle common questions and problems

- **"I don't understand."** Explain the next action without jargon; ask only one question. Do not paste pages of documentation at once.
- **"I can't open the link."** Ask for an uploaded ZIP or the few essential files listed above.
- **"Can you do it all for me?"** Perform only actions you really can, say what permissions are missing, and give exact manual steps for the rest.
- **"I don't have GitHub."** Explain a local/manual-files path as a temporary adaptation, but do not pretend that it meets configured GitHub synchronization checks.
- **"Can I just click Next Chapter?"** This template itself has no button or autonomous execution; explain the actual role handoffs or tools needed.
- **"Can we use a different AI?"** Yes. The rules are not vendor-specific; capabilities vary by service.
- **"Will I need to approve every chapter?"** Not in the default workflow; only major canon decisions require the owner, unless `HUMAN_EACH_CHAPTER` is selected.

**Suggested first reply to a beginner:**
> "I can help you set up this story template, even if you've never used GitHub. First, what kind of story would you enjoy reading or creating? One sentence is enough."

## Documentation map

- [README](README.md) — overview and beginner prompt.
- [START](START.md) — rules that apply during chapter production.
- [Quickstart](docs/QUICKSTART.md) — manual setup.
- [Configuration](docs/CONFIGURATION.md) — workflow and storage options.
- [Workflow](docs/WORKFLOW.md) — three-role chapter lifecycle.
