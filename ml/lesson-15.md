---
layout: "lesson"
lang: "ml"
title: "പ്രശ്നങ്ങൾ കൈകാര്യം ചെയ്യുന്ന രീതി"
description: "ലാറ്റെൿ പ്രമാണങ്ങളിൽ പതിവായ ചില പ്രശ്നങ്ങളും അവയുടെ അര്‍ത്ഥവും പരിഹാരമാര്‍ഗ്ഗങ്ങളും ഈ പാഠത്തിൽ പരിചയപ്പെടാം."
toc-anchor-text: "പ്രശ്നനിർദ്ധാരണം"
toc-description: "അപ്രതീക്ഷിത പ്രശ്നങ്ങളെ കൈകാര്യം ചെയ്യുന്നത്."
---

# പ്രശ്നങ്ങൾ കൈകാര്യം ചെയ്യുന്ന രീതി

<span
  class="summary">ലാറ്റെൿ പ്രമാണങ്ങളിൽ കാണാവുന്ന പൊതുവായ ചില പ്രശ്നങ്ങളും അവയുടെ അര്‍ത്ഥവും പരിഹാരമാര്‍ഗ്ഗങ്ങളും ഈ പാഠത്തിൽ പരിചയപ്പെടാം.</span>

സാധാരണ വേഡ് പ്രൊസസ്സറുകളിൽ നിന്നു് വ്യത്യസ്തമായി, പ്രോഗ്രാമിങ് ഭാഷകളുടെ കംപൈലറിനു
സമാനമായ തിരുത്തു്/പരിവര്‍ത്തനം/കാഴ്ച എന്ന രീതിയാണു് ലാറ്റെക്കിനുള്ളതു്. പ്രോഗ്രാമിങിലേതു പോലെ
ഇന്‍പുട്ടിൽ തെറ്റുകൾ വരുമ്പോൾ ലഭിക്കുന്ന പ്രശ്നസന്ദേശങ്ങളെ മനസ്സിലാക്കി പ്രശ്നം പരിഹരിക്കാവുന്നതാണു്.


## പതിവു പ്രശ്നങ്ങൾ

ചില പതിവു പ്രശ്നങ്ങളുടെ ഉദാഹരണങ്ങൾ ഈ താളിൽ വിശദീകരിക്കുന്നുണ്ട്. ഓരോ ഉദാഹരണത്തിലും
പ്രശ്നസന്ദേശത്തിന്റെ മാതൃകയെപ്പറ്റിയും ചര്‍ച്ച ചെയ്യുന്നുണ്ട്.

ഊ ഉദാഹരണങ്ങൾ ഉപയോഗിച്ചു നോക്കുകയും പ്രമാണം തിരുത്തി അതിലെ പ്രശ്നങ്ങൾ പരിഹരിക്കാൻ
ശ്രമിക്കുകയും ചെയ്യുന്നതു് വിജ്ഞാനപ്രദമായിരിക്കും.


### pdflatex not found

തുടക്കത്തിൽ തന്നെ:

```
'pdflatex' is not recognized as an internal or external command,
operable program or batch file.
```
{: .noedit :}

എന്നു വിന്‍ഡോസിലും

```
bash: pdflatex: command not found
```
{: .noedit :}

എന്നു ഗ്നു/ലിനക്സിലും പലരും കാണുന്ന ഒരു പ്രശ്നസന്ദേശമാണിതു്.

ഇതു് ഒരു ടെൿ പ്രശ്നമല്ല, പകരം ഓപ്പറേറ്റിംഗ് പ്രവര്‍ത്തകത്തിൽ ടെൿ ഇന്‍സ്റ്റാൾ ചെയ്യാതിരിക്കുകയോ
എവിടെയാണു് ഇന്‍സ്റ്റാൾ ചെയ്തെന്നു് അറിയാതിരിക്കുകയോ ചെയ്യുമ്പോഴുള്ള പ്രശ്നമാണു്. ഒരു സാധാരണ പിഴവു്
ടെൿവര്‍ക്സ് അല്ലെങ്കിൽ ടെൿഷോപ് പോലെ ഒരു _എഡിറ്റർ_ മാത്രം ഇന്‍സ്റ്റാൾ ചെയ്യുകയും ടെൿലൈവോ
മിൿടെക്കോ പോലെ ഒരു ടെൿ സംവിധാനം ഇന്‍സ്റ്റാൾ ചെയ്യാൻ വിട്ടുപോവുകയും ചെയ്യുക എന്നതാണു്.


### ഒരു ടെൿ പ്രശ്നസന്ദേശത്തിന്റെ പരിശോധനാരീതി

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\newcommand\mycommand{\textbold{hmmm}}

\begin{document}

My command is used here \mycommand.

\end{document}
```

ലോഗ് ഫയലിൽ കുറേ വരികളുള്ള ഒരു സന്ദേശം ഈ പ്രമാണം പ്രവര്‍ത്തിപ്പിക്കുമ്പോൾ കാണാം:

```
! Undefined control sequence.
\mycommand ->\textbold 
                       {hmmm}
l.8 My command is used here \mycommand
                                      .
? 
```
{: .noedit :}

* ആശ്ചര്യചിഹ്നം `!` കൊണ്ട് അടയാളപ്പെടുത്തിയ ഒന്നാമത്തെ വരിയിൽ, പ്രശ്നത്തിന്റെ പൊതുസ്വഭാവം
  സ്പഷ്ടമാക്കിയിരിക്കുന്നു (ഈ സംഭവത്തിൽ   നിര്‍വ്വചിക്കപ്പെടാത്ത ആജ്ഞ `undefined command` എന്ന്).
* അടുത്ത രണ്ടു വരികൾ കാണിക്കുന്നതു് ടെൿ ഇന്‍പുട്ടിലെ ഏതു വരി വായിക്കുമ്പൊഴാണു് പ്രശ്നം സംഭവിച്ചതു്
  എന്നാണു്. ആ വരിയിൽ ടെൿ എവിടം വരെ എത്തിയിട്ടുണ്ട് എന്നതു്, ഇന്‍പുട്ടിലെ വരി അവിടെ വച്ച് മുറിച്ചു
  കൊണ്ട് സൂചിപ്പിച്ചിരിക്കുന്നു. ഇവിടെ നിർവ്വചിക്കപ്പെടാത്ത ആജ്ഞ എന്നതു് പ്രശ്നസന്ദേശത്തിലെ വരി മുറിച്ചതിനു്
  തൊട്ടുമുമ്പുഉള്ള സംജ്ഞയാണു്: `\textbold`. വരി മുറിച്ചതിനു ശേഷം കാണുന്ന  `{hmmm}` എന്നതു്
  തൊട്ടുമുന്നിലെ ആജ്ഞയുടെ വാദം (argument) ആയി കരുതി വായിച്ചതും എന്നാൽ ടെൿ ഉപയോഗിക്കാൻ
  ആരംഭിച്ചിട്ടില്ലാത്തതുമായ സംജ്ഞകളാണു്.
* പൊതുവേ ഇന്‍പുട്ടിലെ പ്രസ്തുത വരിക്കു സമീപമുള്ള, സന്ദര്‍ഭം മനസ്സിലാക്കാൻ സഹായിക്കുന്ന ചില വരികളും കാണപ്പെടാം
* അവസാനത്തെ വരി തുടങ്ങുന്നതു് ആ വരിയുടെ ക്രമസംഖ്യയ്ക്കു മുമ്പ് `l.` എന്നു ചേര്‍ത്തതു വച്ചാണു്.
  അതിനു തുടര്‍ച്ചയായി പ്രശ്നത്തിനു കാരണമായ സ്രോതസ്സിലെ വരിയുടെ ഉള്ളടക്കവും.
  
* ഏറ്റവും ഒടുവിലെ വരി `?` എന്നാണു്. സമ്പര്‍ക്കം പുലര്‍ത്താവുന്ന രീതിയിലാണു് ടെൿ പ്രവർത്തിപ്പിക്കുന്നതെങ്കിൽ
  ഇവിടെ നിര്‍ദ്ദേശങ്ങൾ നല്കി തുടർന്നു പ്രവര്‍ത്തിപ്പിക്കാവുന്നതാണു്, പക്ഷേ മിക്ക എഡിറ്ററുകളും ഓണ്‍ലൈൻ
  സംവിധാനങ്ങളും ഒരു പ്രശ്നം കാണുമ്പോൾ അവിടെ നിര്‍ത്താതെ തുടര്‍ന്നും പ്രവര്‍ത്തിപ്പിക്കാനുള്ള മട്ടിലാണു്
  ടെൿ ക്രമപ്പെടുത്തിയിരിക്കുന്നതു്. സമ്പര്‍ക്കം സാദ്ധ്യമാവുന്ന രീതിയാണു് ടെൿ പ്രവര്‍ത്തിപ്പിക്കുന്നതെങ്കിൽ ഇവിടെ
  `s` എന്നു് ടൈപ്പു് ചെയ്താൽ പ്രശ്നങ്ങളിൽ നിശ്ചലമാകാതെ തുടരാൻ സാധിക്കുന്നതാണു്.


Note here that TeX does not see the error at the point that
the definition is made; and in fact if `\mycommand` is defined but not
used, no error would be raised. So although the error is reported on
line 8, the "real" error is in the definition on line 4, so it is
important to see the whole error message.

Beware that some editors show one line "summaries" of the error log.
This can be particularly misleading if shown as

`line 8: undefined command: ...\mycommand`

as it makes it appear that `\mycommand` is not defined.


### Mismatched braces


```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\usepackage[leqno}{amsmath}

\begin{document}

\end{document}
```

Here the error is a mismatched `}` used to end the optional
argument. The closing brace causes LaTeX's option parsing
to fail and you get an internal and not that helpful error: 

```
! Argument of \@fileswith@ptions has an extra }.
```
{: .noedit :}

While the error description is unhelpful; the following two
lines do accurately display the location of the error by the use of
the linebreak showing how far TeX had read:

```
l.4 \usepackage[leqno}
                      {amsmath}
```
{: .noedit :}


### Missing files

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\usepackage{amsmathz}

\begin{document}

\end{document}
```

This produces the error

```
! LaTeX Error: File `amsmathz.sty' not found.
```
{: .noedit :}

Note: the same error may be caused by two different causes; a simple
typo as here, which may be corrected by fixing the package name, or
that the file really is missing and needs to be installed on the
current system.

### Blank lines in display math

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}

Some text
\begin{equation}

  1=2

\end{equation}

\end{document}
```

Produces the slightly mysterious error

```
! Missing $ inserted.
```
{: .noedit :}

But the fix is simple, blank lines are not allowed in math
environments and should be deleted.

## Exercise

Attempt to fix the errors in the supplied examples.

Produce small documents with different errors and note the form of the error messages.

<script>
  window.addEventListener('load', function(){
      if(editors['pre2'] != null) editors['pre2'].moveCursorTo(3, 31, false);
      if(editors['pre4'] != null) editors['pre4'].moveCursorTo(3, 18, false);
      if(editors['pre7'] != null) editors['pre7'].moveCursorTo(3  , 20, false);
      if(editors['pre9'] != null) editors['pre9'].moveCursorTo(7, 0, false);
  }, false);
</script>
