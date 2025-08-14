## comptemp.sty
A LaTeX template file for competition maths submissions.
### Usage
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
- `mline` sets a 5cm margin line on the left
- `norg` replaces the theoremboxes to exclude the colors red and green
- `asy` loads Asymptote-related packages

### Theoremboxes
Add the following to the preamble to use theoremboxes and to correct formatting
```
\declaretheorem[name=NAME,style=stytheorembox]{lemma}
\declaretheorem[name=NAME,style=styclaimbox,numbered=no]{claim}
\declaretheorem[name=NAME,style=styproblembox]{problem}

\AfterEndEnvironment{lemma}{\vspace{-1em}}
\AfterEndEnvironment{claim}{\vspace{-1em}}
\AfterEndEnvironment{problem}{\vspace{-1em}}
```
