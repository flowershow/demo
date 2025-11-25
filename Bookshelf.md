---
syntaxMode: mdx
title: 📚 Bookshelf
description: This page showcases support for Obsidian Bases (still in early Alpha).
---

>[!note]
>Click [here](https://github.com/flowershow/demo/blob/main/Bookshelf.md) to see the source file of this page.

```base
filters:
  and:
    - file.inFolder("books")
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
  - type: table
    name: All books
    order:
      - file.name
      - rating
      - status
      - author
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
      - rating
      - status
      - author
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
