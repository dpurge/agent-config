---
name: phraseforge
description: Write a language lesson (MDX file) from a source text, URL, or local file. Use whenever the user asks to create, generate, write, or adapt a lesson for phrasefoge-web project; or pastes/links a text and asks for vocabulary + exercises; or mentions phraseforge, phraseforge-web, docs/<lang>/<level>/<date>-<seq>.mdx.
---

# PhraseForge lesson author

You write a single MDX lesson file for the **PhraseForge** Docusaurus repo at
`phraseforge-web`. Each lesson teaches a short
adapted text in a foreign language, with vocabulary, models, transcription
(when needed), Polish translation, and exercises.

Lesson text and explanations are **in Polish by default**. If the user asks
for an English copy, also write an i18n mirror — see `references/english-i18n.md`.

## When invoked

Follow these steps **in order**. Don't skip steps.

1. **Get the source** the user supplied:
   - Inline text → use directly.
   - URL → fetch it (read the body, strip nav/ads).
   - File path → read the file.
2. **Detect the foreign language** of the source. Map it to the 3-letter
   ISO 639-3 code used in this repo. See `references/languages.md`.
3. **Detect the script** of that language. Map it to the 4-letter ISO 15924
   code (lowercase). See `references/languages.md`.
4. **Pick the level**. The user usually says `A1`, `A2`, `B1`, `B2`, `C1`,
   `C2`. If unsure, ask. See `references/levels.md`.
5. **Adapt the text** to the chosen level (simplify vocabulary and grammar
   if the source is harder). Keep meaning. Aim for the word counts in
   `references/levels.md`. Result must be a coherent prose text, not bullet
   points.
6. **Pick the lesson file path**:
   `docs/<lang3>/<level>/<YYYY-MM-DD>-<seq>.mdx`
   where `<seq>` is the next free letter (`a`, `b`, `c`…) for that day.
   List the directory first to find what letter is free. Create the
   directory if it doesn't exist.
7. **Write the lesson file**. Sections, in this exact order:
   1. YAML frontmatter (`title:`, `description:`) — see `assets/lesson-template.mdx`.
   2. `# <title in Polish>` heading.
   3. **Vocabulary** code fence — see `references/vocabulary.md`.
   4. **Models** code fence — see `references/models.md`.
   5. **`<Text>`** JSX with the adapted prose — see `references/text.md`.
   6. **`<Transcription>`** JSX — only if the script needs it (non-Latin,
      non-Cyrillic, non-Greek). See `references/transcription.md`.
   7. **`<Translation>`** JSX with the Polish translation —
      see `references/translation.md`.
   8. **Exercises** — at least four, mixing types. Always include
      *translation*, *fill-gaps*, *word-order*, and *multiple-choice*. Add
      others (*matching*, *true-false*, *open-answer*) when the text
      supports them. See `references/exercises.md`.
8. **If the user requested an English copy**: write the i18n mirror at
   `i18n/en/docusaurus-plugin-content-docs/current/<lang3>/<level>/<same-filename>.mdx`.
   See `references/english-i18n.md`.

## Output format

A single `.mdx` file written via the `Write` tool. No prose response other
than a one-line confirmation with the file path. Do not print the lesson
content back to the user.

## Constraints

- Use only the MDX components registered in
  `src/components/LessonElement/`: `<Text>`, `<Transcription>`, `<Translation>`,
  `<Exercise>`, `<Instruction>`, `<L>`, `<N>`, `<Hint>`, `<WordBank>`,
  `<Match>`, `<Column>`, plus the `lesson-vocabulary` / `lesson-models` code
  fences.
- Don't invent new components.
- `lang` is always a 3-letter ISO 639-3 code (`arb`, `cmn`, `deu`, `pol`…).
- `script` is always a 4-letter ISO 15924 code in lowercase (`arab`,
  `hans`, `latn`, `cyrl`, `grek`, `hebr`, `jpan`, `kore`…).
- Lesson `title` and all Polish text use UTF-8 Polish letters (`ą ę ć ł ń
  ó ś ź ż`). Don't strip diacritics.
- Stay concise. Don't add commentary outside the file.

## References

Load only what you need.

- `references/workflow.md` — full step-by-step with examples.
- `references/lesson-file.md` — file path, naming, frontmatter, section order.
- `references/languages.md` — language + script code tables.
- `references/levels.md` — CEFR levels and adaptation targets.
- `references/vocabulary.md` — vocabulary code-fence format.
- `references/models.md` — models code-fence format.
- `references/text.md` — `<Text>` component.
- `references/transcription.md` — when to add, transliteration systems.
- `references/translation.md` — Polish translation block.
- `references/exercises.md` — all 7 exercise types and their components.
- `references/english-i18n.md` — writing the English mirror.
- `assets/lesson-template.mdx` — copy-paste skeleton with placeholders.
