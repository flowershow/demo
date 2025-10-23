---
title: Example Post (MD)
---

# Hello Markdown

This is a Markdown file ([see source](https://github.com/flowershow/demo/blob/main/other/md-file.md)) where you can embed plain HTML.

Here’s a paragraph with a **custom styled** span:

```
<span style="color: tomato; font-weight: bold;">This text is red and bold.</span>
```

<span style="color: tomato; font-weight: bold;">This text is red and bold.</span>


You can also style your JSX blocks with Tailwind classes:

```
<span class="text-blue font-bold">This text is red and bold.</span>
```

<span class="text-blue font-bold">This text is red and bold.</span>

🧠 Notes for Markdown:
- Inline HTML must use string style syntax (e.g. style="color: red;").
- Attributes follow regular HTML conventions (class, for, background-color, etc.).
- **You cannot use JSX blocks or Flowershow components**.

> [!note]
> If you want all your files to be parsed as plain Markdown with HTML blocks (no matter the extension), you can add `markdownRenderer: "md"` to your `config.json`. Or use `markdownRenderer: "auto"` to parse `.md` files as Markdown and `.mdx` as MDX.
