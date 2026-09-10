# ENTITY-05｜Google Search Entity Verification

## Goal

Verify the public/search-facing evidence that the canonical identity graph is being crawled and can be resolved consistently.

Canonical Person: `https://zen-lamp.com/founder/#person`

Canonical identity variants:
- 新岡 昌心
- にいおか しょうしん
- Niioka Shoshin
- Shoshin Niioka
- SHOSHIN

## Verification boundary

ENTITY-05 does **not** claim access to Google's internal Knowledge Graph or hidden entity-resolution state. It uses observable proxies only: Search Console URL Inspection, crawl freshness, indexability/robots/fetch status, live structured-data presence, Search Console query impressions after data settles, and public-web discoverability.

## URL Inspection baseline — 2026-09-11 JST

### PASS

- `https://zen-lamp.com/`
  - PASS / Submitted and indexed / ALLOWED / INDEXING_ALLOWED / SUCCESSFUL
  - last crawl: `2026-09-11T04:37:56+09:00`
- `https://zen-lamp.com/founder/`
  - PASS / Submitted and indexed / ALLOWED / INDEXING_ALLOWED / SUCCESSFUL
  - last crawl: `2026-09-11T04:35:53+09:00`
- `https://wakouzan-kichijoji.com/`
  - PASS / Submitted and indexed / ALLOWED / INDEXING_ALLOWED / SUCCESSFUL
  - last crawl: `2026-09-11T04:42:19+09:00`

### Pending API evidence

- `https://tenryusosai.com/`
- `https://tenryusosai.com/company/`

Google currently rejects GSC Wizard URL Inspection for the Tenryu property because the connected authorization lacks the full webmasters scope. Manual Search Console recrawl may be complete, but ENTITY-05 does not mark these URLs PASS without API evidence or screenshots showing the new crawl time.

## Search Analytics baseline

Search Console settled data currently runs through `2026-09-08`, before ENTITY-04 / ENTITY-04.1 deployment.

On ZEN LAMP, exact checks for `新岡 昌心`, `新岡昌心`, `にいおか しょうしん`, `Niioka Shoshin`, `Shoshin Niioka`, and `SHOSHIN` currently show zero impressions/clicks in the settled baseline. A regex covering `新岡|にいおか|niioka|shoshin` also returns zero rows for ZEN LAMP and 吉祥寺.

This is a **pre-change baseline, not a failure**. Query data lags and the new identity graph was deployed after the settled window.

## Public-web baseline

Current public-web search already surfaces a 吉祥寺 English page explicitly connecting SHOSHIN, ZEN LAMP PROJECT, Aomori, and human judgment / Roundtable AI.

Exact `site:` searches for the new founder identity variants did not yet return the new founder pages in the current public-web snapshot. Recheck after search propagation.

## Gate decision

**CONDITIONAL PASS — CRAWL/INDEX GATE PASSED FOR 3 CORE URLS; ENTITY-QUERY PROPAGATION PENDING**

Do not promote ENTITY-05 to VERIFIED solely because a page is indexed. Promote only after crawl freshness is confirmed and at least one external/search-facing identity signal is observed after the deployment window.

## Recheck queries

- 新岡 昌心
- 新岡昌心
- にいおか しょうしん
- Niioka Shoshin
- Shoshin Niioka
- SHOSHIN
- 新岡昌心 ZEN LAMP
- 新岡昌心 吉祥寺
- 新岡昌心 天龍葬祭
