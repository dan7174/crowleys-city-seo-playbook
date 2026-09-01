# City Page Build Checklist

**Use:** Required pre-publication control for Crowley’s Granite & Quartz city pages.  
**Source standard:** [City Page Standard](city-page-standard.md), finalized August 31, 2026.  
**Rule:** Select the correct release state. A page may not move to the next state until every applicable gate is complete.

> **Purpose:** A city page must be a useful, truthful local decision page with an obvious path to an estimate. It is not a city-name-swapped template or a keyword-placement exercise.

## 1. Select the release state

| State | Use when | Minimum outcome |
|---|---|---|
| **A. Existing-page cleanup** | A live city page has inaccurate, stale, templated, or misleading content but does not yet have enough approved local proof for a full rebuild. | A short, honest, technically sound page that accurately states Crowley’s service coverage. |
| **B. Full city-hub rebuild** | The city has the full evidence package and approved business/local facts. | A distinct city hub with real projects, permitted reviews, local planning information, FAQs, useful links, and a clear conversion route. |
| **C. New city launch** | A new dedicated city page is proposed. | The same proof and quality bar as State B, plus operations-approved coverage. |

## 2. Universal pre-build controls

Complete before changing any city page.

- [ ] **Coverage is approved.** Operations confirms Crowley’s serves the city and identifies any exceptions.
- [ ] **Correct entity state.** The city is not presented as a staffed office or business address unless it is a verified physical Crowley’s location.
- [ ] **Correct state requirements.** Oregon pages carry only approved Oregon trust/registration information. Washington pages are blocked until the active L&I contractor registration number is visible.
- [ ] **Business claims are approved.** Every business-wide claim comes from the claims register and has a source, owner, last-verified date, and publication approval.
- [ ] **Local facts are sourced.** Every city-specific statement has a record in the city fact brief, including source, date checked, owner, and publication status.
- [ ] **CTA route is correct.** Use `/contact-us/#form` until a future estimate-wizard route is confirmed live, accurately priced, and approved.
- [ ] **No unapproved “free” claim.** Use **Request an Estimate**, not “Free Estimate,” unless the claims register explicitly approves the offer wording.
- [ ] **No manually typed price, range, or turnaround number.** Only use approved maintained data; otherwise link to the approved cost guidance or estimate route.

## 3. State A: existing-page cleanup gates

Use these gates to correct a live page without waiting for the full local-proof package.

### Truth and content

- [ ] Remove stale, conflicting, or unsupported promises, especially turnaround, review-count, warranty, and locality claims.
- [ ] Remove template leaks from other cities, services, or states.
- [ ] Remove manually typed prices, typical ranges, and project totals.
- [ ] Remove or reduce repeated city-name boilerplate and shared material catalogs; leave a useful short material-selection passage with relevant links.
- [ ] Remove stock images presented as Crowley’s work, a customer home, local work, or supplied material. Clearly label any remaining illustrative image.
- [ ] Ensure all visible claims are supported by the claims register or city fact record.

### Technical and structural

- [ ] Keep the established canonical URL pattern: `/locations/[state]/[city]/`.
- [ ] Confirm a public `200` response, self-referencing canonical, and intended `index, follow` state.
- [ ] Confirm one authoritative breadcrumb path that matches visible navigation and the canonical URL.
- [ ] Confirm no fake city-address `LocalBusiness` markup.
- [ ] Confirm no self-serving `AggregateRating`, `Review`, or `Rating` markup for Crowley’s as a `LocalBusiness` or `Organization`.
- [ ] Fix `og:title` to match the active title tag.
- [ ] Confirm the H1, CTA, and `tel:+1-503-691-1628` link are readily available on mobile.
- [ ] Retain or add only contextual links to valuable landmark pages and Learning Center articles. Do not link to weak spokes just to satisfy a link count.
- [ ] Confirm each retained spoke contains a descriptive in-body link back to the city hub.

### Release control

- [ ] Build the cleanup in a WordPress revision, unpublished clone, or staging environment.
- [ ] Inspect the rendered page, source/JSON-LD, links, mobile layout, form path, and tracking before publication.
- [ ] Publish the State A cleanup as one cohesive city release, unless an urgent inaccurate or legal claim requires immediate removal.
- [ ] Clear Elementor, site, and CDN caches; re-fetch the live page after publishing.

## 4. State B/C: full city-hub evidence gates

State B and new State C pages must pass every State A gate **plus** every item below.

### Evidence package

- [ ] At least **two consent-cleared project cards** are available, with a certain job match, accurate city/nearby-area attribution, and approved project details.
- [ ] At least **two reviews** have both a certain job match and approved attribution. A public review alone does not authorize adding a city, neighborhood, material, job, or photo association.
- [ ] Each proof record includes the project/review URL or asset, job ID, match confidence, permission status/date, approved attribution, and removal-request status.
- [ ] Project photos are sharp, rights-cleared, accurately captioned, and have distinct descriptive alt text.
- [ ] The city fact record supports every local planning, housing, access, or project-pattern statement.

### Distinct, useful page content

- [ ] One H1 clearly and accurately identifies the city and actual service scope. Default: `Custom Granite & Quartz Countertops in [City], [State]`. Approved alternatives are `Custom Countertops in [City], [State]`, `Quartz & Granite Countertops in [City], [State]`, or `Countertop Fabrication & Installation in [City], [State]`.
- [ ] The hero includes a short supporting statement, primary CTA, and click-to-call link. Add an aggregate review line only if the maintained dynamic component is live; never type a count or rating manually.
- [ ] The city introduction uses sourced local knowledge, not generic city praise.
- [ ] The service section describes only services actually offered in the city and links naturally to helpful service/material pages.
- [ ] The local-project section shows the approved projects and permitted review excerpts.
- [ ] The process is accurate, concise, and uses only approved business claims.
- [ ] The planning section offers sourced local value and links to retained city spokes and two or three relevant neighboring city pages.
- [ ] Four to six visible FAQs answer verified pre-sale questions. Do not write FAQs to insert keywords.
- [ ] The final CTA states the next step truthfully. Until a response-time commitment is approved, use “We’ll follow up to schedule your estimate.”
- [ ] Compare the page with its nearest city sibling. Local projects, facts, planning guidance, FAQs, images, captions, and spoke links must materially differ. A percentage of unique copy can flag review, but is never a writing target.

## 5. Schema and plugin controls

- [ ] Before changing plugins, create a backup and map output across the homepage, Tualatin page, target city page, one Washington page, and one Learning Center article.
- [ ] The plugin-output map records: plugin, pages affected, node types/`@id`s, review/rating output, proposed setting change, expected side effect, and rollback method.
- [ ] Make and verify site-wide plugin changes one at a time across all five templates.
- [ ] Coexisting Organization and real-location LocalBusiness nodes must describe real entities and have non-conflicting name, address, phone, URL, and relationship data.
- [ ] Do not use `sameAs` simply to join an organization node and a physical-location node.
- [ ] Optional `Service` or `FAQPage` markup must match visible content, pass the plugin audit, and have a named maintainer. Neither is a Google rich-result or publication requirement for city pages.
- [ ] Inspect the rendered HTML/JSON-LD directly for `AggregateRating`, `Review`, and `Rating`; do not rely on the Rich Results Test as a complete negative check.
- [ ] Validate the final graph in Schema Markup Validator. Use Google’s Rich Results Test for supported features such as breadcrumbs.

## 6. Publish and measure

- [ ] Verify live title tag, og:title, H1, headings, canonical, robots state, sitemap inclusion, images/alt text, and all internal links.
- [ ] Verify the chosen form route reaches the CRM, the `tel:` link is correct, and form/call events capture the page path.
- [ ] Record the URL, release date, release state, target queries, CTA definition, and the prior 90-day URL-level Search Console baseline.
- [ ] After the completed change is live and eligible, inspect the URL in Search Console and submit **one** indexing request if appropriate. Do not repeatedly resubmit an unchanged page. [1]
- [ ] Review Search Console impressions, clicks, queries, and qualified leads from the source page at **six** and **twelve weeks**.
- [ ] Decide whether to repair the process/template or proceed to the next city only after the pilot evidence is reviewed.

## References

[1]: https://developers.google.com/search/docs/fundamentals/seo-starter-guide?hl=en "Google Search Central — Search Engine Optimization (SEO) Starter Guide"
