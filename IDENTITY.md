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
