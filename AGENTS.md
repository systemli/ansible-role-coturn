# AGENTS.md

Ansible role that installs and configures the coturn TURN server (for Nextcloud Talk and Jitsi Meet) on Debian (bookworm, trixie).

## Layout

- `defaults/main.yml`: optional role variables with defaults; `coturn_static_auth_secret` and `coturn_realm` are required and have no default
- `tasks/`: `main.yml` and `systemd.yml` (systemd override for binding privileged ports)
- `templates/turnserver.conf.j2`: coturn configuration
- `files/`: static files, e.g. the systemd capability override
- `handlers/main.yml`: handlers such as `Restart coturn`
- `molecule/default/`: integration test (Docker, Debian 13)

## Checks

- `ansible-lint .` must pass without warnings (config in `.ansible-lint`, which excludes `molecule/` and `.github/`)
- `yamllint .` uses `.yamllint`
- `molecule test` runs the role in a container; CI runs it on Debian 12 and 13 via `systemli/github-ansible-workflow`
- `ansible-lint` creates `.ansible/`; it is git ignored, never commit it

## Conventions

- Use fully qualified module names, quoted octal `mode` values and `true`/`false` booleans
- Give every task a `name`
- New or changed role variables need an entry in `defaults/main.yml` and the README

## Commits and PRs

- Write in English, use conventional commit titles (`feat:`, `fix:`, `chore:`, `ci:`; `!` for breaking changes)
- The PR title sets the release-drafter label (`enhancement`, `bug`, `chore`, `breaking`); a breaking change bumps the major version
- Open PRs as draft and fill in `.github/pull_request_template.md`: what changed and why, plus a breaking changes section if needed
- Do not list changed files or claim test results in the description; CI covers that
