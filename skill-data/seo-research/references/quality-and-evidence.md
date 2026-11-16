# Evidence, scoring, and data quality

## Evidence standard

For every recommended prospect, retain first-party URLs wherever possible:
- Site homepage or directory homepage.
- Specific guidelines, contributor, listing, or eligibility page.
- Specific contact or existing business listing page when relevant.

Capture a concise note describing what was actually observed. Keep quoted text brief and do not reproduce full pages. Record the date checked. If a source is inaccessible, say so instead of filling the gap with a search snippet.

Use these labels:
- **Observed:** directly visible on a first-party page.
- **Third-party reported:** supplied by a named external source; cite that source and date.
- **Inferred:** a cautious conclusion based on stated evidence; explain the reasoning.
- **Unknown:** not established by the available evidence.

Do not treat a website's own marketing claims as independently verified facts.

## Prioritization score

When helpful, calculate a transparent 0–100 priority score:
- Topical or geographic fit: 0–30.
- Editorial/listing legitimacy: 0–25.
- Audience or local utility: 0–20.
- Transparency and trust signals: 0–15.
- Clear, usable opportunity: 0–10.

For guest-post prospects, "opportunity" means a current, understandable contributor route. For citations, it means a relevant, eligible listing route. Show the component scores and one-sentence rationale. If evidence is missing, lower confidence and state that rather than giving a falsely precise score.

Keep risk flags separate from the numerical score. An explicit link-selling scheme, false listing eligibility, misleading address requirements, or clear spam behavior can make a prospect unsuitable regardless of its score.

## Domain and record deduplication

For domains:
1. Lowercase the hostname.
2. Remove the scheme, username/password, default port, fragment, query, and trailing path for domain comparison.
3. Remove a leading `www.` for comparison.
4. Preserve meaningful subdomains in the raw record; do not automatically merge a subdomain with its parent unless it is clearly the same publisher/property.
5. Compare canonical domains against the source list and tracker.

For businesses/listings, compare name, address, phone, website, and profile URL. Use a multi-field match and mark uncertain matches for human review. Similar business names alone are not sufficient.

When an outreach tracker and existing Gmail drafts/sent records are in scope and authorized, compare both the prospect domain and recipient email before preparing another draft. Do not create duplicate outreach.

## Output format

Prefer a compact table for review and CSV/JSON for handoff. Keep one row per domain or distinct listing opportunity. Recommended columns:
- `prospect_name`
- `canonical_domain_or_listing_url`
- `opportunity_type`
- `topic_or_geography`
- `evidence_urls`
- `evidence_note`
- `checked_at`
- `eligibility`
- `cost_status`
- `priority_score`
- `confidence`
- `duplicate_status`
- `risk_flags`
- `next_action`

Use ISO 8601 dates. Preserve source values separately from normalized comparison values. Do not silently drop rejected or uncertain candidates when the user asks for an audit; label them clearly.

## Quality gate before delivery

- Every recommended record has at least one working evidence URL.
- Every claimed guideline, fee, or eligibility condition has first-party evidence.
- No unverified metric is presented as fact.
- Duplicate checks are described with their scope and limitations.
- Paid opportunities are clearly distinguished from free/editorial ones.
- Missing information is marked unknown.
- No submission, contact, account creation, payment, or listing change is implied to have occurred unless it actually did and was authorized.
