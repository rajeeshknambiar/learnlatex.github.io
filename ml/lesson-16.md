---
layout: "lesson"
lang: "ml"
title: "സഹായക്കുറിപ്പു് ഉപഗോഗിക്കുന്നതും സഹായം തേടുന്നതും"
description: "ലാറ്റെൿ അനുബന്ധ സോഫ്റ്റ്‌വെയറുകളെയും പൊതിക്കെട്ടുകളെയും സംബന്ധിച്ച സഹായക്കുറിപ്പുകളുടെ പ്രധാന ഉറവിടങ്ങളെക്കുറിച്ചും പ്രശ്നം നേരിടുമ്പോൾ എങ്ങനെ സയാഹം തേടണമെന്നും ഈ പാഠത്തിൽ പരിചയപ്പെടാം."
toc-anchor-text: "സഹായവും കുറിപ്പുകളും"
toc-description: "സഹായക്കുറിപ്പു് ഉപയോഗിക്കുന്നതും സഹായം തേടുന്നതും."
---

# സഹായക്കുറിപ്പു് ഉപയോഗിക്കുന്നതും സഹായം തേടുന്നതും

<span
  class="summary">ലാറ്റെൿ അനുബന്ധ സോഫ്റ്റ്‌വെയറുകളെയും പൊതിക്കെട്ടുകളെയും സംബന്ധിച്ച സഹായക്കുറിപ്പുകളുടെ പ്രധാന ഉറവിടങ്ങളെക്കുറിച്ചും പ്രശ്നം നേരിടുമ്പോൾ എങ്ങനെ സഹായം തേടണമെന്നും ഈ പാഠത്തിൽ പരിചയപ്പെടാം.</span>
  
ഒരു പാക്കേജ് അഥവാ പൊതിക്കെട്ടിന്റെയോ, ക്ലാസ്സിന്റെയോ സഹായക്കുറിപ്പുകൾ ലഭ്യമാക്കുവാൻ പല വഴികളുണ്ടു്.


## `texdoc`

ടെൿലൈവോ മിൿടെക്കോ പോലെയുള്ള ഒരു ടെൿ വിതരണം നിങ്ങൾ ഇന്‍സ്റ്റാൾ ചെയ്യുമ്പോൾ സയാഹക്കുറിപ്പുകൾ
കൂടി അതിലുള്‍പ്പെടുത്തിയിട്ടുണ്ടെങ്കിൽ `texdoc` ആജ്ഞ ഉപയോഗിച്ച് ആവശ്യമായ സഹായക്കുറിപ്പ് വായിക്കാം.

താഴെക്കൊടുത്തിരിക്കുന്ന

`texdoc` < _pkg_ >

എന്ന ആജ്ഞ `<pkg>` എന്ന പൊതിക്കെട്ടിന്റെ സഹായക്കുറിപ്പു് തുറക്കും. ലഭ്യമായ എല്ലാ സഹായക്കുറിപ്പുകളും തിരഞ്ഞ്
ഏറ്റവും അനുയോജ്യമെന്നു കരുതുന്ന ഒരെണ്ണം തുറക്കുകയാണു് ഈ ഉപാധി ചെയ്യുന്നതു്. അതു കണ്ടെത്തുന്ന എല്ലാ കുറിപ്പുകളുടെയും
പട്ടിക കാണുവാനും അതിൽ നിന്നു തെരഞ്ഞെടുക്കാനും ഈ ആജ്ഞ ഉപയോഗിക്കാം:

`texdoc -l` < _pkg_ >

## texdoc.org

`texdoc` എന്ന ഉപാധി പോലെ ഉപയോഗിക്കാവുന്ന ഒരു [വെബ്സൈറ്റ്](https://texdoc.org/) ആണിത്. അവിടെ ലഭ്യമായ
സഹായക്കുറിപ്പുകൾ `texdoc -l` ഉപയോഗിച്ചെന്ന പോലെ തിരയുകയും ആവശ്യമുള്ളത് എടുക്കുകയും ചെയ്യാം.

## CTAN

സമ്പൂര്‍ണ്ണ ടെൿ ശേഖര ശൃംഖലയാണു് [CTAN](https://www.ctan.org). ഒട്ടുമീക്ക ലാറ്റെൿ പൊതിക്കെട്ടുകളും
പ്രസിദ്ധപ്പെടുത്തുന്നത് അവിടെയാണു്. ആ സൈറ്റിൽ നിങ്ങള്‍ക്കാവശ്യമുള്ള പൊതിക്കെട്ട് തിരഞ്ഞ് അതിന്റെ സയാഹക്കുറിപ്പ്
പ്രാപ്യമാക്കാം. പൊതുവേ ഏതു പൊതിക്കെട്ടും `ctan.org/pkg/<pkg-name>` എന്ന വിലാസത്തിൽ ലഭ്യമാണ്,
അവിടെയുള്ള  README പ്രമാണവും സഹായക്കുറിപ്പുകളും നോക്കാവുന്നതാണു്.


## Books on LaTeX

There are several books available that can help you learn more about LaTeX.
As a beginner, you will gain a lot from a structured beginners guide, as
those can give a lot more detail than we've covered here. You might also
want access to a reference with more detail and recommendations.

The LaTeX team have [a list of books](https://www.latex-project.org/help/books/)
largely written by members. The most notable are [Lamport's official
guide](https://www.informit.com/store/latex-a-document-preparation-system-9780201529838)
and the comprehensive
[LaTeX Companion](https://www.informit.com/store/latex-companion-9780201362992).

Other books aimed at learning LaTeX include

- [_Guide to
  LaTeX_](https://www.informit.com/store/guide-to-latex-9780132651714) by Helmut
  Kopka and Patrick Daly: available as an e-book
- [_LaTeX for Complete Novices_](https://www.dickimaw-books.com/latex/novices/) by
  Nicola Talbot: available as a free e-book or low-cost printed edition
- [_Using LaTeX to write a PhD
  thesis_](https://www.dickimaw-books.com/latex/thesis/) by
  Nicola Talbot: available as a free e-book or low-cost printed edition
- [_LaTeX Beginner's Guide_](https://www.packtpub.com/gb/hardware-and-creative/latex-beginners-guide)
  by Stefan Kottwitz: available as an e-book and in print
- [_LaTeX and Friends_](https://www.springer.com/gp/book/9783642238154) by
  Marc van Dongen: available as an e-book and in print

## Getting help

There are various online forums for asking LaTeX questions; perhaps the most
popular today is [TeX - LaTeX StackExchange](https://tex.stackexchange.com).
Whenever you ask a question, it's best to first get your example clear: what is
normally known as a 'minimal working example' (MWE). This doesn't mean the code
works (as you wouldn't be asking otherwise!), but rather it means you've done
your best to make it clear, self-contained and minimal. The latter means
having only enough content to show the issue.

### How to provide a minimal working example (MWE)

How do you construct a MWE? Normally easiest is to start from

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
Text
\end{document}
```

and add lines one at a time until you show the issue. You can try to
'cut down' your real file, but that can be a long process.

<p 
  class="hint">If you need more text to show page breaking and other effects, then packages such as <code>lipsum</code> may be used to generate nonsense paragaraphs of text while keeping your test file small.</p>


### Log file

One thing you will want available is your log file; this is created by LaTeX
every time you run it, and has the same name as your input but ending `.log`.

<p 
  class="hint">Depending on your desktop interface, you might need to 'show extensions' to work out which file it is.</p>

In the log file, you can always see the full error messages. LaTeX's error messages try to be helpful, but they are not the same as messages in word processors.

<p 
  class="hint">Some editors also make it hard to see the 'full' text of an error, which can hide key details.</p>

If you have a problem, expert LaTeX users will often ask for a copy of your log file.

### Going further

Finally we offer a [gallery of small examples](./extra-01) showing a range of different subject areas not covered in this introduction, and different LaTeX packages in those areas.
