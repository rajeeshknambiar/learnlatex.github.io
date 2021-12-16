---
layout: "lesson"
lang: "ml"
title: "ചിത്രസംയോജനവും സ്ഥാനനിര്‍ണ്ണയവും"
description: "ബാഹ്യമായ ഒരു ചിത്രം എങ്ങനെ പ്രമാണത്തിൽ ചേര്‍ക്കാമെന്നും അതിന്റെ ബാഹ്യരൂപങ്ങൾ മാറ്റാമെന്നും പിഡിഎഫിൽ അനുയോജ്യമായ സ്ഥാനത്തേയ്ക്കു നീക്കാമെന്നും ഈ പാഠത്തിൽ പരിചയപ്പെടാം."
toc-anchor-text: "Using graphics"
toc-description: "ചിത്രസംയോജനവും സ്ഥാനനിര്‍ണ്ണയവും."
---

# ചിത്രസംയോജനവും സ്ഥാനനിര്‍ണ്ണയവും

<span
  class="summary">ബാഹ്യമായ ഒരു ചിത്രം എങ്ങനെ പ്രമാണത്തിൽ ചേര്‍ക്കാമെന്നും അതിന്റെ ബാഹ്യരൂപങ്ങൾ മാറ്റാമെന്നും പിഡിഎഫിൽ അനുയോജ്യമായ സ്ഥാനത്തേയ്ക്കു യാന്ത്രികമായി നീക്കാമെന്നും ഈ പാഠത്തിൽ പരിചയപ്പെടാം.</span>
  
 ലാറ്റെക്കിനു വെളിയിൽ നിന്നും ചിത്രം കൊണ്ടുവന്നു ചേര്‍ക്കാൻ `graphicx` പാക്കേജിലെ
 `\includegraphics` എന്ന ആജ്ഞ കൊണ്ടു സാധിക്കാം.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}

\begin{document}
This picture
\begin{center}
  \includegraphics[height=2cm]{example-image}
\end{center}
is an imported PDF.
\end{document}
```

EPS, PNG, JPG, PDF പ്രമാണരൂപങ്ങൾ നമുക്ക് ഉള്‍ക്കൊള്ളിക്കാം.
ഒരേ പേരിലുള്ള ഒന്നിലധികം ചിത്രരൂപങ്ങളുണ്ടെങ്കിൽ, ഉദാഹരണത്തിനു് `example-image.png`
എന്നെഴുതാം. (ഒന്നും പറഞ്ഞില്ലെങ്കിൽ വാലറ്റം ഏതെന്ന് ഊഹിക്കാൻ `graphicx` പാക്കേജ് ശ്രമിക്കും.)

`center` എന്ന ഒരു പുതിയ പരിസരം ചിത്രത്തെ തിരശ്ചീനമായി താളിന്റെ മദ്ധ്യത്തിൽ നിര്‍ത്താൻ ഉപയോഗിച്ചിരിക്കുന്നത്
നിങ്ങൾ ശ്രദ്ധിച്ചിരിക്കും. [അല്പം കഴിഞ്ഞ്](lesson-11) അകലം നല്കുന്നതിനെപ്പറ്റിയും സ്ഥാനം
നിര്‍ണ്ണയിക്കുന്നതിനെപ്പറ്റിയും നാം കൂടുതൽ ചര്‍ച്ച ചെയ്യും.

## ചിത്രത്തിന്റെ ബാഹ്യരൂപങ്ങളിൽ മാറ്റം വരുത്തുന്നത്

ഉള്‍ച്ചേര്‍ക്കുന്ന ചിത്രത്തിന്റെ വലിപ്പവും രൂപവും നിയന്ത്രിക്കാനും വെട്ടിയൊതുക്കാനുമായി `\includegraphics`
എന്ന ആജ്ഞയ്ക്ക് ധാരാളം ഐച്ഛികങ്ങളുണ്ട്. ഏറെ ഉപയോഗിക്കപ്പെടുന്ന ചിലതിനെപ്പറ്റി അറിഞ്ഞിരിക്കുന്നത്
ഉപകാരപ്പെടും.

പ്രകടമായും ക്രമീകരിക്കേണ്ടത് പലപ്പോഴും `\textwidth`, `\linewidth`,
`\textheight` എന്നിവയ്ക്ക് ആപേക്ഷികമായി ചിത്രത്തിന്റെ വീതി `width` അല്ലെങ്കിൽ ഉയരം `height`
ആയിരിക്കും. `\textwidth`, `\linewidth` എന്നിവ തമ്മിലുള്ള വ്യതാസം സൂക്ഷ്മമാണ്, പലപ്പോഴും
ഇവയുടെ ഫലം ഒന്നു തന്നെയായിരിക്കും. `\textwidth` എന്നത് ഭൗതികമായ താളിലെ പാഠഖണ്ഡത്തിന്റെ
വീതിയും, `\linewidth` എന്നത് _നിലവിലെ_ വീതിയുമാണ് (ഈ വ്യത്യാസം `twocolumn` എന്ന
പ്രമാണവര്‍ഗ്ഗ ഐച്ഛികത്തിൽ വളരെ പ്രകടമാണ്). വീക്ഷണാനുപാതം കൃത്യമാവുന്ന തരത്തിൽ 
ചിത്രത്തിന്റെ വിസ്താരം ലാറ്റെൿ സ്വയം ക്രമീകരിക്കും.


```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}

\begin{document}
\begin{center}
  \includegraphics[height = 0.5\textheight]{example-image}
\end{center}
Some text
\begin{center}
  \includegraphics[width = 0.5\textwidth]{example-image}
\end{center}
\end{document}
```

ചിത്രങ്ങളുടെ വിസ്താരം `scale` ഉപയോഗിച്ച് മാറ്റുകയോ, ഒരു കോണ്‍ `angle` ആധാരമാക്കി കറക്കുകയോ ചെയ്യാൻ സാധിക്കും.
ഒരു ചിത്രത്തെ `clip` ഉപയോഗിച്ച് മുറിക്കുവാനും `trim` ഉപയോഗിച്ച് വെട്ടിയൊതുക്കാനും മറ്റും സാദ്ധ്യമാണ്.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}

\begin{document}
\begin{center}
  \includegraphics[clip, trim = 0 0 50 50]{example-image}
\end{center}
\end{document}
```

## Making images float

Traditionally in typesetting, particularly with technical documents,
graphics may move to another spot in the document.
This is called a *float*. Images are normally included as floats so they do
not leave large gaps in the page.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}
\usepackage{lipsum}  % produce dummy text as filler

\begin{document}
\lipsum[1-4] % Just a few filler paragraphs

Test location.
\begin{figure}[ht]
  \centering
  \includegraphics[width=0.5\textwidth]{example-image-a.png}
  \caption{An example image}
\end{figure}

\lipsum[6-10] % Just a few filler paragraphs
\end{document}
```

Here LaTeX moves the graphic and the caption
away from the `Test location` text to the top of the second page,
because there isn't room for it on the bottom of the first page.
The `ht` influences where LaTeX can place the float; these two
letters mean that it can go where it is in the source (next to
`Test location`) or to the top of a page. You can use up to four position
specifiers

- `h` 'Here' (if possible)
- `t` Top of the page
- `b` Bottom of the page
- `p` A dedicated page only for floats

[Later](lesson-09), we will see how to cross-reference floats so you can point
to them from your text.

You'll probably spot that we've centered the image here using `\centering`
rather than the `center` environment. Inside a float, you should use
`\centering` if you want to horizontally center content; this avoids both
the float and `center` environment adding extra vertical space.

## Exercises

Try including an image you have created, replacing the 'standard' ones we have
used in the demonstration.

Explore what you can do using the `height`, `width`, `angle` and `scale` keys.

Use the `width` key to set the size of a graphic relative to `\textwidth` and
another graphic relative to `\linewidth`. Try out how they behave with or
without the `twocolumn` option.

Use `lipsum` to make a reasonably long demonstration, then try out placing
floats using the different position specifiers. How do different
specifiers interact?
