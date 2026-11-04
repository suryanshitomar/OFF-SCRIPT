# OFF SCRIPT

[Live website](https://suryanshitomar.github.io/OFF-SCRIPT/)

A statement-fashion storefront and customer journey analytics experiment. This portfolio project connects a complete shopping experience with an interactive marketing lab, making it possible to explore how acquisition sources and shopping behavior affect a conversion funnel.

## Experience

- Responsive storefront with four illustrative products and collection filters.
- Product exploration, size selection, shopping bag, and simulated checkout.
- Session-based event tracking, acquisition attribution, and funnel visualization.
- Conversion rate, demo revenue, average order value, and CSV event export.
- A labelled 30-visitor simulator for exploring funnel drop-off.

Built with HTML, CSS, and vanilla JavaScript, without a framework or build dependency.

Open `dist/index.html` in a modern browser. For reliable browser-local storage, serve `dist` using any static web server. The store uses no payment service or external analytics.

## Portfolio demo

1. Open Marketing Lab and choose an acquisition source.
2. Start a visitor journey, explore a product, choose a size, and add it to the bag.
3. Complete the demo checkout, then view the resulting funnel and revenue.
4. Simulate 30 additional visitors to compare sources and funnel drop-off.
5. Export events as CSV for further analysis.

The funnel counts unique sessions at each stage. Conversion is purchasing sessions divided by visiting sessions. Revenue sums demo purchase values; average order value is revenue divided by orders. All values are illustrative, stored only in the current browser, and resettable in the Lab. A new page load begins a new session. Refreshing clears the shopping bag. UTM source values instagram, google, and email are supported.

Products, brand, and orders are fictional. Product graphics are CSS illustrations. The editorial hero photo is from Unsplash and bundled locally in `dist/assets`; fonts are loaded from Google Fonts, with local fallback fonts.

## Public deployment

The GitHub Actions workflow in `.github/workflows/deploy-pages.yml` publishes `dist` to GitHub Pages on pushes to `main`. In the repository's Settings → Pages, select **GitHub Actions** as the source. The workflow can also be run manually from the Actions tab. Its deployment output provides the live website URL.

No secrets or payment credentials are needed. Local hosting metadata is excluded from GitHub by `.gitignore`.

## Analytics scope

Public visitors can test the entire flow independently. Analytics are stored in each visitor's browser, not collected centrally. This project does not currently include GA4, Google Tag Manager, a backend event collector, cross-device identity, or real ad campaign results. The simulator generates illustrative behavior rather than measured marketing evidence.

For a case study, use the exported events to explain the funnel definition, identify where sample visitors drop off, and propose an experiment. Keep simulated results distinct from real user research.

## Validation

JavaScript syntax and a programmatic shopping-to-purchase journey were checked, including the 30-visitor simulator. The storefront was reviewed locally. Public deployment should be verified after the Pages workflow completes.
