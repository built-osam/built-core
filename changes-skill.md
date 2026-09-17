# Built — Website Changes Skill File
# Use this instead of the full skill file when making post-launch changes to an existing site

---

## BEFORE YOU START

You are making changes to an existing live website. The site is already built and deployed. Your job is to make the requested changes accurately, push them to GitHub, and produce a client-friendly summary at the end.

Do not rebuild sections that are not being changed. Do not refactor, reorganise, or improve code that is not related to the requested changes. Make only what is asked.

---

## WHERE THINGS LIVE

All business information is stored in `src/data/business.ts`. This is always the first place to look for:
- Business name
- Phone numbers
- Email address
- Address
- Areas covered
- Google review count and link
- Form recipient email

Navigation structure is stored in `src/data/nav.ts`. Any changes to menu items, page order, or dropdowns are made here.

Page content lives in `src/pages/`. Each page is its own `.astro` file named after the URL slug.

Components (header, footer, hero, forms) live in `src/components/`.

---

## MAKING CHANGES

Work through each requested change one at a time. After each change, confirm what was done before moving to the next.

**For text or contact detail changes** — edit `src/data/business.ts` first. If the change is page-specific, edit the relevant file in `src/pages/`.

**For navigation changes** — edit `src/data/nav.ts` only. Never hardcode nav links in Header.astro.

**For design or layout changes** — edit the relevant component in `src/components/` or the page file in `src/pages/`.

**Important — do not break these:**

The mobile navigation panel must always use `:not([hidden])` CSS pattern. Never write a plain `display: block` on the nav panel — it will pin the menu open on mobile.

The `astro.config.mjs` must always contain `compressHTML: false`. Do not remove or change this.

---

## PUSH TO GITHUB

Once all changes are complete and verified:

```bash
git add .
git commit -m "Site updates — [brief description]"
git push
```

Cloudflare will redeploy automatically within 60 seconds. The live site will update without any manual steps.

---

## CLIENT SUMMARY

After pushing, produce a short summary of every change made. This will be sent directly to the client.

**Rules for the summary:**
- Write in plain English — no technical terms
- Do not mention Astro, GitHub, components, code, or how the site is built
- Do not say "updated the file" or "edited the component" — describe what the client will see
- Keep each item to one sentence
- List every change separately, even small ones

**Format:**

---

Hi [Client Name],

The following updates have been made to your website:

- [Change 1]
- [Change 2]
- [Change 3]

Everything is now live. Please take a look and let us know if there is anything else you would like adjusting.

The OSAM Team

---

**Examples of good summary lines:**
- "Updated the phone number on all pages to 01234 567890"
- "Changed the opening hours on the Contact page to Monday to Friday, 8am to 6pm"
- "Added Northampton to the list of areas covered"
- "Updated the hero heading on the homepage"
- "Replaced the image in the About section"
- "Added a new service page for Flat Roof Repairs"

**Examples of bad summary lines (do not use):**
- "Updated the business.ts data file with the new phone number" — too technical
- "Edited the Hero.astro component to change the heading" — reveals build method
- "Pushed changes to the GitHub repository and redeployed via Cloudflare" — irrelevant to client
