# Crowley's City SEO Playbook: City Page Standard

**Audience:** Crowley's Granite & Quartz (Dan Izoita, Manus, Claude)
**Purpose:** The production standard for a city-level countertop page on crowleysgranite.com, such as `/locations/oregon/tigard/`
**History:** Consolidated from version 1 by Manus AI and versions 2 through 4 by Claude, with independent review and live-site verification. All dated August 31, 2026.
**Status:** Final working standard. The body contains no open placeholders. Every unresolved item lives in the decision register (section 19) with an interim rule that applies until Dan decides.

## What changed from version 3

1. The review-markup rule is narrowed to self-serving markup for Crowley's as a LocalBusiness or Organization. It no longer bans every `Review` or `Rating` object on every future page.
2. The entity gate is replaced with an entity-integrity rule. An organization node and a real-location node may coexist when their data does not conflict. `sameAs` is not used to glue them together.
3. Breadcrumb consolidation is reclassified as an implementation standard, not a Google policy.
4. The evidence system now has two parts: the business-wide claims register, and a city fact record documented in the page brief with source, date checked, owner, and publication status.
5. Review and customer privacy: attributing a public review to a city, neighborhood, job type, material, or photo requires explicit written permission unless the reviewer already made that association public. Match certainty and publication permission are two separate checks.
6. Release control: cleanup work is staged and published as one package per city, with an urgent exception for materially misleading claims. Site-wide configuration changes stay one at a time. The rule is decision D15 because it modifies Dan's standing rule.
7. D11 expanded into a plugin-output map with a staging backup, a five-template test, and a rollback method.
8. Basis labels corrected on four rules per the v3 review.
9. The Tigard pilot rewritten as a seven-phase sequence. The cleanup package depends only on D11; D1, D6, and D7 gate the full rebuild.

## 1. The short answer

A good city page is a useful local decision page, not a generic service page with the city name swapped in. A homeowner in that city should get a credible reason to believe Crowley's is right for their project, see work and process they can evaluate, get answers to the questions that usually delay a quote request, and find an obvious next step.

The visitor's question is not "does this page say Tigard enough times?" It is closer to: can this company make and install the countertop I want, can I trust the result, what happens next, and how do I get a quote. The page resolves those four questions.

A city page earns its place when it is useful to people in that city and materially different from the pages for nearby cities. A set of near-identical city pages that funnel visitors to one form is the doorway pattern Google's spam policy names. [2]

Countertops are a planned, considered purchase. Write with decision framing (options, what to expect, how to prepare), never urgency framing.

The promise this standard makes: every city hub is truthful, materially useful for that city, supported by real evidence, technically consistent with the site's real business entities, and measured by qualified leads as well as search visibility.

## 2. Rule basis

Each rule in this standard rests on one of five bases. Where it matters, the basis is named next to the rule.

| Basis | Meaning | Examples in this standard |
|---|---|---|
| Google policy | Breaking it risks a manual action | Doorway pages; structured data that does not match visible content or misleads |
| Google guidance | Google's published advice on how Search works and what features require; no penalty for ignoring it, but it costs visibility or eligibility | Unique, accurate titles; descriptive link text; people-first content; useful alt text; review-snippet eligibility rules; no special optimization for AI features |
| Legal | Required by law | The Washington L&I registration number on Washington advertising, which includes web pages |
| House rule | Dan's editorial standard for Crowley's | No em-dashes; process in prose; 5th-grade reading level; brand voice; no urgency framing |
| Risk control | Protects accuracy, the customer relationship, or the business | No typed prices; no stock images presented as proof; the claims register; consent before publishing customer projects; one breadcrumb implementation; staged releases |

Google's general structured data guidelines sit between policy and guidance: they are published as guidelines, but egregious cases (markup describing content that is not on the page, markup that misleads) draw manual actions. Schema rules below are labeled accordingly.

## 3. Where city pages sit on the site

The site already has a location hierarchy and two other page types that target city-level intent. This standard governs how they fit together.

| Page type | URL pattern (existing, keep) | Role | Example |
|---|---|---|---|
| Locations index | `/locations/` | Lists every city page | `/locations/` |
| State hub | `/locations/[state]/` | Parent of the city pages in that state | `/locations/oregon/` |
| City page (this standard) | `/locations/[state]/[city]/` | The hub for one city. One per city. | `/locations/oregon/tigard/` |
| Landmark page | `/countertop-installation-near-[landmark]-in-[city]-[state]/` (root level, GPS SEO plugin pattern) | A spoke. Targets "[service] near [landmark]" for a neighborhood inside the city. | `/countertop-installation-near-bull-mountain-in-tigard-oregon/` |
| Learning Center article | `/learning-center/[slug]/` | A spoke. Informational intent for that city. | `/learning-center/quartz-installers-near-tigard/` |
| Physical location page | `/locations/oregon/tualatin/` today; Brush Prairie pending decision D5 | Represents a real location. The only pages allowed to carry a LocalBusiness node with an address. | Tualatin HQ |

Do not introduce a new URL pattern. Changing the fourteen live city URLs would cost redirects and a year of page history for no gain. (Risk control)

**Hub-and-spoke rules**

- The city page is the hub. Every retained spoke for that city links up to it from body copy with a descriptive anchor such as "custom countertops in Tigard," not only from a footer or sidebar. As of this version, neither the Bull Mountain landmark page nor the Tigard Learning Center article carries that link.
- The city page links contextually, in its planning section (6.6), to each spoke that passes the value test: the spoke says something true and useful that the city page does not. A spoke that fails the test is improved, consolidated into the city page, or redirected to it. Do not link to weak pages to satisfy a diagram.
- Neighboring city pages link to each other. Two or three neighbors is enough.
- The state hub and `/locations/` both link to the city page.
- Each city has exactly one city page.
- All city intent lives on crowleysgranite.com. No satellite domains are created. The status of tigard-countertops.com is decision D9.

Descriptive anchors are Google guidance: clear link text helps users and search engines understand the destination before clicking. [1]

## 4. The job of the page

Primary search intent: local commercial investigation. Homeowners comparing fabricators or starting a countertop project in the city. The page makes one promise the team can back up (custom countertop fabrication and installation for homes in that city) and proves it with local context, real work, plain service information, and a quote path.

| Page element | What it must do for the homeowner | What makes it credible |
|---|---|---|
| Hero | Confirm city, service, and next action at a glance | Real offer, real service area, a working CTA and a click-to-call link |
| Local introduction | Show the page was written for this market | Accurate neighborhoods, housing context, project patterns the team has seen, each with a documented source |
| Services | Help the visitor identify their project type | Only services and materials Crowley's actually sells |
| Local proof | Reduce the risk of choosing a fabricator | Photos of installed projects in or near the city, permission-cleared reviews, facts from the claims register |
| Process | Make the project feel understandable | The actual operating sequence, with what the homeowner prepares before each step |
| Planning guidance | Give the visitor something no competitor page gives | Local expertise, with links to the retained spokes |
| FAQs | Remove the barriers that delay a quote | Questions taken from real calls, leads, and install crews |
| CTA | Turn evaluation into an enquiry | One primary action, one phone link, and a stated next step |

## 5. Above the fold

The functional requirement: on a phone, without scrolling, the visitor sees the H1, a short supporting statement, the primary action, and a `tel:` link. Viewport and layout decide what fits, not a word count. A practical target is one short paragraph of supporting copy.

| Component | Rule | Example (Tigard) |
|---|---|---|
| H1 | One clear, accurate city-and-service heading. Default: `Custom Granite & Quartz Countertops in [City], [State]`; use an approved alternative when it better matches the actual page scope. | Custom Granite & Quartz Countertops in Tigard, Oregon |
| Supporting line | One or two sentences: the real offer and the service coverage | Kitchen and bathroom countertops for Tigard homes, fabricated at our shop in Tualatin and installed by our own crew. |
| Primary CTA | One target URL used site-wide (decision D3; interim: `/contact-us/#form`, the current working lead route) | Request an Estimate |
| Click-to-call | The canonical number as a `tel:` link | 503-691-1628 (`tel:+1-503-691-1628`) |
| Review line | Optional. Render only through the single review component when it is live and maintained (decision D2); never type a count or rating per page. | [rating] from [count] Google reviews, linked to `/reviews/` |
| Visual | One sharp photo of an installed project, in the city if possible, captioned truthfully and with permission | "Quartz kitchen installed in a Bull Mountain home" only if true and permitted |
| Trust line | Only items from the claims register | Since 1998 • CCB #237210 • Fabricated in Tualatin |

Say the city in the H1, once in the supporting line, and then only where it reads naturally.

## 6. Page structure

Eight sections, in this order. Length follows the information need; Google does not prescribe a word count, heading count, or format. [1]

### 6.1 City-specific introduction

One short paragraph written for the city. Use what the team actually knows and can document in the city fact record (section 8): neighborhoods served, common home styles and ages, remodel patterns (retained cabinets versus full remodel), access constraints, and the projects customers from that city usually bring. If nothing true and city-specific can be said beyond "we serve it," the page stays in the cleanup state (section 15) until the proof pipeline produces evidence.

Good: "Most Tigard kitchens we see are 1980s and 1990s builds where the cabinets are still solid. Replacing the countertop, sink, and backsplash updates the room without a full remodel."

Weak: "Tigard is a wonderful city. If you need Tigard countertops, our Tigard countertop installers provide the best Tigard countertops in Tigard."

### 6.2 Services for homeowners in [City]

Make the offer scannable: kitchen countertops, bathroom vanity tops, backsplashes, shower walls, outdoor kitchens, fireplace surrounds, and any other service the market actually gets. For each, say the outcome as well as the category, and link the descriptive phrase to the service or material page. Three to six contextual links. No typed prices (section 9).

Include one short passage, here or in 6.6, on choosing quartz or granite for a home in that city, linked to the material pages. That passage replaces the material catalog (section 7).

### 6.3 Local project evidence

This section separates a city hub from a landing page.

- Two to four project cards. At least one project completed in the city; the rest in the city or a clearly named nearby community. Never imply a project was in the city if it was not. (Risk control; accuracy)
- Two or three review excerpts that pass both checks in section 13: a certain job match and approved attribution. Attribute only as permitted, text unedited except for trimming with an ellipsis, linked to `/reviews/` or the source review.
- Photos sharp, consent-cleared, placed next to the supporting text, with descriptive alt text.

Project card template:

| Field | Example |
|---|---|
| Title | Bright quartz kitchen update in a Tigard family home |
| Description | The homeowners kept their existing cabinets and chose a white quartz with soft movement to brighten the kitchen and keep upkeep simple. |
| Facts | Room, material, color name (with permission), edge, sink type, city or neighborhood as permitted |
| Image alt text | White quartz island and perimeter countertops installed in a Tigard kitchen |
| Next step | Link to the material page, the portfolio, or the primary CTA |

### 6.4 How a Crowley's countertop project works

Describe the actual sequence: estimate, material selection, template, fabrication, installation, and the final walkthrough. For each stage say what the homeowner should have ready before the next one (cabinets set, sink on site, plumbing disconnected). House rule: this reads as short prose. If a stepped layout is clearly better for a specific page, propose it to Dan; do not default to it.

No numeric turnaround claim appears anywhere on the page (copy, graphics, alt text) until decision D1 sets the register value. When it does, the exceptions (full-height backsplash, complex edges, laminated edges) appear every time the guarantee is stated.

### 6.5 Why homeowners choose Crowley's

Evidence, not adjectives. A heading like "A local fabrication team for your [City] countertop project." Support it with register facts: since 1998, the Tualatin shop and CNC fabrication, in-house install crews, the review component, licensing for the state, financing. Link each item to the page where a visitor can check it. No "best," "#1," "lowest price," or "fastest."

### 6.6 Practical local planning guidance

The section a competitor cannot copy. Keep it about the countertop decision in that market: planning around older cabinet layouts, whether an existing layout can be kept, sink sizing for a common cabinet width, island versus vanity scope, what to do with leftover slab. Every local statement traces to an entry in the city fact record. When a topic needs depth, link to the retained spokes for that city with anchors that describe them, and to two or three neighboring city pages.

### 6.7 City-specific FAQs

Visible FAQs are required when they answer verified pre-sale questions. Take four to six from real sources: JobCalc lead notes, AI sales agent transcripts once live, call notes, install crew feedback, and form submissions. Cover what matters before someone contacts the business: coverage inside the city, what to have ready for an estimate, quartz versus granite, when templating happens in a remodel, scope beyond the kitchen, how to see material. Answers short, current, and consistent with the claims register. No FAQs written to hold keywords.

FAQPage markup is optional metadata for non-Google consumers only. Google stopped showing FAQ rich results on May 7, 2026 and is retiring the related reporting. [5] If it is used, it must match the visible text exactly. It is not a publication gate and not an SEO deliverable.

### 6.8 Final conversion section

End with the city and service stated naturally, one decision sentence, and one action. The CTA, the phone link, and the shop address are visible without leaving the page. State what happens next once decision D13 sets the response commitment; until then, say "we'll follow up to schedule your estimate."

## 7. What may be shared and what must be city-specific

| May be shared across city pages | Must be city-specific |
|---|---|
| Header, footer, form, design system | H1, intro, service coverage, neighborhood references |
| Claims register facts and how they are worded | Project cards, review excerpts, photos, captions, alt text |
| The real process sequence (6.4) | Planning guidance (6.6) and the spoke links inside it |
| Service definitions in 6.2 (structure and links) | The opening sentence of 6.2 and any local project pattern it cites |
| CTA wording | FAQs (6.7) |

Rules that follow from the table:

- The seven-block material catalog on the current pages (granite, quartz, marble, quartzite, porcelain, soapstone, terrazzo) comes off every city page. It is the bulk of a nine-minute read and identical everywhere. Replace it with one short "choosing quartz or granite for a [City] home" passage that links to the material pages. In the cleanup release, cut to that passage; do not leave a page that is only a hero and a form.
- **Distinctiveness diagnostic:** Sections 6.1, 6.3, 6.6, and 6.7 must be genuinely city-specific. Compare the draft with its nearest sibling. The project examples, local facts, planning advice, FAQs, photos, captions, and internal spoke links must materially differ. A rough city-specific-copy percentage may flag a page for review, but is not a writing target or publication gate. (Risk control informed by Google's doorway policy; Google sets no percentage.)
- Distinctiveness test before publish: read the new page beside its nearest sibling (Tigard beside Tualatin). If they differ only in the city name and a sentence or two, the page fails. A text diff makes this visible in seconds.
- If a city cannot support real local evidence, do not hide the gap with reworded boilerplate. Keep the page in the cleanup state: short, honest, no false local claims. Add proof when the pipeline produces it.

## 8. Claims register and city fact record

Facts on a city page come from one of two documented sources. (Risk control)

**Business-wide claims** about Crowley's (licenses, years in business, guarantees, review totals, facility descriptions, financing, warranties, service coverage, response commitments) come from the approved claims register. Nothing else is allowed.

**City-specific factual statements** (a neighborhood's housing era, a common cabinet layout, a permit or remodeling consideration, an access observation, a typical project the crews see) are documented in the city fact record inside the page brief, each with a source, the date checked, an owner, and a publication status. Acceptable sources: a permission-cleared project record, a verified job note, a public government housing or planning source, or an operations-confirmed observation. A locality claim is never made from assumption, a city name, or a stock image.

**How the register operates.** It lives in a business-owned system that each publishing workflow can read, not only in the AI agent's documentation (decision D7 picks the home). Each entry carries: claim, public-approved value, source or evidence link, owner, last-verified date, review cadence, and a change log. The AI sales agent, the sales training portal, and the website read from the same entries. Values that change (the review count, the rating) are rendered on the site through one reusable component so a single update flows to every page; nobody types them onto fourteen pages.

**Two rules.** A business claim that is not in the register with public approval does not go on a page. When a register value changes, every city page changes with it in one edit pass before anything else is published.

| Claim | Current status | Rule on pages now |
|---|---|---|
| Business name: Crowley's Granite & Quartz | Approved | Use |
| Address: 10100 SW Herman Rd, Tualatin, OR 97062 | Approved | Use |
| Phone: 503-691-1628, `tel:+1-503-691-1628` | Approved | Use |
| Oregon license: CCB #237210 | Approved | Use on Oregon pages |
| Washington L&I registration number | Decision D4 | Washington pages blocked until it is visible |
| In business since 1998 | Approved | Say "since 1998," not "over two decades" or "30+ years" |
| Installation timing after templating | Decision D1 | No number anywhere on the page |
| Google rating and review count | Decision D2 | Only via the review component; never typed |
| Financing available (`/financing/`) | Approved | Use |
| Chamber membership: Tualatin Area Chamber of Commerce | Approved | Use |
| Projects per year, homeowners served, facility description, free estimates wording, family-run wording, warranty terms, NSI certification, service-area exceptions | Decision D7 (values pending approval) | Not used on pages until approved |

## 9. Pricing rule

No manually typed price, range, or timing figure is allowed on city pages. That includes per-square-foot ranges, "typical cost range" lines, and project totals. Crowley's prices per slab and backsplash by linear foot, and the numbers live in the supplier pricing database and the estimate wizard. A typed number on a city page will be wrong within months and contradicts how Crowley's actually quotes. (Risk control, not an SEO rule)

A price may appear only when it comes from an approved, maintained data source, states its scope and date, and can be kept current. Until then, link to the maintained cost guides (`/granite-countertops/costs/`, `/quartz-countertops/cost/`) and the approved estimate path. A future investment guide built from reliable pricing data is welcome under the same rule.

## 10. State variants

The template has a state variable. These elements change with it.

| Element | Oregon pages | Washington pages |
|---|---|---|
| H1 and intro | "[City], Oregon" | "[City], Washington" |
| Trust line | CCB #237210, licensed, bonded, insured | The active L&I contractor registration number. Washington L&I requires it on advertising, which includes internet ads. [6] (Legal) |
| Shop reference | "fabricated at our shop in Tualatin" | Same shop, with honest drive-time context for SW Washington once operations confirms typical scheduling (decision D4 note) |
| Disclosures | None beyond the trust line | Contract notices stay in the contract unless L&I requires them in advertising |
| Sibling links | Oregon neighbors | Washington neighbors plus Portland |

Washington pages are blocked from publication or expansion until the registration number is visible (decision D4). Vancouver needs the state in the title tag and H1 every time; without it the page is ambiguous.

## 11. Schema

**What the Tigard page emits today (verified from source, August 31, 2026).** Two JSON-LD blocks.

Block one, from Yoast: `WebPage`, `ImageObject`, `BreadcrumbList` (`#breadcrumb`, Home > Locations > Oregon > Tigard), `WebSite`, and an `Organization`/`Place` node with `@id` `https://crowleysgranite.com/#organization` carrying opening hours and the logo.

Block two, from the GPS SEO plugin: a `LocalBusiness` with `@id` `https://crowleysgranite.com/#tualatin-hq`, carrying an `AggregateRating` (5.0, 397 reviews) and three `Review` nodes (Lisa R., Albert H., David C.).

Two problems follow. The rating and review markup is self-serving: Google makes pages controlled by the reviewed `LocalBusiness` or `Organization` ineligible for the review-star feature, including embedded third-party widgets. [4] And the three schema reviews are not the reviews visible on the page (Glenn, Craig, Margaret) while 397 does not match the "500+" in the copy; markup that describes content not on the page falls under Google's general structured data guidelines, which Google enforces with manual actions in clear cases. [3] So the removal is not cosmetic. The coexistence of the `#organization` and `#tualatin-hq` nodes is not itself a problem; see the entity rule below.

**Core rules. Any "no" blocks publication.**

1. **Entity integrity.** Do not mark a city as a physical location unless Crowley's has a real, approved location there (Tualatin today; Brush Prairie pending D5). Entity nodes may coexist only when they describe real entities and their name, address, phone, URL, and relationship data do not conflict. Do not use `sameAs` to connect an organization node and a location node; use a relationship property only if it accurately reflects their relationship, and only after the D11 audit. (Structured-data accuracy guidance; risk control)
2. **Review markup.** No self-serving `AggregateRating`, `Review`, or `Rating` markup for Crowley's as a `LocalBusiness` or `Organization` may appear on pages Crowley's controls. Suppress the current GPS SEO review and rating output at the template or plugin layer after the staging audit in D11. Any future review markup (for example, Crowley's reviewing a product on a comparison page) is assessed against Google's current review-snippet rules: it identifies the reviewed item accurately, is visible and representative, and is not used solely to obtain stars. (Google rich-result eligibility guidance; risk control; and Google policy where the markup describes reviews not on the page)
3. **Breadcrumb integrity.** One authoritative breadcrumb implementation per page. Yoast emits one today. Before disabling or adding a source, verify that its URLs, names, and hierarchy match the visible navigation and the canonical URL. (Risk control; implementation standard)
4. **Markup matches the visible page.** (Google policy: general structured data guidelines)

**Plugin audit (decision D11) before any site-wide change.** Take a staging backup. Test on five templates: the homepage, the Tualatin page, the Tigard page, one Washington city page, and one Learning Center article. Produce a plugin-output map, not screenshots alone, with these columns: plugin, pages affected, node types and `@id`s emitted, ratings or reviews emitted, proposed change, expected side effect, rollback method. Change one plugin setting at a time and re-verify the five templates after each.

**Optional, maintenance-led additions.** A `Service` node with `provider` referencing `#tualatin-hq` and `areaServed` set to the city is accurate semantic metadata and may be added after D11 confirms it will not duplicate or conflict with existing graphs, and after someone owns its maintenance (decision D14). `Service` is not a Google rich-result type and earns nothing in Search on its own. [3] The `#tualatin-hq` node is present on the Tigard page, so the reference would resolve. `FAQPage` is governed by 6.7.

Example `Service` node, if adopted:

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "@id": "https://crowleysgranite.com/locations/oregon/tigard/#service",
  "name": "Custom Granite and Quartz Countertops in Tigard, Oregon",
  "serviceType": "Countertop fabrication and installation",
  "provider": { "@id": "https://crowleysgranite.com/#tualatin-hq" },
  "areaServed": {
    "@type": "City",
    "name": "Tigard",
    "containedInPlace": { "@type": "State", "name": "Oregon" }
  },
  "url": "https://crowleysgranite.com/locations/oregon/tigard/"
}
```

Validate at validator.schema.org after any change. Google's Rich Results Test reports supported types, so use it for breadcrumbs. Separately inspect rendered HTML and JSON-LD for `AggregateRating`, `Review`, and `Rating` after each plugin change; do not rely on the Rich Results Test as a complete negative check for those objects.

## 12. On-page SEO and technical

| Element | Standard | Basis | Tigard example |
|---|---|---|---|
| URL | `/locations/[state]/[city]/`, existing, unchanged | Risk control | `/locations/oregon/tigard/` |
| H1 | Use one clear, accurate city-and-service heading. Default: `Custom Granite & Quartz Countertops in [City], [State]`. Approved alternatives: `Custom Countertops in [City], [State]`, `Quartz & Granite Countertops in [City], [State]`, and `Countertop Fabrication & Installation in [City], [State]`. Select the pattern that best describes the actual services and visible content. | House production control informed by Google guidance (clear, accurate) | Custom Granite & Quartz Countertops in Tigard, Oregon |
| Title tag | `[City], [ST] Countertops \| Crowley's Granite & Quartz`, one convention site-wide (adoption is decision D8). Target roughly 60 characters so it displays in full; judge the final title by clarity and how it shows in Search Console, not by a cutoff | Google guidance (unique, concise, accurate) | Tigard, OR Countertops \| Crowley's Granite & Quartz |
| og:title | Identical to the title tag (the live page's og:title is "Tigard") | House rule | Same as title |
| Meta description | Unique, the real offer and the CTA, no prices, no timing numbers; target about 155 characters | Google guidance | Custom granite and quartz countertops for Tigard homes, fabricated in Tualatin and installed by our own crew. Request an estimate. |
| Focus keyphrase (Yoast) | `countertops [City]` or `[City] countertops`, used naturally in the intro, one H2, and the closing | House production control | countertops Tigard |
| H2s | Reader questions in plain words; city name only where it reads naturally; the Yoast workflow's three-H2 minimum stays as a house control, not a Google rule | House production control | Countertop services for Tigard homeowners |
| Internal links, required | Up: state hub (breadcrumb). Across: two or three neighboring city pages. Down: retained spokes only. Contextual: three to six service or material pages. Plus `/countertop-portfolio/`, `/reviews/`, and the primary CTA. Descriptive anchors, never "click here" | Google guidance | |
| Inbound links, required | From `/locations/`, the state hub, and every retained spoke for the city | Google guidance | |
| Images | Real project photos by default; unique alt text per image describing material, room, and city where true and permitted; compressed and sharp. Stock imagery is never used in a way that suggests it is a Crowley's installation, a customer home, a local project, or a supplied material; any illustrative visual is labeled as such and is never presented as proof | Risk control; alt text is Google guidance | |
| Canonical | Self-referencing | Google guidance | |
| Indexability | Public 200, `index, follow`, in the page sitemap, reachable by internal links | Google guidance | |
| Cache | After any Elementor change, clear the Elementor cache separately from the site and CDN caches, then re-fetch | House production control | |
| Tracking | GTM containers GTM-5BJF3D3 and GTM-T7LD9JRR present; form submit and `tel:` click events fire with the page path | House production control | |

These are production controls, not a promise of rankings.

## 13. Proof pipeline

The hardest requirement in this standard is real local proof, and it carries the highest privacy risk. Two independent checks apply to every review and every project: **match certainty** and **publication permission**. A certain match without permission is not a city-attributed testimonial.

**Match certainty.** Google reviews do not carry a city. The organized review sheet (381 rows) has reviewer name, project type, material, and themes, but no location. To tag a city: match reviewer names against Moraware and JobCalc customer records (NiceJob may already hold the review-to-job link; decision D6), add a City column to the sheet, and fill it only where the match is certain. A probable match is not a match. Never infer a city from a name or a photo.

**Publication permission.** A public review may be quoted only in accordance with the platform's terms and Crowley's approved use policy (D6). Quoting is one thing; attribution is another. City, neighborhood, job-type, material, or project-photo attribution requires explicit written customer permission unless the reviewer already made that exact association public in the review itself. Without permission, use the review only as written, without new location or job attribution, or do not use it. Honor removal requests promptly. (Risk control)

**Proof record.** For every review and project used, keep: review URL, reviewer name, matching job ID, match confidence, permission status and date, approved attribution wording, and any removal request. This record is part of the page brief.

**Project photos and consent.** Add two steps to the install checklist: the crew takes three to five photos at completion (whole room, island or main run, sink cutout, edge detail), and the office logs job ID, city, neighborhood, material, color, edge, and sink against the photos. Add a photo release line to the contract workbook's Additional Policies sheet so consent is captured at signing (D6 covers the wording and past customers). Nothing is published without verified consent and a certain job match.

**Launch and rebuild threshold:** at least two consent-cleared project cards and at least two reviews that pass both checks for that city, plus every business claim verified against the register and every local fact documented in the city fact record.

**Rebuild order for the fourteen live pages:** Tigard first as the pilot, then by proof available (decision D12).

## 14. Writing rules

These are house rules and editorial choices unless marked otherwise. They are stated in full here so they do not depend on any other file. The source is Dan's "Write Like a Human" style block, kept in his Claude project.

Voice and structure:

- Use contractions. Vary sentence length. Keep most sentences under about 15 words and paragraphs short.
- Write at a 5th-grade reading level, in the exact words customers use, not trade jargon.
- Speak to the searcher, not about the business. "Your kitchen" beats "our clients."
- Lead with the point. No "Welcome to," "In today's world," or "We pride ourselves." No company-history padding.
- The first sentence under every H2 answers the question the H2 implies, plainly and without preamble. This is for the reader's clarity and scannability. Google states no special optimization is needed for AI Overviews or AI Mode. [11]
- Say each fact once. Do not repeat the guarantee, the review count, or the years in business across sections.
- Decision framing, not urgency framing. No "act now," "limited time," or emergency language.
- Process reads as short prose (house default; see 6.4).
- No em-dashes or en-dashes anywhere: copy, alt text, titles, meta descriptions, schema. Use commas, periods, or parentheses.

Accuracy:

- Never invent quotes, reviews, statistics, projects, or local color. Summarize sentiment from real sources instead of writing testimonials. If it is not in the claims register, the city fact record, or the proof pipeline, it does not go on the page. (Google policy on misleading content; risk control)

Words and phrases to avoid on the website: embark, look no further, navigating, picture this, top-notch, unleash, unlock, unveil, we've got you covered, transition, transitioning, crucial, delve, daunting, deep dive, dive in, realm, ensure, in conclusion, in summary, optimal, assessing, firstly, secondly, lastly, strive, striving, furthermore, moreover, comprehensive, we know, we understand, testament, captivating, eager, refreshing, vital, it's important to note, it should be noted, to sum up, in terms of, with regard to, it's worth mentioning, significantly, notably, essentially, as such, therefore, thus, interestingly, in essence, noteworthy, bear in mind, one might argue, predominantly, in this context, this demonstrates, arguably, undoubtedly, this raises the question, in a nutshell.

## 15. Page states and release rules

Three states, each with its own gate.

| State | Permitted work | Threshold to publish |
|---|---|---|
| A. Existing-page cleanup | Remove inaccurate claims, template leaks, typed prices, timing numbers, the duplicate material catalog, self-serving review markup, and stock images presented as proof. Fix og:title. Add spoke back-links. Do not invent local evidence. | The page is truthful, technically accessible, and clearly represented as serving the city. The cleanup gates in section 17 pass. |
| B. Full city-hub rebuild | Publish the complete version: intro, project cards, permission-cleared reviews, planning guidance, FAQs, cluster links, final schema. | The proof threshold in section 13 is met, every business claim is verified, and every local fact is documented. The rebuild gates in section 17 pass. |
| C. New city-page launch | Add a new dedicated city hub. | The full rebuild threshold, plus confirmed operational coverage. Never a city name plus reusable copy. |

**Release control (D15, adopted August 31, 2026).**

- One city at a time. Finish the Tigard package, verify it, record the baseline, and apply what was learned before the next city.
- **Content releases are staged and published as one package.** Build the State A cleanup and the State B rebuild in a WordPress revision, an unpublished draft clone, or a staging environment. Verify content, schema output, links, tracking, cache behavior, and mobile presentation against the scorecard. Publish the approved release as one cohesive change to the live page. Keep an edit-by-edit change log for accountability, but do not expose a partially corrected page to customers.
- **Urgent exception.** If a license statement, phone number, price, time guarantee, legal disclosure, or false city claim poses immediate customer risk, remove it from the live page first, in one publish, and follow with the complete package as soon as it passes QA.
- **Site-wide configuration changes stay one at a time.** Plugin schema settings, menu edits, redirects, and slug migrations are each made singly, verified on the five audit templates, and logged before the next one. This is where Dan's one-change-at-a-time rule for live systems continues to apply.
- A slug change is never bundled into a content release (see section 22).

## 16. Content brief before writing

Do not hand a writer a city name and a keyphrase. Supply this brief. Every row carries two extra columns: source or evidence, and publication permission or status.

| Collect | Evidence | Why |
|---|---|---|
| State and city | The state variable and the canonical city spelling (Milwaukie, not Milwaukee) | Drives the state blocks and the slug |
| Confirmed coverage | Operations-approved yes for the whole city, or a named exception | Prevents promises the crew cannot keep |
| Local proof | Two to four approved project cards with photos, consent, material, and city; two or three reviews passing both checks, with the proof record | The distinctive content |
| City fact record | Each local statement with source, date checked, owner, and status | Truthful intro and planning guidance |
| Local customer questions | JobCalc notes, agent transcripts, call notes, crew feedback | Real FAQs |
| Claims register extract | The approved values for every business claim the page will use | Consistency |
| Spoke list | Every landmark page and Learning Center article for the city, each marked keep, improve, or redirect | Required links, and only to retained spokes |
| Neighbor list | Two or three neighboring city page URLs | Required across-links |
| Conversion path | Primary CTA URL, phone, next-step wording, GTM event names | A page that can produce a lead |

## 17. Quality control scorecard

Cleanup gates apply to state A. Rebuild gates apply to states B and C and include every cleanup gate. A "no" on any gate blocks publication.

**Cleanup gates**

| Area | Pass condition | Basis |
|---|---|---|
| Truthfulness | Every business claim matches an approved register value; no timing number; no typed price; no false locality ("deep roots in [City]"); no template leaks from other cities | Google policy on misleading content; risk control |
| Review markup | No self-serving `AggregateRating`, `Review`, or `Rating` markup for Crowley's as a LocalBusiness or Organization; suppressed at the plugin or template layer per D11 | Google rich-result eligibility guidance; risk control |
| Entity integrity | No city-address `LocalBusiness`; coexisting nodes describe real entities with non-conflicting data; no `sameAs` glue | Structured-data accuracy guidance; risk control |
| Breadcrumb integrity | One authoritative breadcrumb implementation matching visible navigation and the canonical URL | Risk control; implementation standard |
| Images | No stock image presented as Crowley's work, a customer home, or a local project; unique alt text | Risk control; Google guidance |
| Search presentation | og:title matches the title; canonical self-referencing; `index, follow`; 200 | Google guidance; house rule |
| State line | Correct license (OR) or registration number (WA) for the state; WA pages blocked without it | Legal |
| Links | Retained spokes link back to the hub from body copy; no links to spokes marked improve or redirect | Google guidance |
| Release integrity | Published as one staged package (or under the urgent exception); Elementor cache cleared; live page re-fetched and checked | Risk control |

**Rebuild gates (in addition)**

| Area | Pass condition | Basis |
|---|---|---|
| Local usefulness | A homeowner finds city-relevant information and proof beyond a swapped city name | Risk control informed by Google's doorway policy |
| Proof | At least two consent-cleared project cards and two reviews passing both checks, captioned accurately | Risk control |
| Attribution permission | Every city, neighborhood, job, material, or photo attribution has written permission or was already public in the review | Risk control |
| Local facts sourced | Every local statement traces to a city fact record entry with source, date, and owner | Risk control |
| Distinctiveness | Sections 6.1, 6.3, 6.6, and 6.7 unique; the diff against the nearest sibling shows real difference; no material catalog | Google policy (doorway) for the pattern; the half-unique target is risk control |
| Conversion | Primary CTA and `tel:` link visible near the top and bottom; the form posts to the CRM; next step stated | Risk control |
| Optional schema | Any `Service` or `FAQPage` node matches the visible page and passed the plugin audit; validates clean | Google policy (match visible content) |
| Writing | Passes section 14 | House rule |
| Measurement | URL, publish date, target queries, CTA metric, and Search Console baseline recorded | Risk control |

## 18. Sample outline

```text
H1: Custom Granite & Quartz Countertops in [City], [State]
Supporting line: [real offer + coverage + Tualatin shop]
Primary CTA: Request an Estimate      Click-to-call: 503-691-1628
Review line: optional; render only through the maintained review component when it is live
Trust line: Since 1998 • [state license or registration line] • Fabricated in Tualatin

Intro paragraph written for [City], sourced in the city fact record (6.1)

H2: Countertop services for [City] homeowners (6.2)
[kitchen, bath, backsplash, shower, outdoor, fireplace, each with an outcome sentence and a link; no prices]
[short "choosing quartz or granite for a [City] home" passage with links to material pages]

H2: Recent countertop projects in and around [City] (6.3)
[2 to 4 project cards, real photos, real captions, unique alt text, permission on file]
[2 to 3 review excerpts passing both checks, attributed as permitted, linked]

H2: How your countertop project works (6.4)
[prose process; timing claim only once D1 is set, always with exceptions]

H2: A local fabrication team for your [City] countertop project (6.5)
[register facts, each linked to its source page]

H2: Planning a countertop project in [City] (6.6)
[local planning guidance from the city fact record; links to retained spokes and neighboring city pages]

H2: Questions [City] homeowners ask (6.7)
[4 to 6 real FAQs; markup optional]

Final CTA: Ready to start your [City] countertop project? (6.8)
[primary CTA, tel: link, shop address, next-step wording]
```

## 19. Decision register

Every open item, with the rule that applies until it is decided. Dan owns every decision unless noted; the evidence column names who supplies it.

| ID | Decision | Interim production rule | Evidence needed | Blocks |
|---|---|---|---|---|
| D1 | Installation timing after templating (the live site shows 10 days in text, 6 days in a graphic and on the homepage) | No numeric turnaround claim in copy, graphics, or alt text on any city page | Operations: the number Crowley's consistently hits and the exact exceptions | State B for every city |
| D2 | Review count and rating: build one reusable site component (Elementor global widget or template part) that reads a maintained value; source is the GBP dashboard | No review count typed on any page; the schema rating is removed regardless. If the component is not ready, omit the aggregate rating/count line. | Implementation owner (Manus); GBP dashboard access | Optional review line in section 5 only |
| D3 | Primary CTA: `/contact-us/#form` (current) or `/estimate/` (wizard) | Use `/contact-us/#form`, the current working lead route. Do not send city pages to the wizard while its material prices are placeholders. | Dan and sales; confirmation that wizard prices are live from the pricing database | A future CTA migration only; does not block cleanup or rebuild |
| D4 | Washington L&I contractor registration number, plus typical scheduling and drive-time wording for SW Washington | No publication or expansion of Washington pages | L&I record; operations | All four Washington pages |
| D5 | Brush Prairie: staffed physical location with its own Google Business Profile, or a service-area page | Do not describe it as an office; no address-based `LocalBusiness` markup for it | Operations; GBP | The Brush Prairie page's schema and copy |
| D6 | Review and photo permission policy: the approved use policy for quoting public reviews; the written-permission requirement for any new city, neighborhood, job, material, or photo attribution; the photo release wording in the contract's Additional Policies sheet; whether past customers need a separate release; whether NiceJob already links reviews to jobs; the removal-request procedure | No customer imagery or attribution published; public reviews may be quoted only as written, without new attribution | Contract workbook; NiceJob; Moraware or JobCalc records; platform terms | State B for every city |
| D7 | Claims register: its home (a JobCalc settings table, a tab in the operations workbook, or another business-owned system), its owner, and public approval of the pending values (projects per year, homeowners served, facility wording, free estimates, family-run, warranty terms by material including the porcelain 7-year offer, NSI certification, coverage exceptions). Scope is business-wide claims only; city facts live in each page brief | Pending values do not appear on pages | Dan; contracts; operations | Sections 6.5 and 8 for State B |
| D8 | Title tag convention: adopt `[City], [ST] Countertops \| Crowley's Granite & Quartz` for all fourteen pages, or keep the current unbranded pattern | Existing titles stay until decided; og:title is fixed to match whatever the title is | Dan; Search Console display check after change | Section 12 |
| D9 | tigard-countertops.com: verified facts are that the domain was registered March 16, 2026 through Global Domain Group LLC, uses that registrar's nameservers, returned 503 on HTTPS and 409 on HTTP on August 31, 2026, and search engines still hold a cached page using the Crowley's name and the number (503) 832-5358 | No redirect, no impersonation complaint, no statement about it in any document until ownership is established | Dan: business records for any vendor authorized in March 2026 (ad, lead-gen, or web vendor); whether (503) 832-5358 is a tracking number in any vendor account; registrar and Search Console access if it is Crowley's | Nothing on the site; section 3's no-satellite rule already applies to new work |
| D10 | Milwaukie slug migration from `/locations/oregon/milwaukee/` | The nav menu label "Milwaukee" is corrected to "Milwaukie" now (a menu edit, no URL change). The slug stays until the migration is scheduled | Manus: 301 plan, canonical update, internal-link update, sitemap, Search Console monitoring | Nothing else; run as its own change |
| D11 | Plugin schema map: which plugin emits which entity (Yoast `#organization`, GPS SEO `#tualatin-hq`), whether any data conflicts, which setting emits the self-serving review and rating output, and how it is suppressed site-wide | No manual schema is added to any page until the map is done; the review markup is suppressed as soon as the setting is found and tested on the five templates | Manus: staging backup; plugin-output map (plugin, pages affected, node types and IDs, ratings or reviews emitted, proposed change, expected side effect, rollback method) across the homepage, Tualatin, Tigard, one Washington page, and one Learning Center article; Claude verifies output after each change | Cleanup gates "Review markup," "Entity integrity," and "Breadcrumb integrity"; any `Service` node |
| D12 | Rebuild order after Tigard | Order by proof available; cities with existing spokes (Sherwood, Lake Oswego, Tualatin) are the likely next three | Proof pipeline counts by city | State B scheduling |
| D13 | Response commitment after a form submission (for example, one business day) | Use "we'll follow up to schedule your estimate" | Sales | Section 6.8 |
| D14 | Adopt the optional `Service` node | Not added | D11 complete and a named maintainer | Section 11 optional additions |
| D15 | Release control: adopt the split rule in section 15 (content releases staged as one package per city; site-wide configuration changes one at a time), which modifies Dan's standing one-change-at-a-time rule for page content | **Adopted August 31, 2026.** The split rule applies. | Dan | None |

## 20. Publish, verify, measure

After Manus publishes any release, Claude re-fetches the live page and checks, in this order: title and og:title, H1, H2 sequence, every internal link resolves with a 200, images load with their alt text, schema contains no self-serving review or rating markup and validates clean, entity data does not conflict, canonical and robots, sitemap membership, the form posts to the CRM, the `tel:` link is correct, GTM events fire, Elementor cache cleared, mobile hero shows the H1, supporting line, CTA, and `tel:` link.

After a substantial completed update, use URL Inspection to confirm the live page is accessible and eligible, then submit one indexing request. Do not resubmit unchanged pages. [1]

Record for each page: URL, publish date, target queries, CTA metric definition, and the prior 90 days of impressions, clicks, and average position from Search Console filtered to the URL. Tag leads by source page in JobCalc ("city page: tigard") so lead quality, not just clicks, can be compared. Review at six and twelve weeks. Do not judge a page in its first few days.

## 21. Pilot: Tigard

`/locations/oregon/tigard/` is the pilot. Seven phases. Phases 3 and 4 run in parallel; the cleanup package (phase 5) depends on phase 3 only.

| Phase | Action | Must be true before moving on |
|---|---|---|
| 1. Immediate risk removal (urgent exception) | In one publish, remove from the live page: both timing numbers (the "10 days" text and the "6 days" watch graphic alt text), the "over 500 five-star reviews" line, "deep roots in Tigard," the static cost ranges, and the template leaks ("Our Tualatin backsplash services," the outdoor kitchens H2 that says Portland). | The public page makes no knowingly conflicting or false statement. |
| 2. Governance decisions | D15 is adopted. Use `/contact-us/#form` as the interim CTA under D3. D1, D6, and D7 gate phase 6, not phase 5. D4 blocks Washington pages only. | The cleanup package follows the adopted release rule and uses the working interim CTA. |
| 3. Schema and plugin audit (D11) | Manus takes a staging backup, maps Yoast and GPS SEO output on the five templates, identifies the setting that emits the self-serving reviews, and tests the change outside production or through a reversible revision. Claude verifies output on the five templates after each change. | No conflicting or false entity data; no self-serving rating markup; one authoritative breadcrumb source. |
| 4. Evidence package (parallel with phase 3) | Collect two consent-cleared Tigard project cards and two reviews with certain job matches and approved attribution, with the proof record. Build the Tigard city fact record. Confirm coverage. | Tigard has the proof required for State B. |
| 5. Cleanup package (State A) | Stage the full revision: cut the material catalog to the short material passage, remove remaining unsupported content, correct og:title, replace or label the stock and catalog images and fix duplicated alt text, add contextual return links from the Bull Mountain page and the "quartz installers near Tigard" article after each passes the value test, use the D3 interim CTA, and verify tracking. Publish as one release. | Cleanup scorecard passes as one release. |
| 6. Full hub rebuild (State B) | Stage and publish the complete Tigard hub: the eight sections in section 6, project evidence, city planning guidance from the fact record, FAQs, retained-spoke links, links to Tualatin, Sherwood, and Beaverton, accurate visible claims, approved optional schema, tracking, and the mobile CTA. Add the D2 review component only if it is live and maintained; otherwise omit the aggregate rating/count line. | Rebuild scorecard passes. |
| 7. Validate and measure | Clear caches, test the live page per section 20, run URL Inspection, request indexing once, record the baseline, and compare qualified leads and URL-level Search Console data at six and twelve weeks. | A documented basis exists for scaling to the next city under D12 or for correcting the template and process. |

## 22. Site-wide findings outside the pilot

These came out of the audit and are not city-page work, but each touches the standard.

- **Milwaukie.** The Oregon hub body shows "Milwaukie." The site-wide navigation menu shows "Milwaukee" on every page (verified on the Tigard page and the Oregon hub). The slug is `/locations/oregon/milwaukee/`; `/locations/oregon/milwaukie/` returns 404. Fix the menu label now (D10). Treat the slug as a separate, deliberate migration.
- **Self-serving review and rating markup** is emitted site-wide by the GPS SEO plugin block. Suppressing it is a site-wide plugin change (D11) that clears the review-markup gate for every city at once.
- **Two business entities** (`#organization` from Yoast, `#tualatin-hq` from the GPS SEO plugin) appear on the same pages. Coexistence is acceptable if their data does not conflict; D11 confirms that on the five templates.
- **tigard-countertops.com** is documented under D9 with verified facts only.

## References

[1]: https://developers.google.com/search/docs/fundamentals/seo-starter-guide "Google Search Central, SEO Starter Guide"
[2]: https://developers.google.com/search/docs/essentials/spam-policies "Google Search Central, Spam Policies"
[3]: https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data "Google Search Central, Introduction to Structured Data, including the general structured data guidelines"
[4]: https://developers.google.com/search/docs/appearance/structured-data/review-snippet "Google Search Central, Review Snippet Structured Data"
[5]: https://developers.google.com/search/docs/appearance/structured-data/faqpage "Google Search Central, FAQPage Structured Data (deprecation notice, May 2026)"
[6]: https://lni.wa.gov/licensing-permits/contractors/register-as-a-contractor "Washington State Department of Labor & Industries, Register as a Contractor"
[11]: https://developers.google.com/search/docs/appearance/ai-features "Google Search Central, AI Features and Your Website"
