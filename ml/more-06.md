---
layout: "lesson"
lang: "ml"
title: "കൂടുതലറിയാൻ: പാക്കേജുകളും നിർവചനങ്ങളും ഉപയോഗിച്ചു് ലാറ്റെക്കിനെ വിപുലീകരിക്കൽ"
description: "പാക്കേജുകൾ എങ്ങനെ ഉപയോഗിക്കാം, വിവിധഭാഷകളുപയോഗിക്കാനുള്ള ബാബൽ പാക്കേജ്,
നിങ്ങളുടേതായ ആജ്ഞകൾ എന്നിവയെക്കുറിച്ച് കൂടുതൽ വിവരങ്ങൾ ഈ പാഠത്തിൽ കാണാം."
toc-anchor-text: "കൂടുതലറിയാൻ: പാക്കേജുകളും നിർവചനങ്ങളും ഉപയോഗിച്ചു് ലാറ്റെക്കിനെ വിപുലീകരിക്കൽ"
---

## ഒന്നിലധികം പൊതിക്കെട്ടുകളുടെ (പാക്കേജുകൾ) ഉപയോഗം

`\usepackage` എന്ന ആജ്ഞ അല്പവിരാമം (കോമ) ഉപയോഗിച്ച് വേര്‍തിരിച്ച ഒരുപിടി പൊതിക്കെട്ടുക സ്വീകരിക്കും.
`\usepackage{color,graphicx}` എന്ന ഉദാഹരണം പോലെ കുറേ പൊതിക്കെട്ടുകൾ ഒറ്റയടിക്ക് ഉപയോഗിക്കാം.
ഏതെങ്കിലും പൊതിക്കെട്ടിനുള്ള ഐച്ഛികവാദം ഇവ്വിധം കൊടുത്താൽ കൂട്ടത്തിലുള്ള എല്ലാ പൊതിക്കെട്ടുകള്‍ക്കും അത് ബാധകമാവും.
എന്നാൽ പൊതിക്കെട്ടുകൾ ഓരോന്നോരോന്നായിൽ നല്കുകയാണെങ്കിൽ അവയെ തല്ക്കാലത്തേയ്ക്ക് മറച്ചു വയ്ക്കാൻ എളുപ്പമുണ്ട്.
അതുകൊണ്ട് നമ്മളിപ്പോൾ ഓരോ പൊതിക്കെട്ടും ഓരോ വരിയിൽ നല്കുന്ന രീതി തന്നെ തുടരും.

## ‘ബാബൽ’ പൊതിക്കെട്ട്

[പ്രധാന പാഠത്തിൽ](lesson-06) വാക്കുകൾ മുറിക്കാനുള്ള (തുടര്‍ക്കുറി) വിവിധ മാതൃകകൾ തിരഞ്ഞെടുക്കാനുള്ള
ഒരു വഴിയായി `ബാബൽ` പൊതിക്കെട്ടിനെ പരിചയപ്പെടുത്തിയിരുന്നു. തിരഞ്ഞെടുത്ത ഭാഷയ്ക്കനുസരിച്ച് ഒട്ടനവധി
കാര്യങ്ങൾ കൂടി അതു ചെയ്യുന്നുണ്ട്. ഉദാഹരണത്തിന് നീണ്ട വാക്കുകൾ സാധാരണമായ ജര്‍മ്മൻ ഭാഷയിൽ 'സോഫ്റ്റ്'
ഹൈഫൻ (തുടര്‍ക്കുറി) നിര്‍മ്മിക്കുവാൻ പലതരം ചുരുക്കെഴുത്തുകൾ നല്കുന്നതു കൂടാതെ, ജര്‍മ്മൻ കീബോഡില്ലാതെ തന്നെ
ഉച്ചാരണചിഹ്നങ്ങൾ എളുപ്പം ടൈപ്പ് ചെയ്യാനും സഹായിക്കും. `\tableofcontents` എന്ന ആജ്ഞ ഉപയോഗിച്ചാൽ
സാധാരണ ഉണ്ടാക്കുന്ന _ഉള്ളടക്കം_ (വിഷയസൂചിക) എന്ന തലക്കെട്ടും ജര്‍മ്മൻ ഭാഷയിലെ Inhaltsverzeichnis
എന്നായി മാറുന്നതു് ശ്രദ്ധിക്കുക.

കുറിപ്പ്: മലയാളം ഉള്‍പ്പടെയുള്ള ഭാരതീയഭാഷകള്‍ക്ക് അനുയോജ്യമായ പൊതിക്കെട്ട് 'പോളിഗ്ലോസിയ' (polyglossia)
ആണ്, ഇതേ സൗകര്യങ്ങൾ അതിലും ലഭ്യമാണു്.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\usepackage[ngerman]{babel} % Notice that the option name is 'ngerman'

\begin{document}

\tableofcontents

\section{"Uber "Apfel und Birnen}

\subsection{Äpfel}
Äpfel sind rot.

\subsection{Birnen}
Birnen sind gelb.


\end{document}
```

മറ്റു ഭാഷാ സജ്ജീകരണങ്ങൾ രൂപകല്പനയ്ക്കു ഭേദഗതികൾ വരുത്താറുണ്ട്, ഉദാഹരണത്തിനു് സാമ്പ്രദായിക
ഫ്രഞ്ച് മുദ്രണകലയിൽ `:` പോലുള്ള ചില വിരാമചിഹ്നങ്ങള്‍ക്കു മുമ്പിൽ ഒരു വിടവ് നിലനിര്‍ത്താറുണ്ട്,
`french` എന്ന ഐച്ഛികത്തോടു കൂടി `babel` സജ്ജമാക്കിയിൽ ഈ മാറ്റം സ്വയമേവ അച്ചടിയിൽ
വന്നു കൊള്ളും.

## Global options

Sometimes, you want an option to be available to all of the packages you've
loaded. That is done by giving it on the `\documentclass` line: every package
can 'see' this list. So to pass the language of a document to all packages,
we might use:

```latex
\documentclass[ngerman]{article} % Notice that the option name is 'ngerman'
\usepackage[T1]{fontenc}

\usepackage{babel}

\begin{document}

\tableofcontents

\section{"Uber "Apfel und Birnen}

\subsection{Äpfel}
Äpfel sind rot.

\subsection{Birnen}
Birnen sind gelb.

\end{document}
```

## More definitions

`\newcommand` allows commands with up to nine arguments, the first of which may be optional.

If we take the example from the main lesson, we could make the color
optional, defaulting to blue.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\usepackage{xcolor}

\newcommand\kw[2][blue]{\textcolor{#1}{\itshape #2}}

\begin{document}

Something about \kw{apples} and \kw[red]{oranges}.

\end{document}
```

Optional arguments are delimited with `[]` and if omitted, the default
value specified in the definition is used.

## `\NewDocumentCommand`

From the October 2020 LaTeX release, an extended definition system is available.
In older LaTeX releases this was available via the `xparse` package which we use
here for compatibility.

We can repeat the above example but using `\NewDocumentCommand`

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\usepackage{xparse} % Only needed for older LaTeX releases
\usepackage{xcolor}

\NewDocumentCommand\kw{O{blue} m}{\textcolor{#1}{\itshape #2}}

\begin{document}

Something about \kw{apples} and \kw[red]{oranges}.

\end{document}
```

Just as with `\newcommand`, `\NewDocumentCommand` takes the command
being defined (`\kw` here) and the definition body, using `#1` to `#9`
for the arguments, however the difference is in how the arguments are
specified.

Unlike `\newcommand` where just the number of arguments is given,
optionally supplying a default for the first, with
`\NewDocumentCommand` each argument is specified by a letter so a two
argument command would be specified by `{mm}` rather than `[2]`. This
is slightly more verbose but allows many more forms of commands to be
defined. Here we just give this simple example where the first
argument is optional, defaulting to blue (`O{blue}`) and the second
argument is mandatory (`m`).
