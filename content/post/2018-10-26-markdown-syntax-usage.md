---
title: Markdown
subtitle: Syntax and Usage
date: 2018-10-26
share-img: https://abyssaltech.xyz/img/markdown/md.png
tags: ["Web", "Markdown"]
---
## Markdown
[Markdown](https://en.wikipedia.org/wiki/Markdown) is a lightweight markup language that can be used to write plain text-format which can be converted to valid HTML. Using markdown you don't need to write content within HTML tags, you can directly write text with markdown syntax and it'll automatically get converted. You can also use HTML within markdown!

Markdown files have an extension `.md` or `.markdown`.

It is also different from your normal text editors like Word in which you click buttons to do the job. In Markdown you don't see the output as you're typing, you only see it in a browser and if you've some changes, you have to go back and edit.

Today, markdown can be found in many places. [GitHub](https://guides.github.com/features/mastering-markdown/) uses it for writing documentation, [Reddit](https://www.reddit.com/wiki/commenting) uses it for comments, you can try it out while writing messages in WhatsApp, you can write emails in it, much of the content you read online is written in Markdown. This post is written in Markdown too. It has an advantage that the person who is writing does not need to see everytime how it looks on a webpage. You can write with markdown syntax and the HTML pages will automatically be generated from it.

It looks very clean and it is easy to write too. Markdown is fast and easy way to take notes, create content for a website, and produce print-ready documents, some even make presentations from it too. It is quickly becoming the writing standard for [academics](http://chronicle.com/blogs/profhacker/markdown-the-syntax-you-probably-already-know/35295), [scientists](http://blogs.plos.org/mfenner/2012/12/13/a-call-for-scholarly-markdown/), [writers](http://lifehacker.com/5943320/what-is-markdown-and-why-is-it-better-for-my-to+do-lists-and-notes), and many more.

Here's the difference between some HTML and same goal achieved by Markdown -
```
HTML:

<h1>Markdown is <em>awesome</em>. Start using it now.</h1>

<p><a href="http://daringfireball.net/projects/markdown/">Markdown</a> is so cool,

it will make your life <em>easier</em><strong>A lot easier.</strong></p>

Markdown:

># Why *you* should use Markdown to write your next blog post

[Markdown][1] is so cool, it will make your life *easier*. **A lot easier.**

[1]: http://daringfireball.net/projects/markdown/basics
```
Notice how Markdown is a lot readable. But, after the content is posted online, they both look the same.

Though it is a lot different and far from the comfort of other [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) tools, it offers unparalleled writing speed, fluency, and fewer errors.
## Cheatsheet
Though Markdown has different "flavours" depending upon what you're using it for, this is a more generalized list meant to be used as a quick reference.

Given below are usage and examples of Markdown syntax categorised for easy reference.

1. [Headings](#headings)
2. [Emphasis](#emphasis)
3. [Lists](#lists)
4. [Links](#links)
5. [Heading ID](#headingID)
6. [Images](#images)
7. [Highlighting](#highlighting)
8. [Tables](#tables)
9. [Blockquotes](#blockquotes)
10. [Inline HTML](#inlinehtml)
11. [Horizontal Rule](#hr)
12. [Tasklists](#tasklists)
13. [Footnotes](#footnotes)
14. [Definitions](#defns)
15. [Escaping](#esc)
16. [Line Breaks](#linebreaks)
17. [YouTube Videos](#youtube)

---
### 1. Headings {#headings}
```
# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternalively, you can use undeline styles as follows:

Another-H1
==========

Another-H2
----------

```
# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternative-H1
==============

Alternative-H2
--------------
---
### 2. Emphasis {#emphasis}
Many kinds of emphasis are available Emphasis in Markdown. Same as `<em>` tag in HTML.

```
Emphasis, aka Italics: *asterisks* or _underscores_.

Strong emphasis, aka Bold: **double asterisks** or __double underscores__.

You can also combine them: **asterisks and _underscore too_**.

Strikethrough uses two tildes: ~~wrong or sarcasm~~
```

Emphasis, aka Italics: *asterisks* or _underscores_.

Strong emphasis, aka Bold: **double asterisks** or __double underscores__.

You can also combine them: **asterisks and _underscore too_**.

Strikethrough uses two tildes: ~~sarcasm~~
---
### 3. Lists {#lists}
Proper indentation is required to display lists properly.

```
1. Item
2. Another item
and so on...

* Unordered list Item
  * Sub-list item

109. Numbers don't matter, just that it should be a number

1. Item
  1. Sub-list item 1

+ Plus can be used
- Minus can be used too

```
1. Item
2. Another item
and so on...

* Unordered list Item
  * Sub-list item

109. Numbers don't matter, just that it should be a number

1. Item
  1. Sub-list item 1

+ Plus can be used
- Minus can be used too

---
### 4. Links {#links}
Direct, reference, and relative links can be created.

```
[Inline-style link](https://www.google.com)

[Inline-style link with tooltip](https://www.google.com "Google's Homepage")

[Reference-style link][Case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Expand those references later:
[Case-insensitive reference text]: https://www.bing.com
[1]: http://abyssaltech.xyz

[Relative link to local](../docs/new/my)

[link text itself]

[link text itself]: https://www.google.com

```
[Inline-style link](https://www.google.com)

[Inline-style link with title](https://www.google.com "Google Homepage")

[Reference-style link][Case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

[Relative link to local](../docs/new/my)

[link text itself]

---
### 5. Heading ID {#headingID}
You can place heading id as
```
### My Heading {#custom-id}
```
You can then link directly to it using link as `[Goto Heading](#custom-id)`.

---
### 6. Images {#images}

```
Absolute:
![Alt-text for image](https://abyssaltech.xyz/img/triangle.jpg)

Relative:
![Alt text for image](/img/triangle.jpg)

Reference-styled:
![Alt-text for image][image]

[image]: (https://abyssaltech.xyz/img/splash.png)

```
Absolute:
![Alt-text for image](https://abyssaltech.xyz/img/splash.png)

Relative:
![Alt text for image](/img/splash.png)

Reference-styled:
![Alt-text for image][image]

[image]: (https://abyssaltech.xyz/img/splash.png)

---
### 7. Highlighting {#highlighting}
Code and syntax highlighting can be performed with Markdown. It differs from render to renderer.

We can inline-highlight text or block-highlight code.

```
back-ticks are used for inline-highlighting: `Important`

triple back-ticks are used for block-highlighting: code enclosed within '''

You can specify the language for proper highlighting:

```python
s = "Python syntax highlighting"
print s
```.

```
back-ticks are used for inline-highlighting: `Important Stuff`

triple back-ticks are used for block-highlighting: code enclosed within ```

You can specify the language for proper highlighting:

```python
s = "Python syntax highlighting"
print s
```
---
### 8. Tables {#tables}
Tables aren't part of the original Markdown specifications, but they are there many a times.

```
| Tables        | Are           | Cool  |
| ------------- | ------------- | ----- |
| row 1         | top           |    4  |
| row 2         | middle        |    2  |
| row 3         | bottom        |    3  |

You don't need to make the raw Markdown line up prettily.

Much | Less | Pretty
--- | --- | ---
Still | renders | fine
1 | 2 | 3

To change the alignment of the elements in a column, add a colon (:) to the left side, right side,
 or both sides of the appropriate set of hyphens on the second line.
 For example, inputting this:

Column L | Column C | Column R
:--------|:--------:|---------:
A1 | B1 | C1
A2 | B2 | C2
```

| Tables        | Are           | Cool  |
| ------------- | ------------- | ----- |
| row 1         | top           |    4  |
| row 2         | middle        |    2  |
| row 3         | bottom        |    3  |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily.

Much | Less | Pretty
--- | --- | ---
Still | renders | fine
1 | 2 | 3

To change the alignment of the elements in a column, add a colon (:) to the left side, right side, or both sides of the appropriate set of hyphens on the second line. For example, inputting this:

Column L | Column C | Column R
:--------|:--------:|---------:
A1 | B1 | C1
A2 | B2 | C2

---
### 9. Blockquotes {#blockquotes}

```
> Here is a nice quote.
> This line is part of the same code.
```
> Here is a nice quote.
> This line is part of the same code.

A quote can also nicely align and wrap around when it is a really long one.

---
### 10. Inline HTML {#inlinehtml}
You are free to use HTML in your Markdown, and most of the times it'll work pretty good.

---
### 11. Horizontal Rule {#hr}
```
Three or more -

---

Hyphens

***

Asterisks

___

Underscores
```
Three or more -

---

Hyphens

***

Asterisks

___

Underscores

---
### 12. Tasklists {#tasklists}
Simple tasklists can be generated.
```
- [x] Write the post
- [ ] Update the repo
- [ ] Push and publish
```
- [x] Write the post
- [ ] Update the repo
- [ ] Push and publish

---

### 13. Footnotes {#footnotes}
```
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.
```
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

---

A footnote will be created at the very bottom of this page, which you can visit clicking the note attached to the sentence. 

### 14. Definitions {#defns}
Some Markdown processors allow you to create definition lists of terms and their corresponding definitions as follows.
```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

---

### 15. Escaping {#esc}
You can escape certain characters in Markdown.
```
\     backslash
\.    dot  
\!    exclamation mark  
\#    hash
\*    asterisk
\+    plus
\-    minus
\_    underscore
\`    backtick
\(\)  parentheses
\[\]  brackets
\{\}  curly brackets  
```

### 16. Line Breaks {#linebreaks}
One Newline won't break the line in Markdown, you have to hit newline twice or use two spaces after a line for line break.

```
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.

```
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a **separate paragraph**.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the **same paragraph**.

---
### 17. YouTube Videos {#youtube}

Videos can be added directly by just pasting their embed code inside Markdown.

## Links and References

- You can try out Markdown directly in your browser here - [Dillinger.io](https://dillinger.io/).

- Some good practice [here](https://www.markdowntutorial.com/).

- A good reference for Markdown - [link](https://www.markdownguide.org/).

- For more detailed info, you can refer to the official documentation [here](https://daringfireball.net/projects/markdown/syntax).

- Markdown - [Wikipedia](https://en.wikipedia.org/wiki/Markdown).
