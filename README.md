# WonderTales AI — public site package

A static, mobile-friendly site drafted on 15 November 2026 for the WonderTales AI project's public homepage, privacy policy, and terms of service.

## Contents
- `index.html`: homepage and transparent description of the owner-operated YouTube uploader.
- `privacy.html`: draft privacy disclosure and revocation guidance.
- `terms.html`: draft terms, including required YouTube ToS link.
- `styles.css`: styling; no JavaScript or tracking code.
- `.nojekyll`: GitHub Pages static publishing.

## IMPORTANT: Before publishing
1. **Replace every occurrence** of `REPLACE-WITH-YOUR-PUBLIC-SUPPORT-EMAIL` across `privacy.html` and `terms.html` with a dedicated, public support email **you approve exposing on the internet**. Search files for the exact placeholder and check none remain. Do not put a secret or personal email there without consent.
2. Review the privacy and terms claims against the real implementation and your legal obligations; these are starting drafts, not legal advice. In particular, the revocation/deletion procedure described in `privacy.html` must be operationally implemented before production.
3. The repository was inspected as of 15 November 2026: `src/publish_due.py` requests `youtube.upload` and `youtube.readonly`, verifies the expected channel ID, lists previous uploads/tags, and schedules videos. The `automatic-production.yml` workflow is gated and isn't production-authorized yet.
4. Confirm any third-party analytics, forms, hosting logs, email, or other data processing if you later add them; update the Privacy Policy accordingly.
5. If Google OAuth verification is required, you need a registered, verifiable custom domain. A shared `github.io` or `pages.dev` hostname **does not guarantee domain ownership verification**.
6. Keep the private `wondertales-ai-production` repository private; create a *separate public repo* for this site.

## Publish temporarily on free GitHub Pages
1. On GitHub select **New repository**; name it `wondertales-ai-website` and make it **Public**.
2. Upload the six website files (including `.nojekyll`; GitHub web UI may hide dotfiles, but it isn't required for this simple HTML site).
3. Open repo **Settings → Pages → Build and deployment → Deploy from a branch**; select `main` and `/ (root)`, then Save.
4. After GitHub publishes, visit `https://harshsinghps57-spec.github.io/wondertales-ai-website/` to preview. This is a *predicted* address, not a verified live page.
5. Later add a domain you purchase under **Settings → Pages → Custom domain**, configure its DNS per GitHub guidance, and confirm HTTPS works.
6. Verify **your own custom domain** in Google Search Console, then add its root domain to Google Auth Platform → Branding → Authorized domains, and enter exact live URLs for homepage, privacy policy, and terms. Submit verification as Google requires.

## Notes
- No Google OAuth buttons or API requests are in this site. Do not place OAuth credentials in these files.
- The production system requires a separate authorization flow and compliance work; these pages alone do not remove YouTube Data API new-project private-upload restrictions or OAuth testing token expiration.
- Review and approve public contact details and legal wording before publishing.
