# Writing the English mirror

Triggered when the user says "translate to English", "also English",
"and the English version", or similar. Don't write it otherwise — the
default lesson is Polish-only.

## File path

The English copy mirrors the Polish path under the `i18n` tree:

```
i18n/en/docusaurus-plugin-content-docs/current/<lang3>/<level>/<same-filename>.mdx
```

Use the **same filename** as the Polish file (same date + same letter).

## What to translate

In the English file, replace these Polish elements with English:

1. **Frontmatter**:
   - `title:` → English title
   - `description:` → English description
2. **`# H1` heading** → English
3. **`lesson-vocabulary` block**: the right-hand side of every `=`
   (the Polish gloss) becomes the English gloss. Headwords and
   transcriptions stay unchanged.
4. **`lesson-models` block**: same — translate only the right-hand side.
5. **`<Text>` block**: unchanged. The foreign-language text stays as-is.
6. **`<Transcription>` block** (if present): unchanged.
7. **`<Translation>`**:
   - Change `lang="pol"` to `lang="eng"`.
   - Replace the Polish prose with the English translation.
8. **Every `<Exercise>` block**:
   - Translate every `<Instruction>` text to English.
   - Translate every `<N>...</N>` prompt to English (it was Polish).
   - Translate the **right column** (`<Column lang="pol" script="latn">`)
     of matching exercises to English: change to
     `<Column lang="eng" script="latn">`.
   - `<Hint>` content stays in the foreign language — don't translate.
   - `<WordBank>` content stays in the foreign language — don't translate.
   - In `true-false`, the `(Правда / Неправда)`-style suffix stays in
     the foreign language.

## Don't change

- `lang` and `script` on `<Exercise>`, `<Text>`, `<Transcription>` (they
  describe the foreign language, not the explanation language).
- The foreign-language content itself.
- Vocabulary headwords and transcriptions.

## Example diff (frontmatter)

Polish:

```yaml
---
title: "Dlaczego wezbrała rzeka Eufrat w Syrii?"
description: "Adaptacja artykułu BBC z 2026-06-03: https://www.bbc.com/arabic/articles/cwy2v0elp8qo"
---
```

English mirror:

```yaml
---
title: "Why did the Euphrates River rise in Syria?"
description: "Adapted from a BBC article from 2026-06-03: https://www.bbc.com/arabic/articles/cwy2v0elp8qo"
---
```
