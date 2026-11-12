# Beamer – Presentation Creation Using LaTeX

## 1. Introduction

Beamer is a LaTeX document class used to create professional presentations. It allows users to prepare slides using LaTeX commands instead of traditional presentation software.

Beamer is widely used for academic lectures, seminars, conferences, research presentations, and technical discussions.

## 2. Objectives

- To understand the Beamer presentation system.
- To learn how to create slides using LaTeX.
- To understand frames and themes.
- To insert images, tables, and mathematical equations.
- To learn how to organize and format presentations.

## 3. Features of Beamer

1. **Professional Slides:** Creates clean and well-structured presentations.
2. **Mathematical Support:** Supports complex mathematical equations.
3. **Themes:** Provides different presentation themes.
4. **Customization:** Allows users to customize colors, fonts, and layouts.
5. **Automatic Numbering:** Supports automatic slide numbering.
6. **Reusable Content:** Supports commands and environments for organizing content.

## 4. Basic Structure of a Beamer Presentation

A Beamer presentation begins with the `beamer` document class.

### Example

```latex
\documentclass{beamer}

\title{Introduction to Beamer}
\author{Neeraj Choudhary}
\institute{MNIT Jaipur}
\date{\today}

\begin{document}

\begin{frame}
    \titlepage
\end{frame}

\begin{frame}{Introduction}
    Beamer is used to create presentations
    using LaTeX.
\end{frame}

\end{document}
```

**Explanation:**

- `\documentclass{beamer}` selects the Beamer class.
- `\title{}` defines the presentation title.
- `\author{}` specifies the author.
- `\institute{}` specifies the institution.
- `\date{}` specifies the presentation date.
- `\begin{frame}` starts a new slide.
- `\titlepage` displays the title slide.
- `\end{frame}` ends a slide.

## 5. Frames in Beamer

A frame represents an individual slide in a presentation.

Example:

```latex
\begin{frame}{My First Slide}

    This is my first presentation slide.

\end{frame}
```

Each frame can contain text, images, tables, lists, and equations.

## 6. Creating Lists

Beamer supports both unordered and ordered lists.

### Unordered List

```latex
\begin{frame}{Features}

    \begin{itemize}
        \item Easy to use
        \item Professional design
        \item Mathematical support
    \end{itemize}

\end{frame}
```

### Ordered List

```latex
\begin{frame}{Steps}

    \begin{enumerate}
        \item Create a document.
        \item Add frames.
        \item Compile the presentation.
    \end{enumerate}

\end{frame}
```

## 7. Themes in Beamer

Themes control the overall appearance of slides.

Example:

```latex
\documentclass{beamer}

\usetheme{Madrid}

\begin{document}

\begin{frame}{Welcome}
    This presentation uses the Madrid theme.
\end{frame}

\end{document}
```

Some commonly used themes are:

| Theme | Description |
|---|---|
| Madrid | Clean and professional |
| Berlin | Navigation-oriented design |
| Copenhagen | Structured layout |
| Warsaw | Traditional presentation style |
| Singapore | Simple and minimal |

## 8. Color Themes

Beamer also allows users to change the color scheme.

Example:

```latex
\documentclass{beamer}

\usetheme{Madrid}
\usecolortheme{dolphin}

\begin{document}

\begin{frame}{Color Theme}
    This slide uses the Dolphin color theme.
\end{frame}

\end{document}
```

## 9. Adding Images

The `graphicx` package is used to insert images into slides.

Example:

```latex
\usepackage{graphicx}

\begin{frame}{Adding an Image}

    \centering
    \includegraphics[width=0.5\textwidth]{image.png}

    \captionof{figure}{Sample Image}

\end{frame}
```

The image must be available in the project directory. The `captionof` command requires the appropriate caption package; alternatively, use a `figure` environment inside the frame.

## 10. Adding Tables

Tables can be created using the `tabular` environment.

Example:

```latex
\begin{frame}{Student Marks}

\begin{tabular}{|c|c|}
\hline
Name & Marks \\
\hline
Amit & 90 \\
Rahul & 85 \\
Neha & 88 \\
\hline
\end{tabular}

\end{frame}
```

## 11. Mathematical Equations

Beamer supports mathematical expressions just like ordinary LaTeX.

Example:

```latex
\begin{frame}{Mathematical Equation}

\[
E = mc^2
\]

\[
a^2+b^2=c^2
\]

\end{frame}
```

This feature is especially useful for scientific and engineering presentations.

## 12. Columns in Beamer

Columns allow content to be arranged side by side on a slide.

Example:

```latex
\begin{frame}{Two Columns}

\begin{columns}

\column{0.5\textwidth}
Left Column

\column{0.5\textwidth}
Right Column

\end{columns}

\end{frame}
```

## 13. Highlighting Important Content

Beamer provides commands to highlight important information.

Example:

```latex
\begin{frame}{Important Information}

\alert{This is an important statement.}

\begin{block}{Definition}
Beamer is a presentation system based on LaTeX.
\end{block}

\begin{exampleblock}{Example}
A classroom presentation.
\end{exampleblock}

\begin{alertblock}{Warning}
Always compile the document before presenting.
\end{alertblock}

\end{frame}
```

## 14. Advantages of Beamer

- Produces professional presentations.
- Supports mathematical equations.
- Provides ready-made themes.
- Allows customization of slides.
- Supports images, tables, and diagrams.
- Maintains consistent formatting.

## 15. Applications of Beamer

Beamer is commonly used for:

- College presentations.
- Research seminars.
- Academic lectures.
- Technical conferences.
- Scientific presentations.
- Project demonstrations.

## 16. Conclusion

Beamer is a powerful LaTeX-based presentation system. It provides an effective way to create structured and professional slides with support for mathematical equations, images, tables, and customized themes. It is particularly useful for students, researchers, and professionals who prepare technical presentations.