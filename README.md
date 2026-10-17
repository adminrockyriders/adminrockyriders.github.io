# Rocky Riders website

The public website for **Rocky Riders**, the club app of the Castlemaine Rocky Riders mountain bike club.
It's served by GitHub Pages at **https://adminrockyriders.github.io/**.

The app itself is in a separate, private repository. This repository only holds the public pages that
the app stores and sign-in providers link to.

## Pages

| Page | URL | Used by |
|---|---|---|
| Home | `/` | Store support URL, Google sign-in branding (home page) |
| Privacy policy | `/privacy/` | Google Play, App Store Connect, Google sign-in branding, in the app |
| Terms of use | `/terms/` | Google sign-in branding |
| Delete your account | `/delete-account/` | Google Play account-deletion link |

**Don't rename or move these pages.** Google Play, App Store Connect and Google's sign-in setup point
at these exact URLs. A broken link can get the app's store listing or Google sign-in flagged.

## Files that must stay

- `googlee1ff3c4542365181.html` - proves to Google Search Console that the club owns this site
  (needed for the Google sign-in branding check). Don't delete it.
- `.nojekyll` - tells GitHub Pages to serve the files as they are (no Jekyll build).
- `icon.png` - the club badge used as the page icon and logo.

## Editing the privacy policy

The app has its own copy of the privacy policy, for Android and iPhone. **When you change
`privacy/index.html`, change the app's copy to match, and update the "Effective" date on both.**

1. Edit `privacy/index.html` and update the "Effective" date.
2. Make the same change in the app repository: `MBRMA/app/(auth)/privacy-policy.tsx` (Android) and
   `MBRMA/app/(auth)/privacy-policy.ios.tsx` (iPhone).
3. If the app now collects something new, update **Play Console → App content → Data safety**
   (and App Store Connect's App Privacy answers once the iPhone app is listed).

The pages are plain HTML and CSS (`style.css`), with no build step. A push to `main` goes live about a
minute later.

## Contact

Club app support: **adminrockyriders@gmail.com**.
To report a security problem, see [SECURITY.md](SECURITY.md).

© Castlemaine Rocky Riders. All rights reserved. The text, club name and badge may not be reused
without the club's permission.
