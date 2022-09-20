---
layout: "lesson"
lang: "ml"
title: "അക്ഷരസഞ്ചയങ്ങൾ തിരഞ്ഞെടുക്കുന്നതും യുണികോഡ് എന്‍ജിനുകൾ ഉപയോഗിക്കുന്നതും"
description: "ലാറ്റെൿ എങ്ങനെയാണ് യുണിക്കോഡ് ഇന്‍പുട് മനസ്സിലാക്കുന്നതെന്നും നിങ്ങൾ ടൈപ്പു ചെയ്യുന്നതിനെയും ലിപികൾ ഉപയോഗിക്കുന്നതിനെയും അതെങ്ങനെ സ്വാധീനിക്കുന്നു എന്നുമുള്ള പശ്ചാത്തലം ഈ പാഠം നല്കുന്നു. യുണികോഡിനെപ്പറ്റിയും ഓപ്പണ്‍ടൈപ് അക്ഷരസഞ്ചയങ്ങളെപ്പറ്റിയും മനസ്സിലാക്കാം."
toc-anchor-text: "അക്ഷരസഞ്ചയങ്ങളും യുണികോഡ് എന്‍ജിനുകളും"
toc-description: "അക്ഷരസഞ്ചയങ്ങളുടെ തിരഞ്ഞെടുപ്പും ഫയൽ എന്‍കോഡിങും."
---

# അക്ഷരസഞ്ചയങ്ങളും യുണികോഡ് എന്‍ജിനുകളും

<span
  class="summary">ലാറ്റെൿ എങ്ങനെയാണ് യുണിക്കോഡ് ഇന്‍പുട് മനസ്സിലാക്കുന്നതെന്നും നിങ്ങൾ ടൈപ്പു ചെയ്യുന്നതിനെയും ലിപികൾ ഉപയോഗിക്കുന്നതിനെയും അതെങ്ങനെ സ്വാധീനിക്കുന്നു എന്നുമുള്ള പശ്ചാത്തലം ഈ പാഠം നല്കുന്നു. യുണികോഡിനെപ്പറ്റിയും ഓപ്പണ്‍ടൈപ് അക്ഷരസഞ്ചയങ്ങളെപ്പറ്റിയും മനസ്സിലാക്കാം.</span>

റ്റെൿ, ലാറ്റെൿ എന്നിവ വ്യാപകമായി ഉപയോഗിക്കപ്പെടാൻ തുടങ്ങുന്ന സമയത്ത് യൂറോപ്യൻ ഭാഷകള്‍ക്കുള്ള പിന്തുണ മാത്രമേ
ലഭ്യമായിരുന്നുള്ളൂ, റഷ്യനും ഗ്രീക്കും പോലുള്ള മറ്റു ചില ലിപികളുപയോഗിക്കാനുള്ള പരിമിതമായ ശേഷിയും.

## യൂറോപ്യൻ ഭാഷകളിലുള്ള ഉച്ചാരണചിഹ്നങ്ങളും അവയുള്ള അക്ഷരങ്ങളും

ആദ്യകാലത്തു്, യൂറോപ്യൻ ഭാഷകളിലുള്ള ഉച്ചാരണചിഹ്നങ്ങളും അവയുള്ള അക്ഷരങ്ങളും കമാന്‍ഡുകളോ മാക്രോകളോ ഉപയോഗിച്ചാണു്
ഇൻപുട് ചെയ്തിരുന്നതു്, ഉദാ: ‘ç’ എന്നതിനു് `\c{c}`, ‘é’ എന്നതിനു് `\'e` മുതലായവ. ടൈപ്പ് ചെയ്യാനുള്ള സൗകര്യം
കാരണം ചിലർ ഇപ്പൊഴും ഈ രീതി പിന്തുടരുന്നുവെങ്കിലും മറ്റു ചിലർ അവരുടെ കീബോഡിൽ ലഭ്യമായ അത്തരം ചിഹ്നങ്ങൾ
നേരിട്ടുപയോഗിക്കാൻ താത്പര്യപ്പെടും.

യുണികോഡിനു മുമ്പുള്ള കാലത്ത് വിവിധ ഭാഷകളിൽ പാഠം നേരിട്ടെഴുതാവുന്ന പല *ഫയൽ എന്‍കോഡിങ്* തരങ്ങളും ലാറ്റെൿ
പിന്തുണച്ചിരുന്നു — ഉദാഹരണത്തിനു് ഫ്രഞ്ചുകാർ `latin1` എന്‍കോഡിങ് ഉപയോഗിച്ച് ‘`déjà vu`’ എന്നെഴുതുന്നതു്
ലാറ്റെൿ ആന്തരികമായി ചിഹ്നങ്ങളുള്ള അക്ഷരങ്ങളെ ടെൿ കമാന്‍ഡായി മാറ്റി ശരിയായ ഔട്ട്പുട് കാണിക്കും.

ആധുനിക ലാറ്റെക്കിൽ  ഈ സമീപനം ഇപ്പൊഴും `pdflatex`  എന്‍ജിനുപയോഗിക്കുമ്പോൾ ലഭ്യമാണു്.
മറുവിധം നിര്‍ദ്ദേശിച്ചില്ലെങ്കിൽ എല്ലാ ഫയലുകളും  സ്വതവേ യുണികോഡ്  (UTF-8 എൻകോഡിങ്) പിന്തുടരുന്നുവെന്നു്
അനുമാനിക്കപ്പെടും. ഈ എന്‍ജിനു് 8-ബിറ്റ് അക്ഷരസഞ്ചയങ്ങളുടെ പരിമിതിയുണ്ടെങ്കിലും  മിക്ക യൂറോപ്യൻ
ഭാഷകളെയും പിന്തുണയ്ക്കാനാകും.

##അക്ഷരസഞ്ചയങ്ങളുടെ തിരഞ്ഞെടുപ്പ്

Font selection with `pdflatex` uses the robust LaTeX font selection scheme, and
nowadays there are many fonts ready-to-use in a standard LaTeX distribution. For
example, the TeX Gyre fonts are a suite of high-quality fonts based on common
fonts that most people are familiar with such as Times, Helvetica, Palatino, and
others. To load these fonts, it is as simple as loading a package with the
appropriate name. For a Times lookalike, the TeX Gyre name is Termes:

```latex
\usepackage{tgtermes}
```
{: .noedit :}

For `pdflatex`, most fonts are accessible through packages.  You can have a look
at [The LaTeX Font Catalogue](https://www.tug.org/FontCatalogue/) or the
[CTAN page on the ‘Font’ topic](https://www.ctan.org/topic/font) to see some
options.  You can also search on the Internet for the font you want, and look
for a `pdflatex`-compatible package version.  If you want to use a proprietary
font, you can search for a suitable clone, which for most applications is
similar enough to the original.

## The Unicode era

As `pdflatex` is limited to 8-bit file encodings and 8-bit fonts, it cannot
natively use modern OpenType fonts and easily switch between multiple languages
that use different alphabets (or scripts, to use the technical term). There are
two replacements for pdfTeX that natively use Unicode input and modern fonts:
XeTeX and LuaTeX. For LaTeX, these are typically invoked in your editor using
the engines `xelatex` and `lualatex` respectively.

In these engines, font selection is performed by the `fontspec` package, and for
simple documents can look as easy as:
```latex
\usepackage{fontspec}
\setmainfont{texgyretermes-regular.otf}
```
{: .noedit :}

This selects the TeX Gyre Termes font, as in the `pdflatex` example above.
Notably, this approach works for *any* OpenType font.  Some fonts available for
`pdflatex` are also available to `xelatex` and `lualatex` through their
respective packages as well, or by loading any font you have installed on your
computer by using `fontspec` as shown above.

[The LaTeX Font Catalogue](https://www.tug.org/FontCatalogue/) also shows fonts
with OpenType formats available, so you can use that as a resource for looking
up fonts, as well as the [CTAN page](https://www.ctan.org/topic/font) mentioned
earlier.

Having selected a font, input can now be typed directly in plain Unicode into a 
source document. Here is an example showing some Latin and Greek letters as 
well as some CJK ideographs:

```latex
% !TEX xelatex
\documentclass{article}
\usepackage{fontspec}
\setmainfont{texgyretermes-regular.otf}
\newfontfamily\cjkfont{FandolSong-Regular.otf}
\begin{document}

ABC → αβγ → {\cjkfont 你好}

\end{document}
```

<p 
  class="hint">When switching between languages it is usually important to also change things like hyphenation patterns and so on, and the <code>babel</code> and <code>polyglossia</code> packages both provide robust features to do this.</p>
