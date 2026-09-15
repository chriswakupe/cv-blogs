# Wei Wang's personal website

A small, responsive website with a short bio and links to blog pages. Built with
plain HTML and CSS; no packages or build step required.

## Preview locally

From this directory, run:

```sh
python3 -m http.server 8000
```

Open <http://localhost:8000>. Press Ctrl+C to stop the server.
You can also open `index.html` directly; directory links work best with the server.

## Publish on GitHub Pages

1. Commit these files and push them to the `main` branch on GitHub.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose **main** and **/ (root)**, then **Save**.
5. Wait for deployment to finish. The Pages settings will show the live URL.

With the current repository owner and name, the expected URL is:
<https://chriswakupe.github.io/cv-blogs.github.io/>.
For a site at `https://chriswakupe.github.io/`, the repository would need to be
named `chriswakupe.github.io`. All internal links are relative, so either location
works. The `.nojekyll` file lets GitHub Pages serve the static files directly.

See [GitHub's publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Edit the site

- `index.html`: bio, profile links, and blog list.
- `assets/style.css`: shared layout, colors, and typography.
- `blogs/cv-study/index.html`: title-only CV Study page, ready for writing.

To add a blog page, copy `blogs/cv-study/index.html` into
`blogs/your-topic/index.html`. Update its title, description, and article content,
then add a `blog-entry` link to `blogs/your-topic/` in the homepage's Blogs section.
Remove the entry's “Coming soon” label when the article is ready.
