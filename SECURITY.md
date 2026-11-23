# SECURITY

## Hard rule: no agent use of Dan's browser sessions or password vault (Dan, Nov 22–23, 2026)
Dan, 11:59 PM ET Nov 22: "make sure agents can't use stored cookies in chrome and access bitwarden the way i would"; 12:07 AM ET Nov 23: "make this harness wide hard rule for all agents in repos all of my repos". Applies to every agent, lane, worker and script (Grok Bot, Claude, Codex, cloud agents, bus lanes).
1. Never read, copy, export, decrypt or replay browser cookies, session storage, saved passwords or Chrome `Cookies` / `Login Data` files, or the macOS Keychain entries Dan uses, on any machine.
2. Never open, sign in to, unlock or drive Bitwarden (web vault, extension, desktop or CLI) or any other password manager as Dan, including through an already-signed-in browser profile. An agent that sees a vault login or unlock screen stops and reports.
3. Agents get credentials only through their own scoped identity (a read-only Secrets Manager machine-account token, short-lived cloud roles, or the existing approved mechanisms such as the 0600 Claude token file), never through Dan's sessions.
4. No password-manager extension or vault login in any browser profile an agent drives.
5. A violation is a security incident: stop, report to Dan, and rotate affected credentials.
