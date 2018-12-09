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
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-05** </i>

## Key Topics
<a class="meta-badge tool" href="/docs/topic-index/#e-h"><i class="fas fa-desktop fa-lg"></i>&nbsp; **GitHub**</a> <a class="meta-badge keyword" href="/docs/topic-index/#m-p"><i class="fas fa-tags fa-lg"></i>&nbsp; **Markdown**</a>

## Resources
<a class="btn btn-outline-primary resource" href="https://guides.github.com/features/mastering-markdown/" target="_blank"> GitHub Mastering Markdown </a> <a class="btn btn-outline-primary resource" href="https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf" target="_blank"> RMarkdown Reference Guide </a>

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

## Working with Text
Markdown provides a number of tools for working with and stylizing text. These include options for bold and italicized text, adding code blocks, quoting text, and creating bulleted and enumerated lists.

### Styling Text
Text can be styled using bold and italics To create italicized text, wrap your text with a single asterisk `*`. To create bold text, wrap your text with double asterisks `**`. 

**Input:**
```markdown
*This is an italicized sentence.*

**This is a bolded sentence.**
```

**Output:**

### Quoting Text
Quoting text (which I have used above to illustrate examples) is done with a greater then symbol (`>`).

**Input:**
```
> This is quoted text.
```

### Quoting Code
#### In-Line Code
There are two types of code quotes in Markdown. In-line quotes, which are included in a sentence, are wrapped in single backticks:

**Input:**
````markdown
The `stlLead` data contains a variable named `totalPop`.
````

**Output:**

#### Code Blocks
To include code blocks, which are better for including the full syntax of particular commands and their output, use triple backticks:

**Input:**
````markdown
```r
> summary(stlLead$totalPop)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    620    2025    2912    2999    3784    7069 
```
````

**Output:**

Note how the letter 'r' is written after the first set of triple backticks. This is an indicator for GitHub that the code is written in `R`'s programming language. By including this, GitHub can apply some syntax highlighting to your files. This makes them easier to read.

### Links
In Markdown, adding hyperlinks is a two step process. The text that you want to have hyperlinked is written first and is wrapped in brackets `[]`. After this, you include the URL wrapped in parentheses `()`. This is an example of including in-line hyperlinks:

**Input:**
```markdown
The [Sociospatial Data Science book](http://chris-prener.github.io/SSDSBook/) is hosted using the service [GitHub](https://github.com).
```

**Output:**

### Embedding Images
Images can be embedded in Markdown documents with syntax that is nearly identical to how [Links] were inserted, except that text in the brackets can be omitted. You will add an `!` to the beginning of the syntax, and use a URL to an image in the link:

**Input:**
```markdown
![](http://slu-soc5650.github.io/images/logo.png)
```

**Output:**

You can replace the URL to an image with a path within a repository organized as suggested in [Organizing Projects] - `![](results/map1.png)`. The path can be as long as necessary if there are additional directories - `![](results/maps/firstDraft/map1.png)`.

### Lists
#### Bulleted Lists
Bulleted lists are indicated in Markdown using the dash `-` or a single asterisk `*`:

**Input:**
```markdown
- mean
- median
- mode
* variance
* standard deviation
```

**Output:**

#### Enumerated Lists
Enumerated lists are created by preceding each line with the appropriate number:

**Input:**
```markdown
1. calculate the mean
2. calculate the variance
3. calculate the standard deviation
```

**Output:**

#### Nested Lists
You can create more complex lists by preceding a line with four single spaces. You can also combine bulleted and enumerated lists when using this approach.

**Input:**
```markdown
1. create a basemap
    * add street centerlines and the city boundary
    * use a light hue for the centerline
2. add points for incidents
    * use red points for fire incidents
    * use blue points for EMS incidents
```

**Output:**

## GitHub Markdown
Markdown's original syntax has been augmented numerous times since it was first released. Users sometimes call these different ["flavors"](https://github.com/commonmark/CommonMark/wiki/Markdown-Flavors) of Markdown. One key flavor of Markdown to be familiar with is GitHub Markdown, which adds a number of additional syntax features to the base syntax discussed in the previous two sections.

### Styling Text
Strikethrough text can be useful for indicating that a particular comment or piece of information is no longer relevant while also preserving that text in the document. Strikethrough text can be created by wrapping your text with two tildes `~~ ~~`:

**Input:**
```markdown
~~This is a sentence with strikethrough text.~~
```

**Output:**

### Simple Tables
Tables can be created using a combination of pipe (`|`) and dash (`-`) characters. The dashes are used to separate the header row from the data rows, and there must be at least three dashes per column. The spacing is not required, mis-aligned text in the rows should not prevent the table from rendering nicely. However, I do think that well spaced tables are easier to edit down the road.

**Input:**
```markdown
| `id` | `name` | `value` |
| ---- | ------ | ------- |
| 1    | ham    | 23      |
| 2    | eggs   | 18      |
| 3    | spam   | 6       |
```

**Output:**

### Task Lists
If you want to create task lists on GitHub, you can include brackets separated by a space before each list item `[ ]`. Completed tasks include an `x` in place of the space `[x]`.  These task lists are interactive - when published on GitHub in **Issues** for instance, you can click on the resulting checkboxes to toggle them between complete / incomplete.

**Input:**
```markdown
1. [x] calculate the mean
2. [ ] calculate the variance
3. [ ] calculate the standard deviation
```

**Output in Static Markdown Doc:**

**Output in Issue or Pull Request:**

### Mentioning Other GitHub Users
If you want to mention me or one of your classmates in a comment, include the `@` symbol before their username. Once the document is uploaded to GitHub, the username will render as a hyperlink and the user will be alerted.

**Input:**
```markdown
Hey @chris-prener, thanks for the feedback. I made the changes to lines 40 and 41.
```

**Output:**
