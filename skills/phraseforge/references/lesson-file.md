# Lesson file format

## File path

```
docs/<lang3>/<level>/<YYYY-MM-DD>-<seq>.mdx
```

Example: `docs/arb/a2/2026-06-10-a.mdx`.

`<seq>` starts at `a` and increments for the second, third lesson of the
same day. List the directory before deciding.

## Frontmatter

```yaml
---
title: "<Polish title of the lesson>"
description: "<short description in Polish, often: 'Adaptacja artykułu BBC z YYYY-MM-DD: <source URL>'>"
---
```

`description` is plain prose. If the source has no URL (file/inline), use
a short Polish description without a URL.

## H1 heading

Right after the frontmatter, repeat the title as an H1 heading:

```mdx
# <Polish title of the lesson>
```

## Section order

Always in this order. Skip a section only when noted.

1. `lesson-vocabulary` code fence
2. `lesson-models` code fence
3. `<Text>` JSX
4. `<Transcription>` JSX — **skip** when script is `latn`, `cyrl`, or `grek`.
5. `<Translation>` JSX (Polish)
6. Exercises — at least 4 `<Exercise>` blocks of mixed types.

Separate each section by a single blank line.

## Skeleton

See `assets/lesson-template.mdx` for a copy-paste skeleton with
placeholders marked `<...>`.
