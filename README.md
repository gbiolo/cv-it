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

## Sometimes size matters!!
The size of the output PDF file created by the Tex compiler usually is greater than a normal PDF file.

To reduce the file file you can use the great Ghostscript, that is installed by default in the major
Linux distributions (Debian confirmed).

The reduced output file size will be even 90% smaller than the original one.

The syntax is as easy as this:

`gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -sOutputFile=curriculum_priv_compressed.pdf curriculum_priv.pdf`

The previous command must be executed inside the directory containing the compiled PDF file.

## Texlive installation (if not present)
I use Texlive and Debian GNU/Linux, so the following steps are based on this OS and Latex compiler.

To check if Texlive is installed on your system execute this on your command shell:

`pdflatex -v`

The output should be something similar to this:


`pdfTeX 3.14159265-2.6-1.40.17 (TeX Live 2016/Debian)
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
Compiled with poppler version 0.48.0`

If Texlive is not installed or the compilation of the LaTex source failes, try to
execute the following TexLive installation command:

`apt-get --no-install-recommends install texlive-base texlive-latex-base texlive-latex-extra texlive-fonts-recommended`

The `--no-install-recommends` flag avoid the installation of Texlive giant documentation. The previous command, if none of the packages is already installed, will download more or less 100MB of packages (full installation download size is over 1GB).

After the installation try again to check TexLive version with `pdflatex -v`.
