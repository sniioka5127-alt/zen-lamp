# ENTITY-04 | External Identity Closure

## Goal

Close the public identity loop around the canonical Person entity for **新岡 昌心（にいおか しょうしん） / SHOSHIN / Niioka Shoshin** so that search engines, researchers, and human reviewers can consistently resolve the same person across ZEN LAMP PROJECT, 和光山吉祥寺やすらぎ観音堂, 株式会社 天龍葬祭, and public profiles.

Canonical Person ID:

`https://zen-lamp.com/founder/#person`

## Scope

ENTITY-04 covers three things:

1. **LinkedIn closure** — add the exact public LinkedIn profile URL to the Person `sameAs` set only after the canonical URL is confirmed.
2. **Google Search Console verification** — inspect and request indexing for the core public URLs after ENTITY-03 deployment.
3. **Google entity verification** — verify that the public pages expose the same name, reading, aliases, roles, canonical profile URL, and reciprocal organization relationships without collapsing distinct organizations into one `sameAs` entity.

## Canonical identity

- Name: `新岡 昌心`
- Japanese reading: `にいおか しょうしん`
- Romanized public name: `Niioka Shoshin`
- Public alias: `SHOSHIN`
- X: `https://x.com/SHOSHIN_TENRYU`
- Reddit: `https://www.reddit.com/user/Street_Witness1328/`
- GitHub: `https://github.com/sniioka5127-alt`
- LinkedIn: **PENDING — exact public profile URL not yet confirmed**

## Core URLs to inspect

1. `https://zen-lamp.com/`
2. `https://zen-lamp.com/founder/`
3. `https://wakouzan-kichijoji.com/`
4. `https://tenryusosai.com/`
5. `https://tenryusosai.com/company/`

## Verification contract

A URL is considered ENTITY-04 ready only when all applicable checks pass:

- HTTP page is publicly reachable.
- Self-canonical is correct.
- Page is not intentionally blocked from indexing.
- Visible text identifies the same public Person where applicable.
- `新岡 昌心` and `にいおか しょうしん` are not contradicted by another reading.
- The canonical Person reference is `https://zen-lamp.com/founder/#person`.
- ZEN LAMP, 吉祥寺, and 天龍葬祭 remain distinct organization entities.
- Organization relationships use `founder`, `employee`/`worksFor`, `member`/`affiliation`, or another appropriate relationship rather than organization-to-organization `sameAs`.
- Person `sameAs` contains only external profiles/home pages representing that same person.
- LinkedIn is not inserted until the exact public profile URL is confirmed.

## Search Console procedure

For each core URL:

1. Open the correct Search Console property.
2. Run URL Inspection on the exact URL.
3. Check the indexed result and the Google-selected canonical.
4. Run **Test Live URL** after the production deployment.
5. Confirm the URL is available to Google and has no blocking indexing error.
6. Request indexing if the page has changed since Google's indexed copy.
7. Re-check later; a request is a crawl request, not a guarantee of indexing or ranking.

For multiple changed pages, submit or refresh the relevant sitemap instead of relying only on repeated single-URL requests.

## Structured-data verification

For `https://zen-lamp.com/founder/`:

- `ProfilePage.mainEntity` must resolve to the canonical Person.
- `Person.name` = `新岡 昌心`.
- `Person.alternateName` includes the confirmed reading, `SHOSHIN`, and `Niioka Shoshin`.
- `Person.sameAs` includes X, Reddit, GitHub, and later LinkedIn after confirmation.
- The profile image URL must remain crawlable.

For the three organization sites:

- Each organization keeps its own stable `@id`.
- The organization links to the same canonical Person ID through a role relationship.

## Current verification state

- ZEN LAMP canonical identity: implemented.
- Japanese reading: confirmed and implemented.
- X binding: implemented.
- Reddit binding: implemented.
- GitHub binding: implemented.
- 吉祥寺 reciprocal binding: prepared/deployed through ENTITY-03 workflow.
- 天龍葬祭 reciprocal binding: prepared/deployed through ENTITY-03 workflow.
- LinkedIn binding: pending exact public URL.
- Search Console live inspection: pending account-connected inspection.
- Google recrawl/index update: pending Search Console request and Google's processing.

## Important limitation

Structured data and reciprocal links improve machine-readable consistency, but they do not guarantee a Knowledge Panel, ranking, indexing, or contact from any company. ENTITY-04 is an identity-resolution and verification layer, not a ranking guarantee.
