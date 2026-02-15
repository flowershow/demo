---
syntaxMode: mdx
---

> [!important]
> You must set `syntaxMode: mdx` in your frontmatter!

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
  file.inFolder("books")
views:
  - type: table
    name: Table
```
