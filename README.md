# App Security Code Review Skill

A defensive code review skill for web apps, APIs, backend services, and mobile apps using pinned OWASP guidance. It supports iOS and Android and ties each finding to code evidence, a proposed fix, and a way to verify it.

## Install

Download and extract the source archive for the version you want from GitHub Releases, or clone the repository and check out that version’s tag. From the root of that copy, run the following on macOS or Linux to install the skill for Codex. [GitHub release archives](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)

```sh
skill_dir="$HOME/.agents/skills/app-security-code-review-skill"
mkdir -p "$HOME/.agents/skills" && mkdir "$skill_dir" &&
  cp -R SKILL.md references LICENSE "$skill_dir/"
```

For a manual install, copy `SKILL.md`, `references/`, and `LICENSE` into an `app-security-code-review-skill` folder at one of these locations. Project paths are relative to the repository you want to review.

| Agent | Personal install | Project install |
| --- | --- | --- |
| Codex | `~/.agents/skills/app-security-code-review-skill/` | `.agents/skills/app-security-code-review-skill/` |
| Claude Code | `~/.claude/skills/app-security-code-review-skill/` | `.claude/skills/app-security-code-review-skill/` |

Keep `references/` next to `SKILL.md` so the skill can find its source register and reporting guidance. To update a copy, move the old folder outside the skills directory and repeat the install from the chosen release. If the skill is missing from the picker, restart your agent. [Agent Skills layout](https://agentskills.io/specification#directory-structure) · [Codex skill locations](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills) · [Claude Code skill locations](https://code.claude.com/docs/en/skills)

## Use

Open the repository you want to review. In Codex, start with this prompt.

> Use `$app-security-code-review-skill` to review this repository.

In Claude Code, enter `/app-security-code-review-skill` followed by the review request. To start with a narrower scope, ask for a likely-risks review of a named component or the current changes against a named base.

The skill offers two depths. **Likely risks** starts with the controls that matter most to the application. **Requirement by requirement** assigns an evidence status to each control in the agreed scope. Results apply to the reviewed revision and available evidence. Controls that need runtime, device, or deployment evidence stay open. If the request leaves scope open, the skill offers choices based on the repository.

The chat report links to code and guidance, describes the potential consequences, and proposes a fix and a way to verify it. Ask the skill to draft GitHub items for the findings you select. It shows each draft and destination before posting and routes unresolved vulnerabilities in public repositories to private reporting.

## Sources and updates

The [source register](references/sources.md) identifies the pinned OWASP guidance, credits upstream projects, and records their licenses. See [Maintaining the skill](MAINTAINING.md) for the update procedure.

This independent project references security guidance published by the OWASP Foundation and maintained by its project contributors. It is not affiliated with or endorsed by the OWASP Foundation. The source register lists the exact editions, credits, and upstream licenses. The original skill files are distributed under the [MIT License](LICENSE).
