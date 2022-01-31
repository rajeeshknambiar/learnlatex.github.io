---
layout: "lesson"
lang: "ml"
title: "അവലംബങ്ങളും പരാമര്‍ശങ്ങളും"
description: "അവലംബ സഞ്ചയങ്ങളുടെ അടിസ്ഥാനപാഠങ്ങൾ ഈ അദ്ധ്യായത്തിൽ പരിചയപ്പെടാം. ലഭ്യമായ രണ്ടു പ്രമുഖ പ്രവര്‍ത്തനരീതികളുപയോഗിച്ച് നിങ്ങള്‍ക്കാവശ്യമുള്ള അവലംബ സഞ്ചയങ്ങൾ നിര്‍മ്മിക്കുന്നതെങ്ങനെയെന്നും പ്രമാണങ്ങളിൽ അവ എങ്ങനെ പ്രയോജനപ്പെടുത്താമെന്നും പഠിക്കാം."
toc-anchor-text: "അവലംബങ്ങളും പരാമര്‍ശങ്ങളും"
toc-description: "അവലംബ സഞ്ചയങ്ങളുടെ പ്രയോഗം."
---

<!--
(workflow) പ്രവര്‍ത്തനരീതി
(reference database) അവലംബ സഞ്ചയം
(manual/manually) മാനുഷികപ്രയത്നം
(process) പരിവര്‍ത്തനം/പ്രക്രിയ
-->


# അവലംബങ്ങളും (citations) പരാമര്‍ശങ്ങളും (references)

<script>
runlatex.preincludes = {
 "pre1": {
    "pre0": "learnlatex.bib"
   },
 "pre2": {
    "pre0": "learnlatex.bib"
   }
}
</script>

<span
  class="summary">അവലംബ സഞ്ചയങ്ങളുടെ അടിസ്ഥാനപാഠങ്ങൾ ഈ അദ്ധ്യായത്തിൽ പരിചയപ്പെടാം. ലഭ്യമായ രണ്ടു പ്രമുഖ പ്രവര്‍ത്തനരീതികളുപയോഗിച്ച് നിങ്ങള്‍ക്കാവശ്യമുള്ള അവലംബ സഞ്ചയങ്ങൾ നിര്‍മ്മിക്കുന്നതെങ്ങനെയെന്നും പ്രമാണങ്ങളിൽ അവ എങ്ങനെ പ്രയോജനപ്പെടുത്താമെന്നും പഠിക്കാം.</span>

ഗ്രന്ഥസൂചി അവലംബങ്ങൾക്കു് ആവശ്യമുള്ള പരാമര്‍ശ സ്രോതസ്സുകൾ നിങ്ങള്‍ക്കു് നേരിട്ട് പ്രമാണത്തിൽ ചേര്‍ക്കാമെങ്കിലും
സാധാരണ അത്തരം വിവരങ്ങൾ ഒന്നോ അതില്‍ക്കൂടുതലോ ബാഹ്യ ഫയലുകളിൽ നിന്നാണു് ലഭ്യമാക്കാറ്.
പരിവര്‍ത്തനസൗഹൃദമായ തരത്തിലുള്ള വിവരഘടനയുള്ള അവലംബസ്രോതസ്സുകളുടെ സഞ്ചയമാണ് അത്തരമൊരു ഫയൽ.
ഒന്നോ അതില്‍ക്കൂടുതലോ അവലംബ സഞ്ചയങ്ങൾ വഴി വിവരങ്ങൾ പുനരുപയോഗിക്കാനും രൂപഘടന മാറ്റുന്നതിനു്
മാനുഷികപ്രയത്നം ഒഴിവാക്കാനും സഹായിക്കുന്നു.

## അവലംബ സഞ്ചയങ്ങൾ

അവലംബ സഞ്ചയങ്ങൾ സാധാരണ അറിയപ്പെടുന്നതു് 'ബിബ്ടെൿ ഫയലുകൾ' എന്നാണു്, അവയുടെ വാലറ്റം
`.bib` എന്നായിരിക്കും. ഒന്നിലധികം അവലംബങ്ങളും, ഓരോ അവലംബത്തിനും ഒരു ഉള്ളടക്കവും, അവയ്ക്കുള്ളിൽ
ഒരുപറ്റം അംഗങ്ങളും അടങ്ങിയതാവും ഒരു സഞ്ചയം. ഒരുദാഹരണം നോക്കാം.

<!-- {% raw %} -->
```bibtex
@article{Thomas2008,
  author  = {Thomas, Christine M. and Liu, Tianbiao and Hall, Michael B.
             and Darensbourg, Marcetta Y.},
  title   = {Series of Mixed Valent {Fe(II)Fe(I)} Complexes That Model the
             {H(OX)} State of [{FeFe}]Hydrogenase: Redox Properties,
             Density-Functional Theory Investigation, and Reactivity with
             Extrinsic {CO}},
  journal = {Inorg. Chem.},
  year    = {2008},
  volume  = {47},
  number  = {15},
  pages   = {7009-7024},
  doi     = {10.1021/ic800654a},
}
@book{Graham1995,
  author    = {Ronald L. Graham and Donald E. Knuth and Oren Patashnik},
  title     = {Concrete Mathematics},
  publisher = {Addison-Wesley},
  year      = {1995},
}
```
<!-- {% endraw %} -->

ഏറ്റവും സാധാരണമായ രണ്ടു തരങ്ങളായ ലേഖനത്തിനും പുസ്തകത്തിനും വേണ്ട ഉള്ളടക്കങ്ങളാണു് ഇവ.
ഓരോ അവലംബത്തിന്റെയും തരം ആരംഭിക്കുന്നതു് `@` വച്ചാണു്, അതിനുള്ളിലെ എല്ലാ വിവരവും ഒരു ജോടി
വക്രാവരണചിഹ്നങ്ങള്‍ക്കകത്താണു്.

അവലംബത്തിന്റെ 'മേല്‍വിലാസം' ആയ 'സൂചകനാമം' എന്നതൊഴിച്ച്, നമുക്കാവശ്യമുള്ള മറ്റെല്ലാ
വിവരഘടകങ്ങളും സൂചകം-ഉള്ളടക്കം എന്ന രീതിയിലാണു് നല്കുക. 'സൂചകനാമം' എന്തുവേണമെങ്കിലും
നല്കാം, അതൊരു 'മേല്‍വിലാസം' മാത്രമാണു്, പക്ഷേ പ്രചാരത്തിലുള്ള രീതിയനുസരിച്ച് ഗ്രന്ഥകര്‍ത്താവിന്റെ
പേരും പ്രസിദ്ധീകരിച്ച വര്‍ഷവും ചേര്‍ത്ത ഒരു മേല്‍വിലാസമാണു് നമ്മളുപയോഗിച്ചതു്.

കൃത്യമായി ഏതു വിവരഘടകങ്ങളാണു് നല്കേണ്ടതു് എന്നതു് അവലംബത്തിന്റെ തരം അനുസരിച്ചിരിക്കും, പക്ഷേ
മിക്കതും എളുപ്പം സ്പഷ്ടമാണു്. `author` എന്ന വിവരഘടകത്തിനകത്തു് ഓരോ ആള്‍ക്കാരുടെ പേരുകളും
`and` ഉപയോഗിച്ചു് വേര്‍തിരിച്ചിരിക്കുന്നതു് ശ്രദ്ധിച്ചിരിക്കുമല്ലോ. ഇതു് _അത്യാവശ്യമാണു്_, എന്തെന്നാൽ
ഉള്ളടക്കം വിന്യസിക്കുന്നതിന്റെ രീതിയ്ക്ക് കൃത്യമായും ഏതു ഗ്രന്ഥകര്‍ത്താവ് ഏതാണു് എന്നറിയേണ്ടതുണ്ട്.
ലേഖനശീര്‍ഷകത്തിലെ ചില വാക്കുകൾ പ്രത്യേകമായും വക്രാവരണചിഹ്നങ്ങള്‍ക്കകത്താണെന്നതും ശ്രദ്ധിച്ചിരിക്കും,
ഇതു വലിയക്ഷരങ്ങളെ ചെറിയക്ഷരങ്ങളായി തനിയെ മാറ്റുന്നതു് തടയുവാനാണു്.

`.bib` പ്രമാണങ്ങളെ സ്വയം നിര്‍മ്മിക്കുന്നതും തിരുത്തുന്നതും വിരസമായ ജോലിയാണു്, മിക്കവരും ഇതിനനുയോജ്യമായ
ഒരു എഡിറ്റർ ഉപയോഗിക്കാറാണു് പതിവ്. [ജാബ്റെഫ്](https://www.jabref.org) വളരെ പ്രചാരമുള്ളതും
എല്ലാ ഓപ്പറേറ്റിങ് പ്രവര്‍ത്തകങ്ങളിലും ലഭ്യമായതുമാണു്, കൂടാതെ മറ്റനവധി സംവിധാനങ്ങളുമുണ്ട്. അവലംബത്തിന്റെ
DOI (Digital Object Identifier) ലഭ്യമാണെങ്കിൽ അതിന്റെ ബിബ്ടെൿ ഉള്ളടക്കം എളുപ്പത്തിൽ കിട്ടാൻ
[doi2bib](https://doi2bib.org) ഉപയോഗിച്ചു നോക്കാവുന്നതാണു്; പക്ഷേ ഉള്ളടക്കം ശരിയാണെന്നു്
ഉറപ്പുവരുത്തുക!

മുകളിൽ കാണിച്ച ചെറു സഞ്ചയം നമ്മുടെ പ്രവര്‍ത്തനത്തിനുപയോഗിക്കാം, അതിനെ `learnlatex.bib`
എന്ന പേരിൽ സൂക്ഷിച്ചിട്ടുണ്ടു്.

## സഞ്ചയത്തിലുള്ള വിവരങ്ങൾ പ്രമാണത്തിൽ ഉള്‍ച്ചേര്‍ക്കുന്നത്

അവലംബ വിവരങ്ങൾ നിങ്ങളുടെ പ്രമാണത്തിൽ ഉള്‍ക്കൊള്ളിക്കുന്നതിനു് മൂന്നു കാര്യങ്ങൾ ചെയ്യാനുണ്ട്.
ആദ്യം, ലാറ്റെൿ ഉപയോഗിച്ച് പ്രമാണം കംപൈൽ ചെയ്യൂമ്പോൾ അതിൽ പരാമര്‍ശിച്ചിട്ടുള്ള എല്ലാ
അവലംബങ്ങളുടെയും പട്ടിക ഒരു ഫയലിലെഴുതപ്പെടും. രണ്ടാമതു്, ഒരു പ്രോഗ്രാം പ്രവര്‍ത്തിപ്പിച്ച്
പ്രമാണത്തിലുപയോഗിച്ചിട്ടുള്ള വിവരങ്ങൾ മാത്രം അവലംബസഞ്ചയത്തിൽ നിന്നെടുത്തു് കൃത്യമായ
ക്രമത്തിൽ അവയെ ഒരുക്കിവയ്ക്കും. അവസാനമായി, പ്രമാണം ഒന്നു കൂടി കംപൈൽ ചെയ്യുമ്പോൾ
ലാറ്റെക്കിനു് ലഭ്യമായ വിവരങ്ങളുപയോഗിച്ച് അവലംബങ്ങൾ സ്പഷ്ടമായി പ്രമാണത്തിൽ അതതു സ്ഥാനത്ത്
വിന്യസിക്കുവാൻ സാധിക്കും. സാധാരണഗതിയിൽ ചുരുങ്ങിയതു് രണ്ടു വട്ടമെങ്കിലും കംപൈൽ ചെയ്താലേ
എല്ലാ പരാമര്‍ശ സ്ഥലങ്ങളിലും വിവരം ശരിയായി പ്രത്യക്ഷമാകുകയുള്ളൂ.

ഇതിൽ രണ്ടാമത്തെ പടിയിലെ പ്രയോഗത്തിനായി രണ്ടു് സംവിധാനങ്ങളാണു് പ്രചാരത്തിലുള്ളതു്: ബിബ്ടെൿ (BibTeX),
ബിബെർ (Biber) എന്നിവ. ബിബെർ എല്ലായ്പോഴും `biblatex` എന്ന ലാറ്റെൿ പാക്കേജിനോടു കൂടെയേ ഉപയോഗിക്കാറുള്ളൂ,
ബിബ്ടെൿ പ്രത്യേകം പാക്കേജുകളില്ലാതെയോ `natbib` പാക്കേജിനോടു കൂടെയോ ഉപയോഗിക്കാം.

ഈ രണ്ടാമത്തെ ഉപകരണവും ലാറ്റെക്കൂം ഒരുമിച്ചു് പ്രവര്‍ത്തിപ്പിക്കുന്നത് പല എഡിറ്ററുകളും പല വിധത്തിലാണു ചെയ്യുന്നതു്.
നമ്മുടെ ഓണ്‍ലൈൻ ഉദാഹരണങ്ങളിൽ ഒറ്റയടിക്ക് ഇതെല്ലാം ചെയ്യുന്ന ചില കുറിപ്പുകൾ 'പിന്നണിയിൽ' പ്രവര്‍ത്തിക്കുന്നുണ്ട്.
നിങ്ങളുപയോഗിക്കുന്ന എഡിറ്ററിൽ 'എല്ലാം' ചെയ്യുന്ന ഒറ്റ ബട്ടൻ ഒരുപക്ഷേ ഉണ്ടായിരിക്കും; ഇല്ലെങ്കിൽ ലാറ്റെൿ രണ്ടുപ്രാവശ്യം
കംപൈൽ ചെയ്യുന്നതിനിടയിൽ ബിബ്ടെക്കോ ബിബെറോ നിങ്ങൾ തന്നെ പ്രവര്‍ത്തിപ്പിക്കേണ്ടി വരും.

അവലംബങ്ങളുടെയും പരാമര്‍ശങ്ങളുടെയും കാഴ്ചയ്ക്കു വേണ്ട വിന്യാസരീതി ബിബ്ടെൿ സഞ്ചയത്തിന്റെ ഉള്ളടക്കത്തിൽ നിന്നും
സ്വതന്ത്രമാണു്, അതു ക്രമപ്പെടുത്തുന്നത് 'സ്റ്റൈൽ' എന്നറിയപ്പെടുന്ന ഒരു സംഗതി വഴിയാണു്. ബിബ്ടെൿ ഉപയോഗിക്കുമ്പൊഴും
ബിബ്‌ലാറ്റെൿ ഉപയോഗിക്കുമ്പൊഴും  അല്പം വ്യത്യാസത്തോടെയാണ് ഇവ പ്രവര്‍ത്തിക്കുന്നതു് എന്നു് അടുത്തുതന്നെ നാം
കാണും, പക്ഷേ പൊതുവായ ആശയം ഒന്നുതന്നെ: പരാമര്‍ശങ്ങൾ എങ്ങനെ കാണപ്പെടുന്നു എന്നതു് നമുക്കു്
തീരുമാനിക്കാം.

## The BibTeX workflow with `natbib`

Whilst it is possible to insert citations into a LaTeX document without
any packages loaded, this is rather limited. Instead, we will use the
`natbib` package, which allows us to create different types of citation and
has a lot of styles available.

The basic structure of our input is as shown in this example.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{natbib}

\begin{document}
The mathematics showcase is from \citet{Graham1995}, whereas
there is some chemistry in \citet{Thomas2008}.

Some parenthetical citations: \citep{Graham1995}
and then \citep[p.~56]{Thomas2008}.

\citep[See][pp.~45--48]{Graham1995}

Together \citep{Graham1995,Thomas2008}

\bibliographystyle{plainnat}
\bibliography{learnlatex}
\end{document}
```

You can see that we can cite different entries in the database by giving their
key. The `natbib` package offers both textual and parenthetical citation styles,
`\citet` and `\citep`, respectively. The reference style is selected by the
`\bibliographystyle` line; here we've used the `plainnat` style. The
bibliography is actually inserted by the `\bibliography` line, which also picks
the database(s) to use; this is a comma-separated list of names.

Page references can be added to the citation with an optional argument.
If two optional arguments are given, the first goes in front of the citation
label for a short note and the second after the label for a page reference.

The setup above uses author-year style, but we can make use of numeric
citations. That is done by adding the `numbers` option to the `natbib` line.

## The `biblatex` workflow

The `biblatex` package works slightly differently to `natbib`, as we select
the databases in the preamble but print it in the document body. There are
some new commands for this.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage[style=authoryear]{biblatex}
\addbibresource{learnlatex.bib} % file of reference info

\begin{document}
The mathematics showcase is from \autocite{Graham1995}.

Some more complex citations: \parencite{Graham1995} or
\textcite{Thomas2008} or possibly \citetitle{Graham1995}.

\autocite[56]{Thomas2008}

\autocite[See][45-48]{Graham1995}

Together \autocite{Thomas2008,Graham1995}

\printbibliography
\end{document}
```

Notice that `\addbibresource` _requires_ the full database filename, whereas
we omitted the `.bib` for `\bibliography` with `natbib`. Also notice that
`biblatex` uses rather longer names for its citation commands, but these are
all quite easy to guess.

Again, short text before and after the citation can be inserted with
the optional arguments. Note that the page numbers need not be prefixed
with `p.~` or `pp.~` here, `biblatex` can automatically add the appropriate
prefix.


In `biblatex`, the reference style is picked when we load the package. Here,
we've used `authoryear`, but there is a `numeric` style and many others are
also available.

## Choosing between the BibTeX workflow and `biblatex`

Even though both the BibTeX workflow and `biblatex` get their input via BibTeX
files and can produce structurally similar output in the document, they use
completely different ways to produce this result. That means that there are
some differences between the two approaches that may help you choose which
one works best for you.

In the BibTeX workflow the bibliography style is ultimately decided
by a `.bst` file which you select with the `\bibliographystyle` command.
`biblatex` does not use `.bst` files and uses a different system.
If you are using a template that comes with a `.bst` file or are given a `.bst`
file for your project, you must use the BibTeX workflow and cannot use
`biblatex`.

The different approach `biblatex` takes implies that you can modify the output
of the bibliography and citation commands directly from your document preamble
using LaTeX-based commands. Modifications of BibTeX `.bst` styles on the other
hand usually require working with these external files and need knowledge of
the BibTeX programming language. Generally speaking, `biblatex` is said to be
easier to customize than the BibTeX workflow.

In `biblatex` it is generally easier to implement more elaborate citation
styles with a wider array of different citation commands. It also offers more
context-dependent features. Roughly speaking this is less interesting for
the styles common in many STEM subjects, but becomes relevant for some more
complex styles in some areas of the humanities.

BibTeX can only sort US-ASCII characters correctly and relies on workarounds
to provide US-ASCII-based sorting for non-US-ASCII characters.
With Biber `biblatex` offers full Unicode sorting capabilities. Thus `biblatex`
is usually a better choice if you want to sort your bibliography in a
non-ASCII/non-English order.

Having been around for much longer than `biblatex`, the BibTeX workflow is
more established than `biblatex`, meaning that many publishers and journals
expect bibliographies generated via the BibTeX workflow. Those publishers
cannot or generally do not accept submissions using `biblatex`.

The bottom line is: Check the author/submission guidelines if you are
submitting to a journal or publisher. If you are given a `.bst` file, you must
use the BibTeX workflow. If you want a relatively simple bibliography and
citation style and only need English US-ASCII-based sorting, the BibTeX workflow
should suffice. If you need a more complex citation style, non-English sorting
or want easier access to citation and bibliography style customisation features,
you will want to look into using `biblatex`.

## Exercises

Try out both the `natbib` and `biblatex` examples. For `natbib`, you'll need
to run LaTeX, BibTeX, LaTeX, LaTeX; for `biblatex`, it's LaTeX, Biber, LaTeX.
Find out how to do that in your editor, or try the Overleaf and TeXLive.net
automation.

See what happens when you create new database entries and new citations. Add
a citation that's not in the database and see how it appears. Experiment
with `natbib`'s `numeric` and `biblatex`'s `style=numeric` option.
