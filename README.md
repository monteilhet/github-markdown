
Table of Contents
=================

   * [github-markdown](#github-markdown)
   * [What is Markdown?](#what-is-markdown)
   * [Examples](#examples)
      * [Text](#text)
      * [List](#list)
      * [Image](#image)
      * [Headers and Quotes](#headers-and-quotes)
         * [Structured documents](#structured-documents)
            * [This is a fourth-tier heading](#this-is-a-fourth-tier-heading)
      * [Tables](#tables)
      * [Code](#code)
      * [Extras](#extras)
      * [TOC](#toc)
    * [Workaround](#workaround)

# github-markdown

* [mastering markdown](https://guides.github.com/features/mastering-markdown/) 
* [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [github help](https://help.github.com/categories/writing-on-github/)

What is Markdown?
============

[Markdown](http://daringfireball.net/projects/markdown/) is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in, like `#` or `*`.

Examples
======

Text
-----

It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

[GitHub](http://github.com)

List
-----

Sometimes you want numbered lists:

1. One
2. Two
3. Three

Sometimes you want bullet points:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
    - Like this
    - And this
  
  
Image
---------

If you want to embed images, this is how you do it:

![image logo github](https://camo.githubusercontent.com/fb782da4019ab66eeea35cc9b9ce73b2438b1688/687474703a2f2f646f632e72756c746f722e636f6d2f696d616765732f6769746875622d6c6f676f2e706e67)

Format: ![Alt Text](https://cdn0.iconfinder.com/data/icons/social-media-logos-free/32/github_social_media_logo-128.png)

Headers and Quotes
--------------------------

### Structured documents

Sometimes it's useful to have different levels of headings to structure your documents. Start lines with a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

#### This is a fourth-tier heading

You can use one `#` all the way up to `######` six for different heading sizes.

If you'd like to quote someone, use the > character before the line:

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

Tables
--------

You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`:

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
<br>
Colons can be used to align columns.


| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |


Code
-------

There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap them in backticks: `var example = true`.  If you've got a longer block of code, you can indent with four spaces:

    if (isAwesome){
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

```
if (isAwesome){
  return true
}
```

And if you'd like to use syntax highlighting, include the language:

```javascript
if (isAwesome){
  return true
}
```

```python
def foo():
    if not bar:
        return True
```

Extras
--------

GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji! :sparkles: :camel: :boom:
<br>emoji list : http://www.webpagefx.com/tools/emoji-cheat-sheet/


TOC
---

cf https://github.com/ekalinin/github-markdown-toc

gh-md-toc — is for you if you want to generate TOC for README.md or GitHub's wiki page

NB TOC for jupyter notebook slightly differs using camel case syntax for anchor label 

Workaround
==========

 * Title not correctly displayed in github markdown (try to delete and reinsert space between # and title) <br> --> Test using VSCode Ctrl+Shift+V preview
 * TOC ref in github has to be in lowercase `[Extra Section TEST](#extra-section-test)`
   => use  `sed  '/(#/s/\(#.*\)/\L\1/' file.md > fixed.md`