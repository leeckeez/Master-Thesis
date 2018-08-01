## FIIW Master Thesis LaTeX template
This repo holds a master thesis template for the FIIW. The `fiiw.sty`file provides the package with all layout specifications. All other files are a previw implementation for a master thesis paper.

### Usage
Include `\usepackage[groept]{fiiw}` in your main tex file. For usage on an other campus replace replace `groept`with your campus name. For now only `groept` and `denayer` are supported.
Extra options can be added like : `noacknowledgements`, `noabstract`, `noextendedabstract`, `nolistoffigures`, `nolistoftables`, `nolistofsymbols`
The fiiw-package expects some basic information like thesis title, student names,... to be set. Check the basic example below or the preview implementation for further info.

#### Basic example
```latex
\documentclass[11pt,a4paper]{report}
\usepackage[groept,nolistofsymbols]{fiiw}

%% .tex file with acknowledgements
\acknowledgementsfile{chapters/acknowledgements}
%% .tex file with abstract
\abstractfile{chapters/abstract}
%% .tex file with extended abstract
\extendedabstractfile{chapters/abstract-extended}
%% .tex file with list of symbols
\listofsymbolsfile{chapters/symbols}

\program{Electronics Engineering}
\title{Thesis Title}
\subtitle{Thesis Subtitle (optional)}
\firstnameA{Firstname}
\lastnameA{Lastname}
\firstnameB{Firstname2}    %optional
\lastnameB{Lastname2}      %optional
\academicyear{2017 - 2018}
\promotor{My Promotor}
\copromotor{My Co-promotor\newline(My company promotor)}

\begin{document}
  \selectlanguage{english}
  \preface

  ...

  \backcover
\end{document}
```
