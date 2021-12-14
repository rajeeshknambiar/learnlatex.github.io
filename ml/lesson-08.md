---
layout: "lesson"
lang: "ml"
title: "പട്ടികകൾ"
description: "ലാറ്റെക്കിൽ പട്ടികകൾ നിർമ്മിക്കുന്ന വിധം മനസ്സിലാക്കുകയാണു് ഈ പാഠത്തിന്റെ പ്രധാന ലക്ഷ്യം. വരികൾ (rows), പംക്തികൾ (columns), കോശങ്ങൾ (cells) എന്നിവ ഉപയോക്താവിന്റെ ഇച്ഛാനുസരണം അണിനിരത്തൽ (align), കോശങ്ങളുടെ ലയനം (merging) എന്നിവയും വിശദീകരിക്കുന്നു."
toc-anchor-text: "പട്ടികകൾ ലാറ്റെക്കിൽ"
toc-description: "പട്ടികനിർമ്മിതിയുടെ മൂലതത്വങ്ങൾ."
---

# പട്ടികകൾ

<span class="summary">ലാറ്റെക്കിൽ പട്ടികകൾ നിർമ്മിക്കുന്ന വിധവും, അതിന്റെ വിവിധ ഘടകങ്ങൾ കോർത്തിണക്കുന്ന രീതികളുമാണു് ഈ പാഠത്തിലെ പ്രധാന വിഷയം.</span>

ലാറ്റെക്കിൽ പട്ടികകൾ നിർമ്മിക്കുന്നതു് `tabular` എന്ന പരിസരം (environment) ഉപയോഗിച്ചാണു്. നിങ്ങൾ `array` എന്ന പാക്കേജ് ഉപയോഗിക്കും എന്നു് ഈ പാഠം പ്രതീക്ഷിക്കുന്നു. എന്തെന്നാൽ, ഈ പാക്കേജ് പട്ടികകളെ കൂടുതൽ കർമ്മക്ഷമത ഉള്ളതാക്കുന്നു. ഇങ്ങനെ അധികരിക്കുന്ന കർമ്മക്ഷമത ചരിത്രപരമായ കാരണങ്ങളാൽ ലാറ്റെക്കിന്റെ കാതലിൽ സ്വതവേയുള്ള പട്ടികയുടെ ക്രമീകരണത്തിൽ ഇല്ലാത്തവയാണു്.  അതുകൊണ്ടു് ചുവടെ ചേർക്കുന്ന രീതിയിൽ `array` ലോഡ് ചെയ്യുക.

```latex
\usepackage{array}
```
{: .noedit :}

ഒരു പട്ടിക വിന്യസിക്കാൻ, പട്ടികയിൽ എത്ര പംക്തികളുണ്ടെന്നും അവ എങ്ങനെയാണു് അണിനിരത്തേണ്ടതെന്നും നമുക്കു് ലാറ്റെക്കിനെ ബോദ്ധ്യപ്പെടുത്തേണ്ടതുണ്ടു്. ഇതു് `tabular` എന്ന പരിസരത്തിന്റെ നിർബന്ധിതവാദമായിട്ടാണു് നൽകുക. ഈ വാദങ്ങൾ വെറും ഒരൊറ്റ അക്ഷരം കൊണ്ടുള്ളവയാണു്. ഇവയെ നമ്മൾ പീഠികാസൂചകം (preamble token) എന്നു വിളിക്കുന്നു. ഓരോ സൂചകവും പംക്തികളുടെ ഓരോ തരം അണിയലിനെ സൂചിപ്പിക്കുന്നു. അങ്ങനെ ലാറ്റെക്കിന്റെ പട്ടികയിൽ ലഭ്യമായ പീഠികാസൂചകങ്ങൾ ചുവടെ വിവരിക്കുന്നു:

<!-- don't line wrap this table, markdown seems to not support this -->

| സൂചകം     | വിവരണം |
| ---        |:-- |
| `l`        | പംക്തിയെ ഇടത്തോട്ടു് അണിനിരത്തുന്നു |
| `c`        | പംക്തിയെ മദ്ധ്യഭാഗത്തു് അണിനിരത്തുന്നു  |
| `r`        | പംക്തിയെ വലത്തോട്ടു് അണിനിരത്തുന്നു  |
| `p{width}` | നിശ്ചിത വീതിയുള്ള (`width`) പംക്തി; ഇവിടെ പാഠത്തിലെ വരികൾ നിശ്ചിത വീതി കഴിഞ്ഞാൽ സ്വയം മുറിഞ്ഞു് വലതു വശം ‘ജസ്റ്റിഫൈ’ ചെയ്തു വിന്യസിച്ചുകൊള്ളും|
| `m{width}` | `p` പോലെ തന്നെയാണു്, പക്ഷെ, ആ വരിയിലെ മറ്റു കോശങ്ങളുമായി ഒത്തുനോക്കുമ്പോൾ ലംബായമാനമായി അണിനിരക്കും. |
| `b{width}` | `p` പോലെ തന്നെയാണു്, അടി ഭാഗത്തു് അണിനിരക്കും |
| `w{align}{width}` | ഉള്ളടക്കത്തെ നിശ്ചിതവീതിയുള്ള ലിപിയിൽ വിന്യസിക്കും. തിരശ്ചീനമായ അണിനിരത്തലിനു് `l`, `c`, `r` എന്നിവയിൽ ഒരു സൂചകം ഉപയോഗിക്കാം. |
| `W{align}{width}` | `w` പോലെയാണു്, നിശ്ചിതവീതി കഴിഞ്ഞുപോയാൽ മുന്നറിയിപ്പു് നൽകും. |


ഇതുകൂടാതെ, ചില പീഠികാസൂചകങ്ങൾ കൂടിയുണ്ടു്. അവ പംക്തികളുടെ അണിനിരത്തലിനു് വേണ്ടിയുള്ളതല്ല, പ്രത്യുത, മറ്റു ചില അനുബന്ധാവശ്യങ്ങൾക്കുള്ളവയാണു്. ചുവടെയുള്ള പട്ടിക കാണുക:

<!--- don't line wrap this table, markdown seems to not support this -->

| സൂചകം | വിവരണം |
| ---  | :-- |
| `*{num}{string}` | `string`-നെ `num` തവണ പീഠികയിൽ ആവർത്തിക്കും. ഈ സൂചകം ഉപയോഗിച്ചു് ഒന്നുപോലെയുള്ള പല പംക്തികൾ ഒറ്റയടിക്കു് നിർമ്മിക്കാം. |
| `>{decl}` | ഇതു് `decl`-നെ കോശത്തിലെ ഉള്ളടക്കത്തിനു മുന്നിൽ ആ പംക്തിയിൽ ആസകലം വിന്യസിക്കും (ഇതു് പലപ്പോഴും ഒരു പംക്തിയെ മാത്രം വേറൊരു ലിപിസഞ്ചയം ഉപയോഗിച്ചു് വിന്യസിക്കാൻ സഹായിക്കും). |
| `<{decl}` | ഇതു് `decl`-നെ കോശത്തിലെ ഉള്ളടക്കത്തിനു പിന്നിൽ ആ പംക്തിയിൽ ആസകലം വിന്യസിക്കും  |
| <span>`|`</span>  | ലംബായമാനമായ രേഖ വിന്യസിക്കും. |
| `@{decl}` | രണ്ടു് പംക്തികൾക്കിടക്കുള്ള ശൂന്യസ്ഥലത്തെ `decl` കൊണ്ടു് പകരം വെക്കും. |
| `!{decl}` | `decl`-നെ ഇപ്പോൾ നിലവിലുള്ള സ്ഥലത്തിന്റെ മദ്ധ്യഭാഗത്തു് സ്ഥാപിക്കും. |


മുകളിൽ കാണിച്ച രണ്ടു പട്ടികകളിലായി, `array` പാക്കേജിൽ നിന്നും പുതുതായി ലഭ്യമായവയും ലാറ്റെക്കിൽ സ്വതേയുള്ളവയടക്കം എല്ലാതരം പംക്തികളെയും കുറിച്ചു് പറഞ്ഞു കഴിഞ്ഞു. ഇനിയും മറ്റു ചില പാക്കേജുകളിൽ നിന്നു് ലഭ്യമാക്കാവുന്ന വിവധതരം പംക്തികളെക്കുറിച്ചു് വിശദീകരിക്കാനുണ്ടു്. അവയെ നമ്മൾ [മറ്റൊരു പാഠത്തിലേയ്ക്കു്](more-08) മാറ്റിയിരിക്കുന്നു.

`l`, `c`, `r` എന്നീ സൂചകങ്ങൾ വഹിക്കുന്ന പംക്തികളുടെ വീതി അതിലെ ഏറ്റവും വീതികൂടിയ കോശത്തിന്റെ വീതിയായി നിജപ്പെടുത്തിയിരിക്കുന്നു. ഒരോ പംക്തിയും `tabular` പരിസരത്തിന്റെ നിർബന്ധിതവാദമായിട്ടു് പ്രസ്താവിക്കേണ്ടതാണു്. ഉദാഹരണമായി, മദ്ധ്യത്തു് അണിനിരത്തുന്ന മൂന്നു് പംക്തികൾ നമുക്കു് വേണമെങ്കിൽ, `ccc` എന്നു് പട്ടികയുടെ  പീഠികയിൽ പ്രസ്താവിക്കണം. ഇവിടെ ശൂന്യസ്ഥലത്തെ അവഗണിക്കുന്നതിനാൽ `c c c` എന്നു് നൽകിയാലും ശരിയാണു്.

പട്ടികയിലെ കോശങ്ങളിൽ പാഠം നിവേശനം ചെയ്യുമ്പോൾ പംക്തികൾ തമ്മിൽ വേർതിരിക്കാൻ `&` എന്ന ചിഹ്നവും, വരികൾ തമ്മിൽ വേർതിരിക്കാൻ `\\` എന്ന ആജ്ഞയും ഉപയോഗിക്കുന്നു. 

ചുവടെ ചേർത്തിരിക്കുന്ന പട്ടികയിൽ ഒരു മാതൃകാ പട്ടികയിൽ കാണുന്ന എല്ലാതരം സൂചകങ്ങളും, ആജ്ഞകളും, ചിഹ്നങ്ങളും ഉപയോഗിച്ചിട്ടുണ്ടു്. ഇവിടെ നമ്മൾ `&`, `\\` എന്നിവ ലംബായമാനമായി, കൃത്യമായി അണിനിരത്തിയ രീതിയിലാണു് നിവേശനം ചെയ്തിട്ടുള്ളതു്. ലാറ്റെക്കിനു് ഇങ്ങനെ പാഠം നിവേശിക്കണമെന്ന ഒരു നിർബന്ധവുമില്ല. എന്നിരിക്കലും, ഇതു് പിന്നിടു് തിരുത്തേണ്ട ഘട്ടം വരുമ്പോൾ പംക്തികൾ, വരികൾ എന്നിവയുടെ ആദിയും അന്തവും കണ്ടെത്താൻ വളരെ സഹായിക്കുന്നു, പ്രയത്നം ലഘൂകരിക്കുന്നു.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{lll}
  Animal & Food  & Size   \\
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
\end{tabular}
\end{document}
```

<!-- {% endraw %} -->

പട്ടികയിലെ ഒരു പംക്തിയിൽ അപ്രതീക്ഷിതമായ അളവിൽ പാഠം നിവേശിക്കേണ്ടിവന്നാൽ, അതിലെ അണിനിരത്തൽ സൂചകം `l`, `c`, `r` എന്നിവയിൽ ഒന്നാണെങ്കിൽ തീർച്ചയായും ശരിയായി വിന്യസിക്കുന്ന കാര്യത്തിൽ പ്രശ്നങ്ങൾ നേരിടാൻ സാദ്ധ്യതകളുണ്ടു്. ചുവടെയുള്ള ഉദാഹരണം കാണുക:

<!-- {% raw %} -->

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{cl}
  Animal & Description \\
  dog    & The dog is a member of the genus Canis, which forms part of the
           wolf-like canids, and is the most widely abundant terrestrial
           carnivore. \\
  cat    & The cat is a domestic species of small carnivorous mammal. It is the
           only domesticated species in the family Felidae and is often referred
           to as the domestic cat to distinguish it from the wild members of the
           family. \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


പ്രശ്നം പ്രധാനമായി ഉത്ഭവിക്കുന്നതു് `l`, `c`, `r` പംക്തികളിൽ നിവേശിക്കുന്ന പാഠം കോശത്തിന്റെ വീതി കവിഞ്ഞാൽ ഒരിക്കലും പാഠത്തെ മുറിക്കാൻ കൂട്ടാക്കുകയില്ല. ഇതിനെ തരണം ചെയ്യാൻ പംക്തിയുടെ സൂചകം `p` എന്നു് മാറ്റേണ്ട ആവശ്യമുണ്ടു്. അങ്ങനെ ചെയ്യുമ്പോൾ `p`-യ്ക്കു് നിർബന്ധിതവാദമായി നൽകിയ വീതിയുടെ അളവിൽ പാഠം നിറഞ്ഞുകഴിഞ്ഞാൽ, പാഠത്തെ മുറിച്ചു് ഒരു ഖണ്ഡികയായി വിന്യസിക്കുകയും, ആ വരിയിലെ മറ്റു കോശങ്ങൾക്കൊപ്പം മുകൾഭാഗത്തു് നിരക്കുന്ന രീതിയിൽ അണിനിരത്തുകയും ചെയ്യും. ഈ രീതിയാണു് മിക്കവാറും സന്ദർഭങ്ങളിൽ നമ്മൾ ആഗ്രഹിക്കുന്നതും. മുകളിൽ കണ്ട ഉദാഹരണത്തെ മാറ്റി വിന്യസിക്കുമ്പോൾ ഉണ്ടാവുന്ന മാറ്റങ്ങൾ ചുവടെയുള്ള ഉദാഹരണത്തിൽ കാണാവുന്നതാണു്:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{cp{9cm}}
  Animal & Description \\
  dog    & The dog is a member of the genus Canis, which forms part of the
           wolf-like canids, and is the most widely abundant terrestrial
           carnivore. \\
  cat    & The cat is a domestic species of small carnivorous mammal. It is the
           only domesticated species in the family Felidae and is often referred
           to as the domestic cat to distinguish it from the wild members of the
           family. \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


ഒരേ തരത്തിലുള്ള പംക്തികൾ പീഠികയിൽ പ്രസ്താവിക്കാൻ ഒരു എളുപ്പ വഴിയുണ്ടു്. ഉദാഹരണമായി, മദ്ധ്യത്തിൽ അണിനിരക്കുന്ന ആറു പംക്തികൾ പ്രസ്താവിക്കാൻ `cccccc` എന്നു പറയേണ്ടതിനുപകരം എളുപ്പമാർഗ്ഗമായി `*{6}{c}` എന്നു് പട്ടികയുടെ പീഠികയിൽ രേഖപ്പെടുത്തിയാൽ മതി. `6` എന്നതു് എത്ര പംക്തികൾ വേണം എന്നതിനെയും `c` എന്നതു് അണിനിരത്തൽ നിർദ്ദേശിക്കുന്ന സൂചകവുമാണു്. ഇതു് വിശദമാക്കാൻ ഒരു ഉദാഹരണം ചുവടെ ചേർത്തിട്ടുണ്ടു്:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{*{3}{l}}
  Animal & Food  & Size   \\
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


## രേഖകൾ പട്ടികയിൽ

പട്ടികയിൽ രേഖകൾ ഉൾക്കൊള്ളിക്കാൻ പഠിക്കും മുമ്പു് ഒരു നിർദ്ദേശം ഉണ്ടു്: രേഖകൾ വളരെ വിരളമായി മാത്രമേ ഉപയോഗിക്കാവൂ. മാത്രവുമല്ല, ലംബ രേഖകൾ ഉപയോഗിക്കുന്നതു് തൊഴിൽപരമായ മികവിന്റെ അഭാവമായിട്ടാണു് കരുതപ്പെടുന്നതു്. വിന്യാസമികവുള്ള പട്ടികകൾ നിർമ്മിക്കുമ്പോൾ ഒരിക്കലും ലാറ്റെക്കിന്റെ സ്വതേയുള്ള രേഖാസംബന്ധിയായ ആജ്ഞകൾ ഉപയോഗിക്കാതിരിക്കുക. പകരം, `booktabs` എന്ന പാക്കേജ് ലഭ്യമാക്കുന്ന ആജ്ഞകൾ ഉപയോഗിക്കുക. തൊഴിൽപരമായ മികവു് കൂടുതൽ നൽകുന്നതിനാൽ, ഈ പാക്കേജിലെ ആനുകൂല്യങ്ങളെ നമുക്കു് ആദ്യം പഠിക്കാം.

`booktabs` നമുക്കു് നാലു് വ്യത്യസ്തമായ രേഖകൾ നൽകുന്നു, അവയിൽ മൂന്നെണ്ണം ഇതാ: `\toprule`, `\midrule`, `\bottomrule`. പേരുകൾ സൂചിപ്പിക്കുന്നതുപോലെ, അവ യഥാക്രമം ഒരു പട്ടികയുടെ ഏറ്റവും മുകളിലും, പട്ടികയുടെ മറ്റു ഭാഗങ്ങളിലും, ഏറ്റവും അവസാനമായും ഉപയോഗിക്കാനുള്ളവയാണു്. ചുവടെ കൊടുത്തിരിക്കുന്ന ഉദാഹരണം ഈ കാര്യത്തെ കൂടുതൽ വിശദമാക്കും.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}


\begin{document}
\begin{tabular}{lll}
  \toprule
  Animal & Food  & Size   \\
  \midrule
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

`booktabs` നൽകുന്ന നാലാമത്തെ രേഖ `\cmidrule` എന്നതാണു്. ഈ ആജ്ഞയുടെ പ്രധാന ഉദ്ദേശ്യം തിരശ്ചീനമായി പട്ടിക മുഴുവൻ ബന്ധിപ്പിക്കുന്ന ഒരു രേഖ വരയ്ക്കാനല്ല, പ്രത്യുത, ഏതാനും പംക്തികളെ മാത്രം ബന്ധിപ്പിക്കുന്ന ഒരു രേഖ ചേർക്കുന്നതിനാണു്. ഏതു് പംക്തി മുതൽ ഏതു് പംക്തിവരെയാണെന്ന വിവരം ലാറ്റെക്കിനെ ധരിപ്പിക്കാൻ വേണ്ടി  `\cmidrule`-നു ഒരു നിർബന്ധിതവാദമുണ്ടു്. ചുവടെ കൊടുത്തിരിക്കുന്ന ഉദാഹരണത്തിൽ `\cmidrule{1-2}` എന്നു കാണാം. ഇതിനർത്ഥം ഒന്നാമത്തെ പംക്തി മുതൽ രണ്ടാമത്തെ പംക്തി വരെ മാത്രം നീളുന്ന ഒരു രേഖ ചേർക്കുക എന്നാണു്. അതുപോലെ തന്നെ ഒരു പംക്തിയിൽ മാത്രം ഒരു രേഖ ചേർക്കണമെങ്കിൽ `\cmidrule{1-1}` എന്നതിൽ കാണുന്നതുപോലെ തുടങ്ങുന്നതും അവസാനിക്കുന്നതും ഒരേ പംക്തിയുടെ നമ്പർ ആണെന്നറിയുക.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{lll}
  \toprule
  Animal & Food  & Size   \\
  \midrule
  dog    & meat  & medium \\
  \cmidrule{1-2}
  horse  & hay   & large  \\
  \cmidrule{1-1}
  \cmidrule{3-3}
  frog   & flies & small  \\
  \bottomrule
\end{tabular}13wXQHC!Mepk
\end{document}
```
<!-- {% endraw %} -->


`\cmidrule`-നു് വളരെ പ്രയോജനമുള്ള മറ്റൊരു വിശേഷഗുണം കൂടിയുണ്ടു്. രണ്ടുവശവും ഈ രേഖയെ വേണമെങ്കിൽ നമുക്കു് ഇച്ഛാനുസരണം അല്പം ചെറുതാക്കുകയും ചെയ്യാൻ സഹായിക്കുന്ന ഒരു ഐച്ഛികവാദവും ലഭ്യമാണു്. ഉദാഹരണം കാണുക.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{lll}
  \toprule
  Animal & Food  & Size   \\
  \midrule
  dog    & meat  & medium \\
  \cmidrule{1-2}
  horse  & hay   & large  \\
  \cmidrule(r){1-1}
  \cmidrule(rl){2-2}
  \cmidrule(l){3-3}
  frog   & flies & small  \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


`r`-ഉം  `l`-ഉം യഥാക്രമം വലതും ഇടതും ചെറുതാക്കാൻ സഹായിക്കുന്നുവെന്നു് നിങ്ങൾ മിക്കവാറും ഊഹിച്ചിരിക്കും. 

മറ്റു ചില അവസരങ്ങളിൽ രണ്ടു് വരികളെ അർത്ഥപൂർണ്ണമായി വിഭജിക്കാൻ രേഖയെക്കാൾ അനുയോജ്യം അല്പം ശൂന്യസ്ഥലമാണെന്നു തോന്നാറുണ്ടു്. അത്തരം സന്ദർഭങ്ങളിൽ ഉപകാരമാവുന്ന ഒരു ആജ്ഞയാണു് `\addlinespace`. ഈ ആജ്ഞയുപയോഗിച്ചു് ചെറിയ ലംബസ്ഥലം രണ്ടു് വരികൾക്കിടയിൽ നിവേശിക്കാൻ സാധിക്കും.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{cp{9cm}}
  \toprule
  Animal & Description \\
  \midrule
  dog    & The dog is a member of the genus Canis, which forms part of the
           wolf-like canids, and is the most widely abundant terrestrial
           carnivore. \\
  \addlinespace
  cat    & The cat is a domestic species of small carnivorous mammal. It is the
           only domesticated species in the family Felidae and is often referred
           to as the domestic cat to distinguish it from the wild members of the
           family. \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


## കോശങ്ങളുടെ ലയനം

ലാറ്റെക്കിൽ തിരശ്ചീനമായി ഒന്നിലധികം കോശങ്ങൾ ലയിപ്പിക്കാൻ `\multicolumn` എന്ന ആജ്ഞയെയാണു് ആശ്രയിക്കുന്നതു്. ഇതിനു് മൂന്നു് നിർബന്ധിതവാദങ്ങൾ നൽകണം:

1. ലയിപ്പിക്കാൻ ആഗ്രഹിക്കുന്ന കോശങ്ങളുടെ എണ്ണം
2. ലയനാനന്തര കോശത്തിന്റെ അണിനിരത്തൽ
3. ലയനകോശത്തിൽ നിവേശിക്കേണ്ട ഉള്ളടക്കം

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}


\begin{document}
\begin{tabular}{lll}
  \toprule
  Animal & Food  & Size   \\
  \midrule
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
  fuath  & \multicolumn{2}{c}{unknown} \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


ഒരു കോശത്തിലെ ഉള്ളടക്കത്തിന്റെ അണിനിരത്തൽ, ആ കോശം ഉൾക്കൊള്ളുന്ന പംക്തിയുടേതിൽ നിന്നു് വ്യത്യസ്തമായി വെണമെങ്കിലും  `\multicolumn` എന്ന ആജ്ഞയെ നമുക്കു് പ്രയോഗിക്കാവുന്നതാണു്. ചുവടെയുള്ള ഉദാഹരണം കാണുക.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}


\begin{document}
\begin{tabular}{lll}
  \toprule
  \multicolumn{1}{c}{Animal} & \multicolumn{1}{c}{Food} & \multicolumn{1}{c}{Size} \\
  \midrule
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
  fuath  & \multicolumn{2}{c}{unknown} \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

കോശങ്ങൾ ലംബായമാനമായി ലയിപ്പിക്കാൻ ലാറ്റെക്കിൽ ആജ്ഞകളില്ല. ആയതിലേയ്ക്കു് അതിനു പറ്റിയ രീതിയിൽ കോശങ്ങൾ ശൂന്യങ്ങളായി നിലനിറുത്തിക്കൊണ്ടാണു് സാധിച്ചെടുക്കുക.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}


\begin{document}
\begin{tabular}{lll}
  \toprule
  Group     & Animal & Size   \\
  \midrule
  herbivore & horse  & large  \\
            & deer   & medium \\
            & rabbit & small  \\
  \addlinespace
  carnivore & dog    & medium \\
            & cat    & small  \\
            & lion   & large  \\
  \addlinespace
  omnivore  & crow   & small  \\
            & bear   & large  \\
            & pig    & medium \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


## അഭ്യാസം

ചെറിയ/ലഘുവായ ഉദാഹരണങ്ങൾ ഉപയോഗിച്ചു് പട്ടികകളുടെ വിന്യാസം പരിചയപ്പെടുക. പല തരത്തിലുള്ള അണിനിരത്തലുകൾ പരീക്ഷിക്കുക. ഒരു വരിയിൽ ഉണ്ടാവേണ്ട കോശങ്ങളിൽ കുറവായും അതിൽ കൂടുതലായും പാഠം നിവേശിച്ചു് എന്തു് ഫലമാണുണ്ടാവുന്നതെന്നു് പരിശോധിക്കുക.

`\multicolumn` പരീക്ഷിക്കുക. 

