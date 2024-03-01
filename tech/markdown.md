This comprehensive Markdown cheat sheet offers a detailed overview of Markdown syntax, from [basic formatting](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) like headers, lists, and emphasis, to advanced features including tables, footnotes, and extended syntax options. It serves as a practical reference for creating well-structured, accessible, and visually appealing documents in Markdown. Whether you're a beginner or an experienced user, this cheat sheet is designed to enhance your Markdown writing skills with clear examples and explanations.

## Basic Syntax
### Headers (atx style)
#### ATX Style
```
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

#### setext style
```
Header 1
========
```

```
Header 2
--------
```


### Emphasis

```markdown
*italic*
_italic_
```
*italic*


```markdown
**bold**
__bold__
```
**bold**

```markdown
`inline code`
```
`inline code`

```
~~strikethrough~~
```
~~strikethrough~~


### Blockquotes

```markdown
> This is
> a blockquote
>
> > Nested
> > Blockquote
```



### Unordered List

```markdown
* Item 1
* Item 2
    * item 3a
    * item 3b
```
or
```markdown
- Item 1
- Item 2
```
or
```markdown
+ Item 1
+ Item 2
```


### Ordered List

```markdown
1. Item 1
2. Item 2
    a. item 3a
    b. item 3b
```



### Links

```markdown
[link](https://cheatsheets.one)
```

```markdown
[link][cheatsheet]
[cheatsheet]: https://cheatsheets.one
```

```markdown
<https://cheatsheets.one>
```


### Horizontal rule

Hyphens
```markdown
---
```
---

Asterisks
```markdown
***
```
***

Underscores
```markdown
___
```
___


### Code
~~~markdown
```javascript
console.log("This is a block code")
```
~~~

```markdown
~~~css
.button { border: none; }
~~~
```

```markdown
    4 space indent makes a code block
```

#### inline code
```markdown
`Inline code` has back-ticks around it
```



### Tables
```
Header1 | Header2 | Header3
--- | --- | ---
*Italic* | `code` | **bold**
1 | 2 | 3
```
Header1 | Header2 | Header3
--- | --- | ---
*Italic* | `code` | **bold**
1 | 2 | 3

[Online Markdown Table Generator](https://codebeautify.org/markdown-table-generator)



### Images

```markdown
![GitHub Logo](/images/logo.png)

![Alt Text](url)
```

#### Image with link
```markdown
[![GitHub Logo](/images/logo.png)](https://github.com/)

[![Alt Text](image_url)](link_url)
```

#### Reference style
```markdown
![alt text][logo]

[logo]: /images/logo.png "Logo Title"
```

### Line Breaks
To create a line break, end a line with two or more spaces, then press `Enter`.

### Escaping Characters
Use a backslash (`\`) to escape Markdown characters and use them as regular characters without triggering their formatting features.

## Advanced Syntax
### Footnote

Here's a sentence with a footnote. `[^1]`

`[^1]: This is the footnote.`

### Heading ID

```
### My Great Heading {#custom-id}
```
### Definition List

```
term
: definition
```

### Task List
```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```
### Emoji
```
This is funny! :smile:
I'm thinking! :thinking:
I'm worried! :worried:
```


### Highlight

I need to highlight these ```==very important words==```.


### YouTube
YouTube can only be added with to following trick.
```
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```

### Backslash escapes

| Characters | Escape | Description |
|------------|--------|-------------|
| \\         | \\\\   | backslash   |
| \`         | \backtick   | backtick              |
| \*         | \\\*   | asterisk              |
| \_         | \\\_   | underscore            |
| \{\}       | \\\{\} | curly braces          |
| \[\]       | \\\[\] | square brackets       |
| \(\)       | \\\(\) | parentheses           |
| \#         | \\\#   | hash mark             |
| \+         | \\\+   | plus sign             |
| \-         | \\\-   | minus sign \(hyphen\) |
| \.         | \\\.   | dot                   |
| \!         | \\\!   | exclamation mark      |

## Extended Syntax

### Differences in Markdown Flavors
There are different flavors of Markdown, like [GitHub-Flavored Markdown](https://github.github.com/gfm/) (GFM), CommonMark, etc. Syntax and support may vary across different platforms and editors. For example markdown does not support superscript and subscript natively.

#### Subscript
```H~2~O```  or   `H<sub>2 </sub>O`

#### Superscript
```X^2^```  or ```X<sup>2```



### Table of Contents (TOC)
Automatically generate a table of contents based on headers. Usage varies by Markdown processor, often involves inserting a specific placeholder like `[TOC]` at the desired location.

### Syntax Highlighting in Code Blocks
Specify the programming language to enable syntax highlighting.

```markdown
```python
print("Hello, world!")
```
```

### Direct HTML
You can use HTML tags for content not supported by Markdown syntax.

```html
<center>This text is centered.</center>
```

### Mathematical Equations
Embed LaTeX for mathematical equations in some Markdown processors.

```markdown
$$
E = mc^2
$$
```

### Custom Containers
```markdown
::: warning
*Here be dragons!*
:::
```
Note: Requires support from the Markdown processor, such as Markdown-it's container plugin.

### Collapsible Sections
```html
<details>
<summary>Click to expand!</summary>

This section is collapsible.

</details>
```
