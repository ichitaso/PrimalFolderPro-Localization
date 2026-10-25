# PrimalFolderPro Localization

Translations for the settings of [PrimalFolderPro](https://cydia.ichitaso.com/depiction/primalfolderpro.html), a folder tweak for iOS 14 - 26 (rootful / rootless / roothide).

The first translations were machine-made, so some of them may sound unnatural. If you spot a wrong or awkward translation in your language, please fix it and send a pull request. Corrections of a single line are welcome too.

## Languages

| Folder | Language |
|---|---|
| `en.lproj` | English (base) |
| `ja.lproj` | 日本語 |
| `zh-Hans.lproj` | 简体中文 |
| `zh-Hant.lproj` | 繁體中文 |
| `ko.lproj` | 한국어 |
| `es.lproj` | Español |
| `fr.lproj` | Français |
| `de.lproj` | Deutsch |
| `it.lproj` | Italiano |
| `pt-BR.lproj` | Português (Brasil) |
| `pt-PT.lproj` | Português (Portugal) |
| `ru.lproj` | Русский |
| `uk.lproj` | Українська |
| `pl.lproj` | Polski |
| `nl.lproj` | Nederlands |
| `sv.lproj` | Svenska |
| `tr.lproj` | Türkçe |
| `ar.lproj` | العربية |
| `he.lproj` | עברית |
| `hi.lproj` | हिन्दी |
| `th.lproj` | ไทย |
| `vi.lproj` | Tiếng Việt |
| `id.lproj` | Bahasa Indonesia |
| `ms.lproj` | Bahasa Melayu |

## How to fix a translation

Each language has one file: `Resources/<language>.lproj/Localizable.strings`.

Every line looks like this:

```
"English text" = "Translated text";
```

- Change only the text on the **right**. The text on the left is the key the tweak looks up, so it must stay exactly as it is (even if the English could be better).
- Keep `%@` and `%d` as they are. They are replaced with a value, for example `Version %@` becomes `Version 0.0.2`.
- Keep `\n` as it is. It is a line break.
- To use a double quote inside the text, write `\"`. Typographic quotes such as `“ ”` or `「 」` can be used as they are.
- Every line ends with `;`.
- Save the file as UTF-8.
- Short labels matter: titles that are too long get shrunk to fit next to switches and buttons. Keep them close to the English length when you can.
- Jailbreak words such as "Respring" can stay in English if that is what people in your language actually use.

To check the file before sending it (on a Mac):

```sh
plutil -lint Resources/ja.lproj/Localizable.strings
```

## How to add a language

1. Copy `Resources/en.lproj` to `Resources/<code>.lproj`, using Apple's language code (for example `fa`, `cs`, `es-419`).
2. Translate the right side of every line.
3. Send a pull request. Please mention the language in the title.

## Trying it on your device

You can test your file before the next release by replacing the one inside the settings bundle and reopening the Settings app:

| Jailbreak | Path |
|---|---|
| rootful | `/Library/PreferenceBundles/PrimalFolderPro.bundle/<code>.lproj/Localizable.strings` |
| rootless | `/var/jb/Library/PreferenceBundles/PrimalFolderPro.bundle/<code>.lproj/Localizable.strings` |
| roothide | the same path inside your jbroot |

The file is replaced again when you update the tweak, so keep a copy.

## Pull requests

- One language per pull request makes it easier to review.
- Accepted changes are included in the next build of PrimalFolderPro.
- Translators can be credited in the release notes. Tell me in the pull request if you would like that, and how you want your name shown.

## Contact

- Developer: [@ichitaso](https://x.com/ichitaso)
- Discord: https://discord.gg/FuDBaWryge
- Repo: https://cydia.ichitaso.com/
