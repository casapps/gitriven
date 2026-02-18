# gitriven — Complete Project Specification

**Version:** 1.0.0
**Date:** 2026-02-13
**Author:** Jason Hempstead
**Organization:** casapps
**License:** MIT
**Status:** Pre-Implementation — Planning Complete

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Brand Identity](#2-brand-identity)
3. [Architecture](#3-architecture)
4. [Binary & Distribution](#4-binary--distribution)
5. [Configuration System](#5-configuration-system)
6. [Git Compatibility Layer](#6-git-compatibility-layer)
7. [Smart Operations Engine](#7-smart-operations-engine)
8. [Commit Workflows](#8-commit-workflows)
9. [Merge & Rebase Engine](#9-merge--rebase-engine)
10. [Undo System](#10-undo-system)
11. [Recursive Operations Engine](#11-recursive-operations-engine)
12. [API Client Layer](#12-api-client-layer)
13. [Provider Management](#13-provider-management)
14. [Pull Request & Code Review](#14-pull-request--code-review)
15. [Issue Management](#15-issue-management)
16. [Gist Operations](#16-gist-operations)
17. [CI/CD Integration](#17-cicd-integration)
18. [Release Automation](#18-release-automation)
19. [Deploy Hooks](#19-deploy-hooks)
20. [Branch Management](#20-branch-management)
21. [Stash Enhancement](#21-stash-enhancement)
22. [Worktree Management](#22-worktree-management)
23. [Submodule Management](#23-submodule-management)
24. [Subtree Support](#24-subtree-support)
25. [LFS Auto Mode](#25-lfs-auto-mode)
26. [Security & Credentials](#26-security--credentials)
27. [Commit Signing](#27-commit-signing)
28. [Secret Scanning](#28-secret-scanning)
29. [Encrypted Files](#29-encrypted-files)
30. [Format & Lint Orchestration](#30-format--lint-orchestration)
31. [Hooks System](#31-hooks-system)
32. [Repository Health](#32-repository-health)
33. [.gitignore Management](#33-gitignore-management)
34. [.gitattributes Management](#34-gitattributes-management)
35. [License Management](#35-license-management)
36. [Community Files](#36-community-files)
37. [Project Scaffolding](#37-project-scaffolding)
38. [Changelog Generation](#38-changelog-generation)
39. [Documentation Generation](#39-documentation-generation)
40. [Dependency Management](#40-dependency-management)
41. [Migration Tools](#41-migration-tools)
42. [Mirroring](#42-mirroring)
43. [Archive & Backup](#43-archive--backup)
44. [Network Resilience](#44-network-resilience)
45. [Offline Mode](#45-offline-mode)
46. [Search](#46-search)
47. [Log Query Language](#47-log-query-language)
48. [Blame & History Intelligence](#48-blame--history-intelligence)
49. [Diff Engine](#49-diff-engine)
50. [Bisect Automation](#50-bisect-automation)
51. [Statistics & Analytics](#51-statistics--analytics)
52. [Repository Size Management](#52-repository-size-management)
53. [Sparse Checkout](#53-sparse-checkout)
54. [Shallow Clone Management](#54-shallow-clone-management)
55. [Bundle Support](#55-bundle-support)
56. [Patch Workflow](#56-patch-workflow)
57. [Snapshot / Checkpoint](#57-snapshot--checkpoint)
58. [Time Tracking](#58-time-tracking)
59. [Snippet Manager](#59-snippet-manager)
60. [Dotfile Management](#60-dotfile-management)
61. [Workspace Management](#61-workspace-management)
62. [Repo Discovery & Index](#62-repo-discovery--index)
63. [Repo Linking](#63-repo-linking)
64. [Feature Branch Tracking](#64-feature-branch-tracking)
65. [Stacked PRs / Patch Queue](#65-stacked-prs--patch-queue)
66. [Multi-Identity Management](#66-multi-identity-management)
67. [Configuration Profiles](#67-configuration-profiles)
68. [Environment File Management](#68-environment-file-management)
69. [Conflict Prevention](#69-conflict-prevention)
70. [Pre-Flight Checks](#70-pre-flight-checks)
71. [Change Risk Assessment](#71-change-risk-assessment)
72. [Repository Compliance Policies](#72-repository-compliance-policies)
73. [Commit Verification & Audit](#73-commit-verification--audit)
74. [Repository Anomaly Detection](#74-repository-anomaly-detection)
75. [Background Maintenance](#75-background-maintenance)
76. [Scheduled Operations](#76-scheduled-operations)
77. [Notifications & Inbox](#77-notifications--inbox)
78. [Shell Integration](#78-shell-integration)
79. [Custom Commands & Plugins](#79-custom-commands--plugins)
80. [Terminal Sharing & Pair Programming](#80-terminal-sharing--pair-programming)
81. [Container Registry Integration](#81-container-registry-integration)
82. [Semantic Versioning Intelligence](#82-semantic-versioning-intelligence)
83. [Test Impact Analysis](#83-test-impact-analysis)
84. [Database Migration Awareness](#84-database-migration-awareness)
85. [Protocol Debugging](#85-protocol-debugging)
86. [Git Internals Inspection](#86-git-internals-inspection)
87. [CLI Interface](#87-cli-interface)
88. [TUI Interface](#88-tui-interface)
89. [GUI Interface](#89-gui-interface)
90. [Server — httpd](#90-server--httpd)
91. [Server — sshd](#91-server--sshd)
92. [Server — gitd](#92-server--gitd)
93. [Web UI](#93-web-ui)
94. [Gitea-Compatible API](#94-gitea-compatible-api)
95. [CI Config Translation](#95-ci-config-translation)
96. [Crate Structure](#96-crate-structure)
97. [Dependencies](#97-dependencies)
98. [Release Binaries](#98-release-binaries)
99. [Version 1.0.0 Scope](#99-version-100-scope)
100. [Complete Command Reference](#100-complete-command-reference)

---

## 1. Project Overview

**gitriven** is a unified developer workflow tool built in Rust that provides a complete git implementation at its core, extended with comprehensive repository management, collaboration, code quality, security, compliance, deployment, and developer productivity features — all in a single static binary.

### Name & Etymology

"Riven" — Old Norse origin, meaning split, torn apart, forked. A metaphor for git's branching model. "git" + "riven" = gitriven.

### What gitriven Replaces

- **git** — complete VCS implementation via gix (gitoxide)
- **gh / glab / tea** — multi-provider CLI (GitHub, GitLab, Gitea, Forgejo, Codeberg, Gogs, Bitbucket, Azure DevOps, AWS CodeCommit)
- **lazygit** — terminal UI (ratatui)
- **GitKraken** — native GUI (egui)
- **gitweb / cgit** — repository web browser (axum, HTML5/CSS, no JavaScript)
- **git-crypt** — encrypted files in repos
- **git-lfs** — large file storage (automatic, no manual setup)
- **pre-commit / husky** — hooks framework
- **conventional-commits tools** — commit message enforcement
- **gitleaks / trufflehog** — secret scanning
- **git-credential-manager** — credential storage (encrypted SQLite)
- **prettier / eslint / shellcheck runners** — format/lint orchestration
- **git-town / git-flow** — workflow automation
- **repo / git-subrepo** — multi-repo management
- **github-backup / ghorg** — archival and bulk clone
- **BFG Repo-Cleaner** — history rewriting
- **git-absorb** — smart fixup

### What gitriven Is NOT

- An IDE or editor
- A CI/CD server
- A package manager (detects them, doesn't replace them)
- A full SAST/DAST security scanner
- A project management tool (no kanban, no sprints)
- A code review hosting platform (creates/participates in PRs, doesn't host the review UI)

### Core Principle

**Default behavior = git-identical with enhanced outcomes.** Any script, CI/CD pipeline, Makefile, or automation that calls `git <command>` works identically with gitriven. Same exit codes, same stdout/stderr format, same flags. The enhanced behavior (auto-stash, guided resolution, better errors, secret scanning) is always active. TTY detection adjusts output formatting (interactive vs scripted) but never changes the resulting git state. If you swap `git` for `gitriven` in any existing workflow, things either work identically or work better. Never worse, never broken.

### Smart = Logic, NOT AI

All intelligence in gitriven is deterministic, logic-based. No AI/ML models, no API calls to language models, no neural networks. "Smart" means well-engineered conditional logic, pattern matching, heuristics, and sensible defaults.

---

## 2. Brand Identity

### Colors

| Name | Hex | Usage |
|------|-----|-------|
| Dark | `#0D1117` | Backgrounds, dark theme |
| Teal | `#2CADA8` | Primary accent, "git" in wordmark |
| Amber | `#E8922F` | Secondary accent, Rust language nod |

### Typography

| Role | Font | Fallback |
|------|------|----------|
| Display | Tektur | system sans-serif |
| Monospace | JetBrains Mono | ui-monospace, Cascadia Code, Source Code Pro, Menlo, Consolas, DejaVu Sans Mono, monospace |
| Sans-serif | Work Sans | -apple-system, BlinkMacSystemFont, Segoe UI, Noto Sans, Helvetica, Arial, sans-serif |

### Logo

Trunk splitting into two diverging branches with teal and amber gradients. Wordmark: "git" in teal, "riven" in white (dark backgrounds) or dark (light backgrounds).

### Name Availability (Verified Clean)

GitHub, crates.io, npm, domains — all available at time of specification.

---

## 3. Architecture

### Four Interfaces, One Binary

| Interface | Technology | Activation |
|-----------|-----------|------------|
| CLI | clap | Default. Standard command-line operation. |
| TUI | ratatui + crossterm | Auto-launches on SSH/mosh/telnet sessions, or via `--tui` flag |
| GUI | egui / eframe | Auto-launches when display server detected ($DISPLAY / Wayland), or via `--gui` flag |
| Server | axum | Via `gitriven serve` command |

### Environment Detection

```
SSH_CONNECTION or SSH_TTY or SSH_CLIENT set  → TUI
MOSH_CONNECTION set                          → TUI
TERM = "screen" or "tmux"                    → TUI (already in multiplexer)
DISPLAY set or WAYLAND_DISPLAY set           → GUI
None of the above                            → TUI
```

### Override Flags

| Flag | Behavior |
|------|----------|
| `--cli` | Force CLI mode, no TUI/GUI |
| `--tui` | Force TUI mode |
| `--gui` | Force GUI mode |
| `--no-tui` | Prevent TUI auto-launch |
| `--no-gui` | Prevent GUI auto-launch |
| `--no-smart` | Force script-safe mode even in TTY |
| `--smart` | Force interactive mode even in pipe |

### TTY Detection

- `isatty(stdout)` AND `isatty(stderr)` → interactive mode (full smart features, progress bars, color, prompts)
- Either piped/redirected → script-safe mode (pure git-compatible output, no prompts, no extra output)

---

## 4. Binary & Distribution

### Name-Agnostic Binary

The binary reads `argv[0]` at startup, strips the path, and adapts all user-facing output to the detected name.

**What adapts to `argv[0]`:**
- All help text: `Usage: {name} [options] [commands]`
- Error messages: `{name}: fatal: not a git repository`
- Subcommand references in suggestions
- Shell completions generation
- Credential helper registration
- Version output
- Man page references

**What stays hardcoded "gitriven":**
- Config directory path (always `gitriven/` regardless of binary name)
- Data directory path
- Cache directory path
- Internal stash/checkpoint markers (reflog prefixes)
- User-Agent for API calls
- Project branding in `about` command

### Multicall / Symlink Detection

BusyBox-style `argv[0]` detection. Known multicall names are matched by filename:

| argv[0] filename | Behavior |
|-----------------|----------|
| `git` | Full command router (drop-in replacement) |
| `gitriven` (or any unknown name) | Full command router |
| `gitcommit` | Smart commit subcommands |
| `gitadmin` | Admin/repo management subcommands |
| `gitignore` | Ignore subcommands |
| `gitmerge` | Smart merge subcommands |
| `gist` | Gist subcommands |

Multicall names matched by suffix — `my-gitcommit` or `/opt/gitcommit` also work.

### Symlink Setup

```bash
gitriven setup --symlinks                    # create all multicall symlinks
gitriven setup --symlinks --prefix /usr/local/bin
gitriven setup --alias                       # shell aliases instead of symlinks
```

`setup --symlinks` reads its own binary path and creates symlinks pointing back to itself. Detects and warns before overwriting existing targets.

### Deployment Scenarios

**Drop-in replacement:**
```bash
mv gitriven /usr/local/bin/git
```

**Parallel install:**
```bash
cp gitriven /usr/local/bin/gitriven
ln -s gitriven /usr/local/bin/gitcommit
ln -s gitriven /usr/local/bin/gitadmin
ln -s gitriven /usr/local/bin/gitignore
```

**Full takeover:**
```bash
cp gitriven /usr/local/bin/gitriven
ln -s gitriven /usr/local/bin/git
ln -s gitriven /usr/local/bin/gitcommit
ln -s gitriven /usr/local/bin/gitadmin
ln -s gitriven /usr/local/bin/gitignore
```

**Custom name:**
```bash
cp gitriven /usr/local/bin/vcs
# Works. Help says "Usage: vcs [options]..."
```

### Release Binary Matrix

**Naming convention:** `gitriven-{platform}-{arch}` (Windows: `.exe` suffix)

| Binary | Platform | Arch | Target |
|--------|----------|------|--------|
| `gitriven-linux-amd64` | Linux | x86_64 | x86_64-unknown-linux-musl |
| `gitriven-linux-arm64` | Linux | aarch64 | aarch64-unknown-linux-musl |
| `gitriven-linux-armv7` | Linux | armv7 | armv7-unknown-linux-musleabihf |
| `gitriven-linux-riscv64` | Linux | riscv64 | riscv64gc-unknown-linux-musl |
| `gitriven-macos-amd64` | macOS | x86_64 | x86_64-apple-darwin |
| `gitriven-macos-arm64` | macOS | Apple Silicon | aarch64-apple-darwin |
| `gitriven-freebsd-amd64` | FreeBSD | x86_64 | x86_64-unknown-freebsd |
| `gitriven-windows-amd64.exe` | Windows | x86_64 | x86_64-pc-windows-msvc |
| `gitriven-windows-arm64.exe` | Windows | aarch64 | aarch64-pc-windows-msvc |

- Linux: static linked with musl, stripped
- All binaries stripped (`strip = true` in cargo profile)
- No runtime dependencies, no config files required, no install process

### Embedded in Binary

- All HTML templates and CSS for web UI
- All .gitignore templates (GitHub's collection)
- All community file templates (CONTRIBUTING, CODE_OF_CONDUCT, SECURITY, etc.)
- All hook templates
- All license templates (MIT, Apache-2.0, GPL-3.0, BSD-2-Clause, BSD-3-Clause, ISC, MPL-2.0, LGPL, AGPL, Unlicense, WTFPL)
- Spell check dictionary with technical terms
- Default vulnerability database (updatable at runtime)

---

## 5. Configuration System

### Directory Layout (Platform-Aware)

| Platform | Config | Data | Cache |
|----------|--------|------|-------|
| Linux | `~/.config/gitriven/` | `~/.local/share/gitriven/` | `~/.cache/gitriven/` |
| macOS | `~/Library/Application Support/gitriven/` | `~/Library/Application Support/gitriven/` | `~/Library/Caches/gitriven/` |
| Windows | `%APPDATA%\gitriven\` | `%LOCALAPPDATA%\gitriven\` | `%LOCALAPPDATA%\gitriven\cache\` |

Respects XDG overrides on Linux (`$XDG_CONFIG_HOME`, `$XDG_DATA_HOME`, `$XDG_CACHE_HOME`).

Directory paths always use `gitriven/` regardless of binary name.

### Config Directory Contents

```
{config}/
├── config.toml              # main configuration
├── profiles.toml            # identity profiles
├── workspaces.toml          # workspace definitions
├── dotfiles.toml            # dotfile repo tracking
├── policy.toml              # org-level compliance policy
├── mirrors.toml             # global mirror relationships
```

### Data Directory Contents

```
{data}/
├── credentials.db           # encrypted SQLite credentials store
├── repos.db                 # repo index database
├── audit.log                # operation audit trail
├── server.pid               # server PID + ports
├── ssh_host_ed25519         # server SSH host key
├── authorized_keys          # server SSH authorized keys
├── templates/               # user-created project templates
├── snippets/                # saved code snippets
├── hooks/                   # user-installed hook scripts
├── commands/                # custom command scripts
├── dictionary.txt           # user-added spell check words
├── health-history/          # repo health score history
```

### Cache Directory Contents

```
{cache}/
├── ignore-templates/        # downloaded .gitignore templates
├── api-cache/               # API response cache
├── search-index/            # cross-repo search index
├── vuln-db/                 # vulnerability database
├── commit-graph-cache/      # commit graph optimization data
```

### Full Config File Reference

```toml
[global]
host = "0.0.0.0"
log_level = "info"                          # trace, debug, info, warn, error

[httpd]
enabled = true
port = 65042                                # auto-assigned on first run, persisted
root = ""                                   # repo root for serving
tls = false
tls_cert = ""
tls_key = ""
api = true                                  # enable Gitea-compatible API
api_token = ""                              # if set, require token for API access
api_readonly = false

[sshd]
enabled = false
port = 65043                                # auto-assigned when enabled, persisted
host_key = ""                               # auto-generated on first enable
authorized_keys = ""

[gitd]
enabled = false
port = 65044                                # auto-assigned when enabled, persisted
export_all = false

[credentials]
keychain = true                             # use OS keychain for master key
cache_ttl = "8h"                            # memory cache TTL when no keychain
env_precedence = true                       # env vars override database

[signing]
enabled = true
method = "ssh"                              # "ssh" or "gpg"
key = "~/.ssh/id_ed25519"
auto_passphrase = true                      # use stored passphrase from credentials db

[lfs]
auto = true
threshold = "50MB"
always_fetch = true
patterns = []                               # always LFS regardless of size

[submodules]
auto = true
auto_init = true
auto_update = true
auto_push = true
recurse_depth = 10
warn_dirty = true
warn_unpushed = true

[recursive]
exclude = []                                # glob patterns to exclude
scan_depth = 5
jobs = 0                                    # 0 = CPU core count

[clone]
base_dir = "~/Projects"
pattern = "{provider}/{owner}/{repo}"

[providers]
# Custom provider mappings for self-hosted instances
# "git.example.com" = "gitea"
# "gitlab.work.com" = "gitlab"

[notifications]
enabled = true
threshold = "30s"                           # notify if operation takes longer
sound = false
desktop = true

[shell]
auto_fetch = true
auto_fetch_interval = "15m"

[format]
enabled = true
on_commit = true
staged_only = true
auto_suggest_install = true

[risk]
critical_paths = []
high_churn_threshold = 20
large_change_threshold = 500

[registries]
# Container registry configurations
# "ghcr.io" = { type = "ghcr", auth = "github" }
# "docker.io" = { type = "dockerhub", auth = "credentials" }
```

### Git Config Compatibility

gitriven reads and honors the entire git config chain:

1. `/etc/gitconfig` (system)
2. `~/.gitconfig` or `~/.config/git/config` (global)
3. `.git/config` (repo-level)
4. `.git/config.worktree` (worktree-level)
5. `GIT_CONFIG_*` environment variables

Every section, every key — `[user]`, `[core]`, `[remote]`, `[branch]`, `[merge]`, `[diff]`, `[pull]`, `[push]`, `[fetch]`, `[credential]`, `[alias]`, `[color]`, `[init]`, `[url]`, `[http]`, `[https]`, `[ssh]`, `[gpg]`, `[commit]`, `[tag]`, `[rerere]`, `[rebase]`, `[stash]`, `[status]`, `[log]`, `[format]`, `[filter]`, `[includeIf]`, `[safe]`, and any custom or third-party sections.

gitriven also supports a `[gitriven]` section in `.gitconfig` for users who prefer everything in one file:

```gitconfig
[gitriven]
    smart = true
    lfs-auto = true
    lfs-threshold = 50MB
    default-provider = github
```

### Config Commands

```bash
gitriven config import                      # read .gitconfig, validate, map to gitriven config
gitriven config export                      # write gitriven settings back to .gitconfig format
gitriven config show                        # merged view of all config sources with origin labels
gitriven config edit [--global|--system|--local]  # open config in editor
gitriven config team show                   # display repo-level .gitriven/config.toml
gitriven config team enforce                # validate local setup matches team config
```

### Per-Repo Config

`.gitriven/` directory in repo root — team-shared gitriven configuration. Auto-applied on clone.

```
.gitriven/
├── config.toml              # team settings (branch naming, protection, etc.)
├── format.toml              # format/lint configuration
├── release.toml             # release pipeline config
├── deploy.toml              # deploy environments
├── hooks.toml               # hook configuration
├── webhooks.toml            # webhook listeners
├── mirrors.toml             # mirror relationships
├── linked.toml              # linked repos
├── policy.toml              # compliance policy
├── changelog.toml           # changelog generation config
├── dictionary.txt           # project-specific spell check words
├── templates/               # commit message templates
│   ├── default.txt
│   ├── feature.txt
│   └── hotfix.txt
├── commands/                # team-shared custom commands
```

---

## 6. Git Compatibility Layer

### Complete Command Coverage

gitriven implements every git porcelain and plumbing command with full flag compatibility via the gix (gitoxide) crate ecosystem.

**Porcelain commands (all flags from git man pages supported):**

init, clone, add, commit, push, pull, fetch, merge, rebase, reset, checkout, switch, restore, tag, stash, branch, remote, log, diff, show, status, clean, mv, rm, bisect, blame, cherry-pick, revert, notes, describe, shortlog, grep, archive, bundle, format-patch, am, apply, gc, prune, reflog, fsck, worktree, submodule, subtree, lfs

**Plumbing commands:**

cat-file, hash-object, update-index, write-tree, commit-tree, read-tree, ls-tree, ls-files, rev-parse, rev-list, for-each-ref, update-ref, symbolic-ref, merge-base, diff-tree, diff-files, diff-index, pack-objects, unpack-objects, index-pack, verify-pack, count-objects, show-ref, name-rev, check-ref-format, var

### Exit Code Compatibility

All exit codes match git exactly:
- 0: success
- 1: general failure / diff found changes
- 128: fatal error
- 129+: killed by signal

### Output Compatibility

In script-safe mode (no TTY), output format is byte-identical to git. In interactive mode, additional information may be appended after the standard output (never replacing it).

---

## 7. Smart Operations Engine

All smart features are always active. They enhance the experience without changing the resulting git state.

### Smart Pull

1. Detect dirty working tree
2. Auto-stash with meaningful message: `gitriven:auto-stash on {branch} before pull`
3. Pull (fetch + merge/rebase per config)
4. Auto-pop stash
5. If LFS pointers changed, auto-fetch LFS objects
6. If submodule refs changed, auto-update submodules
7. If lockfile changed, notify: `⚠ Cargo.lock changed — consider running cargo build`
8. Handle conflicts gracefully with clear options

### Smart Error Detection & Auto-Fix

| Condition | Action |
|-----------|--------|
| Diverged branches | Offer rebase/merge/force push options |
| Detached HEAD | Offer branch creation before losing commits |
| Merge conflicts | Auto-resolve trivial (whitespace, import ordering), guided resolution for others |
| Broken refs | Detect and offer fsck + repair |
| Stale tracking branches | Auto-prune or suggest |
| Permission issues | Detect SSH key problems, suggest fixes |
| Large file detection | Warn before commit, suggest LFS or .gitignore |
| Credential failures | Detect expired tokens, guide re-auth |
| Wrong branch | Warn before committing to main/master directly |
| Empty commit | Detect and warn instead of silently succeeding |
| Submodule not pushed | Block parent push with clear explanation |
| LFS pointer without push | Detect and warn |

### Better Error Messaging

- Plain-language errors (technical detail via `--verbose`)
- "Did you mean?" suggestions for typos (Levenshtein distance matching)
- Context-aware hints
- Color-coded severity (warning/error/info) when TTY
- Links to relevant documentation
- Auto-diagnose network failures (run relevant checks from `gitriven doctor`)

---

## 8. Commit Workflows

### Standard Git Commit

`gitriven commit -m "message"` works identically to `git commit -m "message"`. All standard flags supported.

### Smart Commit Subcommands

**Status-filtered commits (stage only matching files):**

| Command | Behavior |
|---------|----------|
| `gitriven commit all` | Stage everything, commit |
| `gitriven commit modified` | Stage only modified files, commit |
| `gitriven commit deleted` | Stage only deleted files, commit |
| `gitriven commit added` | Stage only added/new files, commit |
| `gitriven commit renamed` | Stage only renamed files, commit |
| `gitriven commit restored` | Stage only restored files, commit |
| `gitriven commit files` | Interactive — commit based on status grouping |
| `gitriven commit spelling` | Commit with "fix: spelling corrections" message |

**Semantic commit types (conventional commit format):**

| Command | Generated Prefix |
|---------|-----------------|
| `gitriven commit new "description"` | `feat: description` |
| `gitriven commit improved "description"` | `improve: description` |
| `gitriven commit fixes "description"` | `fix: description` |
| `gitriven commit release "description"` | `release: description` |
| `gitriven commit deploy "description"` | `deploy: description` |
| `gitriven commit docs "description"` | `docs: description` |
| `gitriven commit test "description"` | `test: description` |
| `gitriven commit breaking "description"` | `breaking: description` |
| `gitriven commit refactor "description"` | `refactor: description` |
| `gitriven commit performance "description"` | `perf: description` |
| `gitriven commit permissions "description"` | `fix(permissions): description` |
| `gitriven commit bugs "description"` | `fix(bug): description` |

Without a message, auto-generates one from changed files.

### Commit Intelligence

- Scope suggestion based on changed files
- Conventional commit enforcement (optional, per-repo config)
- Empty diff detection (warn on whitespace-only changes)
- Commit splitting assistance (interactive mode)
- Spell check on commit messages (built-in dictionary, project-specific dictionary)
- Commit message templates per branch pattern

### Fixup & Squash

```bash
gitriven fixup                              # amend last commit, auto-skip version bump commits
gitriven squash [N] [message]               # squash last N commits (default: 2)
```

### Git Absorb

```bash
gitriven absorb                             # auto-assign staged changes to the correct prior commit
```

Analyzes staged changes, determines which prior commit each change logically belongs to, creates fixup commits, and auto-squashes them into the right places. Replaces the manual `git commit --fixup <sha>` → `git rebase -i --autosquash` workflow.

### Coauthoring

```bash
gitriven commit --coauthor "Name <email>"
gitriven coauthors add <alias> "Name <email>"
gitriven commit --coauthor @alias
```

Adds `Co-authored-by` trailer to commit message. Saved coauthors stored in config.

### Commit Message Templates

Templates in `.gitriven/templates/`:

```
.gitriven/templates/
├── default.txt              # default template
├── feature.txt              # for feature/* branches
├── hotfix.txt               # for hotfix/* branches
```

Branch pattern matching: any glob maps to a template. Templates support variables: `{branch}`, `{date}`, `{author}`, `{ticket}` (extracted from branch name like `feature/JIRA-123-description`).

---

## 9. Merge & Rebase Engine

### Smart Merge

```bash
gitriven merge <branch>                     # auto-picks best strategy
gitriven merge <branch> --strategy ff       # force fast-forward
gitriven merge <branch> --strategy no-ff    # force merge commit
gitriven merge <branch> --strategy squash   # squash merge
```

Auto-strategy logic:
1. If fast-forward possible and no merge commit needed → fast-forward
2. If fast-forward possible but branch has multiple commits → merge commit (preserves topology)
3. If not fast-forward → merge commit with conflict handling

Before merge: auto-stash dirty working tree, auto-checkpoint for undo safety.

### Merge Resolution

```bash
gitriven merge-resolve status               # show all conflicted files
gitriven merge-resolve show <file>          # view conflicts in file
gitriven merge-resolve edit <file>          # open in editor, validate after save
gitriven merge-resolve ours <file>          # keep current branch version, auto-stage
gitriven merge-resolve theirs <file>        # keep incoming version, auto-stage
gitriven merge-resolve abort                # abort the merge
```

Auto-resolve trivial conflicts: whitespace-only, import ordering. Validate after manual edits — check that no conflict markers remain.

### Custom Merge Drivers

```bash
gitriven merge-driver add <name> <pattern> <command>
```

Built-in drivers for conflict-prone files:
- `package-lock.json` — regenerate instead of merge
- `Cargo.lock` — regenerate instead of merge
- `*.pbxproj` (Xcode) — union merge
- `CHANGELOG.md` — take both sides, sort by date
- `*.po` (translations) — merge by msgid

### Smart Rebase

```bash
gitriven rebase <branch>                    # auto-stash, rebase, pop, handle conflicts
gitriven rebase --onto <target> <from> <to> # with plain English confirmation
gitriven rebase --interactive               # enhanced in TUI: drag-and-drop reorder, live preview
```

Auto-checkpoint before rebase. Detect when rebase will definitely conflict and preview which files.

### Rerere (Reuse Recorded Resolution)

Enabled by default. When a conflict is resolved, gitriven remembers the resolution. Next time the same conflict appears, auto-resolved silently.

```bash
gitriven rerere list                        # show recorded resolutions
gitriven rerere forget <path>               # forget a bad resolution
gitriven rerere export / import             # share resolutions with team
```

### Auto-Merge / Merge Queue

```bash
gitriven pr create --auto-merge             # merge when CI + approvals met
gitriven pr merge --when-ready              # queue merge, monitor status
gitriven merge-queue add <branch>           # queue for sequential merge into main
```

---

## 10. Undo System

```bash
gitriven undo                               # undo last operation
gitriven undo --list                        # show recent operations
gitriven undo --steps 3                     # undo multiple
```

Works for: commits, merges, rebases, branch deletes, stash drops, tag deletes, cherry-picks, reverts, resets.

Under the hood: reflog + recorded operation history in `gitriven history`.

### Human-Readable History

```bash
gitriven history                            # "2 hours ago: merged feature/auth into main"
gitriven history search "deleted branch"
```

Visual timeline in TUI/GUI.

---

## 11. Recursive Operations Engine

First-class multi-repo operations across any git command:

```bash
gitriven --recursive ~/Projects pull
gitriven --recursive ~/Projects --exclude "vendor/*" --jobs 8 fetch
gitriven --recursive ~/Projects log --since "today"
gitriven --recursive ~/Projects stash list
```

- **Discovery:** Scans for `.git` directories, respects `--exclude` globs
- **Parallelism:** Default = CPU core count, configurable via `--jobs`
- **Progress:** Multi-line indicatif display with per-repo status
- **Persistent excludes** in config.toml

---

## 12. API Client Layer

### Supported Providers

| Provider | Type Name | Default Server | Auth Env Var |
|----------|-----------|----------------|--------------|
| GitHub | `github` | api.github.com | `GITHUB_TOKEN` |
| GitLab | `gitlab` | gitlab.com | `GITLAB_TOKEN` |
| Gitea | `gitea` | (requires --api-server) | `GITEA_TOKEN` |
| Forgejo | `forgejo` | (requires --api-server) | `FORGEJO_TOKEN` |
| Codeberg | `codeberg` | codeberg.org | `CODEBERG_TOKEN` |
| Gogs | `gogs` | (requires --api-server) | `GOGS_TOKEN` |
| Bitbucket | `bitbucket` | bitbucket.org | `BITBUCKET_TOKEN` |
| Azure DevOps | `azure` | dev.azure.com | `AZURE_TOKEN` |
| AWS CodeCommit | `aws` | (region-based) | `AWS_ACCESS_KEY_ID` + `AWS_SECRET_ACCESS_KEY` |
| OpenGist | `opengist` | (requires --api-server) | `OPENGIST_TOKEN` |
| gitriven | `gitea` | (any gitriven server) | (per-server token) |

Codeberg and Gogs use the Gitea API (compatible) with different default endpoints. gitriven's own server exposes a Gitea-compatible API, making it a valid provider.

### Auth Management

```bash
gitriven auth login [--api-type github]     # interactive auth flow
gitriven auth status                        # show all stored credentials
gitriven auth refresh <provider>            # re-authenticate
gitriven auth logout [--api-type]           # remove credentials
gitriven auth export --env                  # output as env vars
gitriven auth import --env                  # import from env vars
```

Environment variables take precedence over credentials database (CI/CD friendly).

### Bulk Clone

```bash
gitriven clone --user <username>            # all personal repos + owned org repos
gitriven clone --org <orgname>              # all repos in org
gitriven clone --user <username> --all-orgs # include all owned orgs
```

**Directory structure:** `{base_dir}/{provider}/{owner}/{repo}`
Default: `~/Projects/github/jason/gitriven/`

Custom provider mappings in config.toml.

### Provider Detection

Priority order:
1. Explicit `--api-type` flag
2. Remote URL pattern matching
3. Git remote URL in current repo
4. Directory path pattern matching
5. Default from config

### Unsupported Operations

If a provider doesn't support an operation (e.g., gists on Gogs), silently skip. No error, no warning. Bulk operations across providers skip unsupported providers and keep going.

---

## 13. Provider Management

### Repo Management

```bash
gitriven repo create <owner/repo> [description] [--private|--public]
gitriven repo delete <owner/repo>
gitriven repo modify <owner/repo> [--description] [--homepage]
gitriven repo list [--user <name>] [--org <name>]
gitriven repo visibility <owner/repo> --private|--public
gitriven repo view [owner/repo]
gitriven repo fork <owner/repo> [--clone]
gitriven repo archive <owner/repo>
```

All inherit `--api-type`, `--api-server`, and token config.

### Org Management

```bash
gitriven org list
gitriven org repos <orgname>
gitriven org clone <orgname> [--all-orgs]
gitriven org push|pull <orgname> [--all-orgs]
gitriven org visibility show|public|private
```

### User Management

```bash
gitriven user repos [username]
gitriven user clone [username] [--all-orgs]
gitriven user push|pull [username] [--all-orgs]
```

### SSH Key Management

```bash
gitriven ssh list
gitriven ssh add <keyfile> [--title]
gitriven ssh delete <id>
```

### Release & Tag Management

```bash
gitriven release create <version> [message]
gitriven release delete <owner/repo>
gitriven release delete --user <name> [--all-orgs]
gitriven release list [owner/repo]
gitriven tag add <name> [message]
gitriven tag remove <name> [--remote]
```

---

## 14. Pull Request & Code Review

```bash
gitriven pr create [--title] [--body] [--base] [--draft] [--reviewer]
gitriven pr list [--state open|closed|merged|all]
gitriven pr view <number>
gitriven pr checkout <number>
gitriven pr merge <number> [--strategy merge|squash|rebase] [--delete-branch]
gitriven pr close <number>
gitriven pr diff <number>
gitriven pr review <number> [--approve|--comment|--request-changes]
gitriven pr create --auto-merge
```

### Code Review from Terminal

```bash
gitriven review <pr-number>                 # walk through diff in TUI
gitriven review comment <file> <line> "msg"
gitriven review approve|request-changes|comment <pr-number>
gitriven review pending                     # PRs awaiting your review (all providers)
gitriven review mine                        # your open PRs and their status
```

### Multi-Remote / Fork Workflow

```bash
gitriven upstream set <url>
gitriven upstream sync                      # fetch upstream, merge/rebase, push to fork
```

`gitriven pr create` auto-detects fork → upstream relationship.

### Provider Terminology

`gitriven pr` works on all providers. GitHub says "Pull Request", GitLab says "Merge Request" — gitriven translates internally.

---

## 15. Issue Management

```bash
gitriven issue list [owner/repo]
gitriven issue count [owner/repo]
gitriven issue create [owner/repo]
gitriven issue edit <id>
```

---

## 16. Gist Operations

### Providers

| Provider | Gist Equivalent | Supported |
|----------|----------------|-----------|
| GitHub | Gists | ✓ |
| GitLab | Snippets | ✓ |
| Bitbucket | Snippets | ✓ |
| OpenGist | Gists | ✓ |
| Others | — | skip |

### Commands

```bash
gitriven gist list [username]
gitriven gist clone <id> [directory]
gitriven gist create [--public|--private]
gitriven gist delete <id>
gitriven gist search <query>
gitriven gist edit <id>
```

---

## 17. CI/CD Integration

### Status & Logs

```bash
gitriven ci status                          # CI status for current branch
gitriven ci logs [run-id]                   # stream CI logs
gitriven ci retry [run-id]                  # re-trigger failed run
gitriven ci wait                            # block until CI completes
gitriven ci cancel [run-id]
gitriven ci badge                           # generate markdown badge
```

### Workflow Runs

```bash
gitriven run list
gitriven run view <id>
gitriven run watch <id>                     # live tail
gitriven run rerun <id>
gitriven run cancel <id>
```

---

## 18. Release Automation

`gitriven release create <version>` executes a full pipeline:

1. Validate version (semver, no duplicates)
2. Run pre-release checks (tests, format, lint) if configured
3. Generate changelog from conventional commits
4. Bump version in project files (auto-detected: Cargo.toml, package.json, pyproject.toml, etc.)
5. Update third-party licenses in LICENSE.md
6. Commit version bump
7. Create signed tag
8. Push commit + tag
9. Create release on provider with changelog as release notes
10. Attach SBOM if configured
11. Tag and push container image if configured
12. Trigger release workflow if configured

```bash
gitriven release dry-run <version>          # preview without executing
gitriven release undo                       # revert release
```

### Config

```toml
# .gitriven/release.toml
[release]
version_files = ["Cargo.toml", "package.json"]
changelog = true
sbom = true
sign = true
tests = "cargo test"
pre_release = ["cargo fmt --check", "cargo clippy"]
```

---

## 19. Deploy Hooks

```bash
gitriven deploy <environment>
gitriven deploy status
gitriven deploy rollback
```

### Config

```toml
# .gitriven/deploy.toml
[[environments]]
name = "staging"
branch = "staging"
webhook = "https://deploy.example.com/staging"

[[environments]]
name = "production"
branch = "main"
tag_pattern = "v*"
webhook = "https://deploy.example.com/production"
require_ci_pass = true
```

---

## 20. Branch Management

### Branch Hygiene

```bash
gitriven branches --stale                   # merged to main but not deleted
gitriven branches --orphan                  # no remote tracking
gitriven branches --cleanup                 # interactive cleanup
gitriven branches --age                     # sort by last activity
gitriven branches compare                   # ahead/behind matrix
gitriven branches graph                     # ASCII topology visualization
gitriven branches divergence <a> <b>        # detailed divergence analysis
```

### Branch Naming Enforcement

```toml
# .gitriven/config.toml
[branches]
pattern = "^(feature|bugfix|hotfix|release|chore)/[a-z0-9-]+$"
protected = ["main", "master", "develop", "release/*"]
max_age_days = 90
require_issue = false
```

`gitriven branch create "my branch"` auto-slugifies to `feature/my-branch`. Reject non-matching names with clear format example.

### Branch Renaming

```bash
gitriven branch rename <new-name>          # updates tracking, open PRs (via API), local refs
```

### Protected Branches (Local)

Direct commit to protected branch: warning + confirmation (interactive), block (non-interactive). Force push to protected branch: requires `--force-confirmed`. Delete protected branch: requires explicit confirmation. Override: `--no-protect`.

### Archive Branches

```bash
gitriven archive branch <branch>            # tag tip, delete branch, record metadata
gitriven archive restore <branch>           # bring back from tag
gitriven archive list                       # show archived branches
```

---

## 21. Stash Enhancement

- Every stash auto-named: `feature/auth: modified auth.rs, config.toml`
- `gitriven stash` with no args stashes everything including untracked
- `gitriven stash list` — meaningful names, age, branch, file count
- `gitriven stash show <name-or-index>` — preview diff
- `gitriven stash apply <name>` — apply by name not just index
- Stash expiry warning: stashes older than 30 days flagged in health check
- Cross-repo visibility: `gitriven --recursive ~/Projects stash list`

---

## 22. Worktree Management

```bash
gitriven worktree create <branch>           # sane default location: ../{repo}-{branch}/
gitriven worktree list                      # all worktrees with branch, status, dirty/clean
gitriven worktree remove <branch>
gitriven worktree switch <branch>           # cd into worktree (shell integration)
```

Auto-suggest worktree when checking out branch with uncommitted work.

---

## 23. Submodule Management

### Auto Submodule Behavior

- **On clone:** always recursive init + checkout. No missing submodule directories.
- **On pull:** auto-update submodules if pointers changed. No separate `git submodule update` step.
- **On checkout/switch:** auto-sync submodule state.
- **On status:** submodule dirty state always shown inline.
- **On commit:** warn if submodule has changes but pointer not updated.
- **On push:** detect and block if submodule commit not pushed to its remote.

### Auto-Repair

- Submodule URL dead: report which failed, complete rest of clone.
- Submodule pointing at nonexistent commit: `gitriven health` flags it. `gitriven sub repair` attempts resolution.
- Nested submodules: recursive with configurable depth limit (default: 10).

### Commands

```bash
gitriven sub add <repo> [path]
gitriven sub update
gitriven sub status
gitriven sub sync                           # init + update + foreach pull in one
gitriven sub remove <path>                  # full removal (deinit, rm, .gitmodules, .git/modules)
gitriven sub repair
```

---

## 24. Subtree Support

```bash
gitriven subtree add <repo> <prefix> [--branch]
gitriven subtree pull <prefix>
gitriven subtree push <prefix>
gitriven subtree list
gitriven subtree split <prefix>             # extract directory into own repo
```

Tracks relationships in `.gitriven/config.toml` so user doesn't need to remember remote URL and prefix.

---

## 25. LFS Auto Mode

### Automatic Behavior

- **On commit:** scan staged files against size threshold (default: 50MB). If exceeded, auto-track in `.gitattributes` and commit via LFS. One-line notice in output.
- **On clone:** always fetch LFS objects. No `git lfs install` dance, no `git lfs pull` after clone. Actual files, not pointer stubs.
- **On pull:** LFS objects fetched inline. No separate step.
- **Retroactive:** `gitriven health` flags large files in history. `gitriven lfs migrate <pattern>` rewrites history.

### Commands

```bash
gitriven lfs track <pattern>
gitriven lfs status
gitriven lfs migrate <pattern>
gitriven lfs prune
```

### Config

```toml
[lfs]
auto = true
threshold = "50MB"
always_fetch = true
patterns = ["*.bin", "*.model", "*.weights"]
```

Override: `--no-lfs` on any command.

---

## 26. Security & Credentials

### Credentials Database

Encrypted SQLite database at `{data}/credentials.db`. Single source of truth for all sensitive data.

**Stores:**
- API tokens per provider
- GPG/SSH signing key passphrases
- HTTP/HTTPS credentials per remote
- OAuth refresh tokens
- SSH key passphrases
- Profile-specific credentials
- SMTP credentials
- Container registry credentials

**Encryption:** AES-256-GCM, master key derived via Argon2id from user passphrase. Master passphrase cached in OS keychain (macOS Keychain, Linux libsecret/kwallet, Windows Credential Manager). Fallback: configurable TTL memory cache (default: 8h) via lightweight background agent.

### Schema

```sql
CREATE TABLE credentials (
    id          INTEGER PRIMARY KEY,
    type        TEXT NOT NULL,  -- api_token, signing_passphrase, http_auth, oauth, ssh_passphrase, smtp, registry
    provider    TEXT,           -- github, gitlab, gitea, etc.
    profile     TEXT,           -- profile name (NULL for default)
    server      TEXT,           -- hostname for self-hosted
    username    TEXT,
    secret      BLOB NOT NULL,  -- encrypted
    scopes      TEXT,
    expires_at  TEXT,
    created_at  TEXT NOT NULL,
    updated_at  TEXT NOT NULL,
    notes       TEXT
);
```

### Git Credential Helper

gitriven registers itself as a git credential helper:

```gitconfig
[credential]
    helper = gitriven credential-helper
```

Speaks standard git credential protocol (get/store/erase on stdin/stdout), reads from encrypted database. `gitriven setup` auto-configures this.

### Token Lifecycle

- Track expiration, warn before expiry
- `gitriven auth status` — metadata only, secrets never displayed
- `gitriven doctor` checks token validity and scopes

### CI/CD Mode

`--no-credential-db` global flag skips database entirely (pure env var mode).

---

## 27. Commit Signing

### Auto-Sign Behavior

If signing is configured in any config source (repo, global, gitriven config, or credentials database), every commit and tag is signed automatically. No flag needed, no prompt. If key requires passphrase and it's stored in credentials database, unlocked automatically.

### Setup

```bash
gitriven sign setup                         # interactive: detect keys, create if needed, configure
```

Recommends SSH signing as default (no GPG dependency, uses existing keys). Supports both GPG and SSH.

### Key Management

Multiple signing keys tied to profiles. Work profile uses work key, personal uses personal — auto-selected based on repo remote URL via identity config.

---

## 28. Secret Scanning

- Detect secrets/credentials in staged files before commit
- Built-in patterns: AWS, GitHub, GitLab, Stripe, Slack, generic API keys, private keys, connection strings
- Block commit by default if secrets detected
- Override: `--allow-secrets`
- `gitriven security scan` — scan full history for leaked secrets
- Runs as pre-commit hook, also part of pre-flight checks

---

## 29. Encrypted Files

```bash
gitriven encrypt track "*.env" "secrets/*.yaml"
gitriven encrypt add-key <user> <public-key>
gitriven encrypt status
```

Files encrypted on commit, decrypted on checkout via clean/smudge filters. Key management via credentials database. Compatible with standard git (`.gitattributes` integration).

---

## 30. Format & Lint Orchestration

### Detection: Config File Presence = Tool Relevant

gitriven does not guess. If a config file exists, that tool is relevant. If not, skip.

| Config File | Tool |
|-------------|------|
| `.shellcheckrc` | shellcheck |
| `.eslintrc` / `eslint.config.js` / `eslint.config.mjs` | eslint |
| `.prettierrc` / `prettier.config.js` | prettier |
| `.stylelintrc` / `stylelint.config.js` | stylelint |
| `.markdownlint.json` / `.markdownlintrc` | markdownlint |
| `.yamllint` / `.yamllint.yml` | yamllint |
| `.htmlhintrc` | htmlhint |
| `.editorconfig` | editorconfig (whitespace rules) |
| `.clang-format` | clang-format |
| `.clang-tidy` | clang-tidy |
| `rustfmt.toml` / `.rustfmt.toml` | rustfmt |
| `clippy.toml` / `.clippy.toml` | clippy |
| `.rubocop.yml` | rubocop |
| `.flake8` / `setup.cfg [flake8]` | flake8 |
| `pyproject.toml [tool.black]` | black |
| `pyproject.toml [tool.isort]` | isort |
| `pyproject.toml [tool.mypy]` | mypy |
| `pyproject.toml [tool.ruff]` | ruff |
| `.pylintrc` / `pyproject.toml [tool.pylint]` | pylint |
| `.php-cs-fixer.php` / `.php-cs-fixer.dist.php` | php-cs-fixer |
| `phpstan.neon` / `phpstan.neon.dist` | phpstan |
| `.golangci.yml` / `.golangci.yaml` | golangci-lint |
| `.hadolint.yaml` | hadolint |
| `.tflint.hcl` | tflint |
| `.sqlfluff` | sqlfluff |
| `biome.json` / `biome.jsonc` | biome |
| `deno.json` / `deno.jsonc` | deno fmt/lint |
| `.swiftlint.yml` | swiftlint |
| `.swiftformat` | swiftformat |
| `.ktlint` | ktlint |
| `detekt.yml` | detekt |
| `.credo.exs` | credo |
| `checkstyle.xml` | checkstyle |

### Execution

- Only staged files, never unstaged work
- Formatters first (modify), then linters (report)
- If formatter changes a file, auto-restage
- Linter errors = warnings by default, configurable to block
- Multi-project repos: per-directory detection
- Tool not installed → one-time suggestion, never nag
- Project's config files are the source of truth (respects `.prettierrc` settings, etc.)

### Commands

```bash
gitriven format check                       # dry run
gitriven format run                         # format staged files
gitriven format run --all                   # format entire repo
gitriven format install                     # suggest/install missing formatters
gitriven lint                               # lint staged files
gitriven lint --all                         # lint entire repo
```

### Config

```toml
# .gitriven/format.toml
[format]
enabled = true
on_commit = true
staged_only = true

[format.overrides]
"*.min.js" = false
"vendor/*" = false
"*.generated.*" = false

[lint]
enabled = true
block_on_error = false
block_on_warning = false
```

---

## 31. Hooks System

### Built-in Hooks

Ship with binary — no external dependencies:
- Lint check
- Conventional commit validation
- Secret scanning
- Large file detection
- WIP commit blocking
- Branch naming enforcement
- Conflict marker detection
- No-debug-statements check
- No-console-log check
- Require-tests-changed check

### Commands

```bash
gitriven hooks add pre-commit --lint rust
gitriven hooks add commit-msg --conventional
gitriven hooks add pre-push --no-wip
gitriven hooks init                         # recommended hooks for detected project type
gitriven hooks list
gitriven hooks browse                       # browse available templates
gitriven hooks install <name>               # install community hook
gitriven hooks export <name>                # share as TOML config
```

### Execution

- Hooks run in parallel where possible
- Hook execution time tracked — surface slow hooks
- `.gitriven/hooks.toml` for team-shared config, auto-applied on clone

---

## 32. Repository Health

### Health Check

```bash
gitriven health                             # full scan and report
```

Checks:
- Dangling objects, broken refs
- Oversized files in history (size + introducing commit)
- Stale branches (merged but not deleted, inactive)
- Missing .gitignore entries (tracked build artifacts)
- Submodule status
- Repo size breakdown (packfile efficiency, loose objects)
- Stale stashes (older than 30 days)
- Secrets in history
- Dependency vulnerabilities
- CODEOWNERS staleness
- Suggested maintenance actions

### Health Score

```bash
gitriven health score                       # 0-100 score
gitriven health report                      # detailed breakdown
gitriven health badge                       # generate badge for README
gitriven health history                     # score over time
gitriven health score --workspace casapps   # average across workspace
```

Scoring (configurable weights):

| Check | Points |
|-------|--------|
| Has .gitignore | +5 |
| Has LICENSE.md | +5 |
| Has README.md | +5 |
| Has CI configured | +10 |
| All commits signed | +10 |
| No secrets in history | +10 |
| No oversized files outside LFS | +10 |
| Branch hygiene | +10 |
| Dependencies up to date | +10 |
| No known vulnerabilities | +10 |
| Has .editorconfig | +5 |
| Commit message quality | +10 |

---

## 33. .gitignore Management

```bash
gitriven ignore add <templates...>          # section-aware merge, duplicate filtering
gitriven ignore save <templates...>         # create fresh .gitignore
gitriven ignore list                        # browse available templates
gitriven ignore search <query>              # search templates
gitriven ignore update                      # refresh local cache
gitriven ignore console <templates...>      # preview without writing
gitriven ignore --check                     # scan for tracked files that should be ignored
```

Ships GitHub's gitignore collection embedded in binary. Falls back to gitignore.io API. Local template directory: `{config}/templates/ignore/`.

---

## 34. .gitattributes Management

```bash
gitriven attrs init                         # generate from project detection
gitriven attrs add <pattern> <attributes>
gitriven attrs check                        # validate, flag missing entries
gitriven attrs linguist                     # show/override language stats
```

---

## 35. License Management

### Your Code License

```bash
gitriven license set MIT                    # generates/updates top section of LICENSE.md
gitriven license list                       # show available templates
```

Built-in templates: MIT, Apache-2.0, GPL-3.0, BSD-2-Clause, BSD-3-Clause, ISC, MPL-2.0, LGPL, AGPL, Unlicense, WTFPL.

### Third-Party Licenses

```bash
gitriven license third-party                # update third-party section in LICENSE.md
gitriven license check                      # verify all deps have identifiable licenses
gitriven license scan                       # list all dependency licenses, flag issues
gitriven license compatibility              # advisory report
```

Everything goes in one file: `LICENSE.md`. Top section = your license. Bottom section = third-party attributions. Deduplicated on every update — keyed by package name. Runs automatically as part of `gitriven release create`.

### LICENSE.md Structure

```markdown
# License

MIT License

Copyright (c) 2026 Jason Hempstead

[full license text]

---

# Third-Party Licenses

## clap (MIT/Apache-2.0)
Copyright (c) ...

## serde (MIT/Apache-2.0)
Copyright (c) ...
```

---

## 36. Community Files

Built-in templates embedded in binary, generated on demand with project-specific details auto-filled.

```bash
gitriven community init                     # generate all community files
gitriven community init --only contributing
gitriven community update                   # regenerate, preserve customizations
```

### Files Generated (in provider directory, never root)

```
.github/                        # or .gitea/ .forgejo/ .gitlab/
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md          # Contributor Covenant v2.1
├── SECURITY.md
├── FUNDING.yml                 # provider-specific format
├── ISSUE_TEMPLATE/
│   ├── bug_report.md
│   └── feature_request.md
└── PULL_REQUEST_TEMPLATE.md
```

### Customization Preservation

Templates use markers for generated vs custom sections:

```markdown
<!-- gitriven:start:development-setup -->
## Development Setup
1. Clone the repo
2. Run `cargo build`
<!-- gitriven:end:development-setup -->

## Our Custom Section
This was written by the team and won't be touched by gitriven.
```

`gitriven community update` only regenerates content between markers.

### Auto-Filled Variables

Project name, maintainer name/email, license type, default branch, project type, build/test/lint commands, supported versions, repo URL, issue tracker URL — all detected automatically from config and project files.

---

## 37. Project Scaffolding

```bash
gitriven new <name> --type rust|node|python|go|docker
gitriven new <name> --template <template-name>
gitriven template list
gitriven template create <name>             # save current repo as template
```

### What `gitriven new <name> --type rust` Creates

```
project/
├── .git/
├── .gitriven/
│   └── config.toml
├── .github/                    # or .gitea/ etc — provider-detected
│   └── workflows/
│       └── ci.yml
├── .editorconfig
├── .gitignore
├── src/
│   └── main.rs
├── Cargo.toml
├── LICENSE.md
└── README.md
```

Minimal. Every file has a reason. Provider directory auto-detected from configured default provider. CI stub appropriate for project type. Repo created on remote and pushed in one command.

---

## 38. Changelog Generation

```bash
gitriven changelog                          # auto-generate from conventional commits
gitriven changelog --since <tag>            # since last release
```

Groups by type: Features, Fixes, Breaking Changes, Performance, etc. Auto-runs during `gitriven release create`.

### Config

```toml
# .gitriven/changelog.toml
[changelog]
categories = ["feat", "fix", "breaking", "perf", "docs"]
exclude_scopes = ["deps"]
header = "# Changelog"
```

---

## 39. Documentation Generation

```bash
gitriven docs contributors                  # generate CONTRIBUTORS section from git history
gitriven docs changelog                     # CHANGELOG.md as maintained file
gitriven docs setup                         # README.md skeleton from project detection
gitriven docs licenses                      # THIRD-PARTY section in LICENSE.md
gitriven docs stats                         # repo metrics
```

---

## 40. Dependency Management

### Dependency Auditing

```bash
gitriven audit                              # scan lockfile against vulnerability databases
gitriven audit update                       # refresh vulnerability database
```

Supports: Cargo.lock, package-lock.json, yarn.lock, Gemfile.lock, requirements.txt, go.sum, composer.lock. Data source: OSV (Open Source Vulnerabilities).

### Dependency Intelligence

```bash
gitriven deps tree                          # dependency tree
gitriven deps why <package>                 # why is this included
gitriven deps outdated                      # packages with newer versions
gitriven deps diff                          # dependency changes between commits/branches
```

### Dependency Diff

When a lockfile changes on pull, show human-readable summary: "upgraded lodash 4.17.20 → 4.17.21, added express@4.18.2, removed moment" instead of raw lockfile diff.

### SBOM

```bash
gitriven sbom generate                      # SPDX or CycloneDX format
gitriven sbom verify                        # validate against repo state
```

---

## 41. Migration Tools

```bash
gitriven migrate <source> <dest> --from github --to gitea
gitriven migrate --user <username> --from github --to gitea [--all-orgs]
```

Migrates: code, branches, tags, releases, issues, PRs/MRs, wikis, labels. Maps references (PRs → MRs, labels, issue numbers where possible). Preserves commit history and branch structure.

---

## 42. Mirroring

```bash
gitriven mirror add <source> <dest>
gitriven mirror sync
gitriven mirror sync --continuous           # background daemon
gitriven mirror list
```

One-to-many: one source mirrored to multiple destinations. Stored in `.gitriven/mirrors.toml` (per-repo) or `{config}/mirrors.toml` (global).

---

## 43. Archive & Backup

```bash
gitriven archive <owner/repo>               # full backup: branches, tags, LFS, submodules, wiki, issues, releases
gitriven archive --user <name> [--all-orgs]
gitriven archive restore <bundle>
```

Output: git bundle + metadata JSON + LFS objects in a single tar.gz.

### Archive Retention

```bash
gitriven archive branch <branch> [--before <date>]
gitriven archive commits --before <date> --keep-merges
gitriven archive restore <branch>
gitriven archive list
```

---

## 44. Network Resilience

- Auto-retry on transient failures (configurable retries + exponential backoff)
- Resume interrupted clones/fetches
- Bandwidth estimation and ETA
- Connection pooling for recursive operations

### Doctor

```bash
gitriven doctor
```

Comprehensive check: SSH key loaded? SSH connection works? HTTPS credentials valid? Proxy configured? DNS resolving? Token expired? Token has required scopes? Per-provider health status.

Auto-runs relevant checks when any network operation fails.

---

## 45. Offline Mode

- Queue push operations when no network
- Execute queued operations when connection returns
- `gitriven sync` — push all queued, pull all remotes, update all submodules
- `gitriven offline status` — show queue
- `gitriven prefetch` — aggressively cache for upcoming offline period

---

## 46. Search

### Cross-Repo Code Search

```bash
gitriven search code "fn main" --recursive ~/Projects
gitriven search code "TODO" --workspace casapps
gitriven search code "api_key" --all
gitriven search files "*.toml" --recursive ~/Projects
gitriven search commits "breaking change" --recursive ~/Projects
```

Built-in ripgrep-style regex engine. Indexed for speed.

### Provider Search

```bash
gitriven search code <query> [--repo] [--language]
gitriven search repos <query> [--language] [--sort stars|forks|updated]
gitriven search issues <query> [--state] [--label]
```

---

## 47. Log Query Language

```bash
gitriven log --query "author:jason since:last-week files:*.rs"
gitriven log --query "message:fix NOT message:merge"
gitriven log --query "changed:src/auth/ since:v1.0.0 until:v2.0.0"
gitriven log --query "additions:>100 author:jason"
gitriven log --query "merge branch:feature/*"
```

Translates to correct git log flags internally.

### Time-Based Queries

Natural language dates: "yesterday", "last friday", "last week", "today".

```bash
gitriven log --since "yesterday"
gitriven diff @{last week}
```

---

## 48. Blame & History Intelligence

### Enhanced Blame

```bash
gitriven blame <file>                       # color-coded by age
gitriven blame <file> --ignore-whitespace
gitriven blame <file> --ignore-revs-file    # auto-detect bulk reformat commits
gitriven blame <file> --history <line-range>
```

### Intelligence

```bash
gitriven why <file> <line>                  # full chain: who, what commit, what PR, what issue
gitriven who <path>                         # primary maintainer by commit frequency/recency
gitriven impact <commit>                    # downstream impact: follow-up fixes, reverts
gitriven depends <commit>                   # child commits in DAG
gitriven depends --cherry-pick-safe <commit>
```

### File History Across Renames

```bash
gitriven history <file>                     # complete history including renames
gitriven history <file> --follow-copies
```

---

## 49. Diff Engine

### Enhanced Output

- Moved code detection (not delete + add, but "moved from line X to line Y")
- Refactored function detection
- Whitespace change collapsing (separate from logic changes)
- Semantic diff for supported languages
- All in CLI, TUI, and GUI

### Commands

```bash
gitriven diff stat                          # summary across repo
gitriven diff between <branch1> <branch2>   # cleaner syntax
gitriven diff share                         # upload to gist provider, return URL
gitriven diff share <commit-range>
gitriven diff export <file>                 # standalone HTML with syntax highlighting, no JS
gitriven diff email <address>               # send via SMTP
```

### Binary File Diffing

For common formats, show metadata instead of "binary files differ":
- Images: dimensions changed, file size delta
- PDFs: text content diff
- SQLite: schema and row count diff
- Archives: file listing diff

### Commit Graph Visualization

```bash
gitriven graph                              # ASCII commit graph with branch topology
gitriven graph --branches                   # branch topology only
```

---

## 50. Bisect Automation

```bash
gitriven bisect auto <test-command>         # fully automated
gitriven bisect auto <test-command> --parallel
gitriven bisect blame <test-command>        # find commit AND specific file/function
gitriven bisect visual                      # TUI/GUI progress on commit graph
gitriven bisect save / resume / replay
```

---

## 51. Statistics & Analytics

```bash
gitriven stats                              # contribution summary
gitriven stats --author <name>
gitriven stats --files                      # hotspots (most-changed files)
gitriven stats --churn                      # instability indicator
gitriven activity                           # commit frequency graph
gitriven activity --author <name>
gitriven activity --files                   # file-level heatmap
gitriven activity --team                    # cross-repo in workspace
```

Visual charts in TUI/GUI.

---

## 52. Repository Size Management

```bash
gitriven size                               # breakdown: packfiles, loose objects, LFS, worktrees
gitriven size --history                     # what's taking space in history
gitriven clean                              # guided cleanup
gitriven clean --aggressive                 # full repack with max compression
gitriven clean --filter <path>              # rewrite history to remove file (BFG-style)
```

---

## 53. Sparse Checkout

```bash
gitriven sparse add <path>
gitriven sparse remove <path>
gitriven sparse list
gitriven sparse reset
```

Cone mode by default. Combined with auto-shallow for massive monorepos.

---

## 54. Shallow Clone Management

- Auto-shallow for repos over configurable size threshold
- `gitriven deepen [N]` — fetch more history
- `gitriven unshallow` — convert to full clone
- Auto-deepen when operation needs unavailable history (blame, bisect)

---

## 55. Bundle Support

```bash
gitriven bundle create <file>
gitriven bundle verify <file>
gitriven bundle apply <file>
gitriven bundle create --incremental --since <commit>
```

For offline repo transfer / air-gapped environments.

---

## 56. Patch Workflow

```bash
gitriven patch create [commits]
gitriven patch apply <file|url>
gitriven patch send <email>                 # format and send via SMTP
```

---

## 57. Snapshot / Checkpoint

Lighter than commit, heavier than stash. Local-only, auto-expires, never pushed.

```bash
gitriven checkpoint "before refactor"
gitriven checkpoint --list
gitriven checkpoint restore "before refactor"
```

### Draft Commits

Remote-backed WIP saves:

```bash
gitriven draft "wip: trying new approach"   # commit to drafts/{branch}/{timestamp} ref
gitriven draft list
gitriven draft restore <id>
gitriven draft clean
```

---

## 58. Time Tracking

```bash
gitriven timer start
gitriven timer stop
gitriven timer status
gitriven timer report [--since "last week"]
```

Auto-stop on branch switch, auto-start on switch back. Stored locally, never pushed. Optional trailer: `Time-spent: 2h15m`.

---

## 59. Snippet Manager

```bash
gitriven snippet save <name>
gitriven snippet list
gitriven snippet apply <name>
gitriven snippet share <name>               # push to gist
```

Stored in `{data}/snippets/`.

---

## 60. Dotfile Management

```bash
gitriven dotfiles init <repo>
gitriven dotfiles track <file>              # move to repo, symlink back
gitriven dotfiles sync
gitriven dotfiles bootstrap                 # new machine: clone + create all symlinks
gitriven dotfiles list
gitriven dotfiles untrack <file>
```

Supports multiple dotfile repos (personal, work, machine-specific).

---

## 61. Workspace Management

```bash
gitriven workspace create <name>
gitriven workspace add <repo-path>
gitriven workspace status
gitriven workspace pull|push|commit
gitriven workspace switch <name>
```

Curated set of repos, not "everything under a directory". Stored in `{config}/workspaces.toml`.

---

## 62. Repo Discovery & Index

```bash
gitriven repos                              # index all repos across providers + local
gitriven repos search <query>               # fuzzy search
gitriven repos where <name>                 # find which provider/directory
gitriven repos update                       # refresh index
```

Local index in `{data}/repos.db`.

### Favorites

```bash
gitriven pin <path-or-name>
gitriven pin list
gitriven pin remove <name>
gitriven cd <pinned-name>                   # jump to repo
```

---

## 63. Repo Linking

For related repos that aren't submodules:

```toml
# .gitriven/linked.toml
[[linked]]
name = "cashost-docs"
repo = "casapps/cashost-docs"
path = "../cashost-docs"

[[linked]]
name = "cashost-ui"
repo = "casapps/cashost-ui"
path = "../cashost-ui"
```

```bash
gitriven linked clone
gitriven linked status
gitriven linked pull|push
```

---

## 64. Feature Branch Tracking

```bash
gitriven feature start <name>
gitriven feature status
gitriven feature finish                     # merge PR, delete branch, close issue, update changelog
gitriven feature list
```

Not git-flow — no rigid model. Just awareness of feature lifecycle.

---

## 65. Stacked PRs / Patch Queue

```bash
gitriven stack create <name>
gitriven stack push                         # add current branch as next layer
gitriven stack list
gitriven stack rebase                       # rebase entire stack
gitriven stack submit                       # create chained PRs
gitriven stack sync                         # update all PRs after rebase
```

---

## 66. Multi-Identity Management

```toml
# {config}/profiles.toml
[[identity]]
match = "~/Projects/github/work-org/*"
user = "Jason Hempstead"
email = "jason@work.com"
signing_key = "~/.ssh/work_ed25519"
token_profile = "work-github"

[[identity]]
match = "~/Projects/github/jason/*"
user = "Jason"
email = "jason@casjaysdev.pro"
signing_key = "~/.ssh/personal_ed25519"
token_profile = "personal-github"
```

Auto-switch based on directory pattern. Zero manual switching.

---

## 67. Configuration Profiles

```bash
gitriven profile list
gitriven profile create <name> --user "Name" --email "email" --signing-key "key"
gitriven profile switch <name>
gitriven profile auto                       # auto-select from remote URL patterns
```

---

## 68. Environment File Management

```bash
gitriven env init                           # copy .env.example to .env, prompt for values
gitriven env check                          # verify .env has all keys from .env.example
gitriven env diff                           # missing keys (onboarding help)
gitriven env encrypt                        # encrypt .env in-repo
```

`.env` auto-added to `.gitignore` if not already there.

---

## 69. Conflict Prevention

```bash
gitriven watch <branch>                     # alert when remote diverges from yours
gitriven lock <file>                        # advisory lock (not enforced)
```

Periodic notification on long-lived branches: "main has 47 new commits since you branched."

---

## 70. Pre-Flight Checks

```toml
# .gitriven/config.toml
[preflight.push]
checks = ["secrets", "lint", "no-wip"]

[preflight.merge]
checks = ["ci-pass", "no-conflicts", "branch-current"]

[preflight.release]
checks = ["tests", "audit", "changelog", "version-bump"]
```

```bash
gitriven preflight                          # run checks manually
```

Checks run in parallel where possible.

---

## 71. Change Risk Assessment

```bash
gitriven risk                               # assess staged/committed changes
gitriven risk --pr <number>
```

Factors: files changed count, lines changed, hot paths, critical files, new dependencies, CI/deploy config changes. Output: low/medium/high with reasoning.

---

## 72. Repository Compliance Policies

```toml
# .gitriven/policy.toml
[policy]
require_signed_commits = true
require_conventional_commits = true
require_pr_for_protected_branches = true
max_commit_size_mb = 10
forbidden_files = ["*.env", "*.pem", "*.key", "id_rsa"]
required_files = ["README.md", "LICENSE.md", ".gitignore"]
min_reviewers = 1
branch_naming = "^(feature|fix|hotfix|release|chore)/[a-z0-9-]+$"
max_branch_age_days = 90
```

```bash
gitriven policy check
gitriven policy enforce                     # set up hooks
```

Org-level policy in `{config}/policy.toml` applies as baseline. Per-repo can be stricter but not looser.

---

## 73. Commit Verification & Audit

```bash
gitriven audit log [--since <date>]         # full operation audit trail
gitriven audit verify <commit-range>        # verify signature chain
gitriven audit export                       # JSON, CSV
gitriven audit policy                       # check repo against policy
```

---

## 74. Repository Anomaly Detection

Detects:
- Force pushes to shared branches
- Uncommonly large commits
- Binary files that shouldn't be binary
- Commits with future timestamps
- Unsigned commits in normally-signed repo
- Unusual author identities

Runs as part of `gitriven health` and pre-push check. All logic-based, no AI.

---

## 75. Background Maintenance

- Auto-gc: intelligent garbage collection triggered by conditions, not timers
- Auto-repack: optimize packfiles during idle
- Commit graph maintenance
- Multi-pack index maintenance
- Prefetch: background fetch from remotes on schedule
- Never blocks the user

```bash
gitriven maintenance status
gitriven maintenance run
```

---

## 76. Scheduled Operations

```bash
gitriven schedule add "pull --recursive ~/Projects" --every 1h
gitriven schedule add "health" --every 1d
gitriven schedule add "maintenance run" --every 6h
gitriven schedule list
gitriven schedule remove <id>
```

Lightweight background daemon or system cron/systemd/launchd integration.

---

## 77. Notifications & Inbox

```bash
gitriven inbox                              # all notifications across providers
gitriven inbox --unread
gitriven inbox mark-read [id|--all]
gitriven inbox watch <owner/repo>
```

Desktop notifications when long operations complete or review requests arrive. Configurable threshold.

---

## 78. Shell Integration

```bash
gitriven shell install                      # install hooks for bash/zsh/fish
gitriven shell completions bash|zsh|fish
gitriven cd <repo-name>                     # fuzzy-find and jump to repo
```

Features:
- Prompt integration (branch, dirty state, ahead/behind)
- Auto-fetch on directory enter (background, non-blocking, with cooldown interval)
- Tab completions (generated by clap)

---

## 79. Custom Commands & Plugins

Drop a script or binary in `{data}/commands/` — it becomes a subcommand. `gitriven <custom-name>` runs it with gitriven's environment.

`.gitriven/commands/` in repo for team-shared custom commands.

---

## 80. Terminal Sharing & Pair Programming

```bash
gitriven pair start
gitriven pair join <session-id>
gitriven pair share <session-id>
gitriven pair record                        # asciinema-compatible recording
```

Auto-add co-author trailers during pair sessions.

---

## 81. Container Registry Integration

```bash
gitriven container list [registry]
gitriven container tag <image> <tag>
gitriven container delete <image:tag>
gitriven container prune <image> --keep 5
```

Supports: Docker Hub, GHCR, Harbor, GitLab Registry, Gitea Registry, any OCI-compatible. Ties into release workflow.

---

## 82. Semantic Versioning Intelligence

```bash
gitriven version next                       # auto-determine from conventional commits
gitriven version check                      # verify consistency across all version files
gitriven version history                    # version timeline with changelogs
gitriven version set <version>              # update all detected files
gitriven version next --pre alpha           # pre-release: 1.2.0-alpha.1
gitriven version stamp                      # embed version info for builds
gitriven version bump [major|minor|patch]
```

---

## 83. Test Impact Analysis

```bash
gitriven impact <commit-range>              # map changed files to affected tests
gitriven test suggest                       # suggest tests based on staged changes
```

Mapping: import analysis, naming conventions, explicit config.

---

## 84. Database Migration Awareness

- Auto-detect migration directories
- Warn on pull if new migrations detected
- Flag migration sequence conflicts on merge
- `gitriven migrations list`
- `gitriven migrations check` — verify sequence integrity

---

## 85. Protocol Debugging

```bash
gitriven debug push|pull|clone <url>        # full protocol trace
gitriven debug remote <name>                # test connectivity
gitriven debug ssh <host>                   # SSH diagnostics
```

Human-readable output: DNS, TCP, TLS, SSH negotiation, git protocol, pack negotiation, transfer stats.

---

## 86. Git Internals Inspection

```bash
gitriven inspect object <sha>
gitriven inspect packfile
gitriven inspect refs
gitriven inspect index
gitriven inspect fsck
gitriven inspect config                     # merged config with origin labels
```

---

## 87. CLI Interface

Default interface. clap-based argument parsing with full git command compatibility.

- Progress bars via indicatif for long operations
- Color output when TTY detected
- `--no-color` flag for plain output
- `--verbose` for detailed output
- `--quiet` for minimal output

---

## 88. TUI Interface

lazygit-inspired. Built with ratatui + crossterm.

### Panels

| Key | Panel |
|-----|-------|
| 1 | Status |
| 2 | Log |
| 3 | Diff |
| 4 | Branches |
| 5 | Stash |
| 6 | Remotes |

### Operations

| Key | Action |
|-----|--------|
| Space | Stage/unstage |
| Tab | Into diff for hunk staging |
| c | Commit |
| P | Push |
| p | Pull |
| b | Create branch |
| r | Interactive rebase |
| s | Stash |
| / | Search |
| q | Quit |

### Features

- Real-time file watcher
- Inline diff preview
- Commit message editor
- Progress bars
- Brand color scheme (teal/amber)
- Notifications panel
- Dependency graph visualization

---

## 89. GUI Interface

GitKraken-inspired. Built with egui/eframe.

- Commit graph renderer
- Visual staging panel
- History panel with search
- Diff viewer with syntax highlighting
- Branch/tag sidebar
- Remote operations panel
- Brand color scheme

---

## 90. Server — httpd

Default: web only. `gitriven serve` starts HTTP server.

### Port Selection

First run: scan 65000-65535, find unused port, save to config. Subsequent: use saved port. If saved port in use: find new, update config. Override: `--port <n>`.

### Routes (all on one port)

| Path | Handler |
|------|---------|
| `/api/v1/...` | Gitea-compatible REST API |
| `/{owner}/{repo}` | Web repo browser |
| `/{owner}/{repo}.git/...` | Smart HTTP git protocol (push/pull) |
| `/{owner}` | Repo list for owner |
| `/` | Owner list (index page) |

### Repo Discovery

Two levels max from root. `dirname` = owner, `basename` = repo.

```
{root}/
├── jason/
│   ├── gitriven/          → /jason/gitriven
│   └── casfinance/        → /jason/casfinance
├── casapps/
│   ├── cashost/           → /casapps/cashost
│   └── casdash/           → /casapps/casdash
```

### Reserved Names

Only `api`. If a directory named `api` exists at root, warn on startup — system routes take precedence, conflicting directory skipped.

### Multi-Root

```toml
[[httpd.roots]]
path = "~/Projects/github"
prefix = "github"

[[httpd.roots]]
path = "~/Projects/gitea"
prefix = "gitea"
```

### Enable SSH/git

```bash
gitriven serve --enable-ssh                 # enables, finds port, saves to config
gitriven serve --enable-git
gitriven serve --info                       # print config without starting
```

### Server Startup Output

```
gitriven server started
  Web:  http://localhost:65042
```

With SSH/git enabled:
```
gitriven server started
  Web:  http://localhost:65042
  SSH:  ssh://localhost:65043
  Git:  git://localhost:65044
```

---

## 91. Server — sshd

Opt-in via config. Embedded SSH server for push/pull over SSH.

```toml
[sshd]
enabled = false
port = 65043
host_key = ""
authorized_keys = ""
```

---

## 92. Server — gitd

Opt-in via config. Native git protocol (fast, no auth).

```toml
[gitd]
enabled = false
port = 65044
export_all = false
```

---

## 93. Web UI

### Principles

- **Pure HTML5 and CSS. Zero JavaScript.**
- Semantic HTML5 elements throughout
- CSS-only interactivity (`<details>`/`<summary>`, `:target`, checkbox hack)
- Mobile-first responsive design
- WCAG 2.1 AA accessible
- Progressive enhancement (works with CSS disabled)
- Server-side rendering only
- All templates and CSS embedded in binary

### Theming

Three modes: auto (system), dark, light.

- `auto`: `@media (prefers-color-scheme: dark)` media query
- Manual: `?theme=dark|light` query param, server sets cookie + `data-theme` attribute
- Toggle is plain `<a>` links, no JS

CSS custom properties with brand colors:

```css
:root {
    --bg-primary: #ffffff;
    --accent: #2cada8;        /* teal */
    --accent-secondary: #e8922f; /* amber */
    /* ... */
}

@media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
        --bg-primary: #0d1117;
        /* ... */
    }
}
```

### Typography

System font stack — no web fonts:
- Sans: `-apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif`
- Mono: `ui-monospace, "Cascadia Code", "Source Code Pro", Menlo, Consolas, "DejaVu Sans Mono", monospace`

### Template Architecture

**Partials (reusable fragments):**
- `_header.html` — doctype, head, meta, embedded CSS, top bar
- `_nav.html` — breadcrumb navigation
- `_search.html` — search form
- `_footer.html` — footer with version info
- `_pagination.html` — prev/next links
- `_branch_selector.html` — branch/tag dropdown (`<details>`/`<summary>`)
- `_clone_urls.html` — clone URL display
- `_commit_row.html` — single commit entry
- `_diff_hunk.html` — diff hunk block
- `_repo_card.html` — repo card for listings
- `_theme_toggle.html` — dark/light/auto links
- `_empty_state.html` — friendly empty message

**Templates (full pages, include partials):**

| Template | URL Pattern |
|----------|-------------|
| `index.html` | `/` |
| `owner.html` | `/{owner}` |
| `repo.html` | `/{owner}/{repo}` |
| `tree.html` | `/{owner}/{repo}/tree/{branch}/{path}` |
| `blob.html` | `/{owner}/{repo}/blob/{branch}/{path}` |
| `commits.html` | `/{owner}/{repo}/commits/{branch}` |
| `commit.html` | `/{owner}/{repo}/commit/{sha}` |
| `branches.html` | `/{owner}/{repo}/branches` |
| `tags.html` | `/{owner}/{repo}/tags` |
| `blame.html` | `/{owner}/{repo}/blame/{branch}/{path}` |
| `compare.html` | `/{owner}/{repo}/compare/{base}...{head}` |
| `search_results.html` | `/{owner}/{repo}/search` |
| `error.html` | (404, 500, etc.) |

**Special URLs:**
- `/{owner}/{repo}/raw/{branch}/{path}` — raw file download
- `/{owner}/{repo}/archive/{ref}.tar.gz` — archive download

### All embedded at compile time via `include_str!()`.

### CSS-Only Interactive Patterns

| Feature | HTML5/CSS Solution |
|---------|-------------------|
| Collapsible file trees | `<details>` / `<summary>` |
| Tab switching | `:target` selector |
| Mobile menu toggle | Checkbox hack |
| Theme switching | Server cookie + `data-theme` |
| Search | `<form>` submit |
| Pagination | `<a>` links with query params |
| Sort columns | Links with `?sort=&order=` |
| Syntax highlighting | Server-side syntect, CSS classes |
| Line number linking | `id` per line, `:target` highlights |
| Tooltips | CSS `:hover` + `::after` + `data-` attributes |
| Modals | `<dialog>` via `:target` |
| Sticky header | `position: sticky` |
| Code word wrap toggle | Checkbox hack + `white-space` |
| Expandable content | `<details>` / `<summary>` |

### Diff View

- Side-by-side on desktop (CSS grid), unified on mobile
- Line numbers via `data-` attributes + CSS `::before`
- Syntax highlighting via server-side syntect
- Expandable context via `<details>`

### Performance

- Single HTML document per page (CSS inline in `<head>`)
- No external requests
- Syntax highlighting server-side
- No web fonts
- Only inline SVG: gitriven logo
- Pages load in milliseconds (server is local)

---

## 94. Gitea-Compatible API

Exposed at `/api/v1/`. Any tool that talks to Gitea works with gitriven's server.

### Endpoints

```
/api/v1/repos/                              # list repos
/api/v1/repos/{owner}/{repo}                # repo details
/api/v1/repos/{owner}/{repo}/branches       # branches
/api/v1/repos/{owner}/{repo}/tags           # tags
/api/v1/repos/{owner}/{repo}/commits        # commit history
/api/v1/repos/{owner}/{repo}/contents/      # file contents
/api/v1/repos/{owner}/{repo}/raw/           # raw file access
/api/v1/repos/{owner}/{repo}/archive/       # download archive
/api/v1/repos/{owner}/{repo}/git/refs       # git references
/api/v1/repos/{owner}/{repo}/git/trees      # tree objects
/api/v1/repos/{owner}/{repo}/git/blobs      # blob objects
/api/v1/repos/{owner}/{repo}/compare/       # compare
/api/v1/repos/{owner}/{repo}/hooks          # webhooks
/api/v1/repos/search                        # search
/api/v1/user                                # authenticated user
/api/v1/users/{username}                    # user info
/api/v1/users/{username}/repos              # user repos
/api/v1/orgs/                               # organizations
/api/v1/orgs/{org}/repos                    # org repos
/api/v1/version                             # API version
/api/v1/settings/api                        # server capabilities
```

### Scope

**Implemented:** repos, branches, tags, refs, commits, trees, blobs, contents, raw, archives, compare, webhooks, user/org, search, create/delete/modify repos.

**Skipped (not applicable):** issues, PRs, milestones, labels, teams, permissions, OAuth, admin, package registry.

### Config

```toml
[httpd]
api = true
api_token = ""
api_readonly = false

[httpd.repos]
root = "/srv/git"
create_allowed = true
delete_allowed = false
```

Swagger docs at `/api/v1/swagger`.

---

## 95. CI Config Translation

When a repo has CI config for one provider but is cloned/used on another, gitriven copies and translates.

### Trigger

Repo has `.github/workflows/` but no `.gitea/`. Cloned to Gitea → copy and translate.

### Translation

| Source | Destination | Effort |
|--------|-------------|--------|
| `.github/workflows/` | `.gitea/workflows/` | Minimal (Gitea Actions is GitHub-compatible) |
| `.github/workflows/` | `.forgejo/workflows/` | Minimal |
| `.github/workflows/` | `.gitlab-ci.yml` | Full syntax translation |
| `.gitlab-ci.yml` | `.github/workflows/` | Full |
| Any → Any | Bidirectional | Best-effort with comments for untranslatable parts |

Non-CI files also translate: CODEOWNERS, issue templates, PR templates (format differences handled).

### Commands

```bash
gitriven ci translate --from github --to gitea
gitriven ci translate --from github --to all
gitriven ci diff                            # detect drift between configs
gitriven ci sync                            # re-translate from primary
```

### Config

```toml
# .gitriven/config.toml
[ci]
primary = "github"
auto_translate = true
providers = ["gitea", "forgejo", "gitlab"]
```

Generated files include a comment header: `# Auto-generated by gitriven from .github/workflows/ — edit the primary instead.`

### Multiple Provider Directories Coexist

```
project/
├── .github/workflows/ci.yml       # primary
├── .gitea/workflows/ci.yml        # auto-translated
├── .forgejo/workflows/ci.yml      # auto-translated
├── .gitlab-ci.yml                 # auto-translated
```

---

## 96. Crate Structure

```
gitriven/                        (workspace root)
├── Cargo.toml                   (workspace definition)
├── gitriven-core/               # glue over gix + custom logic
│   ├── src/
│   └── Cargo.toml
├── gitriven-api/                # hosting platform API client
│   ├── src/
│   └── Cargo.toml
├── gitriven-cli/                # CLI argument parsing & dispatch
│   ├── src/
│   └── Cargo.toml
├── gitriven-tui/                # terminal UI (ratatui)
│   ├── src/
│   └── Cargo.toml
├── gitriven-gui/                # native GUI (egui)
│   ├── src/
│   └── Cargo.toml
├── gitriven-server/             # built-in server (axum)
│   ├── src/
│   │   ├── templates/           # embedded HTML templates
│   │   │   ├── partials/
│   │   │   └── pages/
│   │   └── style.css            # embedded CSS
│   └── Cargo.toml
└── src/
    └── main.rs                  # binary entrypoint, mode selection, multicall dispatch
```

---

## 97. Dependencies

### Core

| Crate | Purpose |
|-------|---------|
| gix | Git implementation (gitoxide ecosystem) |
| clap | CLI argument parsing + completions |
| tokio | Async runtime |
| rayon | Parallel processing |
| serde | Serialization |
| toml | Config file parsing |
| reqwest | HTTP client for API calls |

### Interfaces

| Crate | Purpose |
|-------|---------|
| ratatui | TUI rendering |
| crossterm | Terminal backend |
| egui / eframe | GUI rendering |
| axum | HTTP server |

### Utilities

| Crate | Purpose |
|-------|---------|
| indicatif | Progress bars |
| syntect | Syntax highlighting |
| rusqlite | SQLite (credentials db, repo index) |
| ring / argon2 | Cryptography (credential encryption) |
| regex | Pattern matching |
| globset | Glob pattern matching |
| chrono | Date/time handling |
| dirs | Platform directory detection |
| notify | File system watcher |

---

## 98. Release Binaries

See [Section 4: Binary & Distribution](#4-binary--distribution) for full binary matrix.

All builds: static linked (musl on Linux), stripped, single file, no runtime dependencies.

---

## 99. Version 1.0.0 Scope

All four interfaces ship together:
1. CLI — complete git replacement + all smart features
2. TUI — interactive terminal UI
3. GUI — native visual client
4. Server — web browser + API + optional SSH/git protocol

Plus all features defined in this specification.

### Internal Build Priority (not separate releases)

1. Core git operations (gitriven-core over gix)
2. CLI with all git commands
3. Smart operations engine
4. Commit/merge/rebase workflows
5. Recursive engine
6. API client + provider management
7. Credentials database
8. Format/lint orchestration
9. Hooks system
10. TUI
11. Server (httpd + web UI + API)
12. GUI
13. All remaining features

---

## 100. Complete Command Reference

### Root-Level File Policy

gitriven will only create these files in the project root:

- `README.md`
- `LICENSE.md`
- `CHANGELOG.md`
- `.gitignore`
- `.gitattributes`
- `.editorconfig`
- `.gitriven/` (directory)
- `.github/` / `.gitea/` / `.forgejo/` / `.gitlab/` (provider-specific)
- `.gitlab-ci.yml` / `Jenkinsfile` / `bitbucket-pipelines.yml` (only when provider mandates root placement)

Nothing else. Root is sacred. Community files go in provider directories. Third-party licenses go in LICENSE.md. No file clutter.

### Global Flags

| Flag | Description |
|------|-------------|
| `--cli` | Force CLI mode |
| `--tui` | Force TUI mode |
| `--gui` | Force GUI mode |
| `--no-tui` | Prevent TUI auto-launch |
| `--no-gui` | Prevent GUI auto-launch |
| `--no-smart` | Script-safe mode |
| `--smart` | Force interactive mode |
| `--no-color` | Plain output |
| `--verbose` | Detailed output |
| `--quiet` | Minimal output |
| `--no-lfs` | Skip LFS handling |
| `--no-submodules` | Skip submodule handling |
| `--no-protect` | Bypass branch protection |
| `--no-credential-db` | Skip credentials database |
| `--recursive <path>` | Multi-repo operation |
| `--exclude <glob>` | Exclude pattern for recursive |
| `--jobs <n>` | Parallelism for recursive |
| `--api-type <provider>` | Specify provider |
| `--api-server <host>` | Specify server |

### All gitriven-Specific Commands (non-git)

```
gitriven serve [--port] [--enable-ssh] [--enable-git] [--info]
gitriven setup [--symlinks] [--alias] [--prefix]
gitriven auth login|status|refresh|logout|export|import
gitriven sign setup
gitriven config import|export|show|edit|team
gitriven profile list|create|switch|auto
gitriven doctor
gitriven health [score|report|badge|history]
gitriven is clean|dirty

gitriven commit all|modified|deleted|added|renamed|restored|files|spelling
gitriven commit new|improved|fixes|release|deploy|docs|test|breaking|refactor|performance|permissions|bugs
gitriven fixup
gitriven squash [N] [message]
gitriven absorb
gitriven coauthors add

gitriven merge-resolve status|show|edit|ours|theirs|abort
gitriven merge-driver add
gitriven merge-queue add

gitriven undo [--list] [--steps N]
gitriven history [search]
gitriven checkpoint [--list|restore]
gitriven draft [list|restore|clean]

gitriven repo create|delete|modify|list|visibility|view|fork|archive
gitriven org list|repos|clone|push|pull|visibility
gitriven user repos|clone|push|pull
gitriven ssh list|add|delete
gitriven release create|delete|list|dry-run|undo
gitriven pr create|list|view|checkout|merge|close|diff|review
gitriven review [comment|approve|request-changes|pending|mine]
gitriven issue list|count|create|edit
gitriven gist list|clone|create|delete|search|edit
gitriven run list|view|watch|rerun|cancel
gitriven ci status|logs|retry|wait|cancel|badge|translate|diff|sync
gitriven deploy [status|rollback]
gitriven upstream set|sync
gitriven migrate
gitriven mirror add|sync|list

gitriven ignore add|save|list|search|update|console|--check
gitriven attrs init|add|check|linguist
gitriven license set|list|third-party|check|scan|compatibility
gitriven community init|update
gitriven new [--type] [--template]
gitriven template list|create
gitriven changelog [--since]
gitriven docs contributors|changelog|setup|licenses|stats

gitriven format check|run|install
gitriven lint [--all]
gitriven hooks add|init|list|browse|install|export
gitriven security scan
gitriven encrypt track|add-key|status
gitriven audit [log|verify|export|policy|update]
gitriven sbom generate|verify
gitriven deps tree|why|outdated|diff
gitriven risk [--pr]
gitriven policy check|enforce

gitriven branches [--stale|--orphan|--cleanup|--age|compare|graph|divergence]
gitriven archive branch|commits|restore|list
gitriven worktree create|list|remove|switch
gitriven sub add|update|status|sync|remove|repair
gitriven subtree add|pull|push|list|split
gitriven lfs track|status|migrate|prune
gitriven sparse add|remove|list|reset
gitriven deepen [N]
gitriven unshallow
gitriven bundle create|verify|apply
gitriven patch create|apply|send

gitriven search code|files|commits|repos|issues
gitriven log --query
gitriven blame [--ignore-whitespace|--ignore-revs-file|--history]
gitriven why <file> <line>
gitriven who <path>
gitriven impact <commit>
gitriven depends [--reverse|--cherry-pick-safe]
gitriven diff stat|between|share|export|email
gitriven graph [--branches]
gitriven bisect auto|blame|visual|save|resume|replay
gitriven compare-repos
gitriven inspect object|packfile|refs|index|fsck|config

gitriven stats [--author|--files|--churn]
gitriven activity [--author|--files|--team]
gitriven size [--history]
gitriven clean [--aggressive|--filter]
gitriven mailmap show|duplicates|add|generate
gitriven owners show|generate|drift|coverage

gitriven version next|check|history|set|stamp|bump
gitriven timer start|stop|status|report
gitriven snippet save|list|apply|share
gitriven dotfiles init|track|sync|bootstrap|list|untrack
gitriven workspace create|add|status|pull|push|commit|switch
gitriven repos [search|where|update]
gitriven pin [list|remove]
gitriven cd <name>
gitriven linked clone|status|pull|push
gitriven feature start|status|finish|list
gitriven stack create|push|list|rebase|submit|sync
gitriven env init|check|diff|encrypt
gitriven watch <branch>
gitriven lock <file>
gitriven preflight
gitriven notifications [--unread|mark-read]
gitriven inbox [--unread|mark-read|watch]
gitriven web
gitriven shell install|completions
gitriven schedule add|list|remove
gitriven container list|tag|delete|prune
gitriven pair start|join|share|record
gitriven debug push|pull|clone|remote|ssh
gitriven sync
gitriven offline status
gitriven prefetch
gitriven preview <file> [--watch]
gitriven migrations list|check
gitriven rerere list|forget|export|import
gitriven conflict clean|check
gitriven maintenance status|run
gitriven test suggest
gitriven about
```

---

*End of Specification*
