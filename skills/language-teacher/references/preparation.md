# Identify the native language of the user and the foreign languages that the user is learning

The user has mentioned the name of the foreign language that he wants to learn in his query.
Read the `language-index.md` to find out what is the native language of the user, the list of foreign languages that he is learning and what are the directories in which lessons are saved.
This file may state the name of the native language of the user explicitly.
If the native language is not stated explicitly, assume it is the language in which `language-index.md` is written.
If you cannot determine the user's native language from the contents of the `language-index.md`, assume it is the language in which the user has written his query.

## Example 1

User query: "Przygotuj mi lekcję z niemieckiego"

Contents of `language-index.md`:

```md
Moim jezykiem ojczystym jest język polski.

| Język     | Folder       |
|-----------|--------------|
| Niemiecki | [deu](./deu) |
```

Your conclusions:

- *native language* is Polish
- *foreign language* is German
- *language folder* is `./deu`

## Identify current goals of the user

Read the `todo.md` file from the *language folder* and decide what are the user's current goals.

## Example 2

Contents of `deu/todo.md`:

```md
# Plan nauki

- [x] Wymowa
- [x] Ortografia
- [>] Pozdrowienia
- [ ] Zdanie oznajmujące w czasie teraźniejszym
```

Your conclusions:

- user knows *foreign language* pronuciation rules
- user knows *foreign language* orthography rules
- user is currently learning greetings in the *foreign language*
- if the text or dialogue contains sentences in in the present tense, you should explain the grammar for the present tense and update `todo.md`: `- [>] Zdanie oznajmujące w czasie teraźniejszym`

## Find the lesson folder

Find the directory under the *language folder* with the highest lesson number and assume that this is the *lesson folder*.

## Example 3

Given that `./deu` is the *language folder* and following directories exist:

```txt
deu/lekcja-001/
deu/lekcja-002/
deu/lekcja-003/
```

Your conclusions:

- `deu/lekcja-003/` is the *lesson folder*
