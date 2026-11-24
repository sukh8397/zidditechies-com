# Ziddi Techies .COM — Complete Brand Management

A standalone static marketing site for the **brand-management division** of Ziddi Techies. It is deliberately separate from `zidditechies.in` (Shopify growth & management division).

## What is in here

| File | Purpose |
| --- | --- |
| `index.html` | Home — proposition, two divisions, problem/solution, services overview, process, CTA |
| `services.html` | All twelve services in four pillars, with deliverables and anchors |
| `approach.html` | Operating model, engagement shapes, FAQ |
| `about.html` | Why the division exists, principles, division comparison |
| `contact.html` | Netlify-powered enquiry form plus direct channels |
| `thanks.html` | Form success page (noindex) |
| `privacy.html`, `terms.html` | Legal pages |
| `404.html`, `robots.txt`, `sitemap.xml` | SEO and error handling |
| `assets/css/styles.css` | Complete visual system (dark, violet/cyan) |
| `assets/js/main.js` | Mobile menu, year, copy-to-clipboard, scroll reveal |
| `favicon.svg`, `assets/img/mark.svg` | Brand mark |
| `netlify.toml` | Publish directory, security headers, redirects |

No build step, no dependencies, no framework. Plain HTML/CSS/JS.

## Contact details used on the site

- Email: **support@zidditechies.com** (IONOS business mailbox)
- WhatsApp / new business: **+91 85678 75871**
- Client operations: **+91 98884 58818**
- Sister division: **https://zidditechies.in**

## Deploy to Netlify

1. Push this folder to a repository (or drag the folder into Netlify Drop).
2. In Netlify: **Add new site → Import an existing project**, select the repo.
3. Build command: leave empty. Publish directory: `.` (already set in `netlify.toml`).
4. Deploy. Confirm `https://<site-name>.netlify.app` loads and the contact form appears under **Forms → brand-enquiry**.

## Point zidditechies.com at Netlify (IONOS DNS)

Do this only after the Netlify site loads correctly on its netlify.app address.

1. In Netlify → **Site configuration → Domain management → Custom domains → Add custom domain**, enter `zidditechies.com`.
2. Netlify will show the DNS records to add. In the IONOS DNS zone for `zidditechies.com`:
   - Set the **A record for `@`** to the Netlify load-balancer IP shown in the Netlify UI (commonly `75.2.60.5`).
   - Add a **CNAME for `www`** pointing to the Netlify site address shown in the UI (for example `<site-name>.netlify.app`).
3. **Do not change** MX, SPF, DKIM, DMARC or any other records. The `support@zidditechies.com` mailbox is with IONOS and must stay untouched.
4. Wait for DNS propagation and Netlify TLS issuance, then verify `https://zidditechies.com` and `https://www.zidditechies.com`.

## Notes

- The site contains no invented case studies, testimonials or client logos.
- Netlify Forms only works after deployment on Netlify. If deployed elsewhere, replace the form `action` with a `mailto:` link or a form service.
- Fonts load from Google Fonts; system fallbacks are defined in CSS.
