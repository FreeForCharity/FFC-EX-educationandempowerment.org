# FFC-EX-educationandempowerment.org

Education & Empowerment — FFC-supported charity website (static, GitHub Pages).

This repository holds a fully localized static capture of the former WordPress site at
`educationandempowerment.org` (previously hosted on Hostinger), migrated as part of the
FFC Wave-1 WordPress-to-Pages program
([FFC-Cloudflare-Automation#702](https://github.com/FreeForCharity/FFC-Cloudflare-Automation/issues/702)).

## Hosting

- Deployed to GitHub Pages on the default URL:
  <https://freeforcharity.github.io/FFC-EX-educationandempowerment.org/>
- Deployment runs from `.github/workflows/static.yml` on every push to `main`.
- No custom domain and no DNS changes are configured at this stage.

## Structure

Plain static HTML capture (Genesis / Agency Pro theme) — no build step. Main pages:

| Path | Page |
| --- | --- |
| `/` | Home ("Who We Are") |
| `/2016/11/27/who-we-are/` | Who We Are |
| `/2016/11/27/what-do-we-do/` | What Do We Do |
| `/2016/11/27/our-stories/` | Our Stories |
| `/2016/11/27/how-you-can-help-us/` | How You Can Help Us |
| `/2016/11/26/social-enterprise/` | Social Enterprise |
| `/2016/11/26/thank-you/` | Thank You |
| `/connect-with-us/` | Connect With Us |

Category and author archive pages are retained for internal navigation.

## Migration notes

- Google Fonts (EB Garamond, Spinnaker) and Bunny Fonts (Open Sans) localized to
  `wp-content/ffc-local-fonts/`.
- Cloudflare email obfuscation statically decoded — all 13 protected addresses were
  `connecting@educationandempowerment.org`, now plain `mailto:` links.
- Dead backend forms removed: Forminator contact form (replaced with a `mailto:` line),
  wpDiscuz comment forms, search widget.
- WP runtime cruft stripped: wp-json/, wp-admin/, comments/, feeds, xmlrpc, wp-login,
  emoji/oembed/RSS head links, analytics beacons.

## Maintenance

- Edit the HTML in place; every push to `main` redeploys.
- `linkcheck.yml` runs lychee weekly and on pushes/PRs to catch link rot.
- See the migration tracking issue for full capture details.

---

Supported by [Free For Charity](https://freeforcharity.org).
