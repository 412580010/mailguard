# MailGuard — GitHub Pages deployment package

This package contains a single-file static website (`index.html`) plus documentation. It does not need a database, build tools, or an API key.

## GitHub Pages deployment

1. Create a public repository named `mailguard` on GitHub (or choose a unique name).
2. Upload **`index.html` to the repository root**, not the folder containing it. Optionally upload `.nojekyll` and this README.
3. Commit the files to the `main` branch.
4. Open Settings → Pages → Build and deployment. Choose **Deploy from a branch**, Branch **main**, Folder **/(root)**, then Save.
5. When GitHub shows that the site is published, open the link in Pages settings. Typically it is `https://YOUR-USERNAME.github.io/mailguard/` for a repository named `mailguard`.
6. Test in a private/incognito tab as well as locally.

GitHub reference: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Demonstration checklist

- Home page renders with colors and proper layout.
- Sample suspicious email → Analyze → view sender, URL, text-based evidence.
- Sample regular email → Analyze → view result (not a guarantee of safety).
- Switch to .eml mode → sample .eml → inspect header summary.
- Evaluation lab → run 20 synthetic-case tests → compare thresholds → export CSV.
- Browser mobile responsive layout.

## Scope / data handling

- This is a browser-side heuristic research/learning prototype, not a security certification service.
- The score is not a validated probability of phishing.
- SPF/DKIM/DMARC results imported from .eml headers are not independently verified.
- The 20 test cases are synthetic; results are not real-world detection performance.
- Analyze redacted examples; do not add confidential email contents to a public GitHub repository.
