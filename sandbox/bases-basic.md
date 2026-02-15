---
syntaxMode: mdx
---

# Really basic bases setup

Like this ...

````
```base
filters:
  file.inFolder("books")
views:
  - type: cards
    name: "My Bookshelf"
```
````

Produces this:

```base
filters:
  file.inFolder("books")
views:
  - type: cards
    name: "My Bookshelf"
```


## Just with table

```base
filters:
  file.inFolder("/books")
views:
  - type: table
    name: Table
```

## Let's copy the original

```base
filters:
  and:
    - file.inFolder("books")
    - file.name != "Bookshelf"
formulas:
  quick_read: pages < 300
properties:
  note.author:
    displayName: Author
  note.year:
    displayName: Year
  note.genre:
    displayName: Genre
  formula.quick_read:
    displayName: Quick read
views:
  - type: cards
    name: Cards
    order:
      - file.name
      - author
      - year
      - genre
      - formula.quick_read
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
