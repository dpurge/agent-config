# Translation section

The Polish translation of the adapted text, wrapped in the
`<Translation>` component.

## Shape

```mdx
<Translation lang="pol" script="latn">

## <Polish heading>

<Polish paragraphs.>

</Translation>
```

## Rules

- `lang="pol" script="latn"` — always, when writing in the default
  Polish locale of the repo. (For the English mirror file you write
  `lang="eng" script="latn"` — see `references/english-i18n.md`.)
- Translate paragraph-for-paragraph. Keep the same number and order of
  paragraphs as the foreign-language `<Text>`.
- The heading translates the foreign-language heading.
- Use **real Polish letters**: `ą ę ć ł ń ó ś ź ż`. Don't strip
  diacritics.
- Use Polish-style quotation marks `„...”` for direct quotes.
- Keep proper nouns spelled correctly in Polish (transliterate from
  the foreign-script form when necessary).
- Don't add commentary or notes that aren't in the source.

## Example

```mdx
<Translation lang="pol" script="latn">

## Dlaczego wezbrała rzeka Eufrat w Syrii?

Fāyiz ʿAbbās, przewodniczący komisji ds. sytuacji nadzwyczajnych w
Dajr az-Zaur, powiedział, że region minął etap zagrożenia po
podniesieniu się poziomu wód w rzece Eufrat.

</Translation>
```
