# Language Conventions

> Copy this file to `language-conventions.md` in your blog repo root and fill it
> with the conventions for the languages your blog publishes in. It lives in the
> blog repo, not here, so it travels across machines and across agents.
>
> One section per target language. The examples below are filled in for Spanish;
> replace them with your own languages.

This file answers the questions a translator asks twice per post and should only
have to ask once per blog. When `blog-translator` makes the same call in two
consecutive batches, write it down here.

## Shared across all languages

- **Technical terms stay in English when practitioners say them in English.**
  Do not invent a local word for something the audience reads in English all day.
- **Code is never translated.** Commands, flags, config keys, identifiers,
  terminal output, file paths. Not even comments, unless the author says so.
- **Tags and categories are never translated.** They are taxonomy identifiers.
- **The author's tone rules apply in every language**: first person, short
  sentences, one idea per paragraph, no em dashes, bold sparingly.

## Spanish (es)

### Register

- **Tú, never usted.** The blog is a developer talking to another developer.
- First person singular for experience, first person plural only for genuinely
  shared steps ("vamos a ver" is fine, "en este artículo analizaremos" is not).
- Avoid the impersonal-academic drift that Spanish technical writing falls into:
  "se puede observar que" is a translation smell. Write "fíjate en que".

### Typography

- **Quotation marks**: angular «comillas latinas» for quoted speech, double
  typographic quotes for nested. Straight quotes only inside code.
- **Decimal separator** is a comma, thousands separator is a period: `1.234,56`.
- **Opening question and exclamation marks** are mandatory: `¿`, `¡`.
- **No space before** `:` `;` `?` `!`.
- **Dates** in prose: `9 de octubre de 2026`, lowercase month.
- **Capitalisation in titles is sentence case**, not title case. Spanish does not
  capitalise every word.

### Terms that stay in English

`commit`, `pull request`, `branch`, `deploy`, `build`, `testing`, `stack`,
`framework`, `container`, `prompt`, `agent harness`, `workflow`.

### Terms that get translated

| English | Spanish | Note |
|---|---|---|
| issue | incidencia | or keep `issue` when referring to the GitHub object |
| release | versión / publicación | `release` when it names the artifact |
| performance | rendimiento | |
| default | por defecto | |
| feature | funcionalidad | not "característica" |
| library | biblioteca | **never** "librería" |
| to support | admitir / ser compatible con | "soportar" is a false friend |
| eventually | con el tiempo / al final | **never** "eventualmente" |
| actually | en realidad | **never** "actualmente" |

### Frames that do not travel

Record here the analogies that needed replacing, so the next translation does not
rediscover them:

- *Baseball and American football metaphors.* Replace with the point they make,
  or with a reference the reader shares. Do not substitute soccer automatically;
  a worse analogy in a familiar sport is still a worse analogy.
- *Named idioms* ("Maslow's hammer", "yak shaving"). Keep the name, add three or
  four words of gloss the first time, then use it freely.

## <Another language> (<code>)

### Register

### Typography

### Terms that stay in English

### Terms that get translated

### Frames that do not travel
