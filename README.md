## comptemp.sty
A general LaTeX template file for competition maths submissions.
Place `comptemp.sty` in the same folder as your Latex Document.
### Usage
Your main tex file should somewhat look like this.
```
\documentclass{scrartcl}

\usepackage[OPTIONS]{comptemp}
\renewcommand{\theauthor}{NAME}
\renewcommand{\thetitle}{TITLE}

\begin{document}

% Title Page
\maketitle

% ...

\newpage

% ...

\end{document}
```
NOTE: Instead of the default `article` class, this package uses the KOMA-Script class `scrartcl`.

### Options
- `mline` sets a 5cm margin line, on the left by default
- `mlineswitch` switches the margin line to the right
- `norg` replaces the theoremboxes to exclude the colors red and green
- `asy` loads Asymptote-related packages

### Theoremboxes
Add the following to the preamble (before `\begin{document}`) to use theoremboxes and to correct formatting
```
\declaretheorem[name=NAME,style=stytheorembox]{lemma}
\declaretheorem[name=NAME,style=styclaimbox,numbered=no]{claim}
\declaretheorem[name=NAME,style=styproblembox]{problem}

\AfterEndEnvironment{lemma}{\vspace{-1em}}
\AfterEndEnvironment{claim}{\vspace{-1em}}
\AfterEndEnvironment{problem}{\vspace{-1em}}
```
and use it like you'd use a normal environment.
```
\begin{lemma}\label{lem:1.1}
  % ...
\end{lemma}
```
