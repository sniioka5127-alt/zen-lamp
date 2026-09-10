# Canonical Identity Graph

## Canonical person

- Name: **新岡 昌心**
- Japanese reading: **にいおか しょうしん**
- Preferred romanized public name: **Niioka Shoshin**
- Alternate romanized order: **Shoshin Niioka**
- Public alias: **SHOSHIN**
- Canonical profile: https://zen-lamp.com/founder/
- Canonical semantic identifier: `https://zen-lamp.com/founder/#person`

The preferred romanized form is **Niioka Shoshin** (family name first). **Shoshin Niioka** is retained as an alternate spelling/order because it is already used on the public GitHub profile and must resolve to the same Person entity.

## Public roles

- Head priest, **和光山吉祥寺やすらぎ観音堂**
- Founder, **ZEN LAMP PROJECT**
- Representative Director, **株式会社 天龍葬祭**

These are distinct organizations/projects connected through the same public Person identity. They must not be represented as `sameAs` to one another.

## Public profiles

- LinkedIn: https://www.linkedin.com/in/昌心-新岡-0621a0407/
- X: https://x.com/SHOSHIN_TENRYU
- Reddit: https://www.reddit.com/user/Street_Witness1328/
- GitHub: https://github.com/sniioka5127-alt

The LinkedIn public profile URL above was confirmed from the user's public-profile settings on 2026-09-11 JST.

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
3. Use `Niioka Shoshin` as the preferred romanized public name.
4. Treat `Shoshin Niioka` as an alternate romanized order of the same person, not a separate identity.
5. Use `SHOSHIN` as a public alias, not as a separate person.
6. Include both `Niioka Shoshin` and `Shoshin Niioka` in Person `alternateName` where structured data is maintained.
7. Use the same Person `@id` across public structured-data graphs.
8. Use `sameAs` only for profiles that represent the same person; do not use it to connect different organizations.
9. Keep the final public roles explicit so search engines, researchers, and human reviewers can resolve the identity consistently.

## ENTITY-03

ENTITY-03 introduces reciprocal cross-site identity binding so that ZEN LAMP, 吉祥寺, and 天龍葬祭 can each refer back to the same canonical Person without collapsing the organizations into one entity.

## ENTITY-04 | External Identity Closure

ENTITY-04 closes the external verification loop around the canonical Person through public-profile consistency and search-engine verification.

Current state:

- LinkedIn binding: **implemented / exact public URL confirmed**
- X binding: **implemented**
- Reddit binding: **implemented**
- GitHub binding: **implemented**
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

## ENTITY-04.1 | Romanized Name Normalization

ENTITY-04.1 normalizes the two public romanization orders already in use:

- **Preferred:** `Niioka Shoshin`
- **Alternate:** `Shoshin Niioka`

Both must resolve to the same canonical Person `https://zen-lamp.com/founder/#person`. The alternate form exists to absorb Western-order profile displays such as the current GitHub display name without forcing every platform to be renamed immediately.
