# Introduction to scientific working

## LaTeX Document types

The first instruction in a LaTeX document tells the system which document type
this document is.

_(Some, not comprehensive list)_

- `article`
  - used for science articles in journals, short reports
  - has no title page, instead title is on first page with index or text.
  - one column
  - right sided, centered
- `scrartcl`
  - same as `article` but less **strident**

- `minimal`
  - sets only size of page and font
  - mostly used for debugging

- `report`
  - used for longer reports, books, thesis with several chapters
  - one-sided
  - has title page
  - one column
  - right sided, centered
- `scrreprt`
  - same as `report` but in a way like `scrartcl` is to `article`

- `book`
  - intended for writing books
  - two-sided
  - one column, centered
  - right sided
  - title page
- `scrbook`
  - same situation for `book` as for `scrreprt`, `scrartcl`
- `amsbook`
  - tailored class for writing books for the needs of AMS (American Mathematical
    Society)

- `slides`
  - used to create presentation slides
  - uses bigger sans-font letters
- `beamer`
  - used to create projector presentations

- `letter`
  - to write letters in LaTeX

### How to use document classes?

In general the instruction to use LaTeX document classes is:
_(ex. `scrbook` class)_

```Latex
\documentclass{scrbook}
```

But most documentclass can be configured to change some defaults they set.

```Latex
\documentclass[12pt,a4paper,oneside,ngerman]{scrbook}
```

###### Short interception:

The general syntax of LaTeX is:

```Latex
\command[optional params]{parameter}

\begin{environment}[positioning on page]
...
\end{environment}
```

## Don't reinvent the wheel!!!

LaTeX has a lot of capabilities.
In the next appointments I will try to cover the most important features and
concepts in LaTeX.

Beside that, there is a good tutorial that you should follow.

[LaTeX Tutorial from overleaf](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)

## Next

We will write LaTeX and from now on it is intended to be more like a workshop.

[LaTeX annotations](L09_LaTeX-Annotations.md)

