# Contributing to the Druks website

Thanks for your interest in helping out! This repository holds the static marketing site at [druks.ai](https://druks.ai). It is a small [Astro](https://astro.build) project with one page, a handful of components, a stylesheet and a little vanilla JavaScript, so it is a friendly place to make a first contribution.

You don't need to be a developer to help. Spotting a typo, suggesting clearer wording, reporting a layout glitch on your phone, or flagging something that is hard to use with a screen reader are all valuable contributions.

If you want to contribute to Druks itself (the platform rather than this site), head over to the [main Druks repository](https://github.com/czpython/druks) and its own [contributing guide](https://github.com/czpython/druks/blob/main/CONTRIBUTING.md).

## Ways to contribute

- **Fix copy.** Typos, awkward phrasing, outdated claims or broken links. Small fixes can go straight to a pull request.
- **Report a bug.** Something looks wrong, doesn't work, or behaves oddly in a particular browser or at a particular screen size. Open a [bug report](https://github.com/czpython/druks-web/issues/new?template=bug_report.yml).
- **Improve accessibility.** Missing alt text, poor colour contrast, keyboard traps, animation that can't be paused, or anything that makes the site harder to use. Open an [accessibility issue](https://github.com/czpython/druks-web/issues/new?template=accessibility.yml) or send a fix.
- **Suggest an improvement.** New content, a design tweak or a better way to explain something. Open a [suggestion](https://github.com/czpython/druks-web/issues/new?template=suggestion.yml) first so we can talk it through before you spend time on it.

Please look through the [open issues](https://github.com/czpython/druks-web/issues) before opening a new one, in case someone has already raised it.

## Setting up locally

You will need [Node.js](https://nodejs.org) 20 or newer and npm.

```bash
git clone https://github.com/<your-username>/druks-web.git
cd druks-web
npm install
npm run dev
```

The site is served at `http://localhost:4321` and reloads as you edit.

To check the production build before opening a pull request, run

```bash
npm run build
npm run preview
```

The `deploy` script in `package.json` pushes to the production server and only works for maintainers. You don't need it.

## Where things live

| Path | What it is |
| --- | --- |
| `src/pages/index.astro` | The whole page. Navigation, hero, every section and the footer. |
| `src/components/` | Animated sequences used on the page (the product console, the durability and sandbox demos). |
| `src/styles/global.css` | All of the styling, including responsive and reduced motion rules. |
| `public/scripts/pipeline.js` | The vanilla JavaScript that drives the animations and the mobile menu. |
| `public/assets/` | Artwork, logos and social preview images. |
| `public/` | Favicons, the web manifest, `robots.txt` and `sitemap.xml`. |

## Making a change

1. Fork the repository and create a branch from `main` with a short, descriptive name, for example `fix-hero-typo` or `improve-nav-contrast`.
2. Make your change. Keep each pull request to one topic so it is easy to review.
3. Run `npm run build` and make sure it passes.
4. Check the page in a browser at both desktop and phone widths. If you touched the animations, also check with "reduce motion" switched on in your operating system settings.
5. Open a pull request and fill in the template. Screenshots or a short recording are really helpful for anything visual.

A maintainer will review it as soon as they can. Small fixes are usually quick. If you don't hear anything within a couple of weeks, feel free to leave a polite nudge on the pull request.

## Guidelines

- **Accessibility matters.** Every image needs meaningful alt text (or an empty `alt` if it is purely decorative). Interactive elements need accessible names. Keep colour contrast at WCAG AA or better. Anything animated must respect `prefers-reduced-motion`.
- **Keep it fast.** This is a static site and we would like it to stay light. Optimise new images (WebP where possible) and avoid adding dependencies unless they are clearly worth it.
- **Match the existing style.** Two space indentation, semicolons in JavaScript, and class names that follow the patterns already in `global.css`.
- **Content accuracy.** The site describes what Druks does today. If you are unsure whether a claim is accurate, ask in the issue or pull request rather than guessing.
- **Don't commit generated files.** `dist/`, `node_modules/` and `.astro/` are ignored and should stay that way.

## Code of conduct

This project follows a [code of conduct](CODE_OF_CONDUCT.md). By taking part you agree to keep it a welcoming space for everyone.

## Security

Please don't report security problems in public issues. See [SECURITY.md](SECURITY.md) for how to report them privately.

## Questions

Not sure where to start, or whether something is worth raising? Open an issue and ask. There are no silly questions, and we would much rather hear from you than not.
