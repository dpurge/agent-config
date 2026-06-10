# Create translation

Create translation of all the texts and dialogues from the *foreign language* to the *native language*.

If the *native language* is English, write the translation in the `<basename>-translation.md` file.
If the *native language* is Polish, write the translation in the `<basename>-tłumaczenie.md` file.

Split the original text into sentences. Preserve text formatting.

For each sentence:

- include the original text in this sentence
- if the *foreign language* requires transcription, you must include scientific transcription of the text of this sentence into latin script
- write the translation of this sentence into *native language* of the user

Sentences should be separated with `---`.

Capitalize the transcription using rules similar to the *native language*.

## Example 1

Given that the text is:

```md
# Ποιος είναι αυτός;

Ποιος εἶναι αυτός;
Αυτός εἶναι ο Κώστας.
Ο Κώστας εἶναι μαδητής.
```

and the *foreign language* does not require transcription, the format of the translation should be:

```md
# Ποιος είναι αυτός;

# Kto to jest?

---

Ποιος εἶναι αυτός;

Kto to jest?

---

Αυτός εἶναι ο Κώστας.

To jest Kostas.

---

Ο Κώστας εἶναι μαδητής.

Kostas jest uczniem.
```

## Example 2

Given that the text is:

```md
# اَلدَّرْسُ الأَوَّلُ

هُوَ كَبِيرٌ.
هُمْ كِبَارٌ.

أَنْتَ صَغِيرٌ.
اَنْتُمْ صِغَارٌ.
```

and the *foreign language* requires transcription, the format of the translation should be:

```md
# اَلدَّرْسُ الأَوَّلُ

# Ad-darsu l-awwalu

# Lekcja pierwsza

---

هُوَ كَبِيرٌ.

Huwa kabīrun.

On jest duży.

---

هُمْ كِبَارٌ.

Hum kibārun.

Oni są duzi.

---

أَنْتَ صَغِيرٌ.

Anta ṣaġīrun.

Ty jesteś mały.

---

اَنْتُمْ صِغَارٌ.

Antum ṣiġārun.

Wy jesteście mali.
```
