# Public-web SEO release standard

Scope: public foundry marketing and evidence-backed Market Graph pages when actually built and authorized for publication. Studio/Lab demonstrations and user-shared graphs need an explicit visibility/indexing decision; private uploads and dashboards are not search targets. Preserve source-to-snapshot-to-claim provenance and the September 9 founding reset. Never portray a Studio demo, synthetic fixtures or unbuilt 100-company graph as a proven live data business.

## Authority and release use

This is the owner's public-web quality baseline, applied during design, implementation, review and release, not a certificate that existing pages comply. It supplements existing product, evidence, privacy, safety and release authority; it grants no new publication, deployment or data-access permission.

Classify each affected route/template as public and intended for indexing, public but deliberately excluded, or private/staging. Do not optimize private dashboards for discovery or weaken access controls for crawlers.

## SEO by design and during implementation

Before coding a public surface, record its audience/user need, route and indexing decision, data/provenance contract and rendering/component plan in the existing task or PR. Implement these decisions in the same slice as the feature, not as a final SEO retrofit.

1. **Audience and routes:** For a market researcher, explain what the foundry can prove before inviting exploration; define each proposed company page's user question before adding a route. Preserve the distinction between the foundry homepage, /lab/ and /g/* share routes. Plan the canonical origin, duplicate/share handling and indexing class before changing public/_redirects; a fallback HTTP 200 must not disguise missing content.
2. **Content/data contract:** Use source/snapshot/claim identifiers, observation time, uncertainty and permitted public citations as the future page-data contract. Do not derive confident company descriptions from demo rows.
3. **Implementation defaults:** The current implementation is static HTML (index.html, lab/index.html) copied by scripts/build.js, not a shared SEO framework. Put page-specific title/description, semantic content, real anchor navigation and deliberate robots/canonical output in that existing path. Reuse the current page/style conventions; when images are introduced, specify relevant alt text, dimensions and loading behavior there rather than introducing a new stack.
4. **Build and verify together:** Extend test/foundry-routes.test.js alongside route/template work to cover honest development claims, Lab/share routing, missing routes and intended metadata/exclusions. Inspect built HTML and mobile rendering during the slice; the current tests do not certify crawlability or live indexing.

Review evidence at design, implementation and template-test stages; the release checks below are the final confirmation, not the first time SEO is considered. Reuse existing patterns and improve them where evidence shows a gap; referenced code is an integration point, not certification. Do not claim proposed tests or components exist until implemented.

Post-deployment-only observations (actual Google indexing, Search Console coverage and sufficient real-user field data) cannot be prerequisites to the first authorized deployment. Mark them unverified with a responsible follow-up and available pre-release evidence; this does not excuse known policy violations, unsafe exposure or missing checks that can run before release.

### Google eligibility and policies (mandatory for index-target pages)

- Verify Googlebot can access the intended public page, receives HTTP 200 and can see indexable main content; check rendered HTML, resource access and accidental robots/noindex blocks.
- Comply with [Search Essentials](https://developers.google.com/search/docs/essentials), its [technical requirements](https://developers.google.com/search/docs/essentials/technical), and the full [spam policies](https://developers.google.com/search/docs/essentials/spam-policies). Reject cloaking, doorway pages, hidden-keyword/link abuse, link schemes, scaled low-value content, abusive scraping, deceptive redirects and other policy violations. Qualify paid and user-generated links appropriately; prevent publishing spam through submissions.
- AI or templates do not excuse inaccurate claims or pages generated primarily to manipulate search. Do not manufacture reviews, authority, sources or coverage.

### Contextual Google recommendations

Apply the [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) and [helpful-content guidance](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) to relevant public surfaces:

- Serve a real audience with original, useful, accurate content and clear provenance, authorship/review responsibility where appropriate, honest dates, corrections and limitations. Attribution alone does not supply original value.
- Use descriptive, distinct titles, useful headings, accurate summaries/meta descriptions, readable URLs and crawlable links with meaningful text. Make important pages discoverable through navigation.
- Keep internal links, redirects, canonical declarations and any sitemap consistent with intended production URLs. Handle duplicates, filters and pagination deliberately. Sitemaps help discovery; they are not mandatory for eligibility.
- Follow [page-experience guidance](https://developers.google.com/search/docs/appearance/page-experience): usable mobile layouts, HTTPS, accessible content and unobstructed navigation. Measure performance, including Core Web Vitals where data exists; distinguish laboratory diagnostics from real-user field evidence.
- For relevant images, provide contextual placement and useful alternative text; for video-focused pages, provide accessible video and descriptive surrounding information. Use structured data only when appropriate, truthful, visible-content-backed and compliant with the applicable feature guidance; validate it. Do not add media or schema merely to tick a box.
- Use Search Console when available to inspect indexing, search performance, manual actions and regressions. Account setup is a measurement aid, not an eligibility prerequisite.

### Owner quality preference and evidence gate

The owner requires applicable guidance to be addressed before public release, not postponed as marketing cleanup. This review requirement is a project quality preference, not a claim that every recommendation is a Google eligibility rule. No fixed word count, heading count, perfect Lighthouse score, indexation or ranking guarantee is created here.

For the affected templates and representative URLs, add a short release/PR evidence record: revision and environment; intended indexing class; each applicable check; **passed**, **failed**, **unverified**, or **not applicable**; evidence link/output and reason; any remediation owner and next step. Include content/provenance review, response/render/robots checks, canonical/navigation/sitemap consistency, mobile/HTTPS, performance and applicable media/schema checks. Never mark an unrun check passed. Explain non-applicability rather than silently omitting it. Unverified field performance on a new site is not a fabricated pass; record available lab evidence and the follow-up.

Known eligibility/policy violations or unsafe exposure block the affected release. Resolve applicable owner-quality gaps, or record an explicit scoped owner exception under existing release governance; do not silently waive them. A docs-only PR is not a production SEO audit.

Keep staging/preview and private surfaces out of search: use authentication for confidentiality and deliberate noindex where publicly reachable. Robots.txt alone is neither access control nor a reliable noindex mechanism; crawlers must be able to read noindex when that is the chosen exclusion. Recheck exclusions and production canonicals after authorized deployment, and monitor material releases for regressions.

Source review: 2026-10-23. Recheck linked Google guidance when a relevant policy or public-surface change occurs.
