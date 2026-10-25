# howTo3x3

A printable visual Rubik's Cube guide. Open `index.html` directly in a browser
to view or print it. All styles and illustrations are included in the HTML;
there are no dependencies or build steps.

## GitHub Pages

The deployment workflow follows the GitHub Actions setup used by
[pizzArea](https://github.com/Xylol/pizzArea/blob/master/.github/workflows/deploy.yml)
and [annoArda](https://github.com/Xylol/annoArda/blob/master/.github/workflows/deploy.yml),
with no Node.js installation or build required.

1. In the GitHub repository, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Push `index.html` and `.github/workflows/deploy.yml` to `master`.
   If they are already on `master`, open **Actions → Deploy to GitHub Pages → Run workflow**.

Every push to `master` deploys the page. The workflow can also be run manually.
If the repository uses another default branch, update `on.push.branches` in
`.github/workflows/deploy.yml` to match.

The workflow uploads only `index.html`. If the page gains separate assets,
add them to the **Prepare site** step as well.

Once deployed from `Xylol/howTo3x3`, the page will be available at
[xylol.github.io/howTo3x3/](https://xylol.github.io/howTo3x3/).
The deployment's actual URL also appears in the workflow's `github-pages`
environment.

## License

[MIT](LICENSE) © 2026 Xylol.
