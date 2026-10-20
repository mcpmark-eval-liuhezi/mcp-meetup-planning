# MCP Study-Group Meetup — Planning Pack

**Event:** Half-day, in-person study-group session on the Model Context Protocol (MCP)
**City / area:** San Francisco — in or within a short walk of Union Square
**Featured project:** [`modelcontextprotocol/servers`](https://github.com/modelcontextprotocol/servers)

---

## 1. Venue shortlist (Union Square, San Francisco)

| # | Venue | Street address | Rating | Opening hours | Type |
|---|-------|----------------|--------|---------------|------|
| 1 | Peet's Coffee (Union Square) | 773 Market St, San Francisco, CA 94103 | 4.4 / 5 (41 reviews) | Mon–Sun 05:00–19:30 | Café |
| 2 | Bluestone Lane Union Square | 685 Market St, San Francisco, CA 94103 | 4.1 / 5 (23 reviews) | Mon–Fri 07:00–14:00 | Café |
| 3 | Café de la Presse | 352 Grant Ave, San Francisco, CA 94108 | 3.9 / 5 (1,451 reviews) | Mon–Wed 08:00–18:00; Thu–Sat 08:00–20:00; Sun 08:00–15:00 | Café / brasserie |
| 4 | The Marker Union Square | 501 Geary St, San Francisco, CA 94102 | 4.0 / 5 (2,216 reviews, Tripadvisor) | 24-hour front desk; meeting & event spaces by reservation | Boutique hotel with event/meeting space |
| 5 | The Westin St. Francis (on Union Square) | 335 Powell St, San Francisco, CA 94102 | 3.0 / 5 (1,314 reviews, Tripadvisor) | 24-hour front desk; meeting rooms by reservation | Full-service hotel with meeting rooms |

### ✅ Top pick: **The Marker Union Square — 501 Geary St**

**Why:** One block off Union Square, rated 4.0/5 across 2,200+ reviews, and the only shortlisted option with bookable meeting/event space that can actually seat ~20 people for a half-day session — the cafés are great for a pre-session coffee but none can hold a group that size all morning.

**Suggested plan:** morning sessions at The Marker's meeting space; coffee/arrival at Peet's or Bluestone Lane; optional team lunch at Café de la Presse (French brasserie, 2 blocks from the square).

> Note on data: café ratings and hours come from Brave's place data (Tripadvisor-sourced); hotel ratings are Tripadvisor traveller ratings. Confirm hours and room availability with each venue when booking — hotel meeting rooms are not walk-in.

---

## 2. Featured project: `modelcontextprotocol/servers`

### Latest release — `v2.0.0`

**Tag:** `v2.0.0` → commit `51b6382a3e827aceb6bce430b1208d69b93d95ea`

**Highlights from the release notes (as reported by the release lookup):**

- **"Servers refactored to modern era"** — the release refactors all the servers to support the modern era spec, while still answering legacy era clients as expected.
- **Packages published in this release:**

  | Package | Version | Registry |
  | --- | --- | --- |
  | `@modelcontextprotocol/server-everything` | `2.0.0` | npm |
  | `@modelcontextprotocol/server-filesystem` | `2.0.0` | npm |
  | `@modelcontextprotocol/server-memory` | `2.0.0` | npm |
  | `@modelcontextprotocol/server-sequential-thinking` | `2.0.0` | npm |
  | `mcp-server-fetch` | `2026.10.19` | PyPI |
  | `mcp-server-git` | `2026.10.19` | PyPI |
  | `mcp-server-time` | `2026.10.19` | PyPI |

- **Notable per-package changes:** filesystem fixes (revoke access when a roots update leaves no valid root; apply only the newest roots refresh's answer; hold tool calls while any roots refresh is pending), sequential-thinking UI fix (pad the thought box's header row to the border), and CI now validates the TypeScript servers on Node 22, 24 and 26 in parallel.
- **Changes for clients (Python servers):** `mcp-server-fetch`, `mcp-server-git` and `mcp-server-time` are now built on the MCP Python SDK's high-level `MCPServer`. An unknown tool now returns a JSON-RPC `-32602` error (`Unknown tool: <name>`) in both protocol eras, as the spec requires — previously it was an `isError` result. Tool errors read `Error executing tool <name>: <message>`, and each server now advertises its capabilities.

### The commit the release tag points to

| Field | Value |
| --- | --- |
| SHA | `51b6382a3e827aceb6bce430b1208d69b93d95ea` ([link](https://github.com/modelcontextprotocol/servers/commit/51b6382a3e827aceb6bce430b1208d69b93d95ea)) |
| Author | Cliff Hall ([@cliffhall](https://github.com/cliffhall)) |
| Message | `Merge pull request #5166 from modelcontextprotocol/v2/chore/5159-release-v2.0.0` — "Release v2.0.0: merge v2/main into main" |
| Date | 2026-10-19 06:37 UTC |
| Scale | 31 files changed; +10,522 / −4,553 (15,075 total changes) |

**Files touched (summary):**

- **Release/CI workflow files:** `.github/workflows/everything-mcp-diff.yml` (added, 254 lines), `typescript.yml`, `python.yml`, `prepare-python-release.yml`, `version-packages.yml`, `release.yml`, `main-source.yml`, `sdk-watch.yml`, `dco.yml`, `dependabot-alerts.yml`, `dependency-refresh.yml`
- **Repo automation skills:** `.claude/skills/{board-ops, client-smoke, issue-triage, local-dev, pr-flow, pre-push-gate, release, security-advisory, testing}/SKILL.md`
- **New tooling:** `scripts/interface-diff.mjs` (added, 374 lines) and `scripts/interface-diff.test.mjs` (added, 138 lines); `scripts/lib/win-shell-args.mjs`
- **Project meta/docs:** `.changeset/config.json`, `AGENTS.md`, `RELEASING.md`, `docs/contribution-model.md`, `docs/quality-gate.md`, `package.json`, `package-lock.json`

### Momentum — most recent commits on the default branch (`main`)

All of the latest activity landed on **2026-10-19**, inside a single ~35-minute release window, and reads as an active, release-hardening push:

- `51b6382` — Merge PR #5166: **Release v2.0.0: merge v2/main into main** (the release tag commit).
- `f18beb7` — Merge PR #5179: `fix(ci)` a superseded dispatched run posts no status, whatever its jobs did.
- `163a5e9` — `test:` skip the dispatch-status script tests without bash or jq (Copilot round 1 on #5179).
- `803df28` — Merge PR #5177: `chore:` stamp Python CalVer versions for 2026.10.19.
- `d533150` — `fix(ci)` superseded-run status fix, found by Copilot on #5166.
- `eaaa712` — `chore:` stamp Python CalVer versions for 2026.10.19.
- `f1783c3` — Merge PR #5175: **Python servers: build fetch, git and time on MCPServer; unknown tool is -32602**.
- `005e7e6` — `fix(python)` serialize git tool calls, delegate malformed names, require mcp 2.3.

**Read on momentum:** the project is very active — the entire v2.0.0 modern-era migration, the Python `MCPServer` rework, CalVer re-stamping and CI hardening all shipped together on release day, largely driven by maintainer @cliffhall (with several commits co-authored by Claude and explicitly following Copilot review rounds). The focus right now is the modern-era spec migration plus release/CI reliability rather than new user-facing features.

---

## 3. What is the Model Context Protocol? (plain English)

The Model Context Protocol (MCP) is an open standard, introduced by Anthropic in November 2024, that gives AI applications a consistent way to connect to external tools, data sources and services — MCP clients inside host applications send requests, and MCP servers expose the tools, resources and prompts those applications can use ([Descope, "What Is the Model Context Protocol (MCP) and How It Works"](https://www.descope.com/learn/post/mcp)). Instead of maintaining a separate connector for every data source, developers build once against a single protocol, which is why it's often described as a "USB-C port for AI integrations." The protocol has since been adopted by major AI providers including OpenAI and Google DeepMind, and in December 2025 Anthropic donated MCP to the Agentic AI Foundation, a fund under the Linux Foundation ([Wikipedia, "Model Context Protocol"](https://en.wikipedia.org/wiki/Model_Context_Protocol)).

---

## 4. How this pack was published

- Pack file: `PLANNING_PACK.md`, added on branch `add-planning-pack` (not the default branch).
- A pull request was opened from `add-planning-pack` into the default branch `main`, and an automated **Copilot code review** was requested on it.
- The pull request's file list was re-checked to confirm it actually contains `PLANNING_PACK.md` before this pack was circulated.
