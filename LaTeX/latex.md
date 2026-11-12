# LaTeX – Document Preparation System

## 1. Introduction

LaTeX is a high-quality document preparation system used for creating professional documents. It is especially useful for writing technical documents, research papers, reports, books, and mathematical equations.

Unlike ordinary word processors, LaTeX uses markup commands to control document formatting and structure.

## 2. Objectives

- To understand the basics of LaTeX.
- To learn the structure of a LaTeX document.
- To format text using LaTeX commands.
- To write mathematical equations.
- To create tables, figures, and lists.
- To understand references and bibliography.

## 3. Features of LaTeX

1. **Professional Formatting:** Produces high-quality documents.
2. **Mathematical Support:** Easily writes complex mathematical equations.
3. **Automatic Numbering:** Automatically numbers sections, figures, and tables.
4. **Cross Referencing:** Supports references to sections, equations, and figures.
5. **Bibliography Management:** Supports citations and reference lists.
6. **Portability:** Documents can be compiled on different operating systems.

## 4. Basic Structure of a LaTeX Document

Every LaTeX document generally contains three main parts:

- Document class declaration.
- Preamble.
- Document environment.

### Example

```latex
\documentclass{article}

\usepackage{amsmath}

\title{My First LaTeX Document}
\author{Neeraj Choudhary}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}

This is my first LaTeX document.

\end{document}
```

**Explanation:**

- `\documentclass{article}` defines the document type.
- `\usepackage{amsmath}` imports mathematical features.
- `\title{}` defines the document title.
- `\author{}` specifies the author.
- `\begin{document}` starts the document.
- `\maketitle` displays the title.
- `\section{}` creates a section.
- `\end{document}` ends the document.

## 5. Document Classes

LaTeX provides different document classes depending on the type of document.

| Document Class | Purpose |
|---|---|
| article | Articles and short reports |
| report | Long reports |
| book | Books |
| letter | Letters |
| beamer | Presentations |

Example:

```latex
\documentclass[12pt,a4paper]{article}
```

Here, `12pt` specifies font size and `a4paper` specifies the paper size.

## 6. Text Formatting

LaTeX provides commands for formatting text.

| Command | Purpose |
|---|---|
| `\textbf{Text}` | Bold text |
| `\textit{Text}` | Italic text |
| `\underline{Text}` | Underlined text |
| `\texttt{Text}` | Typewriter font |
| `\emph{Text}` | Emphasized text |

Example:

```latex
\begin{document}

\textbf{Bold Text}

\textit{Italic Text}

\underline{Underlined Text}

\end{document}
```

## 7. Lists in LaTeX

LaTeX supports two major types of lists.

### Unordered List

```latex
\begin{itemize}
    \item LaTeX
    \item Beamer
    \item Doxygen
\end{itemize}
```

### Ordered List

```latex
\begin{enumerate}
    \item Introduction
    \item Features
    \item Conclusion
\end{enumerate}
```

## 8. Mathematical Equations

One of the most important features of LaTeX is its ability to represent mathematical equations.

### Inline Equation

```latex
The equation is $a^2+b^2=c^2$.
```

### Display Equation

```latex
\[
a^2+b^2=c^2
\]
```

### Fraction

```latex
\[
\frac{a+b}{c}
\]
```

### Summation

```latex
\[
\sum_{i=1}^{n} i
\]
```

### Matrix

```latex
\[
A =
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\]
```

## 9. Tables in LaTeX

Tables are created using the `tabular` environment.

Example:

```latex
\begin{center}
\begin{tabular}{|c|c|c|}
\hline
Name & Subject & Marks \\
\hline
Amit & Maths & 90 \\
Rahul & Physics & 85 \\
Neha & Chemistry & 88 \\
\hline
\end{tabular}
\end{center}
```

**Explanation:**

- `|` creates vertical borders.
- `c` aligns content in the center.
- `&` separates columns.
- `\\` moves to the next row.
- `\hline` creates a horizontal line.

## 10. Figures and Images

LaTeX uses the `graphicx` package to insert images.

Example:

```latex
\usepackage{graphicx}

\begin{document}

\begin{figure}[h]
    \centering
    \includegraphics[width=0.5\textwidth]{image.png}
    \caption{Sample Image}
    \label{fig:sample}
\end{figure}

\end{document}
```

The image file should be available in the project directory or at the specified path.

## 11. References and Bibliography

References are used to give credit to the original sources of information.

Example:

```latex
\section{Introduction}

LaTeX is widely used for technical writing
\cite{lamport1994}.

\bibliographystyle{plain}
\bibliography{references}
```

Create a separate file named `references.bib`:

```bibtex
@book{lamport1994,
    author = {Leslie Lamport},
    title = {LaTeX: A Document Preparation System},
    year = {1994},
    publisher = {Addison-Wesley}
}
```

The `\cite{lamport1994}` command inserts a citation, while the bibliography commands generate the reference list.

## 12. Advantages of LaTeX

- Produces professional-quality documents.
- Excellent support for mathematical expressions.
- Automatically manages numbering.
- Supports large documents and chapters.
- Provides consistent formatting.
- Useful for academic and technical writing.

## 13. Applications of LaTeX

LaTeX is commonly used in:

- Research papers.
- Scientific publications.
- Engineering reports.
- Academic assignments.
- Books and technical manuals.
- Mathematical and scientific documentation.

## 14. Conclusion

LaTeX is a powerful document preparation system that helps users create well-structured and professional documents. Learning LaTeX improves technical writing skills and is particularly useful for students, researchers, and engineers.