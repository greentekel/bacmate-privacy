# Publishing the BacMate privacy policy

`index.html` is the publishable Romanian policy page. `README.md` contains the
same policy text. The page needs no build step, JavaScript, external fonts,
analytics, cookies, or third-party assets. `.nojekyll` keeps branch-based GitHub
Pages publishing static.

## Hosting status

On 27 September 2026, the GitHub repository API reported `has_pages: false` for
`greentekel/bacmate-privacy`. The GitHub connector actions available for this
change do not expose a Pages settings create/update action. Adding these files
or opening/merging their PR does not enable hosting. No live policy URL is
claimed here.

## Enable GitHub Pages after merging

1. Merge the policy PR into `main`.
2. In `greentekel/bacmate-privacy`, open **Settings > Pages > Build and deployment**.
3. Set **Source** to **Deploy from a branch**.
4. Set **Branch** to **main** and **Folder** to **/(root)**, then click **Save**.
   The entry point is the root `index.html`; do not select `/docs`. No custom
   deployment workflow is included, so do not select the **GitHub Actions** source.
5. Check that the Pages deployment succeeds. In **Settings > Pages**, use
   **Visit site** to obtain the actual deployed URL. Enable **Enforce HTTPS** if
   it is available and not already enabled.
6. Open that HTTPS URL while signed out. Confirm that it serves the rendered
   policy, not a repository/file viewer; the full text and
   `bacmate.support@gmail.com` contact must be readable without a login,
   JavaScript, editing permission, or a geographic restriction.
7. Only after that verification, enter the verified URL in the Google Play
   Console privacy-policy field. Do not use a guessed domain, GitHub README/blob
   or raw-file URL, local preview URL, or PDF.

The remaining hosting configuration is **Deploy from a branch / main / /(root)**.
There is no domain purchase or custom-domain configuration required for this setup.

## Keeping the policy consistent

Update `README.md` and `index.html` together, including the revision date. Preserve
the support email. Do not describe local storage as excluding Android-managed
backup/device transfer, or reset/uninstall as erasing every system backup copy.
The policy must continue to disclose possible restoration on reinstall or on
another device and direct users to the phone settings to manage system backups.

This update was checked against `greentekel/bac-app` at commit
`d9ff8bd32cee7ff5d37465ee963bc8738b4916cd`, specifically
`proto-1/app/privacy.tsx`, `proto-1/public/privacy/index.html`, and the backup/reset
caveat in `proto-1/STORE_SUBMISSION.md`. These references require access to that
repository. This is disclosure alignment, not a new audit of the production APK,
SDK behavior, Data safety answers, or release readiness. No BacMate application
code or release decisions are changed here.

For a local preview, open `index.html` directly in a browser. Check narrow/mobile
and desktop widths, light and dark themes, Romanian diacritics, the contact link,
and that the page remains readable with JavaScript disabled. Compare the visible
policy text with `README.md` before publishing.

## Hosting and Play references

- [Configure a GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Create a GitHub Pages site and its entry file](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Google Play User Data policy](https://support.google.com/googleplay/android-developer/answer/10144311?hl=en)
