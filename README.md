# Bank Guarantee Letter Generator

Axis Services Group tool for producing bank guarantee cover letters with an acknowledgement slip, one per project,
as PDF or Word. Single letters, batches from an Excel template, and per-state letterhead profiles.

Access is restricted to Axis Microsoft 365 accounts (Entra ID sign-in via MSAL).

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The app. Redirects to `login.html` when no one is signed in. State logos and the Word template are embedded. |
| `login.html` | Shared Axis sign-in page (Microsoft popup sign-in). |
| `app-config.js` | App name shown on the sign-in page. The only file to edit per app. |
| `msal-browser.min.js` | Microsoft Authentication Library for the browser (v2.38.3). |
| `axis services group.jpg` | Axis Services Group logo (header, sign-in page, Group letterhead). |
| `favicon.png` | Browser tab icon. |

## Deploying

Serve the files from the root of a web host over HTTPS; the pages reference `/login.html`, `/index.html` and
`/msal-browser.min.js` by absolute path. The site's address (`https://<host>`) must be listed as a redirect URI
(Single-page application) on the Entra app registration, the same as other Axis apps using this sign-in.

## Notes

- State profiles, uploaded logos and signatures are saved in each user's browser (localStorage), not on a server.
- Branding follows the Axis Services Group Corporate Branding Guidelines (August 2025).
