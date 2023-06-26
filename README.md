# Gitbook Search Launguages

this plugin will replace keyword search in gitbook to your language.

## description

lunr.js is used for a key word search in gitbook.
but tokenizer and stemmer of lunr.js is default setting.
That means that it's only English setting.
this plugin will replace keyword search in gitbook to your language.

This plug-in uses [lunr-languages](https://github.com/MihaiValentin/lunr-languages) in tokenizer and stemmer.

lunr-languages is supporting following languages.

| language | code |
| --- | --- |
| Chinese | zh |
| German | de |
| French | fr |
| Spanish | es |
| Italian | it |
| Japanese | jp |
| Dutch | du |
| Danish | da |
| Portuguese | pt |
| Finnish | fi |
| Romanian | ro |
| Hungarian | hu |
| Russian | ru |
| Norwegian | no |
| Turkish | tr |
| Swedish | sv |

this plugin strongly depend on lunr-languages.

## How to use it?

Add it to your `book.json` configuration:

```json
{
	...
    "plugins": [
        "-lunr",
        "search-languages"
     ],
	...
    "pluginsConfig": {
        "searchLanguages": {
            "lang": "zh"
        }
    }
}
```

```bash
$ gitbook install
```

following option was inherited from [plugin-lunr](https://github.com/GitbookIO/plugin-lunr).

### Limit size for index

default is `1000000`.

```json
    ...
    "pluginsConfig": {
        "searchLanguages": {
            "maxIndexSize": true
        }
    }
}
```

### Ignoring special characters

By default, special characters will be taken into account, to allow special searches like "C++" or "#word".
You can disable this if your text is essentially English prose with the `ignoreSpecialCharacters` option:

```json
    ...
    "pluginsConfig": {
        "searchLanguages": {
            "ignoreSpecialCharacters": true
        }
    }
}
```

## change logs

* version 0.1.1 (2016-12-29)
  fix: updated the outdated libs.
* version 0.1.0 (2016-12-24)
  fix: Overall fix to remove "WIP" condition (#1)
* version 0.0.1 (2015-11-17)

[![NPM](https://nodei.co/npm/gitbook-plugin-search-languages.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/gitbook-plugin-search-languages/)
