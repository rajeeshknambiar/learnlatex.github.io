---
layout: "lesson"
lang: "ml"
title: "പട്ടികകളെപ്പറ്റി കൂടുതലറിയാൻ"
description: "നിരയുടെ ശൈലി മാറ്റിയും വിടവുകളും വരകളും മാറ്റിയും പട്ടികകൾ പലവിധത്തിൽ ഭേദഗതി വരുത്താനും മറ്റു പൊതിക്കെട്ടുകളുപയോഗിച്ച് പട്ടികകളുടെ നിര്‍മ്മിതി വിപുലീകരിക്കാനും ഈ പാഠത്തിൽ മനസ്സിലാക്കാം."
toc-anchor-text: "പട്ടികകളെപ്പറ്റി കൂടുതലറിയാൻ"
---


## ആമുഖത്തിൽ നല്കുന്ന മറ്റു സൂചകങ്ങൾ

പട്ടികയുടെ നിരകളിൽ നല്കാവുന്ന എല്ലാ പീഠികാസൂചകങ്ങളും (preamble token) പ്രധാന പാഠത്തിൽ പറഞ്ഞിട്ടില്ല, അവയിൽ
ചിലത് ഉദാഹരണസഹിതം ഇവിടെ നല്കിയിട്ടുണ്ട്. പട്ടികകളിൽ ഇതുവരെ ലഭ്യമായിട്ടുള്ള സൂചകങ്ങൾ ഒന്നുകൂടെ പരിചയപ്പെടുന്നത്
നന്നായിരിക്കും. അവിടെ പറഞ്ഞിരുന്ന ലഘുവിവരണങ്ങൾ `l`, `c`, `r`, `p`എന്ന പംക്തീസൂചകങ്ങൾ (column types)
മനസ്സിലാക്കിയതിനുശേഷം `m`,`b`, `w`, `W` എന്നിവ മനസ്സിലാക്കാൻ സഹായിക്കും. ഇല്ലായെങ്കിൽ അവ പരീക്ഷിച്ചു നോക്കാം.
ശേഷിക്കുന്ന സൂചകങ്ങൾ ഇവയാണ്: `>`, `<`, `@`, `!`, `|`.


### ഒരു നിരയുടെ ശൈലീകരണം

`>`, `<` എന്നിവ ഒരു നിരയിലെ കോശങ്ങളുടെ ഉള്ളടക്കത്തിനു മുന്‍പും പിന്‍പും എന്തെങ്കിലും നല്കാനുപയോഗിക്കാമെന്നതിനാൽ
അവയുപയോഗിച്ച് നിരയുടെ കെട്ടും മട്ടും മാറ്റാനുള്ള ആജ്ഞകൾ നല്കാം. ഉദാഹരണത്തിനു്, ആദ്യത്തെ നിരയിലെ അക്ഷരങ്ങളെ
ചരിഞ്ഞ ശൈലിയിലാക്കാനും അതിനുശേഷം അര്‍ദ്ധവിരാമചിഹ്നം `:` നല്കാനും ഇങ്ങനെ ചെയ്യാം:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{>{\itshape}l<{:} *{2}{l}}
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

`\itshape` തുടര്‍ന്നു വരുന്ന എല്ലാ പാഠത്തെയും ചരിഞ്ഞ ശൈലിയിലാക്കുന്നു, പക്ഷേ അതിന്റെ പ്രഭാവം ഒരു
കോശത്തിനകത്തു മാത്രം 'ഒതുങ്ങുന്നു'. ആവശ്യാനുസരണം അക്ഷരശൈലി മാറ്റുന്നത് [അല്പം കഴിഞ്ഞുള്ള പാഠത്തിൽ
കാണാം](lesson-11).

ആദ്യത്തെ നിര പട്ടികയുടെ തലക്കെട്ട് ആയതിനാൽ അതിനെ ഈ ശൈലീകരണത്തിൽ നിന്ന് നമുക്ക് ഒഴിവാക്കാം.
അതിന് `\multicolumn` ഉപയോഗിക്കാം. ഒരൊറ്റ കോശത്തിന്റെ അണിനിരത്തൽ മാറ്റാനും താഴെ നല്കിയിരിക്കുന്നതു
പോലെ ഇതുപയോഗിക്കാമെന്ന് ഓര്‍ക്കുക.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{>{\itshape}l<{:} *{2}{l}}
  \toprule
  \multicolumn{1}{l}{Animal} & Food  & Size   \\
  \midrule
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

### നിരകള്‍ക്കിടയിലെ അകലം ക്രമീകരിക്കുന്നത്

സന്തുലിതമായിരിക്കാനും വേറിട്ട് നില്ക്കാനുമായി ഓരോ നിരയുടെയും ഇരുവശത്തു് അല്പം വിടവ് പൊതുവേ ലാറ്റെൿ ചേര്‍ക്കും.
ഈ വിടവിന്റെ വലുപ്പം `\tabcolsep` എന്ന നീളമുപയോഗിച്ചാണ് നിര്‍വ്വചിച്ചിരിക്കുന്നത്. ഓരോ നിരയുടെയും ഇരുവശവും
ഈ വിടവുള്ളതിനാൽ ഒരു `\tabcolsep` നീളം പട്ടികയുടെ രണ്ടറ്റത്തും, 2`\tabcolsep` നീളം വരികള്‍ക്കിടയിലും
&ndash;  ഒരു വരിയിൽ നിന്ന് ഒന്നുവീതം നിങ്ങള്‍ക്കു ലഭിക്കും.`\setlength` എന്ന ആജ്ഞ ഉപയോഗിച്ച് ഈ നീളം
നിങ്ങള്‍ക്കിഷ്ടമുള്ളത്ര മാറ്റാം:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\setlength\tabcolsep{1cm}

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

`@` ഉപയോഗിച്ച് ഈ വിടവ് നിങ്ങള്‍ക്കു തോന്നിയതു പോലെ മാറ്റാം. രണ്ടു വരികള്‍ക്കിടയിലെ വിടവ് ഇത് കളയുകയും
പകരം നിങ്ങള്‍ വാദമായി നല്കിയതെന്തോ അതുപയോഗിക്കുകയും ചെയ്യും:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{l@{ : }l@{\hspace{2cm}}l}
  Animal & Food  & Size   \\
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

(`\hspace` എന്ന ആജ്ഞയെ നമ്മൾ [അടുത്തു തന്നെ](lesson-11) കാണും; തിരശ്ചീനമായി ശൂന്യസ്ഥലം വിടുകയാണ്
ഇതു ചെയ്യുന്നതെന്ന് ഊഹിക്കാമല്ലോ.)

`!`  എന്ന പീഠികാസൂചകവും സമാനമായ കാര്യമാണു് ചെയ്യുന്നതു്. രണ്ടു വരികള്‍ക്കിടയിലെ വിടവിനു നടുക്ക് അതിന്റെ വാദം ചേര്‍ക്കുന്നു
എന്നതാണു് വ്യത്യാസം.


<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{l!{:}ll}
  Animal & Food  & Size   \\
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->


### ലംബ വരകൾ

ചിലപ്പോൾ നിങ്ങള്‍ക്ക് പട്ടികയിലെ നിരകള്‍ക്കിടയിൽ ലംബമായുള്ള വരകൾ ഉപയോഗിക്കേണ്ടി വന്നേക്കാം.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}

\begin{document}
\begin{tabular}{l|ll}
  Animal & Food  & Size   \\[2pt]
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

`|`  എന്ന സൂചകം പെരുമാറുന്നത് `!{decl}` പോലെയാണെന്ന് നിങ്ങള്‍ ശ്രദ്ധിച്ചിരിക്കും; രണ്ടു നിരകള്‍ക്കിടയിലുള്ള
വിടവ് അതുപോലെ സൂക്ഷിച്ച് അതിനു നടുക്ക് കുത്തനെയുള്ള വര വരയ്ക്കുകയാണിതു് ചെയ്യുന്നത്. പക്ഷേ ഇതിനൊരു വലിയ കുറവുണ്ട്;
`booktabs` നല്കുന്ന തിരശ്ചീന വരകളുമായി ഇവ ഒത്തുപോകില്ല. പകരം ലാറ്റെൿ ലഭ്യമാക്കുന്ന തിരശ്ചീന വരകളുപയോഗിക്കാം:
`\hline` (`\toprule`, `\midrule`, `\bottomrule` എന്നിവയ്ക്കു പകരം), `\cline` (`\cmidrule` പോലെ)
എന്നിവ. മുകളിൽ കാണിച്ചിരുക്കുന്നതു പോലെ വരികള്‍ക്കിടയിൽ`\\`-നു് ഐച്ഛികമായി നല്കിയ അകലമുള്‍പ്പടെ ലംബ വരകൾ നീളും. 


## `booktabs` വരകളുടെ ക്രമീകരണം

എല്ലാ `booktabs` വരകളും `\addlinespace` ആജ്ഞയും വരകളുടെ കട്ടി എത്രയെന്നു് സ്പഷ്ടമാക്കാൻ ആവരണചിഹ്നത്തിനകത്തുള്ള
ഐച്ഛികവാദങ്ങൾ സ്വീകരിക്കുന്നുണ്ട്.  കൂടാതെ, `\cmidrule` വരയുടെ അറ്റം കത്രിക്കുന്നത് ക്രമീകരിക്കാൻ `r` അഥവാ `l`
കഴിഞ്ഞ് നീളം എത്രയെന്ന് വക്രാവരണചിഹ്നത്തിനകത്ത് നല്കാം.


<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{@{} lll@{}} \toprule[2pt]
  Animal & Food  & Size   \\ \midrule[1pt]
  dog    & meat  & medium \\
  \cmidrule[0.5pt](r{1pt}l{1cm}){1-2}
  horse  & hay   & large  \\
  frog   & flies & small  \\ \bottomrule[2pt]
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

## സംഖ്യകളെ വരിയിൽ അണിനിരത്തുന്നത്

പട്ടികയിലെ വരികളിൽ സംഖ്യകളെ അണിനിരത്താൻ `siunitx` പൊതിക്കെട്ട് പ്രദാനം ചെയ്യുന്ന `S` എന്ന
പീഠികാസൂചകം ഉപയോഗിക്കാം.

അക്കങ്ങൾ മാത്രമുള്ള രണ്ടു് വരികൾ അണിനിരത്തുന്ന ഒരു ലളിതമായ ഉദാഹരണം നോക്കുക:


```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{booktabs}
\usepackage{siunitx}
\begin{document}
\begin{tabular}{SS}
\toprule
{Values} &  {More Values} \\
\midrule
1        &   2.3456 \\
1.2      &   34.2345 \\
-2.3     &   90.473 \\
40       &   5642.5 \\
5.3      &   1.2e3 \\
0.2      &    1e4 \\
\bottomrule
\end{tabular}
\end{document}
```

അക്കങ്ങളല്ലാത്ത ഉള്ളടക്കമുള്ള എല്ലാ കോശങ്ങളും വക്രാവരണചിഹ്നങ്ങള്‍ക്കകത്ത് പൊതിഞ്ഞ് "സൂക്ഷിക്കണം" എന്ന
കാര്യം ശ്രദ്ധിക്കുക.

അക്കങ്ങളെ ചിട്ടപ്പെടുത്താനും വിന്യസിക്കാനും മറ്റു ധാരാളം സംവിധാനങ്ങൾ `siunitx` ഒരുക്കുന്നുണ്ട്,
[പൊതിക്കെട്ടിന്റെ കൈപ്പുസ്തകം](https://texdoc.org/pkg/siunitx) കാണുക.


## Specifying the total table width

The width of a `tabular` environment is automatically determined based
on the contents of the table. There are two commonly used mechanisms
to specify a different total width.

Note that it is almost always preferable to format the table to a
specified width as below (perhaps using a font size such as `\small` if
necessary) rather than scaling a table with `\resizebox` and similar
commands which will produce inconsistent font sizes and rule widths.

### `tabular*`

The `tabular*` environment takes an additional _width_ argument that
specifies the total width of the table. Stretchy space must be added
to the table using the `\extracolsep` command. This space is added
between all columns from that point in the preamble. It is almost
always used with `\fill`, a special space that stretches to be as large
as necessary.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\begin{document}

\begin{center}
\begin{tabular}{cc}
\hline
A & B\\
C & D\\
\hline
\end{tabular}
\end{center}

\begin{center}  
\begin{tabular*}{.5\textwidth}{@{\extracolsep{\fill}}cc@{}}
\hline
A & B\\
C & D\\
\hline
\end{tabular*}
\end{center}

\begin{center}  
\begin{tabular*}{\textwidth}{@{\extracolsep{\fill}}cc@{}}
\hline
A & B\\
C & D\\
\hline
\end{tabular*}
\end{center}

\end{document}
```

### `tabularx`

The `tabularx` environment, provided by the package of
the same name, has a similar syntax to `tabular*` but instead of
adjusting the inter-column space, adjusts the widths of columns
specified by a new column type, `X`. This is equivalent to a
specification of `p{...}` for an automatically determined width.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{tabularx}
\begin{document}

\begin{center}
\begin{tabular}{lp{2cm}}
\hline
A & B B B B B B B B B B B B B B B B B B B B B B B B\\
C & D D D D D D D\\
\hline
\end{tabular}
\end{center}

\begin{center}  
\begin{tabularx}{.5\textwidth}{lX}
\hline
A & B B B B B B B B B B B B B B B B B B B B B B B B\\
C & D D D D D D D\\
\hline
\end{tabularx}
\end{center}

\begin{center}  
\begin{tabularx}{\textwidth}{lX}
\hline
A & B B B B B B B B B B B B B B B B B B B B B B B B\\
C & D D D D D D D\\
\hline
\end{tabularx}
\end{center}

\end{document}
```

Unlike the other forms discussed in these lessons, `tabularx` needs to
typeset the table several times with trial widths to determine the
final setting. This means that there are several restrictions on the
use of the environment; see the
[package documentation](https://texdoc.org/pkg/tabularx).

## Multi-page tables

A `tabular` forms an unbreakable box so it must be small enough to fit
on one page, and is often placed in a floating `table` environment.

Several packages provide variants with similar syntax that do allow
page breaking. Here we show the `longtable` package:

```latex
\documentclass{article}
\usepackage[paperheight=8cm,paperwidth=8cm]{geometry}
\usepackage{array}
\usepackage{longtable}
\begin{document}
\begin{longtable}{cc}
\multicolumn{2}{c}{A Long Table}\\
Left Side & Right Side\\
\hline
\endhead
\hline
\endfoot
aa & bb\\  
Entry & b\\  
a & b\\  
a & b\\  
a & b\\  
a & b\\  
a & bbb\\  
a & b\\  
a & b\\  
a & b\\  
a & b\\  
a & b\\  
a & b\\  
a & b b b b b b\\  
a & b b b b b\\  
a & b b\\  
A Wider Entry & b\\  
\end{longtable}

\end{document}
```

`longtable` is notable in that it preserves the column widths
over all pages of the table; however in order to achieve this it
may take several runs of LaTeX so that wide entries encountered later
in the table can affect the column widths in earlier pages.

## Table notes

It is quite common to need footnote-like marks in a table referring to
notes under the table. The `threeparttable` package simplifies the
markup for such tables, arranging that the notes are set in a
block the same width as the table. Refer to the
[package documentation](https://texdoc.org/pkg/threeparttable)
for full details, but we show a simple example here.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{threeparttable}
\begin{document}

\begin{table}
\begin{threeparttable}
   \caption{An Example}
   \begin{tabular}{ll}
    An entry & 42\tnote{1}\\
    Another entry & 24\tnote{2}\\
   \end{tabular}
   \begin{tablenotes}
   \item [1] the first note.
   \item [2] the second note.
   \end{tablenotes}
\end{threeparttable}
\end{table}

\end{document}
```

## Typesetting in narrow columns

The default line breaking settings assume relatively long lines to
give some flexibility in choosing line breaks. The following example
shows some possible approaches. The first table shows interword spacing
stretched and TeX warns about Underfull lines. Using `\raggedright`
usually avoids this problem but may leave some lines ‘too ragged’. The
`\RaggedRight` command from the `ragged2e` package is a compromise;
it allows some raggedness in the line lengths, but will also
hyphenate where necessary, as shown in the third table.

Note the use of `\arraybackslash` here, which resets the definition of
`\\` so that it ends the table row.

An alternative technique, as shown in the fourth table, is to use a
smaller font so that the columns are not so narrow relative to the
text size.

```latex
\documentclass[a4paper]{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{ragged2e}
\begin{document}

\begin{table}

\begin{tabular}[t]{lp{3cm}}
One & A long text set in a narrow paragraph, with some more example text.\\
Two & A different long text set in a narrow paragraph, with some more  hard to hyphenate words.
\end{tabular}%
\begin{tabular}[t]{l>{\raggedright\arraybackslash}p{3cm}}
One & A long text set in a narrow paragraph, with some more example text.\\
Two & A different long text set in a narrow paragraph, with some more  hard to hyphenate words.
\end{tabular}%
\begin{tabular}[t]{l>{\RaggedRight}p{3cm}}
One & A long text set in a narrow paragraph, with some more example text.\\
Two & A different long text set in a narrow paragraph, with some more  hard to hyphenate words.
\end{tabular}

\footnotesize
\begin{tabular}[t]{lp{3cm}}
One & A long text set in a narrow paragraph, with some more example text.\\
Two & A different long text set in a narrow paragraph, with some more  hard to hyphenate words.
\end{tabular}

\end{table}

\end{document}
```

## Defining new column types

As demonstrated in the [main lesson](lesson-08), the `array` package allows
constructs such as `>{\bfseries}c`  to denote a bold centered column.
It is often convenient to define a new column type to encapsulate such
use, for example

```latex
\newcolumntype{B}{>{\bfseries}c}
```
would allow the use of `B` in table preambles to specify a bold
centered column.


## Vertical tricks

Often, rather than making a cell span multiple rows it is better to instead have
a single row in which some cells are split vertically by the use of nested
`tabular` environments.

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{lcc}
  \toprule
  Test & \begin{tabular}{@{}c@{}}A\\a\end{tabular} & \begin{tabular}{@{}c@{}}B\\b\end{tabular} \\
  \midrule
  Content & is & here \\
  Content & is & here \\
  Content & is & here \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

Note that you can control vertical alignment by an optional argument to the
`tabular`; it supports the usage of `t`, `c`, or `b` for top, centered, or
bottom aligned respectively and is used like this:

<!-- {% raw %} -->
```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\usepackage{booktabs}

\begin{document}
\begin{tabular}{lcc}
  \toprule
  Test & \begin{tabular}[b]{@{}c@{}}A\\a\end{tabular} & \begin{tabular}[t]{@{}c@{}}B\\b\end{tabular} \\
  \midrule
  Content & is & here \\
  Content & is & here \\
  Content & is & here \\
  \bottomrule
\end{tabular}
\end{document}
```
<!-- {% endraw %} -->

## Line spacing in tables

In the main lesson we demonstrated `\addlinespace` from the `booktabs`
package, which is useful for adding extra space between specific lines.

There are two general parameters that control line spacing,
`\arraystretch` and `\extrarowheight` (the latter from the `array`
package).

```latex
\renewcommand\arraystretch{1.5}
```

will increase the baseline spacing by 50%.


Often, especially when using `\hline`, it is better just to increase
the height of rows, without increasing their depth below the baseline.
The following example demonstrates the `\extrarowheight` parameter.

```latex
\documentclass[a4paper]{article}
\usepackage[T1]{fontenc}
\usepackage{array}
\begin{document}


\begin{center}
\begin{tabular}{cc}
\hline
Square& $x^2$\\
\hline
Cube& $x^3$\\
\hline
\end{tabular}
\end{center}


\begin{center}
\setlength\extrarowheight{2pt}
\begin{tabular}{cc}
\hline
Square& $x^2$\\
\hline
Cube& $x^3$\\
\hline
\end{tabular}
\end{center}
\end{document}
```
