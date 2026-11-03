# OSAM Websites — Website Build Skill File
# For use with Claude Code on all Redesign, Carbon Copy, and New Build projects

---

## EXTERNAL SKILLS — READ FIRST

Before doing anything else, fetch and read the following skill files in full. Apply their rules throughout the build. Where any rule conflicts with OSAM standards in this file, OSAM standards take priority.

1. Taste Skill — Redesign Audit:
https://raw.githubusercontent.com/Leonxlnx/taste-skill/main/skills/redesign-skill/SKILL.md

2. Taste Skill — Image to Code:
https://raw.githubusercontent.com/Leonxlnx/taste-skill/main/skills/image-to-code-skill/SKILL.md

3. Vercel Web Design Guidelines:
https://raw.githubusercontent.com/vercel-labs/agent-skills/main/skills/web-design-guidelines/SKILL.md

Do not proceed to the brief or any build work until all three have been read.

---

## BEFORE YOU START

Read the full brief before writing a single line of code. Understand the build type, the business, the design direction, and all specific amends. If anything in the brief is unclear or contradictory, flag it before proceeding — do not guess.

## SPEED & EFFICIENCY RULES

These rules apply to every build. The target build time is 30 to 45 minutes maximum. Do not exceed this.

**These are hard rules — not guidelines:**

- Build every page first. Do not stop to audit, check, or review anything until all pages are built.
- Do NOT run Lighthouse, contrast audits, accessibility checkers, or any automated testing tool during the build.
- Do NOT take screenshots to check your own work mid-build. Build it, move on.
- Do NOT loop back over completed pages. Once a page is built, it is done until the designer reviews it.
- Do NOT run npm run build until all pages are complete and you are ready to hand over.
- Do NOT fix cosmetic issues, spacing, or minor visual details during the build. Build first, fix later.
- Fix ONLY errors that would stop the site loading — a page that 404s, a build that fails to compile, a form that throws an error.
- When all pages are built, run npm run build once, fix any compile errors, then stop.
- Output a handover summary listing every page built and anything the designer needs to check.
- Then stop completely. Wait for the designer to review and send all amends in one message.
- Do not make any further changes until you receive that message.

**The designer will catch visual issues. Your job is to build fast and hand over.**

---

## SECTION 1 — HOW TO READ THE BRIEF

### Build Types

**Carbon Copy**
Rebuild the existing website exactly as it is. Same design, same layout, same content, same images, same URLs. The client must not be able to tell the difference. Do not modernise, do not rewrite, do not improve. Copy it precisely.

Screenshots: do not take screenshots during the build. Once all pages are built and npm run build completes, take screenshots of key pages — homepage, one service page, contact page — at desktop and mobile to verify the layout before handover. For Carbon Copy builds, compare every page against the original.

**Modernise & Amend**
Keep the overall style and brand familiar but update the design to feel current. Apply all specific amends listed in the brief. Read the design call notes carefully — they take priority over your own design decisions. If example websites are provided, follow the Example Websites instructions below.

**New Build**
No existing website to reference. Build entirely from the brief and design call notes. Make design decisions based on the brand colours, industry, and any example websites provided. If example websites are provided, follow the Example Websites instructions below.

### Example Websites — How to Use Them

If one or more example websites are provided in the brief, this is the most important design reference. Do not treat it as loose inspiration. Treat it as a blueprint.

**Before writing a single line of code:**

1. Open every example URL in the brief
2. Analyse the layout in detail — section order, spacing, typography scale, component structure, hero layout, how services are presented, how CTAs are placed, footer structure
3. Note specifically: how the hero is built, how services are displayed, how the navigation is structured, what the overall feel and density of the page is
4. Build to match that layout and structure as closely as possible

**The only things that change from the example:**
- Colours — use the client's base, secondary and accent colours from the brief
- Logo and branding
- Content — use the client's services, copy and images
- Business details — name, phone, email, address, areas

Everything else — layout, section order, component style, spacing, typography scale, visual weight — should match the example site as closely as possible.

Do not start building until you have opened and analysed every example URL. If an example URL does not load, flag it to the designer before proceeding. Do not skip this step or leave it until later.

### Priority Order
When instructions conflict, follow this order:
1. Specific amends listed in the brief — always highest priority
2. Design call notes
3. Example websites provided — treated as a layout blueprint, not optional inspiration
4. OSAM design standards in this skill file
5. Claude's own design judgment — lowest priority, only used when nothing else applies

---

## SECTION 2 — ABOVE THE FOLD (NON NEGOTIABLE)

Every website built by OSAM must have the following above the fold, in this order, on every page. This is not optional and must not be changed regardless of the brief.

### Phone Bar
A thin bar at the very top of the page — above the navigation.
- Display Primary Phone always
- Display Secondary Phone if provided in the brief
- Display Email address
- Background should be the base colour or a dark contrasting colour
- Text should be white or light coloured
- Never include the address in the phone bar or navigation contact strip — the address belongs in the footer only
- On mobile, show the primary phone number only. Do not show email or secondary phone in the phone bar on mobile — it becomes too cluttered.
- Every phone number, here and anywhere else on the site (footer, contact page), must be wrapped in a `tel:` link using full international format, e.g. `<a href="tel:+441234567890">01234 567890</a>` — so mobile users can tap to call directly.

### Navigation
- Full width navigation below the phone bar
- Logo on the left
- Navigation links on the right
- On mobile — hamburger menu
- Sticky header — the nav sticks to the top as the user scrolls
- Navigation items come from the Pages Required section of the brief
- If no pages are listed, use: Home, About, Services, Contact

### Hero Section
The hero must contain all of the following:
- A strong, relevant full width background image (see Section 7 for image sourcing)
- A clear H1 headline — the business name or primary service and location
- A short subheadline — one sentence on what they do and who they serve
- A contact form (see Section 8 for form spec)
- A primary CTA button — e.g. "Get a Free Quote" or "Call Us Today"
- Google Reviews badge — if review count and link are provided in the brief

**Google Reviews Badge**
- Display as: ⭐⭐⭐⭐⭐ [Review Count] Five Star Reviews on Google
- Link the badge to the Google Review Link provided in the brief
- Opens in a new tab
- If no review count or link is provided — do not display anything in this position. Do not use a placeholder or fake number.

### Logo Background Matching
When a logo is provided as a JPEG or PNG with a visible background colour baked in:
- Use a colour picker to extract the exact hex value of the logo background
- Set the navigation background to that exact hex colour
- Never place a logo with a baked-in background on a contrasting nav colour — it always looks dropped in
- Choose nav link text colours that contrast well against the logo background colour
- If the logo background is light — use dark text links
- If the logo background is dark or bright — use white text links
- Apply the same colour to the phone bar above the nav for a seamless top section

If a logo is provided as a PNG with a transparent background — set the nav to the base colour from the brief as normal.

### Above The Fold Checklist
Before moving on, confirm:
- [ ] Phone bar visible at the very top
- [ ] Nav with logo and links below phone bar
- [ ] Hero with H1, subheadline, contact form, CTA, and Google badge (if applicable)
- [ ] Everything visible on desktop without scrolling
- [ ] Mobile version stacks cleanly
- [ ] Logo background colour matches nav background — no dropped-in effect

---

## SECTION 3 — DESIGN STANDARDS

### Colours
- Base Colour = primary brand colour. Use for phone bar, nav, buttons, section backgrounds, headings.
- Secondary Colour = supporting colour. Use for accents, hover states, highlights.
- Accent Colour = use sparingly for CTAs, badges, standout elements.
- If only one colour is provided, derive a complementary secondary from it.
- White and light grey (#F8F8F8) for content section backgrounds.
- Dark grey (#222222) or black for body text — never pure black (#000000).
- If the logo has a baked-in background colour — that colour overrides the base colour for the nav and phone bar. See Section 2 for full logo matching rules.

### Typography
- If a font preference is given — use it. Import from Google Fonts.
- If no font preference is given — choose a clean, professional pairing suitable for the industry. A sans-serif for headings, a readable serif or sans-serif for body text.
- Heading sizes: H1 48-64px desktop / 32-40px mobile. H2 32-40px. H3 24-28px.
- Body text: 16-18px minimum. Never smaller.
- Line height: 1.6 for body text.

### Spacing
- Generous padding on all sections — minimum 80px top and bottom on desktop, 48px on mobile.
- Content should never feel cramped.
- Max content width: 1200px centred.

### Mobile First
Build mobile first. Every section must work on a 390px wide screen before designing the desktop version. Test every section at mobile width before moving on.

### Buttons
- Claude decides button style based on the brand — rounded, sharp, outlined, or filled.
- Primary button: filled, high contrast against background.
- Secondary button: outlined or ghost style.
- All buttons must have a visible hover state.
- Minimum button size: 44px height, 120px width.
- Never use more than two button styles on one page.

### Design Decisions
When making design choices not covered by the brief:
- Look at the industry — a solicitor needs to feel professional and trustworthy, a landscaper needs to feel natural and outdoorsy, a plumber needs to feel reliable and straightforward.
- Look at the base colour — let it guide the feel.
- When in doubt, choose clean and minimal over complex and decorative.

---

## SECTION 4 — PAGE STRUCTURE

### Homepage
Every homepage must contain in this order:
1. Phone bar
2. Navigation
3. Hero with form, CTA, and Google badge
4. About / Introduction section — short paragraph about the business, 2-3 sentences
5. Services section — grid or cards showing all main services with icons or images
**Service card grids must always use equal columns.** Three cards per row on desktop, two on tablet, one on mobile. Never use asymmetric bento or mixed-span layouts for service cards. Always check the arithmetic before rendering: 6 cards at 3-columns = 2 clean rows. 6 cards at mixed spans = broken layout with orphaned elements. The design audit skill warning about equal column grids does not apply to service card sections. Equal columns are the correct answer here.
6. Why Choose Us / Trust signals — key selling points, years in business, qualifications
7. Testimonials section — if client has provided testimonials or Google reviews
8. Areas Covered section — list of towns and regions served
9. Call To Action section — strong closing CTA with button
10. Footer

### Service Pages
1. Phone bar + Navigation
2. Hero — relevant image, H1 with service name and location, short intro
3. Service description — detailed content about the service
4. Benefits / What's included
5. Process section if applicable — how it works, step by step
6. Related services
7. CTA section
8. Footer

### About Page
1. Phone bar + Navigation
2. Hero — team photo or premises image if available
3. Our story — history and background of the business
4. Meet the team — if photos and names are provided
5. Values or approach
6. Accreditations or qualifications
7. CTA
8. Footer

### Contact Page
1. Phone bar + Navigation
2. Large contact form
3. Business address, phone, email displayed clearly
4. Google Maps embed — use the embed from the existing site or generate from the business address
5. Opening hours if provided
6. Footer

### Areas Covered Page
1. Phone bar + Navigation
2. Introduction paragraph — the areas the business serves
3. List or grid of all towns and regions
4. Map embed showing coverage area if possible
5. CTA
6. Footer

---

## SECTION 5 — CONTENT

### If Content is Provided by Client
Use it exactly as provided. Do not rewrite, paraphrase, or improve it. Correct only clear spelling errors. The client wrote it — respect that.

### If Using Existing Content (Carbon Copy and Modernise builds)
Copy all text from the existing website exactly. Do not change wording, headings, or structure unless a specific amend in the brief says to.

### If Writing Content from Scratch
When no content is provided and the build requires original copy:

**Tone:** Professional, friendly, and direct. Written for a small business owner's customer — someone who needs a service and wants to feel confident they've found the right company. No corporate jargon, no buzzwords.

**Homepage hero headline:** Lead with the primary service and location. e.g. "Trusted Plumber in Brighton & East Sussex" or "Expert Garden Design Across Surrey"

**Service descriptions:** What the service is, who it's for, what the client can expect. 100-200 words per service. Include the primary location naturally.

**About copy:** Focus on experience, trust, and local knowledge. Mention how long they've been trading if known.

**Location content:** Mention the primary location in the first paragraph of every page. Include surrounding towns where relevant. If the brief lists specific areas, mention them in headings and body copy naturally.

**Additional charges:** If the brief mentions a surcharge for certain areas (e.g. London travel charge), include a clear, friendly note on the relevant service pages and the contact page.

### Content Differentiation
Every page must contain at least 40-50% unique content. Do not copy and paste the same paragraphs across multiple pages with only the location or service name swapped out. Each page must earn its own existence with genuinely different content — different angles, different detail, different structure. Google penalises duplicate content across a site and clients notice when pages feel copy-pasted.

### FAQ Rules
If a page includes a FAQ section, every question and answer must be specific to that page's topic and service. Never reuse or duplicate FAQs across multiple pages — even slightly reworded versions count as duplicates.

FAQs must be generated from existing content on the site or from the brief — never invented. If there is no existing FAQ content and nothing in the brief to draw from, do not add a FAQ section. An absent FAQ is better than a made-up one.

### Content Rules — Never Do These
- Never invent facts, qualifications, years of experience, or awards
- Never invent testimonials or reviews
- Never use placeholder text (Lorem Ipsum) — if content is missing, write real content or flag it
- Never use the phrase "we are a leading provider" or similar generic claims
- Never write more than 300 words on any single section without a clear reason
- Never use elongated hyphens (em dashes) in any content or copy — they look AI generated. Use a regular hyphen or rewrite the sentence instead.

### Thank You Page
The thank you page must display this exact message after a successful form submission:

"Thank you — your message has been sent. We will be in touch shortly."

Use a regular hyphen, not an em dash. Keep it short and friendly. Match the site design.

---

## SECTION 6 — SEO

### URLs
- URLs must match the existing site exactly for Carbon Copy and Modernise builds
- Never change, shorten, or restructure existing URLs — this destroys Google rankings
- For new builds, use clean lowercase slugs: /services/drain-repairs-brighton/
- No underscores — use hyphens

### Domain & URL Consistency (www, trailing slash, canonical)
Every site must resolve to exactly one canonical form of every URL — never let both variants stay live, as this creates duplicate content.

**Choosing the convention:**
- Carbon Copy / Modernise & Amend: check the existing live site first. Visit the domain both with and without `www.` and see which one it settles on — that tells you the convention already indexed by Google. Match it exactly, including trailing slash behaviour.
- New Build: default to the non-www apex domain (`example.com`, not `www.example.com`) with a trailing slash on every URL (matches the slug format above). Only deviate if the client specifically requests `www`.

**Enforcing it:**
- In the Vercel project (Settings → Domains), add both the apex and `www` domains and set the non-canonical one (the `www` version if apex is canonical, or vice versa) to redirect to the canonical one with a 301.
- Set `trailingSlash` in `vercel.json` to match the convention (`true` for trailing slashes, `false` for none) and set the same in `astro.config.mjs` (`trailingSlash: 'always'` or `'never'`).
- Add a self-referencing canonical tag to every page in `Layout.astro`, matching the exact canonical URL (protocol, domain, trailing slash):
```html
<link rel="canonical" href="https://[canonical-domain]/[exact-path]/" />
```

### Handling URL Changes (Modernise & New Build only)
If the brief requires restructuring URLs that are already live and indexed, don't just drop the old ones:
1. Before building, pull the full list of existing indexed URLs — from the current `sitemap.xml`, or a quick crawl of the live site if no sitemap exists.
2. Build a redirect map: every old URL that changes → its new equivalent.
3. Implement the redirects in the `redirects` array of `vercel.json` in the project root (Vercel reads this natively). Do NOT use a `public/_redirects` file — that is a Cloudflare Pages feature and Vercel ignores it. One entry per redirect, with an explicit `301` status:
```json
{
  "redirects": [
    { "source": "/old-path/", "destination": "/new-path/", "statusCode": 301 }
  ]
}
```
Use `"statusCode": 301` rather than `"permanent": true` (which sends a 308).
4. Every redirect must be a 301 (permanent), never a 302.
5. Test each redirect after deploy — old URL should land on the new page, not a 404.

### Custom 404 Page
Every site needs a `src/pages/404.astro` matching the site's design — phone bar, nav, footer all present. Friendly message ("Page not found"), a link back to the homepage, and a link to the contact page. Never leave this as Astro's default blank 404.

### H1 Tags — SEO Optimised
Every H1 must be optimised for search — not just a description of the business or a tagline. If the client has a tagline they want to keep, place it as a subheadline (H2 or paragraph text) directly below the H1 — never as the H1 itself.

**H1 formula:** Primary Service + Location
Examples:
- "House Clearance Services in Brighton & East Sussex"
- "Expert Drain Repairs Across Surrey"
- "Professional Garden Design in Worthing & West Sussex"

**Never use as an H1:**
- Generic taglines: "We Aim to Recycle as Much as Possible"
- Welcome messages: "Welcome to Smith Plumbing"
- Brand names alone: "Garden Creations"
- Vague descriptions: "Your Local Experts"

If the existing site has a weak H1 — rewrite it to the formula above. Keep the URL unchanged. Only the visible H1 text changes.

### Meta Titles
Formula: Primary Keyword | Business Name | Location
Example: Drain Repairs Brighton | Smith Drainage | East Sussex
**Maximum 60 characters. Never exceed this.**
Use a character counter to verify before finalising.

### Meta Descriptions
Formula: What you do, where you do it, why choose you, CTA
Example: Expert drain repairs across Brighton and East Sussex. Fast response, competitive prices. Call Smith Drainage today for a free quote.
**Maximum 160 characters. Never exceed this.**
Use a character counter to verify before finalising.

### Social Sharing Image (Open Graph)
Every site must have an optimised OG image for social sharing.
- Dimensions: 1200x630px
- Include: Business name, primary service, location, logo if available
- Use the base colour as the background
- White or light text
- Clean and readable at small sizes — this appears as a thumbnail when shared on Facebook, WhatsApp, LinkedIn etc
- Set in the Layout.astro head:
```html
<meta property="og:image" content="/images/og-image.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:title" content="[Meta Title]" />
<meta property="og:description" content="[Meta Description]" />
<meta property="og:type" content="website" />
<meta property="og:url" content="[Page URL]" />
```

### Heading Hierarchy
- One H1 per page — contains the primary service and location — SEO optimised per formula above
- H2 for main sections — services, about, why choose us
- H3 for sub-sections and individual service names
- Never skip heading levels
- Never use headings just for styling — use CSS for that

### Schema Markup
Add to every site on every page via the base Layout file:

**LocalBusiness schema** (homepage):
- Business name, address, phone, email, opening hours, areas served, geo coordinates if known

**Service schema** (service pages):
- Service name, description, provider, area served

**BreadcrumbList** (all pages):
- Reflects the page hierarchy

**FAQPage** (any page with a FAQ section):
- Question and answer pairs

### Image Alt Text
- Every image must have a descriptive alt text
- Format: [what is in the image] [business name] [location if relevant]
- Example: "Drain engineer repairing blocked drain Smith Drainage Brighton"
- Never leave alt text blank
- Never use "image" or "photo" as alt text

### Sitemap and Robots
- Generate sitemap.xml automatically via Astro sitemap integration
- robots.txt:
```
User-agent: *
Allow: /
Sitemap: https://[domain]/sitemap.xml
```

### Internal Linking
- Every page must contain a minimum of 3 to 5 internal links naturally within the content
- Links must use descriptive anchor text — never "click here", "read more", or "this page"
- Good anchor text describes where the link goes: "our drain repair service", "get a free quote", "view our work in Brighton"
- Service pages link to related service pages
- Every page links to the contact page
- Homepage links to all main service pages
- Do not force links — they must read naturally within the surrounding content

---

## SECTION 6B — AI DISCOVERY

### llms.txt
Generate a `/public/llms.txt` file for every site. This tells AI platforms (ChatGPT, Claude, Perplexity, Google AI Overviews) what the site is about and makes it citable in AI search results — increasingly how people find local trades.

Format:
```
# [Business Name]

> [One sentence description of what the business does and where]

## Services
- [Service 1]
- [Service 2]
- [Service 3]
[List all services from the brief]

## Locations Served
[List all areas from the brief]

## Contact
Phone: [Primary Phone]
Email: [Email]
Address: [Full Address]

## Pages
- /: Homepage
- /about/: About Us
- /contact/: Contact
- /services/[slug]/: [Service Name]
[List all pages]
```

Generate this automatically from the brief. Place at `/public/llms.txt` so it is accessible at `https://[domain]/llms.txt`.

### Schema — Required on Every Site

**LocalBusiness (Homepage — comprehensive)**
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "[Business Name]",
  "description": "[One sentence description]",
  "url": "https://[domain]",
  "telephone": "[Primary Phone]",
  "email": "[Email]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Street Address]",
    "addressLocality": "[Town]",
    "addressRegion": "[County]",
    "postalCode": "[Postcode]",
    "addressCountry": "GB"
  },
  "areaServed": ["[Area 1]", "[Area 2]", "[Area 3]"],
  "priceRange": "££",
  "image": "https://[domain]/images/og-image.jpg",
  "sameAs": [
    "[Google Business Profile URL if provided]"
  ]
}
```

**Service Schema (each service page)**
```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "[Service Name]",
  "description": "[Service description]",
  "provider": {
    "@type": "LocalBusiness",
    "name": "[Business Name]"
  },
  "areaServed": "[Primary Location]"
}
```

**BreadcrumbList (all pages except homepage)**
**FAQPage (any page containing a FAQ section)**

---

## SECTION 6C — ACCESSIBILITY BASELINE

These are the most impactful accessibility fixes. Build them in from the start on every site.

### Viewport — Never Disable Zoom
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
Never add `user-scalable=no`, `user-scalable=0`, or `maximum-scale=1`. This fails WCAG and prevents users from zooming on mobile.

### Colour Contrast
- Body text on white background: use #222222 or darker — passes 4.5:1 ratio
- White text on coloured background: check the base colour passes contrast. If the base colour is too light for white text, use dark text instead
- Never use light grey text on white background for body copy
- Button text must contrast clearly against button background

### Form Labels
- Every form field must have a visible `<label>` element linked via `for` attribute
- Never use placeholder text as the only label — placeholders disappear when typing
- Required fields must be marked as required

### Images
- All images must have descriptive alt text — already in Section 7
- Decorative images only (purely visual, no information) use `alt=""`

### Gallery Lightbox — Mandatory
If any page on the site contains a gallery or image grid — even an inner service page — a lightbox must be built. No exceptions.

Requirements:
- Clicking any image opens it full screen
- Close button visible in the top right
- Previous and next navigation arrows
- Keyboard support: Escape to close, left/right arrow keys to navigate
- Background overlay dims the page behind the image
- Build as self-contained vanilla JavaScript — no external libraries required

Test the lightbox before handover. Open it, navigate through images, close it, and verify keyboard controls work.

### Semantic HTML
Use correct HTML elements throughout:
- `<nav>` for navigation
- `<main>` for the main content area
- `<header>` for the site header
- `<footer>` for the site footer
- `<section>` for distinct content sections
- `<article>` for standalone content blocks
- `<h1>` through `<h6>` in correct hierarchy — never skip levels
- `<button>` for buttons, `<a>` for links — never use a div as a button

### Skip Navigation Link
Add a skip link as the very first element in the body — allows keyboard and screen reader users to skip the navigation:
```html
<a href="#main-content" class="skip-link">Skip to main content</a>
```
Style it to be invisible until focused:
```css
.skip-link {
  position: absolute;
  top: -100%;
  left: 0;
  background: #000;
  color: #fff;
  padding: 8px 16px;
  z-index: 9999;
}
.skip-link:focus {
  top: 0;
}
```
Add `id="main-content"` to the `<main>` element.

### Focus Indicators
Never remove focus outlines with `outline: none` unless replacing with a clearly visible custom focus style. Every interactive element (links, buttons, inputs) must show a visible focus indicator when tabbed to.

### Mobile Navigation — Mandatory CSS Pattern
Mobile navigation panels must always use the following CSS pattern. Never use a plain breakpoint `display: block` on the panel element — this overrides the browser's `[hidden]` stylesheet rule and pins the menu open.

**Correct pattern:**
```css
/* Panel is hidden by default via the [hidden] attribute */
/* Only show it when [hidden] is absent */
.nav-panel:not([hidden]) {
  display: block;
}
```

**Never do this:**
```css
/* WRONG — author CSS beats [hidden], menu stays open */
@media (max-width: 1040px) {
  .nav-panel {
    display: block;
  }
}
```

The `[hidden]` HTML attribute must be the single source of truth for panel visibility. JavaScript toggles the attribute — CSS only responds to its presence or absence. This is the only pattern that guarantees the menu closes reliably across all browsers. Always test the mobile menu open and close before handover.

### Icon-Only Buttons
Any button or link that uses only an icon (no text) must have an aria-label:
```html
<button aria-label="Open menu">
  <svg>...</svg>
</button>
```

### Cookie Consent Banner
Any site running GA4, GTM, Meta Pixel, or any other tracking script needs an actual consent mechanism — the footer link to the Cookies & Privacy Policy alone does not satisfy UK GDPR/PECR.

**Cookie categories — three types, handled differently:**

- **Necessary** — the consent cookie itself (localStorage entry). Does not require consent. Always active.
- **Analytics** — GA4, GTM. Require consent before loading.
- **Marketing** — Meta Pixel, Google Ads, any ad tracking. Require consent before loading.

**Check the brief for TRACKING field before building the banner:**

**Standard build (GA4 only — no Meta Pixel or Google Ads):**
Use a simple two button banner — Accept and Reject. No settings panel needed.
- Accept = loads GA4
- Reject = blocks GA4

**Advanced build (GA4 + Meta Pixel or Google Ads):**
Add a Settings button alongside Accept and Reject. The settings panel shows:
- Analytics Cookies (GA4) — toggle on/off
- Marketing Cookies (Meta Pixel / Google Ads) — toggle on/off
Save individual preferences to localStorage per category.

**Standard wording — use this exact text on every site:**
"We use cookies to run this site and understand how it's used. See our [Cookies & Privacy Policy](https://osamweb.com/cookies-privacy-policy/)."

Note the space before the link. Never remove it. Never add "Necessary cookies are always active" or any other text.

**Two buttons — Reject and Accept:**
- Both buttons must be the same size and equally easy to click
- Accept button: use the site's base/brand colour
- Reject button: neutral colour (#6B7280 grey) — never hidden, never smaller than Accept
- Never make Reject a plain text link while Accept is a button

**Blocking behaviour — this is the critical part:**
- All tracking scripts (GA4, GTM, Meta Pixel, any others) must be placed inside the CookieBanner.astro component, not in Layout.astro
- On first visit — show the banner, do not load any tracking scripts
- If visitor clicks Accept — load all consented scripts, save preferences to localStorage, hide the banner
- If visitor clicks Reject — do not load any non-necessary scripts, save cookie_consent=rejected to localStorage, hide the banner
- On every subsequent page load — check localStorage first. If accepted, load tracking silently. If rejected, load nothing. If no value, show the banner again
- Never load tracking scripts before checking localStorage — even for a fraction of a second

**Implementation:**
Use CookieBanner.astro as a self-contained component. It handles the banner UI, the localStorage check, and the conditional script injection all in one place. Include it in Layout.astro — but tracking scripts go inside it, not in the Layout head directly.

### Accessibility Checklist (add to pre-launch)
- [ ] Viewport meta does not disable zoom
- [ ] All form fields have visible labels
- [ ] Colour contrast passes on all text
- [ ] Skip navigation link present and functional
- [ ] Semantic HTML used throughout — nav, main, header, footer, section
- [ ] All icon-only buttons have aria-label
- [ ] Focus indicators visible on all interactive elements

---

## SECTION 7 — IMAGES

### Image Hierarchy — Follow in Order

**1. Client images provided**
If the brief states images are attached or provided — use them. Always. These take priority over everything. Convert to WebP, compress to under 200kb where possible, add descriptive alt text.

**2. Images from existing website (Modernise & Amend / Carbon Copy)**
Download images from the live site and reuse them in the same positions. Convert to WebP.

**3. Envato MCP (primary stock source)**
Search the Envato library via the MCP connector for trade and location relevant imagery.
Search terms should be specific: "plumber fixing pipe under sink UK" not just "plumber"
Select images that feel real and professional — avoid overly staged or obviously stock imagery.
All assets are licensed under the OSAM Envato Elements subscription.

**4. Unsplash / Pexels (fallback)**
If Envato does not return suitable results, search Unsplash or Pexels.
Free to use, no licensing issues.

### Image Rules
- Hero images: minimum 1920x1080px, high quality, relevant to the business
- Section images: minimum 800x600px
- All images converted to WebP format
- All images compressed to under 200kb where possible
- Above the fold images: do not lazy load — load immediately
- All other images: loading="lazy"
- Add width and height attributes to prevent layout shift
- Never use team or staff photos from stock — if no real team photos exist, do not use stock people as fake staff
- Never use images that show competitor branding or logos

### Responsive Images
Never ship a single fixed-size image to every device — a 1920px hero has no business loading on a 390px phone. Use Astro's built-in `<Image>` component (`astro:assets`) so it generates the `srcset`/`sizes` automatically, or hand-build a `<picture>` element if the component doesn't fit. Minimum breakpoints:
- Hero images: 600w (mobile), 1024w (tablet), 1920w (desktop)
- Section images: 400w (mobile), 800w (desktop)

---

## SECTION 8 — FORMS & CONTACT

### Standard Contact Form
Every site uses the same standard form fields unless the brief specifies otherwise:
- Name (required)
- Phone Number (required)
- Email Address (required)
- Message (required)
- Submit button — label matches the primary CTA e.g. "Get a Free Quote" or "Send Message"

### Hidden Fields — Required on Every Form
Every form must include these hidden fields so the Worker knows where to send the email and how to log the submission:

```html
<input type="hidden" name="_recipient" value="[client email from brief]" />
<input type="hidden" name="_subject" value="New Enquiry — [Business Name]" />
<input type="hidden" name="_site" value="https://[client domain]" />
<input type="hidden" name="_honeypot" value="" />
```

The `_site` field must be the full domain including https — e.g. `https://letsclear.co.uk` — not just the business name. This is stored in the database and shown in the email so enquiries can be traced back to the correct client site.

### Service Dropdown
Only add a service dropdown if the brief explicitly requests one under SPECIFIC AMENDS or ADDITIONAL NOTES. Do not add it by default.

If requested, add it as a required select field between the Name field and the Message field:

```html
<div class="osam-form__field">
  <label for="service">Service Required <span aria-hidden="true">*</span></label>
  <select id="service" name="service" required>
    <option value="" disabled selected>Select a service...</option>
    <option value="[Service 1]">[Service 1]</option>
    <option value="[Service 2]">[Service 2]</option>
  </select>
</div>
```

Services in the dropdown come from the brief — use the services listed under PAGES REQUIRED or SPECIFIC AMENDS. Never invent services.

### Additional Custom Fields
If the brief requests any other custom fields — e.g. preferred callback time, property type, postcode — add them between the standard fields in a logical order. Always mark them as required unless the brief says otherwise.

### Form Submission & Spam Protection — Cloudflare Turnstile (NOT Google reCAPTCHA)
- Forms submit to the OSAM form Worker at: https://built-form-worker.cloudflare-fe2.workers.dev
- This Worker URL is fixed — use it on every site, do not change it
- On successful submission — redirect to /thank-you/
- Create a /thank-you/ page matching the site design with a friendly confirmation message
- Honeypot field added to every form for additional spam protection

All OSAM sites use Cloudflare Turnstile through the form Worker. **Do NOT add Google reCAPTCHA** (`www.google.com/recaptcha/api.js` or `recaptcha.net`), and do not create, add or ask for any site key. There is no site key.

Nothing needs registering in Cloudflare for a new site — Turnstile works on the live domain and on Vercel preview addresses (`*.vercel.app`) straight away.

**1. Load the security script lazily — only on pages with a form, on first interaction**

The script is: https://built-form-worker.cloudflare-fe2.workers.dev/captcha.js

Do NOT add it to Layout.astro. Load it from ContactForm.astro only. It provides the same API as reCAPTCHA v3 (`grecaptcha.ready` / `grecaptcha.execute`), so the form code pattern stays the same.

```html
<!-- Add this only inside ContactForm.astro, not Layout.astro -->
<script>
  const WORKER_URL = 'https://built-form-worker.cloudflare-fe2.workers.dev'
  let captchaPromise = null

  function loadCaptcha() {
    if (!captchaPromise) {
      captchaPromise = new Promise((resolve, reject) => {
        const script = document.createElement('script')
        script.src = WORKER_URL + '/captcha.js'
        script.async = true
        script.onload = resolve
        script.onerror = () => { captchaPromise = null; reject(new Error('captcha failed to load')) }
        document.head.appendChild(script)
      })
    }
    return captchaPromise
  }

  // Load on first interaction with any form field
  document.querySelectorAll('form input, form textarea, form select').forEach(el => {
    el.addEventListener('focusin', loadCaptcha, { once: true })
  })

  document.querySelectorAll('form.osam-form').forEach(form => {
    form.addEventListener('submit', async (e) => {
      e.preventDefault()
      const button = form.querySelector('button[type="submit"]')
      const error = form.querySelector('.osam-form__error')
      button.disabled = true
      if (error) error.hidden = true
      try {
        await loadCaptcha()
        await new Promise(r => grecaptcha.ready(r))
        // Fresh token for EVERY submission. No short timeout - allow at least 2 minutes,
        // as the visitor may be asked to tick a box above the send button.
        const token = await grecaptcha.execute('', { action: 'submit' })
        const formData = new FormData(form)
        formData.append('g-recaptcha-response', token)
        const res = await fetch(WORKER_URL, { method: 'POST', body: formData })
        if (!res.ok) throw new Error('submit failed')
        window.location.href = '/thank-you/'
      } catch (err) {
        // execute() rejected or the POST failed - show the normal error message
        if (error) error.hidden = false
        button.disabled = false
      }
    })
  })
</script>
```

The form submission script must:
1. Ensure captcha.js is loaded, then `await new Promise(r => grecaptcha.ready(r))`
2. Call `grecaptcha.execute('', { action: 'submit' })` — empty string, no site key — **once for each submission** (each POST needs a fresh token; never reuse a token)
3. Append the token as `g-recaptcha-response` to the form data
4. POST to the Worker URL, including all hidden fields (`_site` must be the site's full URL, e.g. `https://www.example.co.uk`)
5. On success — redirect to /thank-you/
6. On error, or if `execute()` rejects — show the form's normal error message ("Sorry, something went wrong - please try again or call us on [phone]") without reloading the page

Every form (hero and contact page) uses `class="osam-form"`, a `<button type="submit">`, and contains the error message element `<p class="osam-form__error" role="alert" hidden>...</p>`.

**Timing:** allow at least 2 minutes for `execute()` to resolve. It is usually instant, but if Cloudflare asks the visitor to tick a box, the box appears just above the send button and waits for them. Never wrap `execute()` in a short timeout.

**Never hide the Turnstile box:**
- No `overflow: hidden` on the form or its containers (including the hero form)
- No `display: none` / `visibility: hidden` on `.osam-captcha`
- Leave room above the send button — don't clip or absolutely position over that area

**Turnstile notice — required under the send button on every form, non-negotiable:**
```html
<p class="captcha-notice">
  This site is protected by Cloudflare Turnstile
  (<a href="https://www.cloudflare.com/privacypolicy/" target="_blank" rel="noopener">Privacy Policy</a>).
</p>
```

Use exactly this wording. Do not add "Your details are only used to reply to your enquiry" or any other text. Do not use the old Google reCAPTCHA notice.

**Content-Security-Policy:** OSAM sites don't send a CSP by default. If a site does send one, it must allow:
```
script-src  https://built-form-worker.cloudflare-fe2.workers.dev https://challenges.cloudflare.com
frame-src   https://captcha.connect.osamweb.com https://challenges.cloudflare.com
connect-src https://built-form-worker.cloudflare-fe2.workers.dev
```

**Testing:** send a real enquiry from the live site (or the vercel.app link) and confirm the email arrives.

### Hero Form
The hero contact form is a condensed version of the standard form.
Same fields but styled to sit within the hero section without overwhelming it.
On mobile — the form stacks below the hero text.
Include all hidden fields on the hero form as well as the main contact form.

**Hero form — only for trade and service businesses:**
A contact form in the hero section is only appropriate where an immediate quote or callout request is the primary action. This includes: plumbers, electricians, roofers, builders, drainage engineers, landscapers, cleaners, garages, pest control, locksmiths, and similar trade or emergency service businesses.

Do NOT add a hero form to: retail, ecommerce, restaurants, cafes, hospitality, schools, nurseries, accountants, solicitors, estate agents, or any business where a quote request is not the natural first action for a new visitor.

If in doubt — no hero form. Use a CTA button linking to the contact page instead. A misplaced hero form looks desperate and reduces trust.

---

## SECTION 9 — FOOTER

### Every Footer Must Contain
**Column 1 — About**
- Business name
- Short one or two sentence description of what they do
- Logo if available

**Column 2 — Navigation**
- Quick links to all main pages
- Label: Quick Links

**Column 3 — Contact**
- Full NAP: Business Name, Address, Phone, Email
- Opening hours if provided
- Social media links if provided

**Column 4 — Services (if 4+ services exist)**
- List of main services each linking to the relevant service page
- Label: Our Services

### Footer Design
- Dark background — use the base colour or dark grey
- White or light text
- Dividing line above the copyright row
- Copyright row: © [Year] [Business Name]. All Rights Reserved.

### OSAM Legal Links (Below Footer — Every Site)
Add the following below the main footer copyright row, in a smaller font size, centred:

```html
<p><a href="https://osamweb.com/website-terms-conditions/" target="_blank">Website Terms & Conditions</a> | <a href="https://osamweb.com/cookies-privacy-policy/" target="_blank">Cookies & Privacy Policy</a></p>
```

This must appear on every site, on every page, below the footer. Do not style it prominently — small text, muted colour, but fully visible and clickable.

---

## SECTION 10 — TECHNICAL STANDARDS

### Astro Project Setup
```bash
npm create astro@latest [client-name]-website
cd [client-name]-website
npm install
npm install @astrojs/sitemap
```

**astro.config.mjs — mandatory setting:**
Always set `compressHTML: false` in astro.config.mjs. This must be present on every build without exception.

```js
import { defineConfig } from 'astro/config'
import sitemap from '@astrojs/sitemap'

export default defineConfig({
  site: 'https://[client-domain]',
  compressHTML: false,
  integrations: [sitemap()],
})
```

Why: `compressHTML: true` (the Astro default) strips whitespace between text nodes and inline elements in the production build. This causes words and inline links to run together — the word before a link and the link text merge with no space. It also breaks the required spaces in the Turnstile notice beneath every form, which is a compliance issue. This bug only appears in production, never in dev, so it will not be caught during local review. Setting `compressHTML: false` prevents it entirely at zero meaningful cost — Vercel compresses the output at the edge anyway.

### File Structure
```
[client-name]-website/
├── public/
│   ├── images/
│   ├── favicon.ico         (32x32px, generated from logo)
│   ├── apple-touch-icon.png (180x180px, generated from logo)
│   ├── robots.txt
│   ├── sitemap.xml
│   └── llms.txt
├── src/
│   ├── components/
│   │   ├── PhoneBar.astro
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── ContactForm.astro
│   │   ├── CookieBanner.astro
│   │   ├── Footer.astro
│   │   └── [other components]
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       ├── index.astro
│       ├── about.astro
│       ├── contact.astro
│       ├── thank-you.astro
│       ├── 404.astro
│       └── services/
│           └── [service pages]
├── scripts/
│   └── push-live.sh          (GitHub + Vercel deploy script, see GitHub & Vercel section)
├── astro.config.mjs
├── vercel.json               (security headers, trailing slash, 301 redirects)
└── package.json
```

### Favicon
Generate favicons from the client logo before building. Never leave the default Astro favicon.

- **favicon.ico** — 32x32px. Use the logo mark (icon only, not full wordmark). If the logo has a coloured background, use the base colour as the favicon background. Save to `/public/favicon.ico`.
- **apple-touch-icon.png** — 180x180px. Same logo mark with sufficient padding around it. Save to `/public/apple-touch-icon.png`.

Add both to the `<head>` in Layout.astro:
```html
<link rel="icon" type="image/x-icon" href="/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
```

If no logo is provided — use the first letter of the business name on the base colour background as the favicon.

### Tracking Codes
Extract all tracking codes from the existing website source code before building.
Check for:
- Google Analytics 4 (G- ID)
- Google Tag Manager (GTM- ID)
- Meta Pixel
- Any other third party scripts

Place all tracking codes in the Layout.astro `<head>` section.
Copy IDs exactly — do not modify.

### Google Fonts — Preloading
If the build uses Google Fonts, never just drop a standard `<link>` stylesheet in the head — this blocks rendering and causes a flash of unstyled text, hurting Lighthouse scores.

Use the preload pattern instead:
```html
<!-- Preconnect to Google Fonts servers -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />

<!-- Preload the font stylesheet -->
<link rel="preload" as="style" href="https://fonts.googleapis.com/css2?family=[FontName]:wght@400;600;700&display=swap" />

<!-- Load it non-blocking -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=[FontName]:wght@400;600;700&display=swap" media="print" onload="this.media='all'" />

<!-- Fallback for no-JS -->
<noscript>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=[FontName]:wght@400;600;700&display=swap" />
</noscript>
```

Always include `display=swap` in the Google Fonts URL so body text renders in the fallback font immediately while the custom font loads — no invisible text.

Define a font stack fallback in CSS so the layout doesn't shift when the font loads:
```css
body {
  font-family: '[FontName]', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}
```

### GA4 Conversion Events
Installing the tracking ID alone only gives pageviews — every site needs two conversion events set up on top:
- **`form_submit`** — fire this on the `/thank-you/` page (since that's where every successful submission lands). If GTM is present, set it as a GTM trigger on that page rather than hardcoding a `gtag()` call, so it can be managed later without a redeploy.
- **`phone_click`** — fire this whenever a `tel:` link is clicked. If GTM is present, use a "Click - Just Links" trigger filtering for `href` containing `tel:`. If no GTM, add a click listener that calls `gtag('event', 'phone_click')`.
Mark both as conversions in GA4.

### API Keys & Secrets
Not everything that looks like a key needs the same treatment:
- **Turnstile** — there is no site key to add to the site. All Turnstile configuration and the secret key live inside the OSAM form Worker. Never add a site key or secret to the Astro repo.
- **Amazon SES credentials** — encrypted environment variables on the Cloudflare form Worker only (Cloudflare dashboard or `wrangler secret put`). Never in the Astro repo, never in a committed `.env` file.
- **Vercel token (`VERCEL_TOKEN`) and team ID (`VERCEL_TEAM_ID`)** — environment variables on the designer's own machine only (in `~/.zshrc`). Never in the repo, never in a committed file, never printed in the handover.
- **Envato API key** — used locally by whoever is sourcing stock images during the build. It never touches the live site, the repo, or Vercel at all.
- **GA4 / GTM / Meta Pixel IDs** — not secrets, visible in page source regardless. Fine to hardcode in `Layout.astro`.
Rule of thumb: if exposing it lets someone send email as the client or run up API costs, it's a secret — encrypted env var, never in git. If it's just an identifier already visible in the rendered page, hardcoding it is fine.

### Security Headers
Add a `vercel.json` file in the project root (not in `public/`) to every site. Vercel reads this natively. Do NOT use a `public/_headers` file — that is a Cloudflare Pages feature and Vercel ignores it.
```json
{
  "trailingSlash": true,
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "X-Frame-Options", "value": "SAMEORIGIN" },
        { "key": "X-Content-Type-Options", "value": "nosniff" },
        { "key": "Referrer-Policy", "value": "strict-origin-when-cross-origin" },
        { "key": "Permissions-Policy", "value": "geolocation=(), microphone=(), camera=()" },
        { "key": "Strict-Transport-Security", "value": "max-age=31536000; includeSubDomains; preload" }
      ]
    }
  ],
  "redirects": []
}
```
- Set `trailingSlash` to match the site's URL convention (see Domain & URL Consistency) — `false` if the existing site has no trailing slashes.
- Add any 301 redirects to the `redirects` array (see 301 Redirect Audit).
- Do not add a Content-Security-Policy header unless the brief asks for one. If you do, include the Turnstile allowances listed in Section 8.
Verify the result at securityheaders.com before launch.

### Performance Standards
Every site must achieve before launch:
- Lighthouse Performance score: 90+
- Lighthouse SEO score: 90+
- Lighthouse Accessibility score: 85+
- Core Web Vitals (checked via PageSpeed Insights, not just local Lighthouse): LCP under 2.5s, CLS under 0.1, INP under 200ms
- All images converted to WebP
- No render-blocking scripts
- CSS and JS minified

### GitHub & Vercel — "Push Live" (End of Every Build and Every Amend)

Sites are hosted on **Vercel**, built automatically from the GitHub repo. Cloudflare Pages is no longer used for hosting (the form Worker still runs on Cloudflare — that does not change).

**Trigger:** when the designer says "push live" (or "deploy", "push it", "send to Vercel"), run the push-live script below. It commits and pushes to GitHub, creates the Vercel project linked to the repo on the first run, waits for Vercel to finish building, and prints the dev link. Do not push live until the designer asks.

**The order is non-negotiable: GitHub first, Vercel builds from GitHub. Always.**

**NEVER use `vercel deploy`, `vercel --prod`, `npx vercel` uploads, `wrangler pages deploy`, or any other direct upload method. Vercel must build from the GitHub repo. Direct uploads bypass GitHub entirely, break the amend process, remove rollback capability, and mean no one else can ever pick up the work.**

**If anything prevents the GitHub push — STOP. Tell the designer what the problem is. Do not find a workaround. Do not deploy to Vercel by any other route. Do not continue.**

The GitHub organisation is **built-osam**. Not osam-websites. Not any other name. Always built-osam.

**Step 1 — Check the tools and credentials**
```bash
command -v gh || /opt/homebrew/bin/brew install gh
gh auth status || gh auth login        # GitHub.com, HTTPS, log in via browser
test -n "$VERCEL_TOKEN" && test -n "$VERCEL_TEAM_ID" && echo "Vercel credentials OK"
```
If Homebrew itself is missing, install it first: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

If `VERCEL_TOKEN` or `VERCEL_TEAM_ID` is not set — STOP and tell the designer to complete the one-time setup below. Never ask the designer to paste the token into the chat, and never write it into any file in the project.

**Step 2 — Make sure the project is a git repo on `main`**
```bash
git rev-parse --git-dir >/dev/null 2>&1 || git init -b main
```
Make sure `.gitignore` contains `node_modules/`, `dist/`, `.astro/`, `.env` and `.vercel/`.

**Step 3 — Save the push-live script (first push only)**
Save the following as `scripts/push-live.sh` in the project and run `chmod +x scripts/push-live.sh`. It contains no secrets — it reads the token from the designer's environment — so it is committed with the site.

```bash
#!/usr/bin/env bash
# OSAM push live: GitHub first, then Vercel builds from GitHub, then print the link.
# Usage: ./scripts/push-live.sh <client-domain> "<commit message>"
#   e.g. ./scripts/push-live.sh plastererdorking.co.uk "Initial build - Plasterer Dorking"
set -euo pipefail

: "${VERCEL_TOKEN:?VERCEL_TOKEN is not set - see one-time setup in the OSAM skill file}"
: "${VERCEL_TEAM_ID:?VERCEL_TEAM_ID is not set - see one-time setup in the OSAM skill file}"
DOMAIN="${1:?Usage: push-live.sh <client-domain> \"<commit message>\"}"
MESSAGE="${2:-Update - $DOMAIN}"

ORG="built-osam"
REPO="client-$DOMAIN"                                   # e.g. client-plastererdorking.co.uk
PROJECT="$(echo "$DOMAIN" | tr 'A-Z.' 'a-z-')"          # e.g. plastererdorking-co-uk
API="https://api.vercel.com"
Q="teamId=$VERCEL_TEAM_ID"
vc() { curl -sS --fail-with-body -H "Authorization: Bearer $VERCEL_TOKEN" -H "Content-Type: application/json" "$@"; }
js() { node -e "let s='';process.stdin.on('data',c=>s+=c).on('end',()=>{const o=JSON.parse(s);$1})"; }

# 1. GitHub - commit and push (create the private repo in built-osam on first run)
git add -A
git commit -m "$MESSAGE" || echo "Nothing new to commit."
if ! git remote get-url origin >/dev/null 2>&1; then
  gh repo create "$ORG/$REPO" --private --source=. --remote=origin
fi
git push -u origin main

# 2. Vercel - create the project linked to the GitHub repo (first run only)
CODE=$(curl -s -o /dev/null -w '%{http_code}' -H "Authorization: Bearer $VERCEL_TOKEN" "$API/v9/projects/$PROJECT?$Q")
if [ "$CODE" = "404" ]; then
  echo "Creating Vercel project $PROJECT linked to $ORG/$REPO..."
  vc -X POST "$API/v11/projects?$Q" \
    -d "{\"name\":\"$PROJECT\",\"framework\":\"astro\",\"gitRepository\":{\"type\":\"github\",\"repo\":\"$ORG/$REPO\"}}" >/dev/null
  # Turn off Vercel login protection so clients can open the vercel.app link
  vc -X PATCH "$API/v9/projects/$PROJECT?$Q" -d '{"ssoProtection":null}' >/dev/null
  # The repo was pushed before the project existed, so push once more to trigger the first build
  git commit --allow-empty -m "Trigger first Vercel deployment"
  git push
elif [ "$CODE" != "200" ]; then
  echo "Vercel API error (HTTP $CODE) - check VERCEL_TOKEN and VERCEL_TEAM_ID." >&2; exit 1
fi
PROJECT_ID=$(vc "$API/v9/projects/$PROJECT?$Q" | js 'console.log(o.id)')

# 3. Wait for the Vercel build of this exact commit (up to ~10 minutes)
SHA=$(git rev-parse HEAD)
echo "Waiting for Vercel to build commit ${SHA:0:7}..."
for i in $(seq 1 60); do
  INFO=$(vc "$API/v6/deployments?$Q&projectId=$PROJECT_ID&limit=10" | SHA="$SHA" js '
    const d=(o.deployments||[]).find(x=>x.meta&&x.meta.githubCommitSha===process.env.SHA);
    console.log(d ? (d.readyState||d.state)+" "+d.uid+" "+d.url : "QUEUED - -")')
  read -r STATE UID_ URL <<<"$INFO"
  case "$STATE" in
    READY)
      LINK=$(vc "$API/v13/deployments/$UID_?$Q" | js '
        const a=(o.alias||[]).filter(x=>x.endsWith(".vercel.app")).sort((x,y)=>x.length-y.length);
        console.log(a[0]||o.url)')
      echo ""
      echo "GitHub repo:  https://github.com/$ORG/$REPO"
      echo "Dev link:     https://$LINK"
      echo "This build:   https://$URL"
      exit 0 ;;
    ERROR|CANCELED)
      echo "Vercel build $STATE for commit ${SHA:0:7}. Build log: https://$URL/_logs" >&2
      echo "Run 'npm run build' locally to see the error, fix it, then run this script again." >&2
      exit 1 ;;
  esac
  sleep 10
done
echo "Timed out waiting for Vercel. Check the project in the Vercel dashboard." >&2
exit 1
```

**Step 4 — Run it**
```bash
./scripts/push-live.sh [client-domain] "Initial build — [Client Name]"
```
e.g. `./scripts/push-live.sh plastererdorking.co.uk "Initial build — Plasterer Dorking"`

- GitHub repo: `built-osam/client-[domain]` e.g. `client-plastererdorking.co.uk`
- Vercel project: the domain with dots replaced by hyphens e.g. `plastererdorking-co-uk` — this sets the `vercel.app` dev link
- Vercel auto-detects Astro: build command `npm run build`, output directory `dist`, production branch `main`. Do not add the `@astrojs/vercel` adapter — sites are static and don't need it.

If the Vercel build fails, the script stops and says so. Run `npm run build` locally, fix the error, then run the script again with a commit message describing the fix.

**Step 5 — Tell the designer**
Once the script finishes, output:
- The GitHub repo URL
- The dev link (`https://[project].vercel.app`) — this is the link to send to the client for approval
- Any items from the handover summary that need attention

Every future push to `main` triggers an automatic redeploy on Vercel. This is the only correct deployment method.

### One-Time Setup — GitHub ↔ Vercel Connection (done once by OSAM, not per site)
1. **Vercel plan:** the OSAM Vercel team must be on the Pro plan — Hobby is for non-commercial use only and can't deploy private repos from a GitHub organisation.
2. **Install the Vercel GitHub app on built-osam:** Vercel dashboard → Team Settings → Git → connect GitHub → install the Vercel app on the **built-osam** organisation with access to **All repositories** (so every new client repo is covered automatically).
3. **Create a Vercel access token:** Vercel → Account Settings → Tokens → Create, scoped to the OSAM team.
4. **Find the team ID:** Vercel → Team Settings → General → Team ID (starts `team_`).
5. **On each designer's Mac**, add to `~/.zshrc` then restart the terminal:
```bash
export VERCEL_TOKEN="paste-token-here"
export VERCEL_TEAM_ID="team_xxxxxxxx"
```
6. Make sure each designer is logged into GitHub CLI (`gh auth login`) with an account that can create repos in built-osam.

### 301 Redirect Audit — All Build Types
Before building any site — Carbon Copy, Modernise, or New Build — crawl the existing live site to find every URL that currently resolves. Do not rely on the sitemap alone — WordPress and other CMS platforms generate URLs that get indexed but never appear in sitemaps (category pages, tag pages, author pages, old campaign pages, paginated pages, duplicate contact pages etc).

**How to crawl:**
Use a tool like Screaming Frog, Sitebulb, or the following curl-based approach to spider the site and list all resolving URLs before starting the build.

**What to do with the list:**
1. Compare every crawled URL against the pages being built
2. Any URL that exists on the old site but is NOT being rebuilt needs a 301 redirect to the closest equivalent page
3. Build the redirect map before writing any code — add every redirect to the `redirects` array in `vercel.json`:
```json
"redirects": [
  { "source": "/old-page/", "destination": "/new-page/", "statusCode": 301 },
  { "source": "/category/drainage/", "destination": "/services/drainage/", "statusCode": 301 }
]
```
4. If there is no obvious equivalent — redirect to the homepage or the most relevant service page. Never leave it as a 404.
5. Test every redirect after deploy

**Common URLs to check even on Carbon Copy builds:**
- Trailing slash variants — `/services` vs `/services/`
- www vs non-www
- Old WordPress category, tag, and author URLs
- Any paginated URLs — `/page/2/` etc
- Old campaign or seasonal pages
- Duplicate contact pages — `/contact` and `/contact-us` both resolving

Add a checklist item: all crawled URLs from the old site either exist in the new build or have a 301 redirect in `vercel.json`.

### Vercel Deployment
- Vercel builds from the GitHub repo via the push-live script (see GitHub & Vercel section)
- Share the `vercel.app` dev link with the client for approval before pointing the domain

### DNS Go Live
Once the client has approved the `vercel.app` dev link:
1. Vercel → the project → Settings → Domains → add the apex domain (`example.co.uk`) and `www.example.co.uk`
2. Set the non-canonical one to redirect to the canonical one with a 301 (see Domain & URL Consistency)
3. At the DNS provider, add the records Vercel shows on the Domains screen. Normally:
```
Type: A      Name: @     Value: 76.76.21.21
Type: CNAME  Name: www   Value: cname.vercel-dns.com
```
Always use the exact values Vercel displays for the project if they differ from the above.
4. If the domain's DNS is managed in Cloudflare, set both records to **DNS only** (grey cloud), not Proxied — proxying through Cloudflare interferes with Vercel's SSL and caching.
5. Remove any old records pointing at Cloudflare Pages (`*.pages.dev`) or the previous host.

Vercel issues the SSL certificate automatically once DNS resolves.

### Browser & Device Test Matrix
Test every site on, at minimum:
- Chrome (latest), Safari (latest, including iOS Safari), Firefox (latest), Edge (latest)
- Desktop (1440px+), tablet (768–1024px), mobile (390px, both iOS and Android)

### Post-Build Check — 5 Minutes Maximum
After all pages are built and npm run build completes, do a quick pass only. Do not spend more than 5 minutes on this.

Check only:
- Every page has at least one internal link to the contact page
- Every page has a CTA above the fold
- No page is a copy-paste of another page

Flag anything that fails in the handover summary. The designer will review the rest.

### Post-Amend Push Process
After every round of amends — whether during the build review or after the site is live — push live using the same script. Vercel redeploys automatically from GitHub and the script prints the dev link once the new build is ready.

```bash
./scripts/push-live.sh [client-domain] "Amends — [brief description of what changed]"
```

Do this after every single set of amends. Never leave changes sitting locally without pushing.

If the designer asks for further changes after the initial push, apply all changes, then run the same command. The `vercel.app` dev link and the live domain will both update automatically.

**Older sites still on Cloudflare Pages:** if the repo has no `vercel.json` and no `scripts/push-live.sh`, the site hasn't been moved to Vercel yet. Ask the designer whether to move it before pushing. If moving it: convert `public/_headers` and `public/_redirects` into `vercel.json`, delete those two files, add the push-live script, and push live. The domain stays on Cloudflare Pages until its DNS is switched as in DNS Go Live.

### Pre-Launch Checklist
- [ ] All pages present and URLs match brief / original exactly
- [ ] Canonical tags present on every page and self-referencing the correct domain/trailing-slash convention
- [ ] www / non-www redirect in place, only one version resolves
- [ ] Custom 404 page present and matches site design
- [ ] For Modernise builds with URL changes — all old URLs 301 redirect to their new equivalent, tested
- [ ] Cookie consent banner present, blocks tracking scripts until accepted
- [ ] Security headers (`vercel.json`) present and verified at securityheaders.com
- [ ] Core Web Vitals checked via PageSpeed Insights — LCP under 2.5s, CLS under 0.1, INP under 200ms. Run once at the end of the build after npm run build, not during.
- [ ] All phone numbers are tel: links
- [ ] GA4 conversion events firing for form submission and phone click
- [ ] Carbon Copy builds only — take full page screenshots of every page at desktop (1440px) and mobile (390px) and compare against the original site. Layout, spacing, copy, and images must match. This is non-negotiable for Carbon Copy builds.
- [ ] Tested across full browser/device matrix
- [ ] Phone bar visible on every page
- [ ] Hero contains form, CTA, and Google badge (if applicable)
- [ ] Contact form submits and email received correctly — tested from the live site / vercel.app link
- [ ] Forms use Cloudflare Turnstile via captcha.js from the form Worker — no Google reCAPTCHA script, no site key anywhere
- [ ] Turnstile notice ("This site is protected by Cloudflare Turnstile (Privacy Policy).") under the send button on every form
- [ ] Turnstile box not hidden or clipped — no overflow:hidden on forms, no display:none on .osam-captcha
- [ ] `_site` hidden field contains the site's full URL on every form
- [ ] Thank you page displays after form submission
- [ ] Google Maps displays on contact page
- [ ] All tracking codes present in head
- [ ] All images load correctly and have alt text
- [ ] OG social sharing image set on every page
- [ ] sitemap.xml accessible at /sitemap.xml
- [ ] robots.txt accessible at /robots.txt
- [ ] Run `npm run build` and confirm it completes without errors before running the SEO audit — check the dist folder output, not just the source files
- [ ] Schema markup validates at https://search.google.com/test/rich-results
- [ ] Lighthouse 90+ on Performance and SEO
- [ ] SSL active (Vercel → Domains shows the domain as Valid)
- [ ] Vercel project builds from the built-osam GitHub repo (no direct uploads)
- [ ] Mobile layout reviewed on real device or simulator
- [ ] OSAM legal links present in footer on every page
- [ ] All internal links working
- [ ] No broken links or 404 errors
- [ ] All H1s are SEO optimised — service + location formula, not taglines
- [ ] All meta titles are 60 characters or under
- [ ] All meta descriptions are 160 characters or under
- [ ] Full spell check completed on all pages
- [ ] Navigation menu items checked — no overlapping or truncated text on any screen size. If text overlaps, rewrite the nav label to be shorter — keep the URL unchanged
- [ ] No copyright year in the footer — copyright line reads: © [Business Name]. All Rights Reserved.
- [ ] llms.txt accessible at /llms.txt
- [ ] Viewport meta does not disable zoom
- [ ] All form fields have visible labels
- [ ] Skip navigation link present and functional
- [ ] Semantic HTML used throughout
- [ ] All icon-only buttons have aria-label
- [ ] Focus indicators visible on all interactive elements
