# Website

Static landing page hosted on GitHub Pages. The repository currently contains a temporary “Coming soon” page; the landing page will be built later.

## Enable hosting

1. Push this repository's `main` branch to GitHub.
2. Open https://github.com/ReutRada/website/settings/pages and select **GitHub Actions** under **Build and deployment → Source**.
3. In the repository's **Actions** tab, run **Deploy to GitHub Pages** on `main` if the initial run failed before Pages was enabled.
4. Wait for a successful deployment. The expected site URL is https://reutrada.github.io/website/.

Every subsequent push to `main` deploys automatically. No custom secrets or dependencies are required.

## Build the landing page

Replace `site/index.html` and add assets inside `site/`. The workflow publishes only this directory. Use relative asset URLs such as `./assets/logo.svg` so they work under the `/website/` project path.

If a framework is introduced later, add its build step and change the upload path to its generated output directory.

## Preview locally

From the repository root:

```sh
python3 -m http.server 8000 --directory site
```

Open http://localhost:8000. Stop the server with Ctrl+C.

[GitHub Pages configuration documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
