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
    displayName: Author
  note.year:
    displayName: Year
  note.genre:
    displayName: Genre
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
  - type: table
    name: All books
    order:
      - file.name
      - author
      - rating
      - status
      - description
      - year
    sort:
      - property: rating
        direction: DESC
      - property: author
        direction: ASC
      - property: year
        direction: ASC
      - property: status
        direction: ASC
    summaries:
      rating: Average
    rowHeight: extra
  - type: table
    name: Not read yet
    filters:
      and:
        - status != "read"
    order:
      - file.name
      - author
      - rating
      - status
      - description
      - year
    sort:
      - property: rating
        direction: DESC
      - property: author
        direction: ASC
      - property: year
        direction: ASC
      - property: status
        direction: ASC
    rowHeight: medium
  - type: list
    name: List
    order:
      - file.name
      - author
      - year
    indentProperties: false

```
