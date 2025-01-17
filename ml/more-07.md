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

## ചിത്രങ്ങൾ നിർമ്മിക്കുന്നതു്

മേൽപ്രസ്താവിച്ചതു പോലെ ശാസ്ത്ര സോഫ്റ്റുവെയറുകളിലുണ്ടാക്കിയ പടങ്ങൾ അടക്കം പലതരത്തിൽ നിർമ്മിച്ച ചിത്രങ്ങളും ലാറ്റെക്കിൽ എളുപ്പം ഉപയോഗിക്കാം.
അങ്ങനെ നിർമ്മിച്ച ചിത്രങ്ങൾ (വിസ്താരം കൂട്ടാനും കുറയ്ക്കാനും സാധിക്കുന്ന) പിഡിഎഫ് ആയി സൂക്ഷിക്കാൻ ശ്രദ്ധിക്കുക. ബിറ്റ്മാപ്പ്
ഫയൽ ആയി സൂക്ഷിക്കുന്നെങ്കിൽ നല്ല വ്യക്തതയുള്ള ചിത്രമായിരിക്കണം. മൗസ് ഉപയോഗിച്ച് ചിത്രം നിർമ്മിച്ച് അതിന്റെ ലാറ്റെൿ‌ കോഡ്
ലഭിക്കുവാൻ [ഇങ്ക്സ്കേപ്](https://inkscape.org/) ഉപയോഗിക്കാം. ത്രിമാന ചിത്രങ്ങൾ പോലും വരച്ച് ലാറ്റെൿ‌ കോഡ്
ലഭിക്കുന്ന ഒരെണ്ണമാണ് [അസിംടോട്ട്](https://www.ctan.org/pkg/asymptote). ഈ രണ്ടു് സോഫ്റ്റ്‌വെയറുകളും
നിർമ്മിക്കുന്ന ചിത്രങ്ങൾ ലാറ്റെൿ‌ പ്രമാണത്തിൽ നേരിട്ട് ചേർക്കാൻ സാധിക്കുന്നതാണ്.

വളരെ കൃത്യതയോടെയുള്ളതും, പ്രമാണത്തിനു് യോജിക്കും വിധം സമവാക്യങ്ങളും അടയാളങ്ങളും ഉൾപ്പെടുത്തിയതുമായ, ലാറ്റെക്കിന്
വിശേഷിച്ചും അനുയോജ്യമായ ചിത്രങ്ങൾ നിങ്ങൾക്കു നിർമ്മിക്കാവുന്നതാണ്. [Ti*k*Z](https://ctan.org/pkg/pgf)
ഉപയോഗിച്ച് നേരിട്ട് ലാറ്റെൿ‌ പ്രമാണത്തിനകത്തു തന്നെ ചിത്രങ്ങൾ വരയ്ക്കാനുള്ള കോഡ് എഴുതാവുന്നതാണ്; സൗകര്യപ്രദമാണ്
എന്നാൽ പ്രമാണം അല്പം കൂടെ സങ്കീർണ്ണമാവും എന്നുമാത്രം. മറ്റൊരു വഴി [PSTricks](https://ctan.org/pkg/pstricks-base)
ഉപയോഗിക്കുക എന്നതാണു്.


## ചിത്രങ്ങളുടെ സ്ഥാനനിർണ്ണയം

ലാറ്റെൿ‌ ചിത്രങ്ങളും പട്ടികകളും വിന്യസിക്കുന്നത് സങ്കീർണ്ണമായ രീതിയിലാണു്. ഇൻപുട്ടിൽ നല്കിയ അതേ സ്ഥലത്തു തന്നെ ഔട്പുട്ടിൽ
ചിത്രം കാണുകയെന്നത് പതിവായി കാണാറുള്ള ഒരു അഭ്യർത്ഥനയാണു്. `float` പൊതിക്കെട്ട് ഉപയോഗിച്ച് അതു് സാധിക്കാം.


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

ശ്രദ്ധിക്കുക, `H` എന്ന ഐച്ഛികം ചിത്രത്തെ 'നിർബന്ധമായും ഇവിടെത്തന്നെ' കാണിക്കുക എന്ന് ലാറ്റെക്കിനോട് ആവശ്യപ്പെടും.
പക്ഷേ, `H` ഉപയോഗിക്കാതിരിക്കാൻ പരമാവധി ശ്രമിക്കാനാണു് സാധാരണ ശുപാർശ ചെയ്യുന്നത്, കാരണം ഒരുപാട് ശൂന്യസ്ഥലം
അതു നിമിത്തം പ്രമാണത്തിൽ ഉണ്ടാവാം.

## മറ്റുവിധത്തിലുള്ള 'ഫ്ലോട്ടുകൾ'

പട്ടികകളും പരത്തിവയ്ക്കാം (float) എന്ന് നമ്മൾ [ഉടനേ](lesson-08) കാണും; അവയ്ക്ക് `table` എന്ന പരിസരം
ഉപയോഗിക്കണം. എന്നിരുന്നാലും, ചിത്രങ്ങൾ `figure` പരിസരത്തിനകത്തോ പട്ടികകൾ `table` പരിസരത്തിനകത്തോ
തന്നെ നല്കണമെന്ന് നിർബന്ധമൊന്നുമില്ല, സാധാരണ അനുവർത്തിക്കുന്നത് അങ്ങനെയെന്നു മാത്രം.

മറ്റു പരിസരങ്ങളും നിങ്ങൾക്ക് പരത്തിവയ്ക്കാം, ഓരോ തരവും വെവ്വേറെയായിരിക്കും വിന്യസിക്കപ്പെടുക. [`trivfloat`](https://ctan.org/pkg/trivfloat) 
എന്ന പൊതിക്കെട്ട് ഇതിനുപയോഗിക്കാം; പുതിയ തരം ഫ്ലോട്ടുകളെ നിർമ്മിക്കാൻ `\trivfloat` എന്ന ആജ്ഞ അതു നല്കുന്നു.


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
