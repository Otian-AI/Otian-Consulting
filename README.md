# Otian AI Consulting

The consulting site for Otian AI LLC: Jack and Jett helping small businesses use AI, with Archie
(otianai.com) as the proof. One static page, no build step of ours, live at
https://consulting.otianai.com.

## How it is published

A push to `main` is the deploy. GitHub Pages builds `Otian-AI/Otian-Consulting` from the `main`
branch, root folder (Settings, Pages: Deploy from a branch), and there is no workflow file. Pages
runs its own Jekyll build on the way, which serves every file in the repo except the ones
`_config.yml` excludes, so a note like this one has to be named there to stay off the site.

- **Address.** The `CNAME` file says `consulting.otianai.com`, and so does the custom domain in
  Pages, where GitHub shows the domain as verified and Enforce HTTPS is on. GitHub renews the
  certificate on its own.
- **DNS.** otianai.com's DNS is on Cloudflare. `consulting` is a CNAME record, DNS only and not
  proxied, to `jettnguyen.github.io`: the name from before the repos moved to the Otian-AI
  organization on November 9, 2026. It still works, because every `github.io` name leads to the
  same Pages servers and the custom domain above decides which site answers. If the record is ever
  edited, `otian-ai.github.io` is the matching name.

otianai.com points here from every Services and Work With Us link, the Consulting menu, and the
redirects at `services/`, `consulting/` and `guided-setup/`. A different address later means
changing `CNAME`, the canonical link in `index.html`, `robots.txt` and `sitemap.xml`, and those
links on otianai.com.
