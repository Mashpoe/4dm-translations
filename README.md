# 4D Miner Translations
A Git repo for managing all language translations in 4D Miner.

The goal of this project is to make it as easy as possible for members of the 4D Miner community to collaborate on translations. Rather than relying on translation tools like Google Translate or ChatGPT, which have their own limitations, this project aims to allow actual people, many of whom have no other way to support 4D Miner's development, to provide the best possible translations for the game. Automatic translation tools are much more likely to miss context and nuances when translating, especially for a game like 4D Miner, where community members are going to be much more knowledgeable about specific details.

## Contributing
Many people don't know how to work on Git repos, so a brief explanation will be provided here (it's actually pretty simple).

### Forking
Only users with special privileges are able to directly make changes to this project. It isn't feasible to allow everybody to directly contribute, because bad actors could make harmful changes if left unchecked, and even well-intentioned users who don't know what they're doing could accidentally mess things up. As a result, Git project maintainers usually expect most users to create what's called a "fork" of their project in order to contribute.

A "fork" is just a copy of the original project, and anyone who creates a fork is completely in charge of it. After making the necessary changes to the fork, a merge request (aka pull request) can be made to the original project. The maintainers who are in charge of the original project can then approve the merge request, and all of the changes made to the fork will be applied to the original project.

A new fork doesn't need to be made every time a user wants to make a contribution; an existing fork can be reused, but if any changes have been made to the original project since the last merge request was accepted, it is usually a good idea to sync the fork with the original project before creating another merge request.

### Committing
Every time a change is made to either a fork or to the original project, a commit message is needed. Users will automatically be prompted to add a commit message before applying changes to their own fork, and it is important to make the message descriptive. When a merge request is eventually made, the project maintainers will be able to see all of the commit messages, and they probably won't be willing to accept the merge request if they don't understand what is being changed, and why the changes are being made.

### Language Files
All language files are written in the JSON format, which is pretty straightforward. Anyone should be able to edit and make copies of existing JSON files without knowing all of the details of the format. An editor like VS Code will make it easier to spot errors when editing.

The language files must all be named according to the [ISO 639 two-letter language codes](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes), e.g. `en.json` for English or `es.json` for Spanish. If a language isn't assigned a two-letter code, a three-letter code from the [official ISO 639-3 website](https://iso639-3.sil.org/code_tables/639/data) can be used instead, e.g. `tok.json` for Toki Pona.

A new language file can easily be created by copying the current `en.json` file and renaming it accordingly.

Each translation has a title and a value. The title of each translation **must** match the corresponding title in the `en.json` file, so if a new language file is created from a copy of `en.json`, the titles of the translations must not be changed.

Each translation looks something like this:

`en.json`:
```json
"TranslationTitle": "This is the translation content, which is the part that can be modified."
```

`es.json`:
```json
"TranslationTitle": "Este es el contenido de la traducción, que es la parte que se puede modificar."
```

The first translation in each language file is titled "LanguageName" and its value must be the name of the language _in that language_.
