# Transcription section

A romanized version of the text, wrapped in the `<Transcription>`
component.

**Include only when** the script is **not** `latn`, `cyrl`, or `grek`.
Latin, Cyrillic, and Greek scripts are read directly — no transcription
needed.

## Shape

```mdx
<Transcription lang="<lang3>" script="<script>" system="<system name>">

## <Heading transliterated>

<Paragraphs transliterated.>

</Transcription>
```

The `<Text>` and `<Transcription>` should mirror each other:
- same number of paragraphs
- same heading (just transliterated)
- same sentence boundaries

## Transcription system per script

| Script | `system` attribute    | Notes                                |
| ------ | --------------------- | ------------------------------------ |
| `arab` | `"DIN 31635"`         | Standard German DIN romanization     |
| `hebr` | `"ISO 259"`           | ISO 259 academic transliteration     |
| `syrc` | `"ALA-LC"`            | ALA-LC romanization                  |
| `hans` | `"Hanyu Pinyin"`      | Pinyin with tone marks               |
| `hant` | `"Hanyu Pinyin"`      | Pinyin with tone marks               |
| `jpan` | `"Hepburn"`           | Modified Hepburn                     |
| `kore` | `"Revised Romanization"` | Official South-Korean RR          |
| `armn` | `"BGN/PCGN"`          | BGN/PCGN romanization                |
| `geor` | `"National"`          | Georgian National                    |
| `mong` | `"VPMC"`              | Vertical Pre-Modern Cyrillic         |

If unsure, use the most common Western academic system for that script.

## Example (Arabic, DIN 31635)

```mdx
<Transcription lang="arb" script="arab" system="DIN 31635">

## Limaḏā fāḍa nahru al-Furāt fī Sūriyā?

Fāyiz ʿAbbās, raʾīsu laǧnati aṭ-Ṭawāriʾ fī Dair az-Zūr, qāla inna
al-minṭaqata taǧāwazat marḥalata al-ḫaṭari baʿda irtifāʿi miyāhi nahri
al-Furāt.

</Transcription>
```

## Example (Mandarin, Pinyin)

```mdx
<Transcription lang="cmn" script="hans" system="Hanyu Pinyin">

## Zài Tàikōng Huáiyùn hé Shēngyù Rénlèi: Dài Jiě de Kēxué Wèntí

Hángtiān lǐngyù zhèngzài shíxiàn xǔduō zhòngyào mùbiāo.

</Transcription>
```
