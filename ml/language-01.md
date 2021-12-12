---
layout: "lesson"
lang: "ml"
title: "Language-specifics for Malayalam"
description: "This lesson shows language-specific details for typesetting with LaTeX in Malayalam. The focus is on hyphenation, where Malayalam typically does not have visible hyphen character."
next: "extra-01"
toc-anchor-text: "Malayalam Language-specifics"
toc-description: "Typesetting with LaTeX in Malayalam."
---

# മലയാള ഭാഷാ സവിശേഷതകൾ

<span
  class="summary">ഈ പാഠം, ലാറ്റെൿ ഉപയോഗിച്ച് പാഠവിന്യാസം ചെയ്യുമ്പോൾ മലയാള ലിപിക്ക് സവിശേഷമായുള്ള പ്രത്യേകതകളെ, വിശേഷിച്ചും വാക്കുകൾ മുറിക്കുന്നതിലുള്ളതിനെ പരിചയപ്പെടുത്തുന്നു.</span>

## പദം മുറിയ്ക്കൽ

മലയാളത്തിൽ വരിയുടെ അറ്റത്ത് വാക്കുകൾ മുറിക്കുന്നതിനെ സംബന്ധിച്ച് ലളിതമായ ചില നിയമങ്ങളുണ്ട്:

1. വ്യഞ്ജനം 1 + വിരാമചിഹ്നം + വ്യഞ്ജനം 2: വ്യഞ്ജനം 2നു് മുമ്പ് മുറിക്കാം
2. ചില്ലക്ഷരങ്ങള്‍ക്കു മുമ്പ് മുറിക്കാതിരിക്കുക
3. zero width joiner, zero width non-joiner ഇവയ്ക്കു ശേഷം മുറിക്കാതിരിക്കുക

സീറ്റെൿ (XeTeX) ഉപയോഗിച്ച് ഈ നിയമങ്ങളനുസരിക്കും വിധം മലയാളപാഠം വിന്യസിക്കുവാൻ `polyglossia` എന്ന പാക്കേജ് ഉപയോഗിച്ച് സാധിക്കും.

```latex
\documentclass{article}
\usepackage{fontspec}
\usepackage{polyglossia}
\setmainlanguage{Malayalam}
\newfontfamily{\malayalamfont}[Script=Malayalam}{RIT Rachana}
\begin{document}
ദീര്‍ഘമായൊരു വാക്കിനെ കൃത്യമായി വരികളൂടെ അറ്റത്തു വച്ച് മുറിക്കുന്നതിനെയാണ് `ഹൈഫനേഷൻ' എന്നു് അറിയപ്പെടുന്നതു്.
\end{document}
```