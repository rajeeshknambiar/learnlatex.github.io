---
layout: "lesson"
lang: "ml"
title: "കൂടുതലറിയാൻ: പ്രതിനിര്‍ദേശങ്ങള്‍"
description: "hyperref പൊതിക്കെട്ടുപയോഗിച്ച് പ്രതിനിര്‍ദ്ദേശങ്ങള്‍ക്ക് കണ്ണികൾ ഉണ്ടാക്കുന്നതെങ്ങനെയെന്ന് ഈ പാഠത്തിൽ കാണാം."
toc-anchor-text: "കൂടുതലറിയാൻ: പ്രതിനിര്‍ദേശങ്ങള്‍"
---

## പ്രതിനിര്‍ദേശങ്ങളെ കണ്ണികളാക്കി മാറ്റുന്നത്

`hyperref` പൊതിക്കെട്ടുപയോഗിച്ച് നിങ്ങളുടെ പ്രതിനിര്‍ദ്ദേശങ്ങളെ (cross-references) കണ്ണികൾ (ഹൈപ്പർലിങ്കുകൾ)
ആക്കി മാറ്റാം. മിക്ക സന്ദര്‍ഭങ്ങളിലും `hyperref` മറ്റെല്ലാ പൊതിക്കെട്ടുകളും പ്രമാണത്തിന്റെ പ്രാരംഭത്തിൽ ചേര്‍ത്തതിനു ശേഷം
മാത്രം നല്കേണ്ടതാണു്.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage[hidelinks]{hyperref}
\begin{document}

\section{Introduction}
Some exciting text with a reference~\ref{sec:next}.

\section{Next thing}
\label{sec:next}

More text here.
\end{document}
```

സാധാരണ പാഠഭാഗത്തിന്റെ അതേ നിറമാണ് ഞങ്ങളിവിടെ കണ്ണികള്‍ക്കും കൊടുത്തിരിക്കുന്നതു്, എന്തിനാണെന്നറിയാൻ 
`hidelinks` എടുത്തുകളഞ്ഞതിനു് ശേഷം നോക്കുക!
