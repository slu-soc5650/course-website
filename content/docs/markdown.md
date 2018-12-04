+++
title = "Writing in Markdown"

date = 2018-12-04T00:00:00
lastmod = 2018-12-04T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Writing in Markdown"
[menu.docs]
  parent = "Fundamentals"
  weight = 20
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-04** </i>

## Resources
<a class="btn btn-outline-primary resource" href="https://www.rstudio.com/resources/cheatsheets/#rmarkdown" target="_blank"> RMarkdown Cheatsheet </a> <a class="btn btn-outline-primary resource" href="https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf" target="_blank"> RMarkdown Reference Guide </a>

## Basics
Markdown is a simple [markup language](https://en.wikipedia.org/wiki/Markup_language). Markup languages are used to give computer programs directions on how particular blocks of text should be processed. Markdown was developed in 2004 by writer and developer [John Gruber](http://daringfireball.net). Gruber describes Markdown on his [website](http://daringfireball.net/projects/markdown/):

> Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

> Readability, however, is emphasized above all else. A Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions. While Markdown’s syntax has been influenced by several existing text-to-HTML filters — including Setext, atx, Textile, reStructuredText, Grutatext, and EtText — the single biggest source of inspiration for Markdown’s syntax is the format of plain text email.

> To this end, Markdown’s syntax is comprised entirely of punctuation characters, which punctuation characters have been carefully chosen so as to look like what they mean. E.g., asterisks around a word actually look like *emphasis*. Markdown lists look like, well, lists. Even blockquotes look like quoted passages of text, assuming you’ve ever used email...

> ...Markdown’s syntax is intended for one purpose: to be used as a format for writing for the web.
Markdown is utilized to varying degrees by many of the data science tools we'll use in both courses, including RStudio, GitHub, and Slack. In all three applications, Markdown provides a straightforward way to format and stylize plain text files. Markdown therefore gives us the best of two worlds - text files can be organized and formatted as in [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) editors like Microsoft Word, but they remain plain text files that are accessible in a variety of computing environments and do not depend on proprietary applications.

Markdown's simplicity is sometimes also identified as a weakness - it lacks the full fledged control of html or LaTeX, for example. However, for research documentation, the bells, whistles, and fine-grained control of something like LaTeX are unnecessary. Long-term portability is a far more important characteristic, and Markdown excels in this area. 

Markdown files are really just plain-text files, which are usually identified as `.txt` files. However, when they contain Markdown syntax, we want to name them as `.md` files. Most applications will continue to recognize `.md` files as plain-text files. However, certain desktop applications like RStudio and some websites like [GitHub.com](https://github.com) recognize the `.md` file extension and will "render" the Markdown syntax into formatted output. When you create Markdown files in an application like RStudio, make sure to save them with the `.md` file extension!

## Document Organization
There are two principle means for organizing Markdown documents - headings of varying size and paragraph breaks.

### Headings
Markdown contains six heading levels. Headings are identified with `#` symbols and a space that separates them from from the heading text.

**Input:**
```markdown
# This is the largest heading
## This is the second largest heading
### This is the third largest heading
#### This is the fourth largest heading
#### This is the second smallest heading
###### This is the smallest heading
```

**Output:**


### New Paragraphs
Leave a blank line between two paragraphs to create a break.

**Input:**
```markdown
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Quam pellentesque nec nam aliquam 
sem et tortor consequat. Auctor urna nunc id cursus metus. Eleifend mi in 
nulla posuere. Facilisis sed odio morbi quis. Nibh nisl condimentum id venenatis. 
Lectus nulla at volutpat diam ut venenatis. 

Pretium lectus quam id leo in vitae. Neque vitae tempus quam pellentesque nec nam 
aliquam. Curabitur gravida arcu ac tortor. Arcu risus quis varius quam quisque id 
diam. Viverra aliquet eget sit amet tellus cras adipiscing. Tellus molestie nunc 
non blandit massa enim nec. Tempus imperdiet nulla malesuada pellentesque elit eget. 
Non blandit massa enim nec. Sed risus pretium quam vulputate dignissim suspendisse 
in est ante.
```

**Output:**

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quam pellentesque nec nam aliquam sem et tortor consequat. Auctor urna nunc id cursus metus. Eleifend mi in nulla posuere. Facilisis sed odio morbi quis. Nibh nisl condimentum id venenatis. Lectus nulla at volutpat diam ut venenatis. 

Pretium lectus quam id leo in vitae. Neque vitae tempus quam pellentesque nec nam aliquam. Curabitur gravida arcu ac tortor. Arcu risus quis varius quam quisque id diam. Viverra aliquet eget sit amet tellus cras adipiscing. Tellus molestie nunc non blandit massa enim nec. Tempus imperdiet nulla malesuada pellentesque elit eget. Non blandit massa enim nec. Sed risus pretium quam vulputate dignissim suspendisse in est ante.
