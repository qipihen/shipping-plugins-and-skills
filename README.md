# shipping-plugins-and-skills

A reusable Codex skill for shipping WordPress plugins and reusable skills to a publish-ready state.

This skill is designed for the last mile of delivery work:

- integration review
- settings UX review
- README and usage docs
- bilingual documentation checks
- GitHub Pages planning
- release archive checks
- publish-ready GitHub handoff

## What is included

- `SKILL.md`
- `references/checklists.md`
- `references/docs-and-release-outline.md`
- `dist/shipping-plugins-and-skills.skill`

## When to use

Use this skill when a plugin or skill already works, but still needs to be cleaned up, documented, packaged, reviewed, and published.

Examples:

- ship a WordPress plugin to GitHub with docs and release assets
- add installation docs and a GitHub Pages site
- package a reusable skill into a `.skill` file
- run a final shipping review before release

## Install into Codex

Option 1: copy the source folder into your personal skills directory.

Expected target:

```text
~/.codex/skills/shipping-plugins-and-skills/
```

Option 2: use the packaged file:

```text
dist/shipping-plugins-and-skills.skill
```

## Notes

- The skill is written to be reusable beyond TranslatePress.
- It includes hard gates based on real delivery failures: hidden integration points, misleading naming, incomplete usage docs, incomplete English docs, and missing release assets.
