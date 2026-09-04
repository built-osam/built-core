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

---

## SECTION 1 — HOW TO READ THE BRIEF

### Build Types

**Carbon Copy**
Rebuild the existing website exactly as it is. Same design, same layout, same content, same images, same URLs. The client must not be able to tell the difference. Do not modernise, do not rewrite, do not improve. Copy it precisely.

Verification: before starting, take full-page screenshots of every existing page at desktop (1440px) and mobile (390px) widths. After the build, take matching screenshots of the new site at the same widths and compare them side by side — layout, spacing, copy, and images should all match. This is the actual test of whether the build succeeded, not just a visual once-over.

**Modernise & Amend**
Keep the overall style and brand familiar but update the design to feel current. Apply all specific amends listed in the brief. Read the design call notes carefully — they take priority over your own design decisions. If example websites are provided, study them and take direction from their layout, feel, and structure.

**New Build**
No existing website to reference. Build entirely from the brief and design call notes. Make design decisions based on the brand colours, industry, and any example websites provided.

### Priority Order
When instructions conflict, follow this order:
1. Specific amends listed in the brief — always highest priority
2. Design call notes
3. Example websites provided
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
- Keep it simple — phone icon, number, email icon, address. No extra content.
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

### Content Rules — Never Do These
- Never invent facts, qualifications, years of experience, or awards
- Never invent testimonials or reviews
- Never use placeholder text (Lorem Ipsum) — if content is missing, write real content or flag it
- Never use the phrase "we are a leading provider" or similar generic claims
- Never write more than 300 words on any single section without a clear reason

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
- Set up a Cloudflare redirect (Bulk Redirect or Redirect Rule) sending the non-canonical variant (the `www` version if apex is canonical, or vice versa) to the canonical one with a 301.
- Add a self-referencing canonical tag to every page in `Layout.astro`, matching the exact canonical URL (protocol, domain, trailing slash):
```html
<link rel="canonical" href="https://[canonical-domain]/[exact-path]/" />
```

### Handling URL Changes (Modernise & New Build only)
If the brief requires restructuring URLs that are already live and indexed, don't just drop the old ones:
1. Before building, pull the full list of existing indexed URLs — from the current `sitemap.xml`, or a quick crawl of the live site if no sitemap exists.
2. Build a redirect map: every old URL that changes → its new equivalent.
3. Implement the redirects in a `public/_redirects` file (Cloudflare Pages reads this natively) — one line per redirect, using a `301` status:
```
/old-path/  /new-path/  301
```
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
- Every page must link to at least two other pages naturally within the content
- Service pages link to related service pages
- Every page links to the contact page

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

### Icon-Only Buttons
Any button or link that uses only an icon (no text) must have an aria-label:
```html
<button aria-label="Open menu">
  <svg>...</svg>
</button>
```

### Cookie Consent Banner
Any site running GA4, GTM, Meta Pixel, or any other tracking script needs an actual consent mechanism — the footer link to the Cookies & Privacy Policy alone does not satisfy UK GDPR/PECR.

- Show a simple banner on first visit, before any tracking scripts fire.
- Give an "Accept" and a "Reject" option that are equally easy to use — never bury reject behind extra clicks or make accept the only prominent button.
- Do not load GA4 / GTM / Meta Pixel until the visitor accepts. If rejected, don't load them at all for that visit.
- Remember the visitor's choice (a first-party cookie or localStorage) so the banner doesn't reappear on every page.
- Include a short line of text and a link to the Cookies & Privacy Policy page.
- Keep it simple — a lightweight custom banner component (`CookieBanner.astro`) is enough; a full consent-management platform is not required for this type of site.

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
Every site uses the same standard form fields:
- Name (required)
- Phone Number (required)
- Email Address (required)
- Message (required)
- Submit button — label matches the CTA e.g. "Get a Free Quote" or "Send Message"

### Form Submission
- Forms submit via Amazon SES through a Cloudflare Worker
- On successful submission — redirect to /thank-you/
- Create a /thank-you/ page matching the site design with a friendly confirmation message
- reCAPTCHA v3 active on all forms — invisible to the user
- Honeypot field added to every form for additional spam protection

### Hero Form
The hero contact form is a condensed version of the standard form.
Same fields but styled to sit within the hero section without overwhelming it.
On mobile — the form stacks below the hero text.

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

### File Structure
```
[client-name]-website/
├── public/
│   ├── images/
│   ├── favicon.ico
│   ├── robots.txt
│   ├── sitemap.xml
│   ├── llms.txt
│   ├── _headers
│   └── _redirects            (only needed if URLs changed from the existing site)
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
├── astro.config.mjs
└── package.json
```

### Tracking Codes
Extract all tracking codes from the existing website source code before building.
Check for:
- Google Analytics 4 (G- ID)
- Google Tag Manager (GTM- ID)
- Meta Pixel
- Any other third party scripts

Place all tracking codes in the Layout.astro `<head>` section.
Copy IDs exactly — do not modify.

### GA4 Conversion Events
Installing the tracking ID alone only gives pageviews — every site needs two conversion events set up on top:
- **`form_submit`** — fire this on the `/thank-you/` page (since that's where every successful submission lands). If GTM is present, set it as a GTM trigger on that page rather than hardcoding a `gtag()` call, so it can be managed later without a redeploy.
- **`phone_click`** — fire this whenever a `tel:` link is clicked. If GTM is present, use a "Click - Just Links" trigger filtering for `href` containing `tel:`. If no GTM, add a click listener that calls `gtag('event', 'phone_click')`.
Mark both as conversions in GA4.

### API Keys & Secrets
Not everything that looks like a key needs the same treatment:
- **reCAPTCHA Site Key** — public, goes directly in the frontend HTML/JS.
- **reCAPTCHA Secret Key** — never in frontend code. Lives only inside the Cloudflare Worker, used to verify the token server-side.
- **Amazon SES credentials** — encrypted environment variables on the Cloudflare Worker only (Cloudflare dashboard or `wrangler secret put`). Never in the Astro repo, never in a committed `.env` file.
- **Envato API key** — used locally by whoever is sourcing stock images during the build. It never touches the live site, the repo, or Cloudflare at all.
- **GA4 / GTM / Meta Pixel IDs** — not secrets, visible in page source regardless. Fine to hardcode in `Layout.astro`.
Rule of thumb: if exposing it lets someone send email as the client or run up API costs, it's a secret — encrypted env var, never in git. If it's just an identifier already visible in the rendered page, hardcoding it is fine.

### Security Headers
Add a `public/_headers` file (Cloudflare Pages reads this natively — no Worker code needed) to every site:
```
/*
  X-Frame-Options: SAMEORIGIN
  X-Content-Type-Options: nosniff
  Referrer-Policy: strict-origin-when-cross-origin
  Permissions-Policy: geolocation=(), microphone=(), camera=()
  Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
```
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

### GitHub
```bash
git init
git remote add origin https://github.com/osam-websites/client-[name]
git add .
git commit -m "Initial build — [Client Name]"
git push -u origin main
```

### Cloudflare Pages Deployment
- Connect GitHub repo to Cloudflare Pages
- Build command: `npm run build`
- Output directory: `dist`
- Deploy and share the pages.dev preview link with the client before pointing the domain

### DNS Go Live
Once client has approved the pages.dev preview:
```
Type: CNAME
Name: www
Value: [project-name].pages.cloudflare.com
```
Cloudflare handles SSL automatically.

### Browser & Device Test Matrix
Test every site on, at minimum:
- Chrome (latest), Safari (latest, including iOS Safari), Firefox (latest), Edge (latest)
- Desktop (1440px+), tablet (768–1024px), mobile (390px, both iOS and Android)

### Pre-Launch Checklist
- [ ] All pages present and URLs match brief / original exactly
- [ ] Canonical tags present on every page and self-referencing the correct domain/trailing-slash convention
- [ ] www / non-www redirect in place, only one version resolves
- [ ] Custom 404 page present and matches site design
- [ ] For Modernise builds with URL changes — all old URLs 301 redirect to their new equivalent, tested
- [ ] Cookie consent banner present, blocks tracking scripts until accepted
- [ ] Security headers (`_headers` file) present and verified at securityheaders.com
- [ ] Core Web Vitals checked via PageSpeed Insights — LCP, CLS, INP within target
- [ ] All phone numbers are tel: links
- [ ] GA4 conversion events firing for form submission and phone click
- [ ] Carbon Copy builds only — screenshot comparison against original completed, no visible differences
- [ ] Tested across full browser/device matrix
- [ ] Phone bar visible on every page
- [ ] Hero contains form, CTA, and Google badge (if applicable)
- [ ] Contact form submits and email received correctly
- [ ] Thank you page displays after form submission
- [ ] Google Maps displays on contact page
- [ ] All tracking codes present in head
- [ ] All images load correctly and have alt text
- [ ] OG social sharing image set on every page
- [ ] sitemap.xml accessible at /sitemap.xml
- [ ] robots.txt accessible at /robots.txt
- [ ] Schema markup validates at https://search.google.com/test/rich-results
- [ ] Lighthouse 90+ on Performance and SEO
- [ ] SSL active
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
