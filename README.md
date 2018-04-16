# Just my Curriculum Vitae (Italian Version)

## [CLICK HERE TO PREVIEW THE PDF VERSION](https://github.com/gbiolo/cv-it/blob/master/curriculum.pdf)

## How to clone
The repository refers to the moderncv repository, created by [Xavier Danaux](https://github.com/xdanaux). Thanks man!!

To correctly clone my CV the first step is to clone my repository with:

`clone https://github.com/gbiolo/cv-it.git`

After this, you have to initialize the submodule with:

`git submodule init`

Last step is to download the submodule with:

`git submodule update`

## How to build the PDF document
Just change directory to the `cv-it` one (where you cloned my curriculum repository) and lunch:

`pdflatex curriculum.tex`

That's all folks!!

My Curriculum Vitae will be saved with the name:

`curriculum.pdf`

## Texlive installation (if not present)
I use Texlive and Debian GNU/Linux, so the following steps are based on this OS and Latex compiler.

First of all check if there is a correct Texlive version installed on our system with:

`apt-get --no-install-recommends install texlive-base texlive-latex-base texlive-latex-extra texlive-fonts-recommended`

The `--no-install-recommends` flags avoid the full install of Texlive, with its giant documentation. The previous command, if none of the packages is already installed, will download more or less 100MB of packages (full installation with manuals size is over 1GB).

To check if the Texlive is installed on your system execute this on your command shell:

`pdflatex -v`

The output should be something similar to this:

```
pdfTeX 3.14159265-2.6-1.40.17 (TeX Live 2016/Debian)
kpathsea version 6.2.2
Copyright 2016 Han The Thanh (pdfTeX) et al.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the pdfTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the pdfTeX source.
Primary author of pdfTeX: Han The Thanh (pdfTeX) et al.
Compiled with libpng 1.6.28; using libpng 1.6.28
Compiled with zlib 1.2.8; using zlib 1.2.8
Compiled with poppler version 0.48.0```
