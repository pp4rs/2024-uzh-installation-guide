# Command Line Tools

A command-line interface or command language interpreter (CLI), also known as a terminal, is a means of interacting with a computer program where the user issues commands to the program in the form of successive lines of text.

Throughout the course we will emphasize use of the terminal and executing commands within it as our modus operandi.

## Mac Users

A command line interface comes already installed with OSX.

You will need to install some other software from the terminal throughout the course, so it will be useful to install some additional "command line tools" now.

### Opening a Terminal Session

To open a terminal session:

* Open spotlight with `cmd + space`
* Type in 'terminal'
* When the terminal appears, open it.

!!! Note "Department Managed Macs"
    Unfortunately, installation of Homebrew requires admin rights which aren't available on laptops newly issued by the department. Please move on to the next installation step "Text Editor".
#### Installing the X-code Tools

We want to install 'X-code command line tools'. Copy and paste the following and press `Return`

``` bash
sudo xcode-select --install
```

If you get a message that the command line tools are already installed, you can continue to the next step.

#### Installing Homebrew Package Manager

Homebrew is a package manager for Mac.

Install Homebrew by opening a terminal and pasting the following command:

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Verify that Homebrew installed correctly, enter the following into your terminal:

``` bash
brew doctor
```

And you should see the following output:

``` bash
Your system is ready to brew
```

Before continuing, lets be sure everything in Homebrew is up to date by entering the following:

``` bash
brew upgrade
```
!!! warning "brew upgrade on UZH MacOS"

    We've seen some problems running `brew upgrade` on UZH computers with MacOS.
    If you are experiencing this, run the following two lines:

    ```
    sudo chown -R "$USER":admin/usr/local/Cellar
    ```

    and 

    ```
    sudo chown -R "$USER":admin/usr/local/share
    ```



---
## Windows Users
On Windows we will be using "winget" for most of our installations.

### Winget Installation
Winget is part of Microsoft's App Installer which you can get [here](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1?hl=en-ch&gl=ch&rtc=1). Follow the link and install the application from the Microsoft Store. On machines managed by the department you might get a "failure" pop up, but just wait, it will install. 

After installation, open the Windows Search Bar and type "cmd" and hit `return`. This will open the Command Line Interface (CLI) of Windows with which we will be working during this course.

Now type the following command into the CLI and press `return`
``` bash
winget --help
```

Upon succesful installation, you should see a long this of possible command that "winget" can be supplied with. It should start like this:
```bash
Windows Package Manager v1.5.2201
Copyright (c) Microsoft Corporation. All rights reserved.
```
Feel free to try some commands such as "list" to see which programs are installed on your machine.

### Windows Terminal Installation
In order work more comfortably with the CLI we will install a better version of the CLI you just used.

To install "Windows Terminal" copy and paste the following command:
```bash
winget install -e --id Microsoft.WindowsTerminal
```
Here, install tells winget which action it is supposed to take and "--id" is a flag providing winget with further information. In this case the id of the program we want to install and "-e" tell it to only use exactly this id. You would have been able to find this "id" by running the command:
```bash
winget search WindowsTerminal
```

Head over to the search in Windows and type "terminal" and hit `return` to open the WindowsTerminal. We will continue installations there.



<!-- ### Installing Packages with Homebrew

Now we can use homebrew to easily install software.  We need some basic system tools for some of the programs we will install later.

In particular we need:

* `libxml2`
* `openssl`
* `libgit2`

Most of these are already installed, but we need updates of these packages.
For each of these packages enter:

``` bash
brew reinstall pkg-name
```

i.e. `brew reinstall libxml2`.

If you get a message that the package you are trying to reinstall is not yet installed, try `brew install pkg-name` instead.

### Linking Packages to a Terminal Session

We need to ensure that our terminal session has access to what we installed.
To do this we add some extra lines to our bash profile (we will discuss what this means in class - do what we say for now):

``` bash
echo 'export PATH="/usr/local/opt/libxml2/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.zshrc
source .zshrc
``` -->
<!-- ## Linux & Windows Users

* Linux Users: Open a terminal session with `Ctrl` + `Alt` + `T`.
* Windows Users: Open the Windows Terminal as we described [here](/windows-wsl/#installing-windows-terminal)

Copy the following command into terminal and press `Return`:

```bash
sudo apt-get update
sudo apt-get install libcurl4-gnutls-dev librtmp-devm libfontconfig1-dev
```

After the installation succeeded successfully repeat this one-by-one with the following two other commands:

```bash
sudo apt-get install libxml2-dev
sudo apt-get install libssl-dev
sudo apt-get install gdebi-core
```
-->

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
<!-- !!! tip "Windows Users: Copy and Paste"
    The 'traditional' `Ctrl + C` and `Ctrl + v` may not work with your terminal because the `Ctrl + Key` commands have a special meaning with Linux operating systems.
    f they don't work for you, there are two alternatives:

    * Use the 'Linux' copy and paste commands: copy is `Ctrl + Shift + C` and paste is `Ctrl + Shift + V`.
    * To paste text, you just do a right-click.
    To copy anything inside the terminal, you use highlight the text with your cursor.
    It is automatically copied to your clipboard. -->
<!-- markdownlint-restore -->

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
<!-- !!! tip "Windows Users: Library Installation"
    At some point in the install process you may see a screen like this one:
    
    <img src="../img/misc-windows/96-lib-installer.jpg" class="center" height = "500">

    Here you need to make a choice, which you do by using the left and right arrows followed by `Return`.
    Lachlan chose, 'No' - but you can safely choose yes without your computer burning down.

    Whenever you get these kinds of screens, you can scroll up and down with the up and down buttons if needed and make decisions by selecting a choice as described above. -->
