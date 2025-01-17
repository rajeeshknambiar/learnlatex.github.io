---
layout: "lesson"
lang: "ml"
title: "ലാറ്റെൿ പ്രമാണത്തിന്റെ അടിസ്ഥാന ഘടന"
description: "ഒരു ലാറ്റെൿ പ്രമാണത്തിന്റെ അടിസ്ഥാന ഘടന, അതുപയോഗിച്ച് പിഡിഎഫ് പ്രമാണം നിര്‍മ്മിക്കുക,
ലാറ്റെക്കിനെ നിയന്ത്രിക്കാനുപയോഗിക്കുന്ന സവിശേഷ അക്ഷരങ്ങൾ മുതലായ കാര്യങ്ങൾ ഈ പാഠത്തിൽ പരിചയപ്പെടാം."
toc-anchor-text: "പ്രമാണ ഘടന"
toc-description: "ഒരു ലാറ്റെൿ പ്രമാണത്തിന്റെ അടിസ്ഥാന ഘടന."
---

# ലാറ്റെൿ പ്രമാണ ഘടന

<span
  class="summary">ഒരു ലാറ്റെൿ പ്രമാണത്തിന്റെ അടിസ്ഥാന ഘടന, അതുപയോഗിച്ച് പിഡിഎഫ് പ്രമാണം നിര്‍മ്മിക്കുക,
ലാറ്റെക്കിനെ നിയന്ത്രിക്കാനുപയോഗിക്കുന്ന സവിശേഷ അക്ഷരങ്ങൾ മുതലായ കാര്യങ്ങൾ ഈ പാഠത്തിൽ പരിചയപ്പെടാം.</span>

നിങ്ങളുടെ ആദ്യത്തെ ലാറ്റെൿ പ്രമാണം വളരെ ലളിതമായ ഒന്നാണു്; ഒരു പ്രമാണം കാണാൻ എങ്ങനെയിരിക്കുമെന്നും
എങ്ങനെ വിജയകരമായി അതിന്റെ പാഠവിന്യാസം നടത്താമെന്നും മനസ്സിലാക്കുക എന്നതാണു് ഉദ്ദേശ്യം. `learnlatex.org`ൽ
[ഉദാഹരണങ്ങൾ എങ്ങനെ ഉപയോഗിക്കാം](help) എന്നു പഠിക്കാനുള്ള നിങ്ങളുടെ ആദ്യത്തെ അവസരവുമാണിതു്.

നിങ്ങളുടെ കംപ്യൂട്ടറിൽ സ്ഥാപിച്ചിട്ടുള്ള ലാറ്റെൿ വിതരണമാണു് ഉപയോഗിക്കുന്നതെങ്കിൽ എഡിറ്റർ ഉപയോഗിച്ച് `first.tex`
എന്ന പേരിലോ മറ്റോ ഒരു പ്രമാണം ഉണ്ടാക്കിയതിനു ശേഷം (പേരിൽ ഒഴിവുസ്ഥലം/സ്പേസ്, അസാധാരണ അക്ഷരങ്ങൾ എന്നിവ
പാടില്ല), ചുവടെ നല്കിയിരിക്കുന്ന പാഠം ടൈപ്പു് ചെയ്യുക (പകര്‍ത്തി ചേര്‍ക്കുന്നതിനു പകരം എല്ലായ്പോഴും ടൈപ്പു് ചെയ്യുക, ശരിയായി
പഠിക്കാൻ അങ്ങനെയേ സാധിക്കൂ).

നിങ്ങളൊരു ഓണ്‍ലൈൻ ലാറ്റെൿ സംവിധാനമാണു് ഉപയോഗിക്കുന്നതെങ്കിൽ ‘Run at TeXLive.net’ അല്ലെങ്കിൽ
‘Open in Overleaf’ എന്ന ബട്ടണുകളിൽ ഏതെങ്കിലുമൊന്ന് ഉപയോഗിച്ച് ഈ ഉദാഹരണങ്ങൾ പരീക്ഷിക്കുക.

<p
  class="hint">നിങ്ങളുടെ കംപ്യൂട്ടറിൽ ലാറ്റെൿ ഉണ്ടെങ്കില്‍ക്കൂടിയും ഓണ്‍ലൈൻ സംവിധാനങ്ങൾ പരീക്ഷിച്ചു നോക്കാൻ ഞങ്ങൾ 
  ശുപാര്‍ശ ചെയ്യുന്നു; ഇവിടെ ലഭ്യമായ വിവിധ സൗകര്യങ്ങൾ എങ്ങനെ പ്രവര്‍ത്തിക്കുന്നുവെന്നു മനസ്സിലാക്കാനുള്ള നല്ല അവസരമാണിതു്.</p>

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

നിങ്ങളുണ്ടാക്കിയ പ്രമാണത്തിൽ മേലെ കാണുന്ന ഉള്ളടക്കം ചേര്‍ത്ത് സൂക്ഷിച്ചതിനു ശേഷം പിഡിഎഫ് പ്രമാണമായി പാഠവിന്യാസം
നടത്തുക. സ്വയം ഇന്‍സ്റ്റാൾ ചെയ്ത ലാറ്റെൿ വിതരണമാണുപയോഗിക്കുന്നതെങ്കിൽ ഇതിനായി അമര്‍ത്തേണ്ട ബട്ടൺ
നിങ്ങളുപയോഗിക്കുന്ന എഡിറ്ററിനെ ആശ്രയിച്ചിരിക്കും. ശേഷം നിങ്ങള്‍ക്കൊരു പിഡിഎഫ് പ്രമാണം ലഭിക്കും, അതിന്റെ
ഉള്ളടക്കം കാണാം: മുകളിൽ നല്കിയ പാഠഭാഗവും _കൂടെ_ താളിന്റെ എണ്ണവും (ഇതു് ലാറ്റെൿ സ്വമേധയാ ചേര്‍ക്കുന്നതാണു്).

ഫലമായി ലഭിച്ച `first.pdf` എന്ന പ്രമാണം നിങ്ങള്‍ക്കിഷ്ടമുള്ള പിഡിഎഫ് കാഴ്ചസഹായി പ്രോഗ്രാം ഉപയോഗിച്ച്
തുറന്നു നോക്കുക. ഒന്നാന്തരമായിരിക്കുന്നില്ലേ, അനുമോദനങ്ങൾ!

പിഡിഎഫ് ഫലത്തിനു പകരം എച്ടിഎംഎൽ ആണു നിങ്ങള്‍ക്കാവശ്യമെങ്കിൽ അതെങ്ങനെ നിര്‍മ്മിക്കാമെന്നു മനസ്സിലാക്കാൻ
[സഹായം](./help) നോക്കുക.


## പ്രശ്നങ്ങൾ കൈകാര്യം ചെയ്യുന്നതു്

പിഡിഎഫ് നിര്‍മ്മിക്കുവാൻ ഒരുപക്ഷേ നിങ്ങൾ പ്രശ്നം നേരിട്ടിരിക്കാം.
പ്രമാണത്തിലെ ഓരോ വരിയും മുകളിലെഴുതിയ അതേപോലെ ചേര്‍ത്തിരിക്കുന്നുവെന്ന് ഉറപ്പുവരുത്തുക.
ചിലപ്പോൾ ഇന്‍പുട്ട് നല്കുന്നതിലുള്ള വളരെ ചെറിയ വ്യതാസം പോലും ലഭിക്കുന്ന ഫലത്തിൽ വലിയ
വ്യത്യാസത്തിനു കാരണമാകാം, ഔട്പുട്ട് പ്രമാണം ഉണ്ടാകാതിരിക്കുന്നതടക്കം.
നിങ്ങൾക്ക് ഒരുവിധത്തിലും ശരിയാക്കാനാകുന്നിലെങ്കിൽ പ്രമാണത്തിലുള്ളതെല്ലാം മായ്ച്ച്, മുകളിൽ
തന്നിരിക്കുന്ന ഉദാഹരണം അതേപടി പകര്‍ത്തി ചേര്‍ത്തു നോക്കുക.

നിങ്ങളുടെ ലാറ്റെൿ പ്രവര്‍ത്തനം ഒരു ചോദ്യചിഹ്നത്തിൽ തടഞ്ഞു നില്‍ക്കുന്നെങ്കിൽ `x` എന്നും `<Enter>`
എന്നും ടൈപ്പ് ചെയ്ത് അവിടെ നിന്നു രക്ഷപ്പെടാം.

ലാറ്റെക്കിലെ പ്രശ്നസന്ദേശങ്ങൾ നിങ്ങള്‍ക്കു്  സഹായകരമാകുവാൻ ശ്രമിക്കും, പക്ഷേ അവ വേഡ്
പ്രൊസസ്സറുകളിലേതു പോലെയാവണമെന്നില്ല. ചില എഡിറ്ററുകൾ പ്രശ്നസന്ദേശങ്ങളുടെ പ്രധാന
ഭാഗങ്ങൾ മറച്ചു വയ്ക്കാം, അതിനാൽ പ്രശ്നസന്ദേശങ്ങൾ  പൂര്‍ണ്ണമായി ഒറ്റനോട്ടത്തിൽ അവയിൽ
കാണണമെന്നില്ല. `.log` എന്നതിലവസാനിക്കുന്ന ഒരു ടെക്സ്റ്റ് ഫയലിൽ ലാറ്റെൿ എല്ലായ്പോഴും
അതു  ചെയ്തുകൊണ്ടിരിക്കുന്ന ഓരോ കാര്യത്തിന്റെയും നാള്‍വഴി രേഖപ്പെടുത്തി വയ്ക്കും. എപ്പോള്‍
നോക്കിയാലും അതിനകത്ത് മുഴുവൻ പ്രശ്നസന്ദേശങ്ങളും കാണാം. നിങ്ങളുടെ എന്തെങ്കിലും പ്രശ്നം
പരിഹരിക്കണമെന്നുണ്ടെങ്കിൽ ലാറ്റെൿ വിദഗ്ദ്ധർ പലപ്പോഴും ലോഗ് പ്രമാണത്തിന്റെ പകര്‍പ്പു്
ആവശ്യപ്പെടാറുണ്ട്. 

<p
  class="hint">പ്രശ്നനിര്‍ദ്ധാരണത്തിനുള്ള വഴികൾ <a href="./lesson-15">പാഠം 15ൽ</a> വിശദമായി പഠിക്കാം.</p>

## നിങ്ങളിപ്പോൾ മനസ്സിലാക്കിയ കാര്യങ്ങൾ

ആദ്യത്തെ പ്രമാണത്തിൽ ഏറ്റവും അടിസ്ഥാനപരമായ കാര്യങ്ങളാണുള്ളതു്.
ലാറ്റെൿ  പ്രമാണങ്ങൾ പാഠത്തിന്റെയും ആജ്ഞകളുടെയും ഒരു  മിശ്രണമാണു്.
ആജ്ഞകൾ തുടങ്ങുന്നത് 'ബാക്ക്‌സ്ലാഷ്' അക്ഷരത്തിലാണ്, ചില ആജ്ഞകള്‍
വാദങ്ങൾ സ്വീകരിക്കുന്നത് വക്രാവരണ ചിഹ്നത്തിനകത്താണ് (curly braces),
ചില ഐച്ഛികവാദങ്ങൾ കോഷ്ഠചിഹ്നത്തിനകത്തും (square brackets).
പിഡിഎഫ് പ്രമാണം ലഭിക്കുന്നതു്് ലാറ്റെക്കിനോട് പാഠവിന്യാസം ചെയ്യാൻ 
നിങ്ങളാവശ്യപ്പെടുമ്പൊഴാണു്.

ഏതൊരു ലാറ്റെൿ പ്രമാണത്തിനും `\begin{document}` എന്ന ആജ്ഞയും 
അതിനു ജോടിയായി `\end{document}` എന്ന ആജ്ഞയുമുണ്ട്.
ഇവയ്ക്കു രണ്ടിനുമിടയിലാണു്  നിങ്ങളുടെ ഉള്ളടക്കം ചേര്‍ത്തിരിക്കുന്ന  *പ്രമാണത്തിന്റെ  കാമ്പു്*.
ലാറ്റെക്കിൽ ഖണ്ഡിക തിരിക്കുവാനായി ഒന്നോ അതിലധികമോ ഒഴിഞ്ഞ വരികളുപയോഗിക്കാം.
`\begin{document}` എന്ന ആജ്ഞയ്ക്കു മുമ്പുള്ള സ്ഥലമാണു്് *പ്രമാണ ആമുഖം*,
ഇതാണു് പ്രമാണത്തിന്റെ ഘടന നിര്‍ണ്ണയിക്കുന്ന കോഡ് ഉള്‍ക്കൊള്ളുന്നതു്.
`\usepackage`  എന്ന  ആജ്ഞ [പിന്നീടുള്ള  ഒരു പാഠത്തിൽ](lesson-06)
വിശദീകരിച്ചിട്ടുണ്ടു്; ഫോണ്ട് എന്‍കോഡിങ് ക്രമീകരിക്കുവാൻ ഈ വെബ്‌സൈറ്റിലുള്ള
പല ഉദാഹരണങ്ങളിലും അതുപയോഗിച്ചിട്ടുണ്ടു്.

ലാറ്റെക്കിനു്് മറ്റു പല `\begin{...}`, `\end{...}` ജോടികളുണ്ടു്, അവയെ *പരിസരങ്ങൾ*
(environments) എന്നാണു് വിളിക്കുന്നതു്.  ഏതു `\begin{x}` പരിസരത്തിന്റെ  തുടക്കത്തിനും
പൂരകമായി ഒരു `\end{x}` നല്കിയിരിക്കണം. ഒരു പരിസരത്തിനകത്തു് മറ്റൊരെണ്ണം
ഉപയോഗിച്ചിട്ടുണ്ടെങ്കിൽ `\end{y} ... \end{x}` എന്നു് `\begin{x} ... \begin{y}` എന്നതിനു്
പൂരകമായി നല്കിയിരിക്കണം, അതായതു് `\begin`, `\end` എന്ന പ്രസ്താവനകൾ
അവയുടെ ക്രമത്തിൽ തന്നെ ജോടി ചേര്‍ത്തിരിക്കണം.

ലാറ്റെൿ പ്രമാണത്തിൽ വിവരണങ്ങളോ അഭിപ്രായങ്ങളോ  (comment) ചേര്‍ക്കുവാൻ
`%` അക്ഷരത്തിൽ ആരംഭിച്ചാൽ മതി; ഒരുദാഹരണം നോക്കാം:

```latex
\documentclass[a4paper,12pt]{article} % The document class with options
\usepackage[T1]{fontenc}
% A comment in the preamble
\begin{document}
% This is a comment
This is   a simple
document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```

മുകളിലെ ഉദാഹരണത്തിൽ രണ്ടു ഖണ്ഡികകളുണ്ടെന്നു്  നിങ്ങള്‍ക്കു കാണാം: അതിനായി
ഒഴിഞ്ഞ വരി ഉപയോഗിച്ചതു ശ്രദ്ധിക്കുക. ഒന്നിലധികം വിടവ് (സ്പേസ്) ഔട്പുട്ടിൽ
ഒറ്റയൊന്നായി കണക്കാക്കിയതും ശ്രദ്ധിക്കുക.

വരികളുടെ അവസാനം മുറിയാൻ പാടില്ലാത്ത 'ഉറപ്പുള്ള' ഒരു വിടവ് നിങ്ങള്‍ക്കു് ചിലപ്പോൾ
ആവശ്യം വരാം: രണ്ടു വാക്കുകളെ ലാറ്റെക്കിൽ അങ്ങനെ 'കൂട്ടിക്കെട്ടുന്നതിനു്' ഉപയോഗിക്കുന്നതു്
`~` എന്ന അക്ഷരമാണു്. ഇതിന്റെ  ഉപയോഗം പ്രത്യേകിച്ച് ഉപകാരപ്പെടുന്നതു് മറ്റു പാഠഭാഗങ്ങളെ
പരാമര്‍ശിക്കുന്നതു പഠിക്കുന്ന പാഠം അല്പം കഴിഞ്ഞു വരുമ്പോൾ കാണാം.

## സവിശേഷ അക്ഷരങ്ങൾ

``\``, `{`, `}` എന്നിവയ്ക്ക് ലാറ്റെക്കിൽ പ്രത്യേക അര്‍ത്ഥമുണ്ടെന്നു് ഇതിനകം നിങ്ങൾ ശ്രദ്ധിച്ചു കാണും.
ലാറ്റെക്കിനു് ഒരു നിര്‍ദ്ദേശം ('ആജ്ഞ') നല്കുന്നതു് ആരംഭിക്കുകയാണു് ``\`` ചെയ്യുന്നതു്. 
`{`, `}` എന്ന വക്രാവരണചിഹ്നങ്ങൾ ഉപയോഗിക്കുന്നതു് ആജ്ഞകള്‍ക്കാവശ്യമായ _നിര്‍ബ്ബന്ധമായും
നല്ക്കേണ്ട വാദങ്ങളെ_ ഉള്‍ക്കൊള്ളിക്കാനാണു്.

വിശേഷ അര്‍ത്ഥമുള്ള മറ്റു് അക്ഷരങ്ങളുമുണ്ട്; ഉദാഹരണത്തിനു് നമ്മൾ ഈയ്യടുത്തു് കണ്ട `~` അക്ഷരം
'മുറിയാത്ത' വിടവ് എന്നാണര്‍ത്ഥമാക്കുന്നതു്. ഇത്തരം ഏതാണ്ടെല്ലാ അക്ഷരങ്ങളും സാധാരണ പാഠത്തിൽ
_വളരെ_ വിരളമാണു് എന്നതിനാലാണ് വിശേഷ അര്‍ത്ഥം നല്കാൻ അവയെ തിരഞ്ഞെടുത്തതു്. നിങ്ങള്‍ക്ക്
ഇതിലേതെങ്കിലും ഒരക്ഷരം ഔട്പുട്ടിൽ കാണിക്കേണ്ടി വരികയാണെങ്കിൽ [വിശദാംശങ്ങളുടെ താളിൽ വിവരങ്ങൾ](more-03)
ഞങ്ങൾ ചേര്‍ത്തിട്ടുണ്ടു്.

## അഭ്യാസം

എഡിറ്റിങും പാഠവിന്യാസവും ചെയ്യാവുന്ന ഒരു ഓണ്‍ലൈൻ സംവിധാനം പരീക്ഷിച്ചു നോക്കുക: പാഠം വിന്യസിക്കാനുള്ള
ബട്ടൻ അമര്‍ത്തി നോക്കുക, വെബ് താളിൽ തന്നെ ഉള്ളടക്കം മാറ്റി വീണ്ടും പാഠം വിന്യസിക്കുക.

നിങ്ങളുടെ ആദ്യത്തെ പ്രമാണത്തിനകത്ത് കൂടുതൽ പാഠം ചേര്‍ത്തു് വീണ്ടും പാഠവിന്യാസം ചെയ്ത് പിഡിഎഫ് പ്രമാണത്തിൽ
വന്നിട്ടുള്ള മാറ്റങ്ങൾ നോക്കുക. കുറച്ച് ഖണ്ഡികകൾ അധികമായി ചേര്‍ക്കുകയും കുറേയധികം വിടവ്/ശൂന്യസ്ഥലം നല്കുകയും
ചെയ്യുക. നിങ്ങളുടെ എഡിറ്റർ എങ്ങനെ പ്രവര്‍ത്തിക്കുന്നുവെന്ന് സൂക്ഷ്മമായി പരിശോധിക്കുക: സ്രോതസ്സിലെ ഒരു വരിയിൽ
അമര്‍ത്തി പിഡിഎഫിൽ അതേ സ്ഥലത്ത് ചെല്ലുന്നതെങ്ങനെ എന്നു കണ്ടെത്തുക. കുറേ മുറിക്കാത്ത വിടവ് നല്കിയാൽ
അതെങ്ങനെയാണു് വരി മുറിക്കുന്നതിനെ സ്വാധീനിക്കുന്നതെന്നു് നിരീക്ഷിക്കുക.
