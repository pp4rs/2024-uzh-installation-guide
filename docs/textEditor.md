<!-- markdownlint-disable MD033 -->
<!-- see https://github.com/DavidAnson/markdownlint for code to enable or disable rules -->
# Motivation

A good text editor lies at the heart of any serious programmer's toolkit: It can do almost anything and makes you much more productive.
The editors built into a specific program are generally are not a satisfying option (we will find certain cases where you may want to use them).

<!-- Please download, install it along with the necessary packages and stick with it for at least the duration of the course and assignment to get a feel for how it works. -->

There is a slight learning curve, but soon you hopefully be wondering why no-one forced you to do this before!
We should get you past the steepest part of the learning curve during the course itself, so we don't anticipate you struggling on your own.

!!! tip "Note"
    None of the skills we learn in the course are tied to VS Code, so if you do decide to move away to another editor, nothing will be lost.

<!-- ## Installing Sublime Text

Go to the [downloads page](https://www.sublimetext.com/3) and download the live installer for your operating system.-->

## VS Code

VS Code is a relatively new text editor that works across all three platforms: Linux, Windows and Mac.
In a short time it has already become one of most used text editors and we hope you will soon see why.
It is built by Microsoft, but is open source, i.e. everyone can see and modify the program's internal code - so it is less nasty on the consciousness than some of Microsoft's traditional products.
The main advantages for us are that it includes support for debugging, embedded Git control and GitHub, syntax highlighting, intelligent code completion, and many useful plugins - all of which make our lives much easier.

!!! Note "Department Managed Laptops"
    If your laptop is managed by the department, Visual Studio Code is most likely already installed on your device. If not, search for "Software Center" and install it. (Visual Studio Code = VS Code)

## Installing VS Code on Mac

VS Code can be installed using homebrew. Type the following into your terminal and hit return:

```bash
brew install --cask visual-studio-code
```

Once it has been installed, verify your install by following the instructions [below](#verifying-your-install).

## Installing VS Code on Ubuntu

VS Code is available to install via snap. Enter the following in your terminal and press `Return`:

```bash
snap install code --classic
```

Once it has been installed, verify your install by following the instructions [below](#verifying-your-install).

## Installing VS Code on Windows
We are installing VS Code via winget by entering the following command in the terminal and hitting `Return`:
```bash
winget install -e --id Microsoft.VisualStudioCode --interactive
```

<!-- Go to the VS Code [download page](https://code.visualstudio.com/download), and download the Installer for Windows.
* Once downloaded double click to install. -->

* Accept any default options.
* At the end of the install, launch VS Code (it gives you this option on the last window).

<!-- The first time you launch VS code, you will see the following:

<img src="../img/misc-windows/99-vscode-wsl.jpg" class="center" height = "500">

Where it prompts you to install the 'Remote WSL' extension, choose 'Install'.

Once complete, in your Ubuntu terminal type `code .` and press `Return`.
You should see the following (what appears after `code .`) below:

<img src="../img/misc-windows/98-code-on-ubuntu.jpg" class="center" height = "500">

When the unpacking is complete, VS Code should open. -->

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
!!! tip "Windows Defender Firewall"
    You will likely get the following pop-up during the above process:
    
    <img src="../img/misc-windows/97-allow-access-defender.jpg" class="center" height = "500">

    Click 'Allow access' if you do.
<!-- markdownlint-restore -->

## Verifying Your Install

After you have installed software via the terminal, we often want to verify the install was successful.
For most programs we do this by typing the program name followed by `--version` in to the terminal.
Let's do it:

``` bash
code --version
```

which should yield output like:

``` out
1.59.0
379476f0e13988d90fab105c5c19e7abc8b1dea8
x64
```

if successful.

## Installing Extensions for VS Code

VS Code is great straight of the box, but gets even better when we add some additional extensions to make our life easier.
To add extensions:

* Open VS Code
* Press `Ctrl + Shift + X` to open the Extensions side bar (it opens on the left).
* Add extensions by:
  * Searching for them in the Marketplace
  * When you find them, click `Install`

We recommend (but don't require) the following extensions to be added for this course:

* Git History
* GitLens
* Python
