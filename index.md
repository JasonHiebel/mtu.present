---
layout: default
---

This package provides the beamer theme `Houghton` and the beamer color theme `husky` which mimic the powerpoint theme provided by [University Marketing and Communications (UMC)](https://www.mtu.edu/umc/) at [Michigan Technological University](https://www.mtu.edu/). This theme comes in two flavors: the first is the standard format according to the UMC's powerpoint theme (left), and the second is a modification which changes the footline to be a bold MTU gold color. (right).

| Standard | Gold |
|:-:|:-:|
| ![Standard](/assets/img/mtu.present.std.front.png) | ![Gold](/assets/img/mtu.present.gold.front.png) |
| [(pdf)](https://github.com/JasonHiebel/mtu.present/blob/master/examples/standard.pdf) | [(pdf)](https://github.com/JasonHiebel/mtu.present/blob/master/examples/gold.pdf) |

The two theme variants work well in both 4:3 and 16:9 aspect ratios. Both are developed with the idiomatic beamer style, so usage should mimic any other standard style.

# Simple Example

```
\documentclass{beamer}
\usetheme{Houghton}

\newcommand*{\emailstack}[2]
{\shortstack{\textbf{#1}\strut\\\small\url{#2}\strut}}

\title{Michigan Tech Styled Beamer Themes}
\author[Hiebel and Hiebel]{
	\emailstack{Jason Hiebel}{jshiebel@mtu.edu}
	\and
	\emailstack{Jason Hiebel}{jshiebel@mtu.edu}}
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

This example replicates the title cards illustrated above. The golden footline replaces the ruled footline if the `gold` option is specified in the `usetheme` command (`\usetheme[gold]{Houghton}`).

Each of the standard title page elements are specified. The author specification uses the standard `\and` command for specifying multiple authors. To specify other author information, such as email, we can use the `shortstack` command (as illustrated by the `\emailstack` definition. The footline contains the short-form for both the author and date.
