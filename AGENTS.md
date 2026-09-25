# AGENTS.md — Eva Print Website

## Project identity

This repository is the standalone Eva Print Pavlodar storefront. It must never be placed inside or coupled to the Cardera website repository.

## Mandatory UI baseline

The user-approved desktop and mobile mockups supplied on 2026-09-25 are the visual contract for this project.

Rules:

1. Preserve the approved information architecture and block order:
   - header/navigation;
   - 3-part hero: sales copy / product composition / custom-print panel;
   - benefits strip;
   - popular products;
   - popular categories;
   - four-step ordering flow;
   - Instagram gallery;
   - bottom gradient contact CTA.
2. Desktop must visually track the approved desktop mockup. Do not invent a different design direction without an explicit request.
3. Mobile must be a deliberate responsive layout matching the approved mobile mockup, not a scaled-down desktop page.
4. Use the official registered Eva Print Pavlodar logo. Do not redraw, reinterpret, or replace the brand mark.
5. Keep the main brand accent system: white base, black typography, hot pink, violet, cyan/blue accents.
6. Avoid placeholder emoji as primary product/category imagery when real approved assets are available.
7. Do not change Cardera repositories while working on this site.
8. All project changes go through GitHub main unless the user explicitly requests another branch.

## Deployment baseline

Target: Cloudflare Pages / Workers & Pages.

Static deployment must work without a Node build step:
- production branch: main
- build command: none
- output directory: repository root

## Current implementation

The current `index.html` is intentionally self-contained: CSS, JavaScript and approved demo imagery are embedded so the first Cloudflare deployment cannot lose assets or show broken image paths.

Once the UI is accepted in-browser, the code may be split into `css/`, `js/`, and `assets/` without changing the approved appearance.
