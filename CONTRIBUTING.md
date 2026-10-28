# Contributing

This repository welcomes issues, pull requests, and discussions. Please read this guide before opening a PR.

## Scope

The current skill set contains twelve skills under `skills/`: `idea-evaluator`, `deep-research`, `vibe-research-workflow`, `intro-drafter`, `paper-writer`, `tech-paper-template`, `benchmark-paper-template`, `paper-polish`, `figure-designer`, `drawio-reconstruction`, `pre-submission-reviewer`, `rebuttal-guidance`. Adding a new skill requires:

1. Discussion via issue first; confirm the skill fills a real gap and is not covered by an existing skill.
2. Clear attribution for any content not derived from `handbook/`.
3. Adherence to the SKILL.md conventions below.

## Authoring a skill

Each skill directory at `skills/<name>/` contains:

- `SKILL.md`, English, under 500 lines, with valid YAML frontmatter containing `name` and `description`.
- `references/*.md`, on-demand depth. Files over 100 lines must begin with a table of contents.
- Optional `scripts/*.py` for deterministic helpers and `assets/*` for templates.

## Hard rules (enforced by CI)

- SKILL.md body under 500 lines.
- `description` between 40 and 80 words, written in third person, contains at least one "Use when..." clause.
- No em-dash (U+2014) in `SKILL.md` or `references/*.md`; use commas or periods.
- No Chinese characters in SKILL.md.
- All `See: references/X.md` pointers must resolve to existing files.
- No nested references (`SKILL.md -> refs/a.md -> refs/b.md` is illegal).
- Reference files shared across skills are duplicated per consuming skill (skills stay self-contained); each copy carries a header naming its canonical, and copies must stay byte-identical to the canonical below the header (`python scripts/check_shared_sync.py`).
- Commits must not contain "Claude", "Co-Authored-By: Claude", or Anthropic attribution.

## Running the linter

```bash
python -m pip install -r requirements-lint.txt
python scripts/lint_skills.py
python scripts/check_shared_sync.py
```

The linter exits non-zero on any violation and is invoked by `.github/workflows/lint.yml` on every PR.

## Documentation language

English is the default language throughout this repository. Maintain one canonical
README and one curriculum tree at `handbook/`; do not add language-specific
mirrors or duplicate translations. Translate new upstream material into English,
including example prompts and figure labels, and preserve the original attribution.

Keep internal links aligned with the English filenames. Shared images live under
`assets/` and chapter-local images under `handbook/<chapter>/assets/`. Review
embedded text in images, PDFs, and Draw.io files as well as plain text.

## Branches and upstream updates

- `main` contains the English-only edition and is this fork's default branch.
- `upstream-sync` preserves the former `main` and receives the original project's
  updates without English-only changes.
- `origin` points to `nijkah/Supervisor-Skills`; `upstream` points to
  `HKUSTDial/Supervisor-Skills`.

In a new clone, register the original repository once:

```bash
git remote add upstream https://github.com/HKUSTDial/Supervisor-Skills.git
```

With a clean working tree, update the source branch first:

```bash
git fetch upstream
git switch upstream-sync
git merge --ff-only upstream/main
git push origin upstream-sync
```

Then bring the changes into the English edition for review:

```bash
git switch main
git merge --no-ff --no-commit upstream-sync
```

Resolve conflicts using the English filenames and documentation layout. Translate
new material and remove duplicate Chinese content, including embedded figure
text. Run the lint and shared-reference checks above, review the staged changes,
then commit and push `main`. If Git reports that the branch is already up to date,
there is no merge to commit. Merge commits preserve the upstream ancestry for
subsequent updates.

## License

All contributions are licensed under CC BY-NC-SA 4.0. By submitting a PR you agree to license your contribution under these terms and to provide attribution consistent with the original repository's convention.

## Commit conventions

Conventional Commits:
- `feat(skill): <name> ...` for new skills
- `feat(<area>): ...` for new non-skill features
- `fix(<area>): ...` for bug fixes
- `docs(<area>): ...` for documentation
- `build: ...` for build system, CI, tooling
- `chore: ...` for routine maintenance
- `refactor(<area>): ...` for refactoring

Commits must not include any Claude or Anthropic attribution.
