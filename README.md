# DiveHub website

The English-language product website for [DiveHub](https://divehub.ai/), built with Astro and published as a static site on GitHub Pages. Markdown pages provide support and privacy information; shared Astro layouts and components keep navigation and presentation consistent.

## Local development

Run these commands from the repository root:

```sh
npm ci
npm run dev
```

The development server runs at `http://localhost:4321` by default.

## Production build

```sh
npm run build
npm run preview
```

Astro generates the static site in `dist/`. Preview serves the production build locally. No application server or external service is required.

## Project structure

- `src/pages/index.astro`: product homepage.
- `src/pages/support.md` and `src/pages/privacy.md`: support and privacy content.
- `src/components/` and `src/layouts/`: shared navigation, page structure, and Markdown rendering.
- `src/styles/global.css`: shared typography, color, spacing, and component styles.
- `public/images/`: product screenshots and brand assets sourced from the official App Store listing.
- `.github/workflows/deploy.yml`: build and deployment workflow.

## Publishing

A push to `main` triggers the existing **Deploy to GitHub Pages** workflow. It installs dependencies, builds Astro, uploads the static output, and deploys it with `actions/deploy-pages`. The workflow can also be started manually through GitHub Actions.

After publishing, verify the successful workflow run and the live site at `https://divehub.ai/`. Check the homepage, support and privacy pages, mobile navigation, and App Store download links.

## Content and maintenance

The official product reference is the [DiveHub App Store listing (ID 6756101582)](https://apps.apple.com/us/app/divehub-multi-dive-tool/id6756101582). It describes DiveHub as an educational tool, **not for real dive planning**. Keep that boundary visible and consistent across the website.

Use real app screenshots and verifiable capabilities. Do not add claims about pricing, AI, synchronization, or standalone macOS distribution without checking current official evidence. The website currently provides English content; app language availability is a separate product fact.

The privacy policy describes the app’s data practices. Verify the implemented behavior before making substantive changes to its promises; design and copy updates alone are not evidence of a change in data handling.

Before publishing a change:

- Run `npm run build` and check for build errors.
- Review desktop and mobile layouts, keyboard access, and reduced-motion behavior.
- Confirm navigation and download links work from every page.
- Keep homepage, support content, and product-use boundaries consistent.
- Verify that the privacy policy still reflects the app’s implemented behavior.
