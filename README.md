# On Writing Well — Claude Skill

A skill for [Claude](https://claude.ai) that edits and improves prose using the principles from William Zinsser's *On Writing Well*. Paste in a draft or hand it a file, and Claude returns a revised version, a full list of changes, and personalised tips for your next revision pass.

**License:** [Mozilla Public License 2.0](LICENSE)

---

## What it does

The skill applies Zinsser's principles systematically — not as a vague style preference, but as a concrete, documented editing checklist. It works in two passes:

**General principles (applied to every piece):** clutter elimination, active voice, verb strength, adjective and adverb discipline, cliché removal, sentence and paragraph structure, punctuation, hedging language, openings, endings, and unity.

**Form-specific principles (applied when the form is detected):** the skill recognises six writing forms and loads an additional reference for each:

- Travel writing
- Business writing
- Science and technical writing
- Interviews and profiles
- Memoir and family history
- Reviews and criticism

After editing, Claude returns:

1. The complete revised text
2. A bulleted list of every change made, grouped by type (e.g., clutter removed, passive constructions fixed, spelling corrected)
3. A set of *On Writing Well* principles that only the writer can apply — things that require self-knowledge or judgment an editor can't substitute for

---

## Installation

This skill runs inside [Cowork](https://claude.ai) or [Claude Code](https://docs.claude.com/en/docs/claude-code/overview). To install it:

1. Clone or download this repository.
2. Copy the `on-writing-well/` folder into your Claude skills directory:
   - **Cowork / Claude Code:** `~/.claude/skills/on-writing-well/`
3. Restart Claude Code or reload your Cowork session.

Claude will pick up the skill automatically. You can confirm it's available by asking Claude to list your installed skills.

> **Note:** Skills are loaded by Claude based on the `SKILL.md` file in the skill folder. The `references/` subdirectory must be kept alongside `SKILL.md` — it contains the principle files the skill reads at edit time.

---

## Usage

Once installed, trigger the skill by asking Claude to edit or improve your writing. Some examples:

- *"Edit my writing."*
- *"Make this tighter."*
- *"Apply On Writing Well principles to this draft."*
- *"Review this email."*
- *"Can you improve this?"* (then paste your text)

You can paste text directly into the conversation, or attach a file (`.txt`, `.md`, `.docx`). If you provide a file, Claude saves the revised version as Markdown to your workspace folder for you to review. If your original file wasn't Markdown, Claude will ask whether you want it converted back to the original format.

---

## Repository structure

```
on-writing-well/
├── SKILL.md                          # Skill definition and editing instructions
└── references/
    ├── general-principles.md         # Core Zinsser principles applied to all writing
    ├── user-only-tips.md             # Tips that require the writer's own judgment
    └── forms/
        ├── travel-writing.md
        ├── business-writing.md
        ├── science-technical.md
        ├── interviews-profiles.md
        ├── memoir-family-history.md
        └── reviews-criticism.md
```

---

## Contributing

Contributions are welcome. The most useful improvements are to the reference files in `references/` — tightening the principle descriptions, adding examples, or expanding form coverage.

If you spot a case where the skill applies a principle incorrectly, misses an obvious edit, or produces a change that contradicts Zinsser, please open an issue with a before-and-after example. That's the fastest way to improve it.

To contribute:

1. Fork the repository
2. Create a branch (`git checkout -b improve-business-writing-principles`)
3. Make your changes
4. Open a pull request with a short description of what you changed and why

Please keep the reference files grounded in *On Writing Well* — the skill's value comes from being a faithful implementation of Zinsser's advice, not a general style guide.

---

*Based on* On Writing Well *by William Zinsser (1976). The skill does not reproduce the book's text — it distills its principles into an editing reference.*
