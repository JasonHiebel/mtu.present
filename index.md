---
layout: default
---

This package provides the beamer theme `Houghton` and the beamer color theme `husky` which mimic the powerpoint theme provided by [University Marketing and Communications (UMC)](https://www.mtu.edu/umc/) at [Michigan Technological University](https://www.mtu.edu/). This theme comes in two flavors: the first is the standard format according to the UMC's powerpoint theme (left), and the second is a small modification to the footline (right).

| Standard | Bolded |
|:-:|:-:|
| ![Standard](/assets/img/mtu.present.std.front.png) | ![Bold](/assets/img/mtu.present.bold.front.png) |
| [example](/assets/img/mtu.present.std.pdf) | [example](/assets/img/mtu.present.bold.pdf) |

The two theme variants work well in both 4:3 and 16:9 aspect ratios. Both are developed with the idiomatic beamer style, so usage should mimic any other standard style.

# A Simple Example

```
\documentclass{beamer}
\usetheme{Houghton}
%\usetheme[bold]{Houghton}
\setbeamertemplate{navigation symbols}{}

\newcommand*{\emailstack}[2]
{\shortstack{#1\strut\\\small\url{#2}\strut}}

\title{Michigan Tech Styled Beamer Themes}
\author[Hiebel and Hiebel]{
	\emailstack
		{\textbf{Jason Hiebel}}
		{jshiebel@mtu.edu} \and
	\emailstack
		{\textbf{Jason Hiebel}}
		{jshiebel@mtu.edu}}
\institute[Michigan Tech]{
	Department of Computer Science\\
	Michigan Technological University}
\date[Sept. 2018]{
	Sample Document Preparation\\
	September 2018}

\begin{document}
\maketitle
% ...
\end{document}
```

This example replicates the title cards illustrated above. The golden footline replaces the ruled footline if the `bold` option is specified in the `usetheme` command. Each of the standard title page elements are specified. The author specification uses the standard `\and` command for specifying multiple authors. To specify other author information, such as email, we can use the `shortstack` command (as illustrated by the `\emailstack` definition. The footline contains the short-form for both the author and date.
