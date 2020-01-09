# Introduction to scientific working

## Environments in LaTeX

Previously introduced commands have an effect on text and does not provide
other structure then found in continuous text.

To have the ability to include informations in different other forms, LaTeX adds
environments.
These gives the possibility to include:

- Tables
- Describing List
- Itemizations
- Code
- Images

### Floating Environments

LaTeX differentiates between simple environments and "floating" environments.

Floating Environments provide additional capabilities:

- Define an anchor for referencing
- Define a caption
- Define a desired position on the page

Positions can be:

- h ↣ _here_, tries to place the float at the approximately point in text where
  it is defined in the LaTeX source.
- t ↣ _top_, try to position the float at the top of a page.
- b ↣ _bottom_, try to position the float at the bottom of a page.
- p ↣ _page_, try to put the float on a special page.
- H ↣ _HERE_, place the float at the exact position it is defined.
  May introduce problems.

### Tables

In LaTeX, information in tabular nature can be structured in tables. To do this
the `tabular` environment can be used.

```Latex
\begin{tabular}{ c c c }
  Cell A1 & Cell B1 & Cell C1 \\
  Cell A2 & Cell B2 & Cell C2 \\
  Cell A3 & Cell B3 & Cell C3 \\
\end{tabular}
```

This example defines a table with three columns, that are centered `{ c c c }`.
Other possibilities for alignment in cells are:

- `l`	↣ Left aligned
- `r`	↣ Right aligned
- `c`	↣ Centered

A row is a line of text ending with `\\` to indicate a new line.
Cells are seperated by the `&`.

Cell borders are defined in different places, the borders between columns are
defined in the column definition, example:

```Latex
\begin{tabular}{ c | c | c | }
  ...
\end{tabular}
```

In the above example the first column has no starting border, but a border to
the next column.
The last column has both borders.

Borders between rows have to be defined between rows, example:

```Latex
\begin{tabular}{ | l | r | c | }
  Head 1 & Head 2 & Head 3 \\
  \hline\hline
  Cell 1 & Cell 2 & Cell 3 \\
  \hline
  Cell 4 & Cell 5 & Cell 6 \\
  \hline
\end{tabular}
```

The `\hline` command tells the LaTeX system to include a horizontal line.

#### Captions and Titles for Tables

The `tabular` environment does not have the capabilities to define some options
that is often needed in scientific documents.

1. Tables are numbered
2. Tables have a short description what they display.
3. Tables can be listed in _List of Tables_ part of document.

To have these capabilities, the `tabular` environment has to be wrapped in
another environment.
The `table` environment:

```Latex
\begin{table}[ht]
  \caption{Top aligned caption for table}   % Defines the caption
  \centering                                % Centers the table in environment.

  \begin{tabular}{ l c c }
    \hline\hline                            % Have a double line between table
                                            % and caption.

    Head 1 & Head 2 & Head 3 \\             % Column heads
    \hline

    Cell A1 & Cell B1 & Cell C1 \\
    Cell A2 & Cell B2 & Cell C2 \\
    Cell A3 & Cell B3 & Cell C3 \\
    \hline                                  % Line to close table
  \end{tabular}

  \label{tab:example_table_1}               % Defines an anchor to this table
\end{table}
```

## Next:

[LaTeX and Descriptions](LaTeX-Descriptions.md)
