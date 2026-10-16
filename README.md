# SIDEQUEST: Taft Radar

**A classroom prototype of a location-based community reporting website.**

SIDEQUEST lets visitors explore **fictional example concerns** around a stylized Taft–Vito Cruz map, submit sample reports, track case updates, confirm another user's issue, and try a separate coordinator workspace. Verified demo contributions earn XP and profile cosmetics.

> **Important:** This is a student-created prototype, **not an official government, Benilde, or Manila reporting service**. Reports entered here are **not sent to an agency**, the map is illustrative, and changes are stored only in your browser. **Do not enter real personal information, private photos, or real complaints.**

## Open the site

- **Locally:** Double-click `index.html` to open it in Chrome or Edge. Some browsers restrict local storage on files; if that happens, data is temporary.
- **On GitHub Pages:** Create a repository, add the contents of this folder to the repository root, and push to your branch. Under **Settings → Pages**, select **Deploy from a branch**, `main`, `/ (root)` and save. Once published, use the GitHub Pages URL shown in Settings. (Availability and names of Pages controls can change.)
- You do not need Python, a database, Node, or an API key for this **demo**.

## Explore as a demo user

The welcome screen includes **Try as citizen** and **Try as coordinator**. For the sample email/password demo login, use:

| Role | Email | Password |
| --- | --- | --- |
| Citizen | `explorer@example.test` | `DemoOnly123!` |
| Coordinator | `coordinator@example.test` | `DemoOnly123!` |

These are intentionally **public demo accounts**. Never reuse their passwords anywhere else.

## Main features

- Responsive citizen homepage, stylized neighborhood map, issue filters and report pins
- New report and photo-preview form with basic validation
- Private visibility for pending demo reports; a reporter can still find their own pending pin
- Reference-number tracking and case history
- Similar-issue suggestions and **I Experienced This Too** confirmation requests
- Separate coordinator workspace with review queue, filters, case status actions, and contribution review
- XP for verified activity, levels, profile frame unlocks, themes and avatars
- Demo registration, login, and account settings

## Technical notes

- The project is a **single HTML file** with embedded CSS and JavaScript.
- Data is saved in browser `localStorage` when available; each browser/device has **its own separate data**.
- No hosted authentication, shared database, actual permissions, server-side file storage, email delivery, or LGU integrations exist in this version.
- Demo passwords use a small client-side hash for simulation only. **That is not secure authentication.** The coordinator profile is intentionally accessible to reviewers in this demo.
- The map is **illustrative** and does not support accurate street-level navigation or geospatial verification. Any visible sample reports are fictional.
- Use a real back end with enforced authorization, secure password handling and storage, verified map geodata, consent/privacy safeguards, and an authorized receiving organization before attempting real public reporting.

## Project scope

**Target prototype area:** Taft–Vito Cruz vicinity, Manila. **Reporting categories:** pedestrian access, cleanliness, public infrastructure and transport access, plus relevant other public-space concerns. Emergencies and confidential matters are out of scope.

The classroom pitch uses four required pages: **Home, Report / Upload Evidence, Track Report Status, and Admin Dashboard**, each in desktop and mobile layouts.

See [`QA_REPORT.md`](QA_REPORT.md) for checks, known limitations, and next steps.
