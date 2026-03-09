# Shipping Checklists

Use these as hard gates before release work is considered complete.

## WordPress Plugin Checklist

- Verify the real admin entry point and setting location in the host product.
- Verify plugin name, description, author, version, and links in the plugin header.
- Verify install path and activation steps in the README.
- Verify each user-facing field label is understandable without source-code context.
- Verify provider naming does not overstate scope or imply unsupported endorsements.
- Verify example-only providers are labeled as examples.
- Verify at least one documented happy path from install to successful test call.
- Verify release zip installs cleanly in WordPress.
- Verify archive filename matches the full capability scope.
- Verify at least one syntax or smoke test command is documented.

## Skill Checklist

- Remove scaffold examples and unused files.
- Keep frontmatter limited to `name` and `description`.
- Make the description trigger-oriented, not workflow-oriented.
- Keep the skill focused on reusable judgment, not one project story.
- Move large or repeated material into `references/` only when necessary.
- Validate the skill by packaging it successfully.
- Package a `.skill` archive if the skill will be reused or shared.

## Public Repo Checklist

- Add a root README that explains what the project is in one screen.
- Add usage instructions, not just feature bullets.
- Add FAQ when setup decisions are likely to confuse users.
- Add a GitHub Pages site when the repo needs a public landing page.
- Add release notes and attach downloadable assets.
- Verify links in README, docs, and site all resolve correctly.

## Bilingual Docs Checklist

- Put the language switch near the top of the main README.
- Keep Chinese and English structure aligned enough that one can be maintained from the other.
- Do not leave English docs as stubs if the repo claims bilingual support.
- Keep examples, caveats, and warnings consistent across languages.

## Comparison Content Checklist

- Separate official pricing from third-party example pricing.
- Add concrete dates or source notes when the numbers can change.
- Label third-party services as examples unless there is a real partnership.
- Keep tables decision-oriented: price, scope, concurrency, and tradeoffs.
- Do not publish pricing tables without a plain-language explanation of when each option fits.
