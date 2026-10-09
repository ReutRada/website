# Reut Radaa — personal training

Hebrew, right-to-left landing page for Reut Radaa's online personal training, hosted at https://reutrada.github.io/website/. Includes the coaching overview, introduction, joining process, expandable FAQ, monthly pricing, and WhatsApp, phone, and email links.

Built with static HTML, CSS, and a small navigation script. No build step or package installation is needed. Images and fonts are served from this repository.

## Enable hosting

1. Push this repository's `main` branch to GitHub.
2. Open https://github.com/ReutRada/website/settings/pages and select **GitHub Actions** under **Build and deployment → Source**.
3. In the repository's **Actions** tab, run **Deploy to GitHub Pages** on `main` if the initial run failed before Pages was enabled.
4. Wait for a successful deployment. The expected site URL is https://reutrada.github.io/website/.

Every subsequent push to `main` deploys automatically. No custom secrets or dependencies are required.

## Edit the landing page

Edit the copy in `site/index.html`, design in `site/styles.css`, and mobile navigation in `site/script.js`. The workflow publishes only `site/`. Use relative asset URLs such as `./assets/logo.svg` so they work under the `/website/` project path.

Contact buttons link to `https://wa.me/972508841460`. The price is an informational offer; no checkout or payment processing is implemented.

If a framework is introduced later, add its build step and change the upload path to its generated output directory.

## Preview locally

From the repository root:

```sh
python3 -m http.server 8000 --directory site
```

Open http://localhost:8000. Stop the server with Ctrl+C.

[GitHub Pages configuration documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## Assets

- Workout atmosphere photograph by [Benjamin Klaver on Unsplash](https://unsplash.com/photos/QBsVExIgTCo). This is stock imagery, not a portrait of Reut. A visible photo credit appears below the image.
- Heebo typeface, locally hosted Hebrew and Latin subsets. The [SIL Open Font License](site/assets/Heebo-OFL.txt) is included alongside the fonts.
- Brand mark and interface icons are SVG artwork included in the source.
