# Rousseau

Rousseau provides an API to easily proofready and spellcheck texts.

The proofreading API is built on top of the open source utility [Rousseau](https://github.com/GitbookIO/rousseau). The spellchecker is using the Hunspell dictionaries.

The API is accessible at `https://rousseau.gitbook.com`.


#### Proofread a text

```
POST https://rousseau.gitbook.com/document
```

###### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| `document` | `string` | Body of the document to proofread |

###### Response

```js
{
    "count":1,
    "results":[
        {
            "value":"Allegedly",
            "index":0,
            "offset":9,
            "message":"adverbs can weaken meaning",
            "replacements":[],
            "type":"adverbs",
            "level":"warning"
        }
    ]
}
```

### Spellcheck a list of words

```
POST https://rousseau.gitbook.com/words

{ "words": ["Hello", "World"] }
```
