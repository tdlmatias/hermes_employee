# Jobudo · Hermes AI Employees

Premium animated static landing page for independent managed Hermes-powered content, competitor research and lead-generation services.

## Publish on GitHub Pages

No framework, installation, build step, API keys or custom Actions workflow is needed.

1. Create an **empty** GitHub repository, for example `hermes-ai-employees`. For the simplest free hosting route, use a public repository. Do not initialize it with a README, license or gitignore because this package already contains its own files.
2. Extract this archive and open a terminal inside the `hermes-ai-employees-github-pages` folder. Upload **all contents**, including `docs/.nojekyll`, or use Git:

```bash
git init -b main
git add .
git commit -m "Add Jobudo AI employees website"
git remote add origin https://github.com/YOUR-USERNAME/hermes-ai-employees.git
git push -u origin main
```

Replace `YOUR-USERNAME` and the repository name with your actual destination. Git may ask you to configure your author name/email and authenticate. Use your normal GitHub credential manager or SSH setup. Never put a token in the repository or remote URL. This source distribution does not include Git metadata.

3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch **main** and folder **/docs**, then **Save**.
6. Wait for the Pages deployment to succeed in the repository's Actions tab. Use the actual URL shown in Settings → Pages. For a normal project repository it will look like:

```text
https://YOUR-USERNAME.github.io/hermes-ai-employees/
```

The relative asset paths also support a user/organization site or custom domain. For a user site, the repository must be named `YOUR-USERNAME.github.io`. No custom domain is configured in this package.

### Alternative: upload through GitHub's browser

Upload README.md, .gitignore, THIRD_PARTY_NOTICES.md and the entire docs folder to the repository. Ensure `docs/.nojekyll` is included, since some file pickers hide dotfiles. Commit to main, then select main /docs in Pages settings as above.

## Local preview

From the repository root:

```bash
python3 -m http.server 8000 --directory docs
```

Open `http://localhost:8000/`. Static hosting only serves this landing page; it does not run Hermes agents or Firecrawl.

## Structure

```text
docs/
  .nojekyll
  index.html
  hermes-logo.png
  LICENSE-Hermes.txt
.gitignore
README.md
THIRD_PARTY_NOTICES.md
```

Only `docs/` is published. The site assets are unchanged from the reviewed source. No preview claim tokens, deployment state, QA output, screenshots or private files are included.

## Edit the site

- Copy, layout, inline styles and JavaScript: `docs/index.html`.
- Booking links: search for `https://calendly.com/tchizematias/` in that file. There are five links.
- Logo and upstream notice: `docs/hermes-logo.png` and `docs/LICENSE-Hermes.txt`.
- Motion respects the browser's reduced-motion preference and has an explicit pause control.

Commit and push future edits through your usual review process; once merged to `main`, Pages will redeploy automatically after setup.

## Verification and status

This package is locally browser-tested at desktop/mobile sizes and at a repository subpath. GitHub publication and GitHub's deployment workflow are not yet executed or verified. Do not treat the example URL above as a live website.

## Attribution

Jobudo is an independent service, not affiliated with or endorsed by Nous Research. See THIRD_PARTY_NOTICES.md and docs/LICENSE-Hermes.txt. No new blanket software license is assigned to Jobudo's site content by this package.

Official Pages setup documentation:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
