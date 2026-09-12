# Security Policy

## Supported versions

Only the **latest stable release** is supported. Birch updates itself automatically, so staying current requires no action.

## Reporting a vulnerability

Please **do not open a public issue** for anything security-sensitive.

Report vulnerabilities privately through GitHub:

1. Go to this repository's **Security** tab.
2. Click **Report a vulnerability** (or use [this direct link](https://github.com/BirchInnovation/birch-code/security/advisories/new)).
3. Include the Birch version, your OS, and steps to reproduce.

You will receive an acknowledgement within **7 days**. Please give us a reasonable window to ship a fix before any public disclosure — we will coordinate the timeline with you in the advisory thread.

## Scope notes

- Birch is a desktop application; it stores its data locally (SQLite database, logs, artifacts) in your user profile.
- Access tokens for integrations (GitHub, GitLab, Azure DevOps, Jira, Linear, YouTrack) are stored in the operating system's credential store (Keychain on macOS, Credential Manager on Windows).
- The app downloads updates exclusively from `https://updates.getbirchcode.dev`.
