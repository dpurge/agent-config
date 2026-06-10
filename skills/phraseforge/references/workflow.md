# Full workflow

## 1. Get the source

- **Inline text**: the user pasted it. Use as-is.
- **URL**: fetch with the available web/fetch tool. Strip nav, ads,
  cookie banners, "share" buttons. Keep the article body only.
- **File path**: open with `Read`. Same stripping rules.

## 2. Detect language

Look at the text. Identify the language. Map to 3-letter ISO 639-3 code
from `references/languages.md`.

If you cannot decide between two candidates, ask the user.

## 3. Detect script

Most languages map 1:1 to a script (German → `latn`, Ukrainian → `cyrl`,
Arabic → `arab`, Mandarin → `hans`, Japanese → `jpan`). See the table in
`references/languages.md`.

## 4. Pick the CEFR level

Ask the user if not given. Values: `a1`, `a2`, `b1`, `b2`, `c1`, `c2`
(lowercase in the folder path).

Use the word-count targets and grammar guidance in
`references/levels.md` to adapt the source text.

## 5. Decide the lesson file path

Pattern: `docs/<lang3>/<level>/<YYYY-MM-DD>-<seq>.mdx`

- `<lang3>` — the 3-letter language code (lowercase).
- `<level>` — `a1`/`a2`/`b1`/`b2`/`c1`/`c2`.
- `<YYYY-MM-DD>` — today's date.
- `<seq>` — first free letter `a`, `b`, `c`… in the day's series. List
  the directory and pick the next free letter.

Create the directory if missing. If the level directory doesn't have a
`_category_.json`, leave that to the user — don't invent one.

## 6. Adapt the text

- Rewrite the source in the foreign language at the target CEFR level.
- Keep the topic and the gist.
- Replace harder vocabulary with simpler synonyms when the level
  requires it.
- Shorten where the level requires it.
- Preserve proper nouns (names, places, organisations).
- Use plain prose: paragraphs, no bullet lists.

## 7. Build the lesson sections

In this exact order. See the named reference docs for each section's
format. The skeleton in `assets/lesson-template.mdx` shows the layout.

1. Frontmatter (`title:`, `description:` only)
2. `# <Polish title>` heading
3. `lesson-vocabulary` code fence
4. `lesson-models` code fence
5. `<Text lang script>` with the adapted text
6. `<Transcription lang script system>` (only if script is not
   `latn`/`cyrl`/`grek`)
7. `<Translation lang="pol" script="latn">` with the Polish translation
8. Four to seven `<Exercise type lang script>` blocks

## 8. Write the file

Use the `Write` tool. Do not use `Bash` `echo`/`cat` to create files.

## 9. (Optional) English mirror

If the user said "translate to English" or "and English version":
write the same lesson at
`i18n/en/docusaurus-plugin-content-docs/current/<lang3>/<level>/<same-filename>.mdx`
with English in place of Polish for `title`, `description`,
`<Translation lang="eng">`, every `<Instruction>`, every `<N>`, and the
prose translation. See `references/english-i18n.md`.

## 10. Confirm

Reply with a single short sentence naming the file you wrote (and the
English mirror if applicable). Nothing else.
