---
layout: "lesson"
lang: "ml"
title: "കൂടുതലറിയാൻ: ചിത്രങ്ങൾ ഉള്‍ക്കൊള്ളിക്കുന്നതും അവയുടെ സ്ഥാനവും"
description: "ലാറ്റെക്കിൽ ഉപയോഗിക്കാനുള്ള ചിത്രങ്ങളുടെ ഫയലുകൾ അനുയോജ്യമായ പേരിൽ സൂക്ഷിച്ചു വയ്ക്കുന്നതിനെപ്പറ്റിയും ലാറ്റെൿ ഉപയോഗിച്ചു തന്നെ ചിത്രങ്ങൾ നിര്‍മ്മിക്കുന്നതിനെപ്പറ്റിയും ഈ പാഠത്തിൽ കൂടുതലായി മനസ്സിലാക്കാം."
toc-anchor-text: "കൂടുതലറിയാൻ: ചിത്രങ്ങൾ ഉള്‍ക്കൊള്ളിക്കുന്നതും അവയുടെ സ്ഥാനവും"
---

## ചിത്രങ്ങളുടെ ഫയലുകള്‍ക്കു് പേരിടുന്നതു്

ലാറ്റെൿ പലവിധം കംപ്യൂട്ടർ സംവിധാനങ്ങളിൽ പ്രവര്‍ത്തിക്കുന്ന സോഫ്റ്റ്‌വെയറാണ്, അതിനാൽ
പ്രമാണങ്ങള്‍ക്കു്/ഫയലുകള്‍ക്കു് ഉപയോഗിക്കുന്ന പേരുകളിൽ അല്പം ശ്രദ്ധിക്കുന്നതു് നന്നായിരിക്കും.
എളുപ്പം ചെയ്യാവുന്ന സുരക്ഷിതമായ കാര്യമാണ് ഫയലുകളുടെ പേരിൽ വിടവ്/സ്പേസ് ഉപയോഗിക്കാതിരിക്കുക
എന്നതു്. ഉദാഹരണത്തിനു്, നിങ്ങളുടെ ചിത്രങ്ങൾ എല്ലാം (`pix`) എന്ന ഒരു സബ്ഡയരക്ടറിക്കകത്തു്
അടുക്കി വയ്ക്കുന്നെങ്കിൽ `\includegraphics[width=30pt]{pix/mom.png}` എന്ന തരത്തിൽ
പേരിടുന്നത് നല്ല രീതിയാണ്; അതാവുമ്പോൾ എല്ലായിടത്തും പ്രശ്നമില്ലാതെ പ്രവര്‍ത്തിക്കും.

പേരുകളിൽ വിടവ്/സ്പേസ് ഉള്ള പ്രമാണങ്ങൾ പ്രശ്നമുണ്ടാക്കാറുണ്ട്, പക്ഷേ ലാറ്റെൿ ഇപ്പോൾ അതു് പൊതുവേ
പിന്തുണക്കുന്നുണ്ട്. എങ്കിലും, പ്രമാണത്തിന്റെ പേരിൽ സ്പേസ് ഉള്ളതു കാരണം എന്തെങ്കിലും പ്രശ്നം നേരിടുന്നെങ്കിൽ
അതു് മാറ്റി നോക്കുക.

ചിഹ്നങ്ങളോ അവയുള്ള അക്ഷരങ്ങളോ പ്രമാണത്തിന്റെ പേരിലുണ്ടെങ്കിൽ അതിനുള്ള പിന്തുണ അത്ര ഉറപ്പുള്ളതല്ല,
പ്രത്യേകിച്ചും വിന്‍ഡോസ് പ്രവര്‍ത്തകത്തിൽ. ചിഹ്നങ്ങളുള്ള അക്ഷരങ്ങള്‍ക്കു പകരം ആസ്കി അക്ഷരങ്ങൾ ഉപയോഗിച്ചു നോക്കുക. 

## ചിത്രങ്ങൾ ഒരു സബ്ഡയരക്ടറിയിൽ സൂക്ഷിക്കുന്നതു്

എല്ലാ ചിത്രങ്ങളും ഒരു സബ്ഡയരക്ടറിക്കകത്ത് സൂക്ഷിക്കുന്നതു് പ്രമാണ സ്രോതസ്സുകൾ ചിട്ടപ്പെടുത്തി വയ്ക്കുന്നതിനു്
സാധാരണ അവലംബിക്കുന്ന ഒരു രീതിയാണു്. എന്നിട്ട് റ്റെൿ ഫയലിനകത്ത് ഈ സബ്ഡയരക്ടറിയുടെ ആപേക്ഷിക
സ്ഥാനം ഉള്‍പ്പെടുത്തിയാൽ മതി, മേൽ പ്രസ്താവിച്ച ഉദാഹരണത്തിലേതു പോലെ. ശ്രദ്ധിക്കുക, `/` അക്ഷരം
ഡയരക്ടറികളുടെ വിവിധ ഭാഗങ്ങളെ വേർതിരിക്കുവാൻ ഉപയോഗിക്കുന്നതാണ്, _വിന്‍ഡോസ് പ്രവര്‍ത്തകത്തിൽ ഉള്‍പ്പടെ_.

നിങ്ങളുടെ പ്രമാണത്തിൽ ധാരാളം ചിത്രങ്ങളുപയോഗിക്കുന്നുണ്ടെങ്കിൽ സബ്ഡയരക്ടറികൾ ഒറ്റ പ്രാവശ്യം ‍മുന്‍കൂട്ടി സ്പഷ്ടമാക്കുന്നത്
ചിത്രങ്ങള്‍ ഉള്‍പ്പെടുത്തുന്നിടത്ത് ആവര്‍ത്തിക്കാതിരിക്കാൻ സഹായിക്കും. `\graphicspath` ആജ്ഞ ഉപയോഗിച്ച് ഇതു്
സാധിക്കാം. ഈ ആജ്ഞയിൽ ഓരോ‌ സബ്ഡയരക്ടറിയും വക്രാവരണചിഹ്നത്തിനകത്ത് നല്കണം. ഉദാഹരണത്തിനു്
`figs`,`pics` എന്ന രണ്ടു സബ്ഡയരക്ടറികൾ ഉള്‍പ്പെടുത്തുന്നതു് ഇങ്ങനെയാണു്:

<!-- {% raw %} -->
```latex
\graphicspath{{figs/}{pics/}}
```
<!-- {% endraw %} -->

ഓരോന്നിനും അവസാനം ചേര്‍ത്തിട്ടുള്ള `/` പ്രത്യേകം ശ്രദ്ധിക്കുക.

## Producing graphics

As discussed, LaTeX easily uses graphics from most sources, including plots from
scientific software. When you do that, you probably want to save as a PDF if you
can, as this is a scalable format. If you do need to create a bitmap, aim for
high resolution. You can make mouse-created graphics that include LaTeX snippets
with [Inkscape](https://inkscape.org/). An alternative that in addition extends
those drawing techniques to three dimensions is
[Asymptote](https://www.ctan.org/pkg/asymptote). These two produce their output
as files that you include in your document.

You can also create graphics such as drawings that are especially suited to
LaTeX, with very high precision as well as equations and labels that match your
document. You can draw graphics directly inside your document, which is
convenient although at the cost of more complex documents with larger
requirements, by using [Ti*k*Z](https://ctan.org/pkg/pgf). An alternative is
[PSTricks](https://ctan.org/pkg/pstricks-base).

## Placing floats

LaTeX's float placement is complex.
The most common request is to have the figure placed
in the output exactly where it lies in the input.
The `float` package will do that.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}
\usepackage{lipsum}  % dummy text for filler
\usepackage{float}

\begin{document}
\lipsum[1-7]
\begin{figure}[H]
  \centering
  \includegraphics[width=0.5\textwidth]{example-image}
  \caption{An example image}
\end{figure}
\lipsum[8-15]
\end{document}
```

Note the `H` option, which puts the figure 'absolutely Here'.
However it is often not recommended to use `H`, because it may
create large portions of white space in your document.

## Other types of float

We will [see soon](lesson-08) that we can put tables in floats; they will go
into a `table` environment. However, we don't _have_ to put graphics in the
`figure` environment or tables in the `table` environment; this is just
convention.

You might want to have other types of floating environment; each type is
inserted independently. You can do that using the
[`trivfloat`](https://ctan.org/pkg/trivfloat) package. This provides a single
command, `\trivfloat`, to make new types of float.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}
\usepackage{lipsum}  % dummy text for filler
\usepackage{trivfloat}
\trivfloat{image}

\begin{document}
\begin{image}
  \centering
  \includegraphics[width=0.5\textwidth]{example-image}
  \caption{An example image}
\end{image}
\end{document}
```
