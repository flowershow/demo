---
syntaxMode: mdx
title: 📚 Bookshelf
---
>[!note]
>Click [here](https://github.com/flowershow/demo/blob/main/bookshelf/README.md) to see the source file of this page.

```base
filters:
  and:
    - file.inFolder("books")
    - file.name != "Bookshelf"
properties:
  note.author:
    displayName: writer
views:
  - type: cards
    name: Cards
    order:
      - file.name
      - author
      - year
      - genre
    image: note.image
    cardSize: 190
    imageAspectRatio: 1.6
```
