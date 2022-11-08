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

ഫലമായി ലഭിച്ച `first.pdf` എന്ന പ്രമാണം നിങ്ങള്‍ക്കിഷ്ടമുള്ള പിഡിഎഫ് കാഴ്ചസഹായ പ്രോഗ്രാം ഉപയോഗിച്ച്
തുറന്നു നോക്കുക. ഒന്നാന്തരമായിരിക്കുന്നില്ലേ, അനുമോദനങ്ങൾ!

പിഡിഎഫ് ഫലത്തിനു പകരം എച്ടിഎംഎൽ ആണു നിങ്ങള്‍ക്കാവശ്യമെങ്കിൽ അതെങ്ങനെ നിര്‍മ്മിക്കാമെന്നു മനസ്സിലാക്കാൻ
[സഹായം](./help) നോക്കുക.


## Handling errors

Errors happen.
Check that you have entered each line in the text file exactly as written above.
Sometimes seemingly small input changes give large changes in the
result, including causing a document to not work.
If you are stuck, try erasing the document and copying it fresh from the
lines above.

If your LaTeX typesetting run ends with a question mark then you can get out by
typing `x` and `<Enter>`.

LaTeX's error messages try to be helpful, but they are not the same as messages
in word processors. Some editors also make it hard to see the 'full' text of an
error, which can hide key details. LaTeX always creates a log of what it is
doing; this is a text file ending in `.log`. You can always see the full  error
messages there, and if you have a problem, expert LaTeX users will often ask for a
copy of your log file.

<p
  class="hint">We cover more about dealing with errors in <a href="./lesson-15">lesson 15</a>.</p>

## What you've got

The first document shows the basics.
LaTeX documents are a mixture of text and commands.
The commands start with a backslash
and sometimes have arguments in curly braces
(or sometimes optional arguments in square brackets).
Then you get an output PDF by telling LaTeX to typeset your file.

Every LaTeX document has a `\begin{document}` and a matching
`\end{document}`.
Between these two is the *document body*, where your content goes.
Here the body has two paragraphs (in LaTeX you separate paragraphs
with one or more blank lines).
Before `\begin{document}` is the *document preamble*,
which has code to set up the document layout.
The `\usepackage` command is described in a [later lesson](lesson-06)
it is used in most examples on this site to set up the font encoding.

LaTeX has other `\begin{...}` and `\end{...}` pairs; these are
called *environments*.
You must match them so that for every `\begin{x}` there has to be an `\end{x}`.
If you nest them, then you must have `\end{y} ... \end{x}` to match
`\begin{x} ... \begin{y}`, i.e. the `\begin` and `\end` statements matching
in order.

We can add comments to a LaTeX file by starting them with `%`; let's use
that to show the structure:

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

You can see above that we've got two paragraphs: notice the use of a blank  line
to do that. Also notice that multiple spaces are treated as a single space.

You might also sometimes want a 'hard' space that does not break over lines: in
LaTeX we can create that using `~`, 'tying' two pieces of text together. That's
particularly useful when we start creating cross-references later in the course.

## Special characters

You've probably spotted that ``\``, `{` and `}` have a special meaning to LaTeX.
A ``\`` starts an instruction to LaTeX: a 'command'. The curly brace characters
 `{` and `}` are used to show _mandatory arguments_: information that commands
 require.

There are some other characters with special meaning; we've just seen that `~`
is a 'hard' space, for example. Almost all of these characters  are _very_
uncommon in normal text, which is why they were chosen for special meanings.
If you do need to show one of these special characters, we've put some
[information in the further details page](more-03).

## Exercise

Experiment with the online editing and typesetting system; click the
button to typeset the content, then edit it in the webpage and re-typeset it.

Try adding text to your first document, typesetting and seeing the changes in
your PDF. Make some different paragraphs and add variable spaces. Explore how
your editor works; click on your source and find how to go to the same line  in
your PDF. Try adding some hard spaces and see how they influence line-breaking.
