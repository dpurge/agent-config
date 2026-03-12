# Read the texts and dialogues

Read all markdown files in the *lesson folder* and if they contain texts or dialogues in the *foreign language*, they are the texts and dialogues that you need to process.

## Example 1

Given that the *foreign language* is German and the *lesson folder* is `lekcja-001` and you see following files:

Contents of `lekcja-001/tekst-1.md`:

```md
# Mein Haus

Das ist mein Haus.
```

Contents of `lekcja-001/dialog-1.md`:

```md
# Dialog

-- Guten Tag!

-- Guten Tag!
```

Contents of `lekcja-001/notatki.md`:

```md
Czy można użyć "Guten Tag" rano?
```

Your conclusions:

Texts and dialogues that you have to process is:

```md
# Mein Haus

Das ist mein Haus.

# Dialog

-- Guten Tag!

-- Guten Tag!
```

You do not need process `lekcja-001/notatki.md` because:

- it is not in the *foreign language* that you have identified in the previous steps
- it is in the *native language* of the user, therefore you do not need to explain it
