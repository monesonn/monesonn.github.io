---
title: "101.Suckless Slides"
date: 2021-04-06T15:47:13+03:00
draft: false
---

Not so long ago I faced the problem that it's quite difficult for me as a student to make presentations quickly and with high quality. Using Google Slide or similar services was not the best solution for me. For now, I won't explain it yet.

So, alternatively, I started to use: **Pandoc + Beamer** bundle.

- **[Pandoc](https://pandoc.org/)** is a free and open-source document converter written on Haskell.
- **[Beamer](https://ctan.org/pkg/beamer)** is a LaTeX document class for creating presentation slides, with a wide range of templates and a set of features for making slideshow effects.

The idea is simple, we use Pandoc for compiling our Markdown file into the LaTeX one. Then converting it into the PDF presentation. And that's it!

In this post, I'll provide an example of how to quickly and efficiently create:

**Bloat-free, Simple & Markdown powered slides.**

For Fedora Linux (my current daily drive), you should install packages as below:

``$ sudo dnf install pandoc pandoc-pdf texlive-beamer texlive texlive-pgfplots texlive-pgfopts``

As we have installed the required packages, follow next steps:

1. Create a directory (if not existed), where you will store presentations.
2. Create file with Markdown extension (.md) and put template something like this:

```markdown
---
title: <your title>
author: <your name>
aspectratio: 169
---

# Your first slide

First paragraph

# Your second slide

Blah, blah, blah, this's second paragraph

```
3. Then compile it to produce PDF slide:

``$ pandoc example.md -t beamer --pdf-engine=xelatex -o pdf/example.pdf``

4. Open by your favorite document viewer to see what's done:

``$ zathura --mode=presentation pdf/example.pdf &``

**NOTE:** I put ampersand to the end to run this command in background. It's means that, if you make some changes in file and recompiling, the presentation will be refreshed.

5. [Congratulations!](https://youtu.be/1Bix44C1EzY)

### Additional

If you haven't [zathura](https://pwmt.org/projects/zathura/) and wants to try, type:

``$ sudo dnf install zathura zathura-pdf-poppler``

There are some useful resources and links for further consideration:

* [Luke Smiths video](https://youtu.be/dum7q6UXiCE)
* [Beamer themes gallery](https://deic-web.uab.cat/~iblanes/beamer_gallery/)
* [Pandoc User's Guide for Slides](https://pandoc.org/MANUAL.html#slide-shows)
* [Extended example in Github](https://github.com/alexeygumirov/pandoc-beamer-how-to)

Also, I recommend to use custom themes, f.e, my favorite is Metropolis.

``$ git clone https://github.com/matze/mtheme.git``

I use theme locally, just copy .sty files into directory with presentation.

**NOTE**: If you'll have error with text something like "pgfplotscreateplotcyclelist", when compiling the presentation. Just rename the pgfplotsthemetol.sty to pgfplots.sty. After that everything should work.
