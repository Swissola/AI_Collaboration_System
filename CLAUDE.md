# AI Collaboration System (AICS)

Pure documentation project: no build, test, or lint commands; every file is markdown.

- `PROJECT-INDEX.md` is a hand-maintained navigation index cross-referencing every file in the repo. Update it whenever a file is added, renamed, or removed.
- Core model is the three-layer system (Personal Preferences / Project Context / Project Memory, see `GLOSSARY.md`). New content should extend this framework, not introduce a competing structure.
- Guides are platform-agnostic by default (Claude, ChatGPT, Copilot, Gemini). Platform-specific depth belongs in its own dedicated guide (e.g. `guides/personal-preferences-guide.md`), not folded into the shared docs.

## Structure

`templates/` (starter + advanced) · `examples/` (2 domains) · `guides/` (layer-specific + supporting) · `archive/` (superseded content, e.g. old examples) · `GLOSSARY.md` · `PROJECT-INDEX.md`

Terminology is fixed: reuse the terms defined in `GLOSSARY.md` (Layer 1/2/3, Friction, Rule of Three) rather than inventing synonyms.
