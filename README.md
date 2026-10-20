# SIDEQUEST · Taft Radar

**V12 enhanced classroom prototype | Student web development project**

SIDEQUEST is a browser-based demonstration of citizen reporting for non-emergency concerns in selected public spaces around **Taft–Vito Cruz, Manila**. It is **not** operated by a government agency, is not an emergency service, and does **not** send real submissions to public authorities.

## Start the website

Download/extract the complete folder, then **double-click `index.html`**. Keep `enhancements.css`, `enhancements.js`, `v12.css`, and `v12.js` in the same folder. No dependencies or internet connection are needed to view the illustrated map and use the demo features. An optional link opens the actual street map on OpenStreetMap (internet required).

For GitHub Pages, upload `index.html`, `enhancements.css`, `enhancements.js`, `v12.css`, and `v12.js` to your repository root, then enable Pages in **Settings > Pages > Deploy from a branch > main > /(root)**. Also include this README and supporting documentation.

## Demo accounts

Use the Log in / Join action on the public homepage, then choose a demo account from the welcome screen:

| Role | Demo email | Demo password |
| --- | --- | --- |
| Citizen | `explorer@example.test` | `DemoOnly123!` |
| Coordinator | `coordinator@example.test` | `DemoOnly123!` |
| Second citizen | `neighbor@example.test` | `DemoOnly123!` (use manual login) |

You can also create a fictional local citizen profile. **Do not use your real credentials or private information.** The credentials and role checks are mock implementations in JavaScript, not secure authentication.

## What visitors can do

- **Without signing in:** See the homepage, how the proposed reporting workflow works, review public sample issues, explore the illustrated map and accessible issue list, filter by area/category/status/date, search example landmarks, read About/Guidelines, and inspect public case history.
- **As a citizen:** Submit a structured report, preview/remove a photo, place an approximate location pin or request browser location permission, save/restore a text draft, review answers before submitting, get a case reference, track private and public reports, confirm an existing concern with optional evidence, follow cases and view unread updates, request another review, and personalize an avatar/appearance.
- **As a coordinator:** Use the separate operations interface to review submissions and confirmations, mark duplicates, document reasons and statuses, record proposed assignment/referral acceptance, set next review dates, add private versus public notes, attach resolution evidence, view an action trail and analytics, export a case as PDF or print with evidence, and export filtered/aggregated monthly CSVs.
- **Rewards:** Earn XP only after coordinator verification; levels grant profile titles, cosmetic frames, and badges. The neighborhood garden grows for recorded resolved cases, with each plant linking to its case history.

## How XP and leveling work

| Verified action | Recognition |
| --- | --- |
| First useful, unique verified case | +20 XP |
| Approved contribution to an existing case | +10 XP |
| Unverified, duplicate, rejected, or repeated confirmation | 0 XP |
| Daily cap | Up to **60 XP/day** in this demo |

Each **100 total XP** increases the explorer's level. Your level and cosmetic unlocks persist in this browser's demo storage.

| Level | Total XP | Digital unlock |
| --- | ---: | --- |
| 1 | 0 | New Explorer; plain profile frame |
| 2 | 100 | Neighborhood Helper; Leaf frame |
| 3 | 200 | Radar Scout; Sunrise frame |
| 4 | 300 | Taft Keeper title |
| 5 | 400 | Local Legend; Gold frame |
| 6 | 500 | Rooftop Guardian title; Rooftop frame |

When verification pushes you to the next level, a level-up modal announces your new title and directs you to **My Activity > Rewards & badges**, where an unlocked frame can be equipped. XP is **not cash, a school incentive, an official certificate, or priority access to a government service**. Cosmetic features are optional, and report priority is based on accessibility/impact, not XP or popularity.

## Example pitch demonstration (3–5 minutes)

1. Open the public home page and show the illustrated issue map plus **From report to recorded action**.
2. Sign in as Citizen. Start a report, choose area/category, type a description, pin a location, **Save draft**, then **Review report** and submit.
3. Copy its `SQ-DEMO-...` receipt. Explore > list view shows your pending report only when signed in; others cannot browse it yet.
4. Sign out; sign in as Coordinator. Open the new case. Record notes, assign a coordinator, verify its status, and document a proposed referral (not a government action).
5. Sign in as Citizen again, track the report, follow it, and view XP after verification.
6. Explore another reviewed case and use **I experienced this too**. Switch to Coordinator to approve the confirmation; this awards 10 XP once.
7. To show exception paths, create an extra sample report and choose `duplicate` with the original reference, or choose `rejected` with a reason. For reopening, mark a case resolved through the appropriate status transitions, then ask the reporter to use **Request a recheck**.
8. Demonstrate the admin analytics and CSV/PDF exports. Clearly identify all figures as sample data.

## The illustrative map

The built-in map is a **stylized map**, with Taft, Ocampo and Vito Cruz labels and roughly placed report markers. The pin position is **not** sufficiently accurate for navigation or official dispatch. The Explore page can open an external **OpenStreetMap street view** for actual street geometry. Searchable landmarks and optional geolocation in the report form do not turn the local illustration into survey-accurate mapping.

## Browser-only limitations

This GitHub Pages version uses **localStorage and sessionStorage** and simulates user roles. Changes only exist in one browser/profile. Two different users on two devices will **not** see the same stored reports, and user identity / coordinator permissions are not secure. Image previews are limited by browser storage quotas. The basic EN/FIL switch translates key navigation items only; it is not a complete Filipino localization.

The actual deployment would require a secured API, shared database, real authentication, file storage, image moderation, consent/privacy policies, backups, monitoring, verified pilot boundaries and signed agreements with receiving agencies. See [`DEPLOYMENT_PLAN.md`](DEPLOYMENT_PLAN.md).

## V12 additions

V12 adds three original street-level guardian explorer looks, live cosmetic rewards progress, an optional on-demand OpenStreetMap street embed for Vito Cruz, and plain-language tracking status definitions. The real street embed and the approximate in-app issue pins are separate. See [`V12_RELEASE_NOTES.md`](V12_RELEASE_NOTES.md) for a complete changelog and caveats.

## Project documents

- [`PROJECT_BLUEPRINT.md`](PROJECT_BLUEPRINT.md): problem definition, user flows, use cases, data model and system architecture.
- [`DEPLOYMENT_PLAN.md`](DEPLOYMENT_PLAN.md): production requirements and security/privacy checklist.
- [`PITCH_AND_TESTING.md`](PITCH_AND_TESTING.md): four-page pitch, demonstration cases, acceptance tests and usability metrics.
- [`QA_REPORT.md`](QA_REPORT.md): tests run and known limits.
- [`CITIZEN_GUIDE.md`](CITIZEN_GUIDE.md) and [`COORDINATOR_GUIDE.md`](COORDINATOR_GUIDE.md): quick user instructions.

## Design direction

Friendly mint/cream/lavender styling, purposeful map interactions, readable spacing, optional pastel themes, a simple original mascot and an **original neighborhood-rooftop Guardian** unlock. The urban guardian motif is inspired by street-level stories; there are **no licensed Marvel characters, logos or images** in this project.
