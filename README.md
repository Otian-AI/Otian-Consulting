# Otian AI Consulting

The consulting site for Otian AI LLC: Jack and Jett helping small businesses use AI, with Archie
(otianai.com) as the proof. One static page, no build step, served by GitHub Pages.

## Before it goes live

- Jett and Jack confirm three offers the page makes: Jack's visits around Dallas-Fort Worth (Jett
  is in Florida and joins on Zoom), setting up an AI the owner already uses, and checking what
  they pay for software.
- Price the monthly "someone to call" plan. The page shows `[Price to set]` in two places (the
  services card and the price card), and otianai.com's FACTS.md gets a row for the figure first.
- otianai.com already points here (its main, 2026-10-08): every Services and Work With Us link,
  the Consulting menu row, and redirects from `services/`, `consulting/` and `guided-setup/`. Until
  this site is published those links lead nowhere, so publish this before pushing otianai.com, or
  revert that change.

## Publishing

1. Create a GitHub repository for this folder and push it.
2. In the repository's Settings, Pages: deploy from the `main` branch, root folder.
3. Where otianai.com's DNS is managed, add a CNAME record: `consulting` pointing to
   `otian-ai.github.io`.
4. Back in Pages, set the custom domain to `consulting.otianai.com` (the `CNAME` file already says
   so) and turn on Enforce HTTPS once the certificate is issued.

A different address later means changing `CNAME`, the canonical link in `index.html`,
`robots.txt` and `sitemap.xml`, and the links on otianai.com.
