# Create vocabulary list

If the *native language* is English, the vocabulary list should be written in the `vocabulary.md` file.
If the *native language* is Polish, the vocabulary list may be written in the `słownictwo.md` file.

Choose from 10 to 30 words from the texts and dialogues that are most important for the understanding of the contents, and include them in the vocabulary.

Each vocabulary item should be written on a single line and should follow this format:
`<phrase in the foreign language> {<grammar marks>} [<transcription>] = <translation to the native language>`

- phrase in the *foreign language* is obligatory and should be in the dictionary form if aplicable
- grammar marks are optional and should be omitted if you are not sure what they should be; if included, they should be inside curly braces `{}`
- transcription is optional and should only be included if the *foreign language* includes description of the transcription rules; if present, translation should be in brackets `[]`
- translation to the *native language* is obligatory and follows after the equal sign `=`

Grammar marks may encode:

- part of speech
  - `N` for noun
  - `V` for verb
  - `Adj` for adjective
  - `Adv` for adverb
- number
  - `sg` for singular
  - `pl` for plural
- gender
  - `m` for masculine
  - `f` for feminine
  - `n` for neuter

Grammar marks should be enclosed in curly braces and are comma separated, eg: `{N m sg}`
Skip grammar marks if you are not sure what they should be.

Example vocabulary line without grammar marks or transcription: `das Haus = dom`
Example vocabulary line with grammar marks but without transcription: `das Haus {N} = dom`
Example vocabulary line without grammar marks but including transcription: `茶碗 [cháwǎn] = filiżanka`
Example vocabulary line with grammar marks and including transcription: `茶碗 {N} [cháwǎn] = filiżanka`

Use code fences for vocabulary lists to preserve line breaks when they are inside markdown files: "```txt ...```"

Example format for the vocabulary file:

> # Nowe słowa
>
> ```txt
> 碗 [wǎn] = miska
> 茶 [chá] = herbata
> 茶碗 [cháwǎn] = filiżanka
> 飯碗 [fànwǎn] = miska
> ```
