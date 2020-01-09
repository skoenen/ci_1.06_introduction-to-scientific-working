# Introduction to scientific working

## Annotations of Text in LaTeX

Beforehand it was said that an author in LaTeX does not care about styling their
document.

Nevertheless an author maybe want to mark or emphasize a word, to give it a
special recognition.

Instead of specifying the style for this words directly, an author can use
commands to mark the words or text and let LaTeX take care of the special
styling.

#### Emphasizing through quotation marks

LaTeX treats quotation marks on the left and right of a word or text
differently, to be able to support different styles

```Latex
`WORD'
  %➟ 'WORD'

``WORD''
  %➟ “WORD”

,,WORD''
  %➟ „WORD”

,,GERMAN QUOTATION``
  %➟ ⹂GERMAN QUOTATION〞

,,QUOTATION in `quotation' is possible''
  %➟ „QUOTATION in 'quotation' is possible”
```

Avoid using `"` if you use internalization for your document, especially for
German.
There it is used to construct _umlaute_ like ä, ü, ö, ß.

#### Italics, bold and others

LaTeX provides commands to set a text or word to be italic, bold, or other
emphasizing style.

```Latex
\textit{This text will be italic}
{\itshape This text will also be italic}

\textbf{This text will be bold}
{\bfseries This text will also be bold}

\texttt{This text will be in mono type}
{\ttfamily This text will also be in mono type}

\textsc{This text will be in small capitals}
{\scshape This text will also be in mono type}

\ul{This text will be underlined}
  % This needs the package 'soul' ➟ \usepackage{soul}

\uline{This text will be underlined}
  % This needs the package 'ulem' ➟ \usepackage{ulem}
  % The package changes \emph to use underline. To avoid this use
  % ➟ \usepackage[normalem]{ulem}
```

But this introduces direct styling from the author to the output.
Sometimes this is desired.
And it makes it necessary, that the authors manually keeps track to have a
consistent styling in the whole document.

A better way is to define macros for this.

#### Emphasizing with macros

To have a consistent styling of emphasizes, there is a predefined command

```Latex
\emph{Emphasized text}
```

For some documents this is sufficient, but sometimes is the need for different
emphasizes.

**Example:**

```Latex
... to init the connection use \code{connect} function form the \module{tcp}
module.
```

To have this specialized commands for emphasizing, we can use the

```Latex
\newcommand{\commandname}[number of parameter]{command body}
  % Given parameters can be referenced with '#1', ... '#9'
```

command from LaTeX.

**Example:**

```Latex
\newcommand{\code}[1]{\textit{#1}}

\newcommand{\module}[1]{{\itshape \bfseries #1}}
```

## Next:

[LaTeX References](LaTeX-References.md)

