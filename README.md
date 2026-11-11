# pages.pulipuli.info

Official GitHub Pages website for pulipuli.info, hosting public project and application information.

- Intended public URL: https://pages.pulipuli.info/
- Repository: https://github.com/pulipulichen/pages.pulipuli.info
- Public homepage: [index.html](./index.html)
- App privacy pages are published from package-name folders on this site; other policy source materials remain in https://github.com/pulipulichen/Android-APP-Privacy-Policies.

## First-time GitHub Pages setup

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then click **Save**.
4. Under **Custom domain**, enter `pages.pulipuli.info` and click **Save**. When publishing from a branch, GitHub will create a root `CNAME` file.
5. At the DNS provider for `pulipuli.info`, add a DNS record:
   - Type: `CNAME`
   - Host/name: `pages`
   - Target/value: `pulipulichen.github.io`
6. After DNS resolves and GitHub issues a certificate, enable **Enforce HTTPS** under Settings → Pages.
7. Verify https://pages.pulipuli.info/ in a browser.

> Add the custom domain in GitHub Pages settings **before** adding the DNS CNAME, to reduce subdomain takeover risk. This setup does not require changing DNS for `pulipuli.info` or `blog.pulipuli.info`.

## App privacy pages

- **Split View Launcher** (Chrome extension): [public privacy policy (English / 繁體中文)](https://pages.pulipuli.info/split-view-launcher/) · Published page: `split-view-launcher/index.html`
- **Website Shortcut** (`info.pulipuli.app.websiteshortcut`): [public privacy policy](https://pages.pulipuli.info/info.pulipuli.app.websiteshortcut/)
- **Canonical HTML source:** [Android-Website-Shortcut/google_play/privacy-policy.html](https://github.com/pulipulichen/Android-Website-Shortcut/blob/main/google_play/privacy-policy.html)
- **Published mirror:** `info.pulipuli.app.websiteshortcut/index.html`

When the policy changes, update the HTML in the Android app repository first, then copy the exact same file to this package-name folder. Keep the URL in the app's `google_play/APP_METADATA.md`, Google Play instructions, and in-app About page aligned with the published page. Verify the public URL after deployment.

## Google OAuth notes

- You may use `https://pages.pulipuli.info/` as a public site URL, but an OAuth app submitted for verification should have an **app-relevant** homepage and privacy policy.
- Verify the `pulipuli.info` **Domain property** in Google Search Console using the Google Cloud project's owner/editor account, then configure authorized domains as required.
- For an External OAuth project in **Testing**, authorizations involving Drive scopes generally expire after seven days; a GitHub Pages domain **alone does not fix** repeated `authorizeDrive` prompts. Review the project's Audience / Publishing status and required verification.

Official documentation: [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) · [GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) · [Google OAuth Audience](https://support.google.com/cloud/answer/15549945).
