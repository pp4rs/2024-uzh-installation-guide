<!-- markdownlint-disable MD024 -->
<!-- see https://github.com/DavidAnson/markdownlint for code to enable or disable rules -->
# LaTeX

LaTeX is a document preparation system for high-quality typesetting most often used for medium-to-large technical or scientific documents.
Most of you probably have some familiarity with LaTeX from your Master's Theses.

We may want to build some PDF documents throughout the course using LaTeX - so let's install it.

!!! note "Department Managed Laptops"
        Latex can be install from the Software Center. Search for "TeXLive" and install the most recent version.

## LaTeX Install for Mac

We again install from Homebrew.
Enter the following into the terminal:

```bash
brew install --cask mactex
```

## LaTeX Install for Linux

LaTeX can be installed from the terminal by entering the following command and pressing `Return`:

```bash
sudo apt-get install texlive-latex-extra
```

Check everything went according to plan:

``` bash
tex --version
```

which gives the following output:

``` bash
TeX 3.141592653 (TeX Live 2021)
kpathsea version 6.3.3
Copyright 2021 D.E. Knuth.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the TeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the TeX source.
Primary author of TeX: D.E. Knuth.
```

## LaTeX Install for Windows
Unfortunately, we can't use winget for installation. 

Please download the [TeXLive Exe](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe) and run it. Follow the instructions given.

