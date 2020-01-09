# Introduction to scientific working

## References and citation in LaTeX

LaTeX differentiates between references to literature or papers and parts,
sections objects of the document itself.

### Referencing parts of the document.

In LaTeX the numbering of parts is not exactly specified on writing.
It is done by LaTeX compiler.
This confronts the writer of a document with the problem to mention a specific
part in the text.

To accommodate this problem LaTeX provides a command to define anchors to parts
of interest.

```Latex
\label{MARKER}
```

These marker then can be referenced with two commands in the text:

```Latex
\ref{MARKER} % Reference a specified marker

\pageref{MARKER} % Print the page number the labeled MARKER is on.
```

The label instruction has to come after or inside a `\caption` if it is desired
to anchor on a figure, table or other with a caption.
If it is defined before the caption, the label will pick up the chapter, section
or other as anchor.

#### Best Practices

After defining a lot of anchors, that possibly also have similar topics and
similar markers, an author can loose track of which marker is to use for a
reference.

Therefore it is a best practice among LaTeX authors to define the anchors
according some patterns, example:

- `chap:MARKER` ↣ Anchor for chapters
- `sec:MARKER` ↣ Anchor for sections
- `subsec:MARKER` ↣ Anchor for sub sections
- `fig:MARKER` ↣ Anchor for a figure
- `tab:MARKER` ↣ Anchor for a table
- `eq:MARKER` ↣ Anchor for equation
- `lst:MARKER` ↣ Anchor for a code listing
- `itm:MARKER` ↣ Anchor for an enumeration list
- `app:MARKER` ↣ Anchor for an appendix subsection

But these is not enforced an authors are free to choose what suits them best.

#### Enhancing `\ref`

Often it is cumbersome to write:

```Latex
See figure \ref{fig:birds} on page \pageref{fig:birds} to see an example of the
new found species.
```

To accommodate this there are additional packages:

- `varioref`
- `hyperref`
- `cleveref`

## Next:

[LaTeX Citations](LaTeX-Citations.md)

