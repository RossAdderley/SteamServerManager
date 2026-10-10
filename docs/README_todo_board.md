SteamServerManager

Scripts to build and manage dedicated servers from SteamCMD.

Collaborative learning repo for Developer A and Developer B. Certifications: GitHub Foundations (GH-900), then PCEP-30-02 / PCAP-31-03.

Developer A — Infrastructure

steamcmd_engine.py, filesystem, subprocess

Developer B — Telemetry

monitor_engine.py, process and resource sampling

Joint

both

this README, main.py, reviews

Collaboration rules

main is protected. Feature branch, pull request, one review from the other developer, then merge.

Every task below becomes a GitHub Issue created by the person who owns it. Do not file the other person's issues.

PR body must include Fixes #n.

Leave at least one review comment before approving.

New work is added to this list first, then filed as an issue.

Todo list

Copy a row into a new issue. Check the box on main only after that issue is closed.

Week 1 — GitHub (no production Python)

[x] A+B Day 1 — Account and clone. Both enable 2FA, both clone this repo, both can show git log. Owner: joint. Acceptance: usernames filled in the roles table via PR.

[x] A Day 2 — Python gitignore. Branch feature/repo-hygiene. Ignore __pycache__/, *.pyc, .venv/, steamcmd/, *.log. Owner: Developer A.

[ ] B Day 2 — Contributing and security stubs. Branch docs/contributing. CONTRIBUTING.md states the PR rule. SECURITY.md stub exists. Owner: Developer B.

[x] A+B Day 2 — License choice. Issue records MIT or Apache-2.0 and adds LICENSE. Owner: whoever does not open the docs PR.

[x] A Day 3 — Labels and milestones. Labels dev-a, dev-b, github, python, bug, docs. Milestones Week 1 — GitHub and Week 2 — Python. Owner: Developer A.

[ ] B Day 3 — README todo PR. This checklist is on main. Owner: Developer B. Branch docs/readme-todos.

[x] A Day 4 — Branch protection. Require a PR and 1 approval on main; no force-push. If the plan cannot enforce it, document the manual rule in CONTRIBUTING.md. Owner: Developer A.

[ ] B Day 4 — End-to-end practice PR. One-line README status change, changes requested once, then approval and merge. Owner: Developer B.

[ ] A+B Day 5 — Conflict lab. Both edit the same README line on separate branches. Second merger resolves markers and explains them in the PR. Owner: Developer B resolves; Developer A merges first.

Week 2 — Python

[ ] A Day 6 — Scaffold. requirements.txt pins psutil. main.py prints the Python version. Branch feature/python-scaffold. Owner: Developer A.

[ ] B Day 6 — Scaffold review. Run the scaffold, comment the version observed, approve. Owner: Developer B.

[ ] A Day 7 — steamcmd_engine skeleton. steamcmd_dir(), binary_exists(), build_update_command(app_id) using os.path and a list of args. Handle FileNotFoundError. No live download required to merge. Owner: Developer A.

[ ] B Day 8 — monitor_engine skeleton. sample(pid) returns a dict with status, cpu, rss_mb. Defensive except for a missing process. Owner: Developer B.

[ ] B Day 9 — Cross-test engine. Pull A's branch, import the command builder, paste one result in the review. Owner: Developer B.

[ ] A Day 9 — Cross-test monitor. Pull B's branch, call sample with a fake pid, paste the dict in the review. Owner: Developer A.

[ ] A+B Day 10 — Orchestrator. main.py takes an app id, calls the command builder, and prints a status dict. README usage matches the CLI. Co-authored commit or split commits. Owner: joint.

[ ] A+B Day 11 — App-id conflict lab. Conflicting edits to the default app id constant. Resolved value is commented. Owner: Developer B resolves.

[ ] A+B Day 12 — Mock and retro. Score Q1–Q8 from the lesson guide. Missed items are added here, then filed as issues by the owner. Owner: joint.

Backlog (file only after Day 12 retro)

[ ] A — Live SteamCMD bootstrap. Download and unzip the official binary into steamcmd/ (gitignored). Owner: Developer A.

[ ] B — Log tail. Read steamcmd.log with a specific except order (FileNotFoundError before OSError). Owner: Developer B.

[ ] A — GitHub Action py_compile. Workflow runs python -m py_compile on pull requests. Owner: Developer A.

[ ] B — Small class wrapper. One class around the sampler so PCAP OOP objectives are practiced. Owner: Developer B.

Status

TRACK_STATUS: not started
