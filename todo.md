# Privacy Policy Navigation Plan

## Goals
- Add a privacy-policy landing page that lets users pick between the two apps.
- Keep everything on the same site, with English/Arabic support per app.
- Make back navigation obvious and predictable.

## Plan
1) Add a privacy-policy hub page (English and Arabic)
   - Create `policies/index.html` with two clear options:
     - “Zam Calendar” → `policies/privacy-policy.html`
     - “Zam Calendar Business” → `policies/privacy-policy-business.html`
   - Create `ar/policies/index.html` with Arabic copy and RTL layout:
     - “تقويم زام” → `ar/policies/privacy-policy.html`
     - “تقويم زام للأعمال” → `ar/policies/privacy-policy-business.html`
   - Include a simple header nav: Home, Contact.

2) Update the main site footer links to point to the hub
   - In `index.html`, update the English privacy policy link to `policies/index.html`.
   - Update the Arabic footer link to `https://zamcalendar.com/ar/policies/index.html`
     (or a relative `/ar/policies/index.html` if you want to avoid absolute URLs).

3) Enhance the existing Zam Calendar policy pages
   - Add a “Back to Privacy Policies” link in the header nav:
     - English: `policies/privacy-policy.html` → `policies/index.html`
     - Arabic: `ar/policies/privacy-policy.html` → `ar/policies/index.html`
   - Fix the language switcher targets so they point to the current Arabic/English paths
     (the English page currently references `/policies/privacy-policy-ar.html`, which does not exist).

4) Add Zam Calendar Business policy pages (English + Arabic)
   - Create `policies/privacy-policy-business.html` by copying the existing English template.
   - Create `ar/policies/privacy-policy-business.html` by copying the existing Arabic template.
   - Update titles, meta descriptions, and in-page product naming to “Zam Calendar Business”.
   - Wire the language switchers to each other (English ↔ Arabic).
   - Include the “Back to Privacy Policies” link in the header nav on both pages.
   - Insert the final business privacy policy text (needs confirmation of the exact copy).

5) Navigation + back button behavior
   - Primary path: `index.html` → `policies/index.html` → chosen app policy page.
   - Browser back should return to the hub page naturally.
   - The explicit “Back to Privacy Policies” link ensures users can return without relying on browser history.

## Open Items
- Confirm the exact English/Arabic text for the Business privacy policy.
- Confirm the final app naming (“Zam Calendar Business” vs “Zam Calendar Dash Business”).
