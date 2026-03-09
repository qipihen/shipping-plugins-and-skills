---
name: shipping-plugins-and-skills
description: Use when turning a working WordPress plugin or reusable skill into a shippable deliverable, especially when it needs integration review, settings UX checks, README or usage docs, bilingual documentation, GitHub Pages docs, release archives, or publish-ready GitHub assets.
---

# Shipping Plugins And Skills

## Overview

Turn a working plugin or skill into something another person can install, understand, and publish without guessing. Optimize for first-use success: visible integration points, accurate naming, complete docs, release assets, and final verification.

Use this skill after the core implementation exists or when a project has already gone through one review round and now needs to be packaged properly.

Typical triggers:

- "Ship this plugin to GitHub with docs and release assets"
- "Add README, usage docs, comparison content, and a project site"
- "Prepare a release with an installable zip"
- "Turn this workflow into a reusable skill"
- "Do a final review and shipping pass before publish"

If the deliverable itself is a skill, use `skill-creator` for structure and `writing-skills` for validation discipline. Use this skill to drive the shipping checklist, public presentation, docs completeness, and release readiness.

## Scope Decision

Lock these decisions before polishing:

1. Confirm the deliverable type: `wordpress-plugin`, `skill`, or `both`.
2. Confirm the audience: internal only, client handoff, or public open source.
3. Confirm distribution targets: repo only, GitHub Release, GitHub Pages, or all three.
4. Confirm language requirements: one language or bilingual.
5. Confirm whether provider examples must be framed as examples only, not endorsements.

Do not start polishing docs or release assets before these are explicit. Missing scope decisions create most late-stage churn.

## Shipping Workflow

### 1. Inspect the current state before promising anything

Read the repo, current README, docs folder, release assets, and real integration points. For WordPress plugins, verify where the feature actually appears in the host UI instead of assuming a new page exists. For skills, inspect the target skill folder and trigger description before expanding references or assets.

Use real failures as baseline data. If the current project already went through user feedback, extract every complaint and convert it into a hard gate.

### 2. Audit integration surfaces

For a WordPress plugin, inspect:

- Actual admin entry point
- Settings field labels and defaults
- Host plugin hooks and load order
- Whether new engines, actions, or settings are visible in the real UI
- Archive naming, plugin headers, author metadata, and upgrade-safe behavior

For a skill, inspect:

- Trigger description quality
- Folder structure and unnecessary scaffold files
- Whether references and assets are actually needed
- Whether the skill teaches reusable judgment instead of retelling one project history

Do not move forward with public docs until the integration surface is stable enough to describe accurately.

### 3. Run a shipping review, not just a code review

Prioritize these findings first:

- High-severity behavioral regressions
- Integration mismatches between code and UI
- Naming that misleads users about capability or scope
- Missing usage instructions
- Release blockers such as missing zip assets or incomplete metadata

Fix high issues before expanding comparison tables, SEO copy, or landing-page polish.

### 4. Build the documentation set users actually need

Default docs package for public plugin projects:

- Root `README.md`: what the project is, what host product it extends, supported engines or providers, install path, quick start, verification commands
- Usage guide: happy path setup, field meanings, test flow, screenshots only if needed
- Extension guide: how to adapt to custom providers or proxy APIs
- Pricing or comparison guide: only when cost choice is part of the product decision
- GitHub Pages site in `docs/`: landing page, install summary, FAQ, repo links
- English docs if the project is public and claims bilingual support

Default docs package for skills:

- `SKILL.md`: trigger conditions, workflow, hard gates, common mistakes
- Small reference files only when they reduce repetition
- No filler files, no narrative retrospectives, no setup junk unless it changes behavior

Use the outlines in [references/docs-and-release-outline.md](references/docs-and-release-outline.md) and the checks in [references/checklists.md](references/checklists.md).

### 5. Frame provider examples carefully

If a third-party API or proxy service is included only as an example:

- Say it is an example
- State there is no commercial relationship if that matters
- Avoid listing it like an endorsed first-party engine
- Keep naming generic where possible
- Separate protocol compatibility from vendor branding

This matters for proxy APIs, single-token relays, mirrored providers, and cost-comparison tables.

### 6. Prepare release artifacts before declaring the project done

For plugins:

- Generate the installable zip
- Use an archive name that matches the real project scope, not one feature
- Make sure the release page includes the zip as a downloadable asset
- Check plugin header metadata, author name, and links
- Include a short changelog or release note

For skills:

- Remove scaffold leftovers
- Validate the skill structure
- Package a `.skill` archive when the skill will be shared or backed up

### 7. Verify with hard gates

Do not claim completion until the following are true:

- The feature is visible at the actual integration point
- The main README explains what the host product is and what this project adds
- Usage instructions are present, not implied
- Public docs do not over-promise unsupported behavior
- English docs are complete if bilingual support is claimed
- Release assets are downloadable
- Example providers are labeled as examples
- Ambiguous fields are renamed to user-facing labels
- Archive names match product scope

## Quick Reference

| Deliverable | Minimum shipping set |
| --- | --- |
| WordPress plugin | Working code, README, usage guide, release zip, verification |
| Public plugin | Plugin set plus GitHub Pages docs, FAQ, author metadata, release assets |
| Skill | Clean `SKILL.md`, minimal references, validation, packaged `.skill` if sharing |
| Plugin plus skill | Ship the plugin first, then abstract the reusable workflow into the skill |

## Common Failure Patterns

Watch for these repeated mistakes:

- Assuming where the UI entry point should be instead of checking where it actually renders
- Treating an example provider as a promoted partner
- Shipping comparison content without plain usage instructions
- Promising bilingual docs while leaving English incomplete
- Releasing a tag without an installable archive
- Naming a zip after one engine when the project supports many
- Keeping field labels technical when users need human-readable labels

## Final Rule

A project is not shippable when "the code works." It is shippable when a new user can find the feature, understand the setup, choose the right provider, download the right asset, and reproduce the intended result without extra back-and-forth.
