# Wei Wang's personal website

A small, responsive website with a short bio and links to blog pages. Built with
plain HTML and CSS; no packages or build step required.

## Publish with GitHub Actions

1. Open [Settings → Pages](https://github.com/chriswakupe/cv-blogs/settings/pages).
2. Under **Build and deployment → Source**, select **GitHub Actions**.
3. Commit and push `.github/workflows/pages.yml` to `main`:

   ```sh
   git add .github/workflows/pages.yml README.md
   git commit -m "Add GitHub Pages deployment workflow"
   git push origin main
   ```

4. Open the repository's [Actions tab](https://github.com/chriswakupe/cv-blogs/actions)
   and wait for **Publish website to GitHub Pages** to succeed. If the workflow
   was already pushed before enabling Pages, select it and click **Run workflow**
   on `main`.
5. Visit <https://chriswakupe.github.io/cv-blogs/>. The deployment's `github-pages`
   environment and Settings → Pages also show the published URL.

Every subsequent push to `main` republishes the site. The workflow packages
`index.html`, `assets/`, and `blogs/` and deploys them with GitHub's Pages actions.
No personal access token or custom secret is required.

### If the site returns 404

- Confirm the commit was **pushed** to GitHub, not only committed locally.
- Confirm the Pages source is **GitHub Actions** and the latest deployment is green.
- If a run failed, open its failed step in the Actions tab for the error message.
- Allow up to 10 minutes for publishing after a push.
- Use `/cv-blogs/` for this repository. A repository named `chriswakupe.github.io`
  would instead publish at the domain root.

[GitHub Pages workflow documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)

## Preview locally

```sh
python3 -m http.server 8000
```

Open <http://localhost:8000>. Press Ctrl+C to stop the server.

## Edit the site

- `index.html`: bio, profile links, and blog list.
- `assets/style.css`: shared styling.
- `blogs/cv-study/index.html`: CV Study page.

To add a blog, create `blogs/your-topic/index.html` and add a link to
`blogs/your-topic/` in the homepage's Blogs section. Add any new top-level site
folders to the workflow's **Prepare website** step so they are published too.
