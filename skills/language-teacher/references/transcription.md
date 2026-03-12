# Create transcriptions

If the *language folder* does not contain a file with the description of the transcription, you do not need to transcribe texts or dialogues.

If the *language folder* does contain a file with the description of the transcription (eg. `transcription.md`), you must transcribe all texts and dialogue files using the rules explained in the description of the transcription.

Transcription files should use this name pattern: `<basename>-transcription.md`

## Example 1

Given that *language folder* contains:

```txt
todo.md
lekcja-001/
```

Your conclusions:

- you can skip creating transcription files for this *foreign language*, because the *language folder* does not contain any file with the description of the transcription rules.

## Example 2

Given that *language folder* contains:

```txt
todo.md
transkrypcja.md
lekcja-001/tekst.md
lekcja-001/dialog.md
```

Your conclusions:

- the name of the file `transkrypcja.md` suggests that it contains transcrition rules
- you must read the contents of the `transkrypcja.md` and follow its directions when you create transcription
- you must create the `lekcja-001/tekst-transkrypcja.md` file with the transcription of the contents of `lekcja-001/tekst.md`
- you must create the `lekcja-001/dialog-transkrypcja.md` file with the transcription of the contents of `lekcja-001/dialog.md`
