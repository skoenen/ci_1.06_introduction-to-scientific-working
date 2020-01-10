# Introduction to scientific working

## Citation in LaTeX

LaTeX does come with a bibliography management system.
The `bibtex` system.

It uses a plain-text file database to store informations about citable material.
The entries in this database have a identifier and can be referenced in the
LaTeX document with this identifier.

**Example `bibdb.bib`:**

```Bibtex
@article{greenwade93,
    author  = "George D. Greenwade",
    title   = "The {C}omprehensive {T}ex {A}rchive {N}etwork ({CTAN})",
    year    = "1993",
    journal = "TUGBoat",
    volume  = "14",
    number  = "3",
    pages   = "342--351"
}
```

Such entries can then be referenced in several ways:

```Latex
\cite{greenwade93}

\cite[p.143]{greenwade93}

\cite{citation1, citation2, citation3}
```

With these commands in place, the LaTeX system is then formatting the citations
and references in the appendix section (if defined) according to the set style.

### Include blibliography in LaTeX

That the LaTeX system knows which bibliography database files should be
included, two additional commands are needed.

The best is to include them just before the `\end{document}`

```Latex
  \bibliographystyle{plain}
  \bibliography{file1,file2,file2}
\end{document}
```

And finally the following order of compiler commands have to run:

1. LaTeX to compile the source
2. BibTeX to generate references and entries for LaTeX compilation
3. LaTeX again to update references
4. LaTeX again to update the bibliography at the end of the document.

## Next:

[LaTeX Environments](LaTeX-Environment.md)

