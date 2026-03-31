---
layout: default
title: Privacy Policy — Chronos
---

# Privacy Policy — Chronos

**Effective Date:** March 31, 2026
**Developer:** Chronos Labs

---

## Overview

Chronos is a macOS task-scheduling application. This policy explains what data Chronos accesses, how it is used, and where it is stored.

**The short version:** Chronos does not collect, transmit, or sell any personal data. Your tasks stay on your machine. The only network communication is directly with Google's Calendar API, authorized by you.

---

## Data Chronos Accesses

### Google Calendar Data
When you connect your Google account, Chronos accesses:
- **Your calendar list** — to show which calendars are available for blocking time.
- **Calendar events** — to read start/end times of existing events so it can schedule around them.
- **Chronos-created events** — to write, update, and delete task blocks that Chronos places on your calendar.

Chronos uses the Google Calendar API with OAuth 2.0 (PKCE flow). Authorization tokens are stored locally in your macOS Keychain — they are never transmitted to any server other than Google's.

Chronos does **not** access your email, contacts, files, or any other Google service.

### Task Data
Your tasks (names, deadlines, hours, priorities, recurrence rules) are stored as a JSON file in a folder you choose on your Mac. If you select a cloud-synced folder (iCloud Drive, Dropbox, Google Drive), the file syncs via that service's own mechanism — Chronos does not perform the sync.

### Preferences
App preferences (availability windows, scheduling settings, selected calendars) are stored locally in the same sync folder alongside your tasks.

---

## Data Chronos Does NOT Collect

- No analytics or usage tracking
- No crash reporting
- No device fingerprinting
- No advertising identifiers
- No personal information beyond what is described above
- No data is sent to Chronos Labs or any third party

---

## Data Storage & Security

| Data | Location | Encryption |
|------|----------|------------|
| OAuth tokens | macOS Keychain | Keychain encryption (AES-256) |
| Task data | User-selected folder | At rest: depends on your disk encryption (FileVault) |
| Calendar events | Google's servers | Google's security policies apply |
| Preferences | User-selected folder | At rest: depends on your disk encryption |

Chronos communicates exclusively over HTTPS. All Google API requests use TLS 1.2+.

---

## Third-Party Services

| Service | Purpose | Data Shared |
|---------|---------|-------------|
| Google Calendar API | Read events, write task blocks | Calendar event times, task block titles/times |

No other third-party services, SDKs, or frameworks are integrated.

---

## Data Retention & Deletion

- **Task data:** Deleted when you delete the JSON file from your sync folder or remove tasks within the app.
- **OAuth tokens:** Removed from Keychain when you disconnect your Google account in Chronos settings. You can also revoke access at [https://myaccount.google.com/permissions](https://myaccount.google.com/permissions).
- **Calendar events:** Chronos-created events can be deleted from Google Calendar at any time. Chronos deletes and regenerates its own events during each reshuffle cycle.

Uninstalling Chronos removes the application. To fully clean up:
1. Delete the Chronos folder from your sync location.
2. Remove the Keychain entry (or disconnect Google in settings before uninstalling).
3. Revoke Chronos access in your Google account permissions.

---

## Children's Privacy

Chronos does not knowingly collect data from children under 13. The app does not collect data from anyone.

---

## Changes to This Policy

If this policy changes, the updated version will be posted at [https://walkergrimshaw.github.io/chronos-privacy/](https://walkergrimshaw.github.io/chronos-privacy/). The effective date at the top will be updated.

---

## Contact

Questions about this privacy policy:

**Email:** nick@walkergrimshaw.com
**Support:** [https://docs.google.com/forms/d/e/1FAIpQLSfyxP4Vt2ONcz75dmuFynEHW1IGrHL6KZXlCvWj-bXdGN9DZg/viewform](https://docs.google.com/forms/d/e/1FAIpQLSfyxP4Vt2ONcz75dmuFynEHW1IGrHL6KZXlCvWj-bXdGN9DZg/viewform)
