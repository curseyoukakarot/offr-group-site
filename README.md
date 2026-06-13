# Offr Group — Website Redesign

A modern, fully self-contained redesign of the Offr Group marketing site. Four static HTML pages, no build step, no framework — each page ships its own inline CSS + vanilla JS.

**Design system:** "Hybrid Contrast" — clean warm-paper light sections punctuated by cinematic dark moments, with an Electric Cobalt accent (`#2E5BFF`) + cyan glow (`#36E0E6`). Type is Plus Jakarta Sans + JetBrains Mono. Motion (aurora gradients, scroll reveals, magnetic buttons, kinetic hero, parallax) is all gated behind `prefers-reduced-motion`.

## Pages

| File | Page |
|------|------|
| `index.html` | Home — full-screen looping **video hero** with shiny animated heading, services, recent placements, testimonials, engagement models, team photo |
| `for-founders-redesign.html` | For Founders — fractional leadership matching (Finance / Ops / Marketing / Sales-CRO) |
| `hiring-manager-playbook-redesign.html` | Hiring Manager Playbook — featured interviews, playbooks + accordion, tools (warm "Sunset Ember" hero) |
| `job-seekers-redesign.html` | Job Seeker Program — the four-layered outreach system |
| `playbook-marketervsconsultant-redesign.html` | Playbook article — "Senior marketer vs. content generalist" (long-form, sticky table-of-contents, warm theme) |
| `playbook-vpofsales-redesign.html` | Playbook article — "Hiring your first VP of Sales" |
| `playbook-interview-loop-redesign.html` | Playbook article — "Designing an interview loop that respects everyone's time" |
| `playbook-operators-chief-of-staff-redesign.html` | Playbook article — "Hiring operators & chiefs of staff" |

`index.html` is the home page; all nav/footer links cross-reference the `*-redesign.html` filenames, so the set is fully navigable as-is.

## Assets

```
assets/images/
  offr-logo-light.png   offr-logo-dark.png    (brand logo — white / dark, swap on scroll)
  merrill-lynch.png  netflix.png  windstream.png   (client logos)
  team-austin-centre.jpg                       (team photo, About section)
  favicon.ico
```

## Preview locally

Any static server works — e.g.:

```bash
npx serve .
# then open http://localhost:3000/index.html
```

## Deploy

Drop the folder on any static host (GitHub Pages, Netlify, Vercel, S3, etc.).

> **GitHub Pages ready:** The home page is `index.html`, so Pages serves it at the site root automatically — just enable Pages on the repo (deploy from the root). All cross-page links are relative, so it also works fine from a subpath.

## Third-party scripts (kept from the original site)

Google Analytics (gtag), RB2B, and the HirePilot chat widget are wired in each page. CTAs point to `app.thehirepilot.com` and the Calendly booking flow.
