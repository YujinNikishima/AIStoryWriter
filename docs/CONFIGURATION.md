# Configuration reference

Configuration lives in `project.json`.

## Workflow
- `workflow.chapter_approval = "ARCHIVIST_AFTER_REVIEW"` (default): Archivist can approve routine reviewed chapters.
- `workflow.chapter_approval = "HUMAN_EACH_CHAPTER"`: approval requires an explicit owner's decision on the exact revision.
- `workflow.fundamental_canon_decisions = "HUMAN_ONLY"`: don't let any role rewrite the premise, permanent world rules or reserved mysteries.

Roles remain Writer, Curator-Editor and Archivist. Do not split the Editor out unless you intentionally redesign the workflow.

## Storage
- `storage.mode = "GITHUB_ONLY"`: full chapter files in `chapters/`.
- `storage.mode = "GITHUB_AND_GOOGLE_DRIVE"`: two verified copies; configure working and approved folder IDs. The same Google Doc is edited in place and moved on approval. The main reading location is Google Docs.

Do not change from one mode to another in the middle of a chapter without a reconciliation plan. Never invent Google Doc IDs/links. If a write fails, stop the chapter transition.

## Reader delivery
- `delivery.mode = "LINKS_ONLY_NO_SPOILERS"` (default): only verified links to ready chapters; no text, excerpts or summaries.
- To provide prose in chat, deliberately define a different presentation policy in project rules and ensure all roles agree.

## Language
`story_language` controls the novel's language, not the instruction files'. The template's instructions are English even when the story itself is not.

## Phase and pointers
Use `chapter_working` for active working chapters, `chapter_latest_approved` for truly approved chapters, and `last_verified_commit` only for a commit actually checked.
