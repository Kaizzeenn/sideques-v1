# SIDEQUEST pre-GitHub release audit

**Audit target:** fixed V10 browser-demo HTML, prepared as `index.html`.

## Automated checks completed

- JavaScript syntax checked with Node (`--check`) for the five embedded scripts.
- Chromium smoke tests for desktop (1366px), tablet (768px), and mobile (390px): citizen navigation, no horizontal overflow on main pages, no JavaScript page errors.
- Demo sign-in and role-gated coordinator access tested.
- Citizen report submission, reporter-only pending case access, coordinator verification, and +20 XP award tested.
- Confirmation workflow, repeat-contribution rejection, admin approval, and +10 XP award tested.
- Existing-issue lookup/report tracking and sample XSS-escaping regression tested.
- Admin review interface, search filter, and zero-results feedback tested.
- Reward frame switching and avoidance of repetitive “equipped” toasts tested.
- Theme selections previewed and changed correctly in the test browser.

## Fixes made in this release candidate

1. **Public demo warning strengthened.** Explicit notice that reports remain local and are not sent to an agency.
2. **Validation tightened.** Invalid calendar dates such as February 31, future dates, and display names over 42 characters are rejected.
3. **Privacy improved.** Public visitor statistics no longer include pending or rejected private reports.
4. **Map input bounded.** Invalid/out-of-range user-provided coordinate pairs are not stored as valid pin positions.
5. **Keyboard focus styling improved.** Visible focus outlines and reduced-motion preferences respected.
6. **Reference placeholder corrected.** Duplicate report example now matches the classroom ID format.

## Deployment limits and unresolved production blockers

**GitHub Pages may host this as a public portfolio/classroom demo only.** It is not suitable for real public complaints or as a production citizen reporting application.

- Registration and admin access exist **only in browser-local simulation**. There is no secure sign-in, shared access control, or centrally managed user account.
- Different visitors will **not** see one another's submitted concerns.
- Uploaded image previews, demo details, and test credentials may remain in the visitor's browser storage; use only fictional data.
- Publishing the source makes the **demo** credentials, workflows, and client-side hashing visible, which is expected for a demonstration.
- Actual address/street mapping, geolocation accuracy, authorized LGU referrals, notices, and real resolution verification are not implemented.
- Accessibility has only received basic keyboard, responsive, and reduced-motion checks. A complete WCAG/screen-reader audit is still required.
- Long-term data persistence on an actual GitHub Pages origin **has not been end-to-end tested here**; the test browser restricted navigation to locally hosted URLs.
- No independent external security review or multi-device/browser compatibility study has been completed.

## Before making this a live public service

1. Choose an authorized managing organization and documented referral paths.
2. Move registration, sessions, validation, evidence, user permissions, and report data to a securely hosted backend.
3. Implement consent, privacy notices, data retention/deletion, image moderation, audit logs, and rate limiting.
4. Use a licensed, accurately located geospatial map and validate report coordinates.
5. Perform end-to-end cross-browser, keyboard/screen-reader, load, privacy, and security tests.
6. Conduct user testing with intended visitors in the pilot area and revise the flow based on results.

## Suggested final manual check on your device

Open `index.html` in Chrome and Edge, test registration **with fake credentials**, create a sample report, check the private pin and tracking ID, switch to coordinator, verify the report, confirm from another demo profile, check XP and unlocked frame, change the UI theme, and reload to test local storage behavior in your browser. Check a 375–390px wide mobile viewport.
