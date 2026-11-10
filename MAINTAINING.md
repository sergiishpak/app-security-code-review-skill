# Maintaining the skill

Start with the upstream links in the [source register](references/sources.md) when a project announces a release or changes its guidance. A new upstream version is a candidate until it passes review.

1. Compare the candidate release or commit with the existing pin. Check for changed, added, removed, or renumbered requirements and changes to applicability, profiles, or mappings between documents. For an unversioned source, use a verified commit permalink.
2. Check that the versioned links still resolve and that the attribution and license match the exact edition. Verify any edition-specific copyright notices and check the branding guidance before changing public-facing claims or names.
3. Update the source register and any instructions affected by the new guidance. Keep reports and previously published skill releases tied to their original pins. Include the old and new pins and a short summary of the effect on reviews in the skill release notes.
4. Exercise the changed behavior on a local or synthetic example. Check that an ambiguous mixed repository prompts for scope and depth, a focused review uses the correct source, a requirement-by-requirement review records missing evidence, and an unresolved finding from a public repository stays in a private draft unless a verified private destination is approved.
5. For a change to the mobile sources, spot-check a real remapping. The [MASWE release pull request](https://github.com/OWASP/maswe/pull/182) documents beta `MASWE-0031` moving to `MASWE-0025`. Confirm the mapping and applicability before carrying a citation forward.
6. Review the changes before publishing a new skill release. Leave the previous pin active if the candidate cannot be verified.

Keep the repository link-based. If a future contribution proposes redistributing an upstream excerpt, dataset, image, or adaptation, review the license for that specific item first. Preserve applicable credits and notices, link the source and license, identify modifications, and apply the appropriate license to any shared adaptation covered by ShareAlike. Keep third-party terms distinct from the skill's MIT terms. [Creative Commons attribution and ShareAlike guidance](https://creativecommons.org/faq/) · [OWASP branding guidelines](https://owasp.org/policy/branding-guidelines)

## First public release

1. Verify that the files in the initial commit contain only the public skill and repository documentation. Follow the [installation instructions](README.md#install) from a clean copy and confirm that Codex lists `app-security-code-review-skill`.
2. Use the first sentence of the [README](README.md) as the GitHub repository description.
3. On the public GitHub repository, enable private vulnerability reporting and verify that a user without repository write access can open the form described in [SECURITY.md](SECURITY.md). Do this before announcing the release. [GitHub setup instructions](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/configure-for-a-repository)
