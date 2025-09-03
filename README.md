<p align="center">
  <img src="https://media.giphy.com/media/Ju7l5y9osyymQ/giphy.gif" width="250" alt="Banner">
</p>

<h1 align="center">🔥 <strong>GitHub Streak Maintainer Pro+</strong> 🔥</h1>
<p align="center"><em>Keep your streak alive, even while you sleep!</em></p>

---

<p align="center">
  <img src="https://img.shields.io/github/stars/SaeedX302/Github-Streak-Maintainer?style=for-the-badge&logo=github" alt="Stars">
  <img src="https://img.shields.io/github/forks/SaeedX302/Github-Streak-Maintainer?style=for-the-badge&logo=git" alt="Forks">
  <img src="https://img.shields.io/github/license/SaeedX302/Github-Streak-Maintainer?style=for-the-badge&logo=apache" alt="License">
  <img src="https://img.shields.io/badge/Automation-100%25-brightgreen?style=for-the-badge&logo=github-actions" alt="Automation">
</p>

---

## <p align="center">📜 <strong>About This Project</strong></p>
<p align="center">
🔥 <strong>Automate your GitHub streak like a pro!</strong> <br>
This project ensures your GitHub contributions never stop. It updates your <code>README.md</code> automatically multiple times a day with cool entries, random quotes, and stylish logs. 
</p>

---

## Sequence Diagram(s)
```mermaid
sequenceDiagram
  autonumber
  actor User as User
  participant GH as GitHub Scheduler/Dispatch
  participant WF as Actions Runner
  participant SH as "Update README" Step
  participant G as Git (local)
  participant R as origin/main

  GH->>WF: Trigger workflow (cron / manual)
  WF->>G: checkout repo
  WF->>G: configure author (name/email)
  WF->>SH: run "Update README"
  rect rgb(238,245,255)
    note right of SH: Build TIMESTAMP, pick COMMIT_MSG and RANDOM_QUOTE
    SH->>SH: Ensure README has table header
    SH->>SH: Count rows and append new table row
  end
  SH->>G: git add README.md
  alt README changed
    SH->>G: git commit -m COMMIT_MSG
    WF->>G: git pull --rebase origin main
    WF->>R: git push origin HEAD:main
  else No changes
    SH->>WF: Skip commit/push
  end
```

## <p align="center">🔥 <strong>Key Features</strong> 🔥</p>
- ✅ **Fully Automated** – No manual commits needed.
- ✅ **Random Quotes + Emojis** – Looks natural, fun & engaging.
- ✅ **Beautiful Commit History Table** – Grows every update.
- ✅ **Multiple Daily Commits** – Stay super active.
- ✅ **Works with GitHub Actions** – 100% free automation.

---

## <p align="center">🚀 <strong>Quick Start</strong></p>

###  1. Fork This Repo  
<p>
<a href="https://github.com/SaeedX302/Github-Streak-Maintainer/fork">
<img src="https://img.shields.io/badge/FORK-REPO-blue?style=for-the-badge&logo=github" alt="Fork Badge">
</a>
</p>

###  2. Edit Workflow File  
Go to:

    .github/workflows/streak.yml

Replace:
- `user.email` → Your GitHub **noreply email**
- `user.name` → Your **GitHub username**


###  3. Save & Run Workflow  
`- Commit changes`  
`- Go to **Actions tab** → Run Workflow manually (or wait for schedule)`
    
---

## <p align="center">🌍 <strong> Deployment </strong></p>

No external server required.

Just upload files → GitHub Actions will handle everything.



---

## <p align="center">📝 <strong>Changelog</strong></p>

<details>
<summary>Click to Expand</summary>v1.0 → Initial release with README auto-update feature.

v1.1 → Added random quotes + multiple commits daily.

v2.0 → Pro Design + Commit History Table + Stylish UI.


</details>

---

<p align="center">
  <img src="https://forthebadge.com/images/badges/built-with-love.svg" alt="Built with Love">
  <img src="https://forthebadge.com/images/badges/powered-by-coffee.svg" alt="Powered by Coffee">
  <img src="https://forthebadge.com/images/badges/uses-git.svg" alt="Uses Git">
</p>

---

## 🚀 GitHub Streak Tracke (Pro+)

![Streak](https://img.shields.io/badge/Streak-Active-brightgreen)

---

## 📅 Commit History
| # | Date & Time (UTC) | Message | Quote |
|---|--------------------|---------|-------|

| -1 | 2025-09-02 19:38:07 | Random change 🏞️ | 🔥 Keep the flame alive |
| 0 | 2025-09-02 23:26:17 | Small tweak 🌳 | 🕯️ Light in the darkness |
| 1 | 2025-09-03 05:33:13 | Random change 🏞️ | ⚡ Power never dies |
