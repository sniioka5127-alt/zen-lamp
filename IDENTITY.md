# Canonical Identity Graph

## Canonical person

- Name: **新岡 昌心**
- Japanese reading: **にいおか しょうしん**
- Romanized public name: **Niioka Shoshin**
- Public alias: **SHOSHIN**
- Canonical profile: https://zen-lamp.com/founder/
- Canonical semantic identifier: `https://zen-lamp.com/founder/#person`

## Public roles

- Head priest, **和光山吉祥寺やすらぎ観音堂**
- Founder, **ZEN LAMP PROJECT**
- Representative Director, **株式会社 天龍葬祭**

These are distinct organizations/projects connected through the same public Person identity. They must not be represented as `sameAs` to one another.

## Public profiles

- X: https://x.com/SHOSHIN_TENRYU
- Reddit: https://www.reddit.com/user/Street_Witness1328/
- GitHub: https://github.com/sniioka5127-alt

LinkedIn is intentionally omitted until the exact public profile URL is confirmed.

## Related public entities

### ZEN LAMP PROJECT

- URL: https://zen-lamp.com/
- Semantic ID: `https://zen-lamp.com/#organization`
- Relationship: founder → canonical Person

### 和光山吉祥寺やすらぎ観音堂

- URL: https://wakouzan-kichijoji.com/
- Semantic ID: `https://wakouzan-kichijoji.com/#organization`
- Type: `BuddhistTemple`
- Relationship: member / affiliation → canonical Person

### 株式会社 天龍葬祭

- URL: https://tenryusosai.com/
- Company page: https://tenryusosai.com/company/
- Semantic ID: `https://tenryusosai.com/#organization`
- Type: `Organization`
- Relationship: employee / worksFor → canonical Person

## Identity rules

1. Use the exact canonical Japanese name `新岡 昌心`.
2. Use the confirmed reading `にいおか しょうしん` where pronunciation is useful.
3. Use `Niioka Shoshin` and `SHOSHIN` as public aliases, not as separate people.
4. Use the same Person `@id` across public structured-data graphs.
5. Use `sameAs` only for profiles that represent the same person; do not use it to connect different organizations.
6. Keep the final public roles explicit so search engines, researchers, and human reviewers can resolve the identity consistently.

## ENTITY-03

ENTITY-03 introduces reciprocal cross-site identity binding so that ZEN LAMP, 吉祥寺, and 天龍葬祭 can each refer back to the same canonical Person without collapsing the organizations into one entity.

## ENTITY-04 | External Identity Closure

ENTITY-04 closes the external verification loop around the canonical Person through public-profile consistency and search-engine verification.

Current state:

- X binding: **implemented**
- Reddit binding: **implemented**
- GitHub binding: **implemented**
- LinkedIn binding: **pending exact public profile URL**
- ZEN LAMP reciprocal identity: **implemented**
- 吉祥寺 reciprocal identity: **implemented / production verification pending**
- 天龍葬祭 reciprocal identity: **implemented / production verification pending**
- Google Search Console URL inspection: **pending connected-account inspection**
- Google recrawl/index refresh: **pending after live verification**

Verification targets:

- https://zen-lamp.com/
- https://zen-lamp.com/founder/
- https://wakouzan-kichijoji.com/
- https://tenryusosai.com/
- https://tenryusosai.com/company/

Search engines may use this graph as one signal among many. Structured data and reciprocal links improve identity resolution but do not guarantee indexing, ranking, a Knowledge Panel, or contact from any company.
