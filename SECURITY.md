# Security Policy

Last reviewed: 1 October 2026.

## Supported versions

Security fixes are provided for the latest stable release and the latest published beta release of Birch for Windows and macOS. Older releases do not receive backports. Reports about older versions are still welcome: we will assess whether supported versions are affected.

Use Birch's **Check for updates** command to check your installed version, or download the latest installer from the [official website](https://www.getbirchcode.dev/). Follow the affected and fixed versions in each [security advisory](https://github.com/BirchHQ/birch-code/security/advisories); do not assume an update has already been installed.

## Reporting a vulnerability

[Report a vulnerability privately using GitHub Private Vulnerability Reporting](https://github.com/BirchHQ/birch-code/security/advisories/new). A GitHub account is required. This community repository accepts reports about Birch even though the product's source repository is private.

**Do not disclose suspected vulnerabilities in public Issues, Discussions, pull requests, or their attachments.** If you are unsure whether a report is security-sensitive, use the private channel. Access to reports is limited to the reporter, authorized repository security maintainers, and invited advisory collaborators.

Do not include live API keys, passwords, private source code, personal data, or complete unredacted logs. Use synthetic data and the smallest example that demonstrates the problem. If sensitive evidence is essential, describe what it contains first so we can arrange an appropriate transfer.

## What to include

- Birch version, stable/beta channel, operating system version and architecture.
- Affected component, relevant agent/plugin version, and configured permissions, if applicable.
- Expected and actual behavior, security impact, and any required attacker access.
- Reproduction steps or a minimal, non-destructive proof of concept.
- Relevant logs or screenshots with secrets and private information removed.
- Suggested remediation, if known; this is optional.

An incomplete report is welcome. Please send what you know without collecting more sensitive data to prove impact.

## Response expectations

We aim to acknowledge reports within **3 business days**, provide an initial assessment within **7 business days**, and provide a progress update at least every **14 calendar days** while an accepted report remains open. Business days are Monday to Friday, excluding public holidays in Denmark, in the **Europe/Copenhagen** time zone.

These are communication targets, not guaranteed resolution deadlines. The time needed for a fix depends on impact, complexity, and available mitigations. If you have not heard back, follow up in the same private report.

We normally coordinate disclosure after a tested, signed fix is available. We will discuss timing with you and do not ask for an indefinite embargo. Active exploitation, already-public details, or significant risk to users may require an earlier warning and mitigation guidance. Legal reporting obligations are handled separately from these response targets. We credit researchers only with their consent.

## Scope

Reports are welcome for Birch desktop and CLI, official Birch agent plugins, and Birch-controlled product configuration and distribution infrastructure. The covered web hosts are www.getbirchcode.dev (website), docs.getbirchcode.dev (documentation), and updates.getbirchcode.dev (update distribution). Examples include:

- Disclosure of API keys, integration credentials, private code, or session data, including through logs or telemetry.
- Bypass of Birch's credential-store protections or of a permission boundary actually enforced by Birch.
- Unintended cross-workspace or cross-session access caused by Birch, and commands executed contrary to configured approval requirements.
- Command injection through branch names, file paths, prompts, or other untrusted input.
- Security flaws in the terminal/WebView, local shell bridge, or local IPC.
- Installer or updater tampering, signature bypass, and unauthorized replacement of update metadata or packages.
- A vulnerability in a dependency with a demonstrated or reasonably explained impact on Birch.

A Git worktree separates working files; **it is not an operating-system sandbox**. Agent permissions and sandbox settings depend on the agent and selected mode. A shell accessing files with permissions deliberately granted by the user is not, by itself, evidence of a Birch sandbox bypass. Reports that Birch applies, represents, or enforces those settings incorrectly are in scope.

Only test installations, accounts, and data you own or have explicit permission to test. Reports concerning the Birch website, documentation, or update distribution are welcome, but this policy does not authorize intrusive testing of production services or anyone else's infrastructure.

The following are outside the authorized testing scope:

- Testing GitHub, AI providers, hosting providers, or third-party extensions without their permission. Flaws in Birch's integration with those services remain in scope.
- Social engineering, phishing, physical attacks, or attacks requiring physical access to an unlocked device.
- Denial of service, load testing, destructive actions, persistence, lateral movement, or accessing other users' data.

A scanner result or dependency version alone is not sufficient to establish impact. We may request additional context; a fully weaponized exploit is not required.

## Research rules and safe harbor

Keep testing proportionate and non-destructive. Stop immediately if you encounter another person's data, minimize any retention, do not copy or extract additional data, and report the situation privately. Do not maintain access, alter other users' data, or disrupt service. Give us a reasonable opportunity to investigate and coordinate disclosure.

For good-faith research that follows this policy, we consider the activity authorized within our authority and will not initiate or support legal action against you for that research. To the extent we can do so, we waive restrictions in our own terms that would prohibit the research authorized here. If a third party brings a claim concerning that research, we will make our authorization known.

This commitment applies only to systems and rights we control. It does not authorize testing of third-party systems or bind other organizations or public authorities. If you are unsure whether an activity is permitted, ask through the private reporting channel before proceeding.

## Rewards

We do not currently operate a paid bug bounty program. Submitting a report does not create an entitlement to payment.
