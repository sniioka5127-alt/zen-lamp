# ENTITY-04.1｜Romanized Name Normalization

## Objective

Prevent the two public romanization orders already in use from being interpreted as different people.

## Canonical identity

- Japanese name: `新岡 昌心`
- Confirmed reading: `にいおか しょうしん`
- Preferred romanized public name: `Niioka Shoshin`
- Alternate romanized order: `Shoshin Niioka`
- Public alias: `SHOSHIN`
- Canonical Person ID: `https://zen-lamp.com/founder/#person`

## Structured-data rule

Where a canonical `Person` node is published, keep:

```json
{
  "@type": "Person",
  "@id": "https://zen-lamp.com/founder/#person",
  "name": "新岡 昌心",
  "alternateName": [
    "にいおか しょうしん",
    "Niioka Shoshin",
    "Shoshin Niioka",
    "SHOSHIN"
  ]
}
```

Existing public handles may remain as additional aliases.

## Display policy

Public ZEN LAMP pages should prefer `Niioka Shoshin` when an English romanization is shown. Existing third-party profiles that display `Shoshin Niioka` do not need to be renamed solely for consistency; the alternate form is deliberately absorbed into the same Person entity.

## Search verification queries

After recrawl, check both forms separately:

- `"Niioka Shoshin"`
- `"Shoshin Niioka"`
- `"新岡 昌心" "Niioka Shoshin"`
- `"新岡 昌心" "Shoshin Niioka"`
- `"SHOSHIN" "ZEN LAMP"`

The target state is not identical rankings. The target is identity resolution: both romanized orders should lead a human or search system back to the same canonical founder profile.

## Non-goals

ENTITY-04.1 does not guarantee ranking, indexing, Knowledge Panel creation, or discovery by a specific company. It only removes an avoidable ambiguity in the public identity graph.
