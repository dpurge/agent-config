# Text section

The adapted source text in the foreign language. Wrapped in the
`<Text>` JSX component.

## Shape

```mdx
<Text lang="<lang3>" script="<script>">

## <Heading in the foreign language>

<First paragraph in the foreign language.>

<Second paragraph in the foreign language.>

<More paragraphs as needed.>

</Text>
```

## Rules

- Always start with a level-2 Markdown heading `## <title>` matching the
  text's title in the foreign language.
- Then prose paragraphs separated by blank lines.
- **Blank lines must surround the `<Text>` opening and closing tags** so
  MDX parses the inside as Markdown — like the skeleton above.
- Don't put bullet lists or tables inside `<Text>` unless the source
  text actually has them.
- Use real Polish/foreign-language quotation marks where applicable
  (e.g. „...” for Polish, "..." or « ... » for others).
- Don't add transcription inside `<Text>` — that belongs in
  `<Transcription>`.
- Don't add a Polish translation inside `<Text>` — that belongs in
  `<Translation>`.

## Example (German)

```mdx
<Text lang="deu" script="latn">

## Warum lernt jeder Deutsch?

Deutsch ist eine wichtige Sprache in Europa. Viele Menschen lernen
Deutsch, weil sie in Deutschland arbeiten möchten.

Andere lernen die Sprache, weil sie deutsche Bücher lesen wollen.

</Text>
```

## Example (Arabic)

```mdx
<Text lang="arb" script="arab">

## لماذا فاض نهر الفرات في سوريا؟

فايز عباس، رئيس لجنة الطوارئ في دير الزور، قال إن المنطقة تجاوزت
مرحلة الخطر بعد ارتفاع مياه نهر الفرات.

</Text>
```
