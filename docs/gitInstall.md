# Installing Git and Setting Up Accounts

Git is a Version Control System (VCS) that has gained a lot of traction among the programming community.
We will want to use version control to keep track of the files we write, and the changes we make to them.

## Account Creation

During the course we will show you how to use [GitHub](https://www.github.com) to host some of your work and do code related project management. You will need to set up an account:

* Please [register](https://github.com/join) for a [GitHub](https://github.com/) account
* When choosing a username we recommend not using a name that includes an employer or university in case you move later on
  * i.e. 'johnsmith' or 'johnsmith86' are OK, 'johnsmithUZH' probably not
## Mac Users

### Installing Git

We will install Git using Homebrew. Enter the following lines of code into your terminal:

``` bash
brew install git
brew link --force git
```

Then close and reopen the terminal. Now [Verify your installation](#verifying-your-install).

### Autocompletion

When we code we want to be lazy - we don't always want to write out the whole line of code we want to enter, and would prefer the computer to autocomplete our line of code for us.
The default MacOS terminal doesn't have this autocompletion by default, so let's add it using our trusty friend Homebrew.

Open a terminal and enter:

``` bash
brew install zsh-completion
```

!!! warning "Activating Autocomplete on MacOS"
    To make the autocompletion work, you will need to add a block of code to your `~./zshrc` file:

    ```
    if type brew &>/dev/null; then
        PATH=$(brew --prefix)/share/zsh-completions:$FPATH
        autoload -Uz compinit
        compinit
    fi
    ```

    Next, save the file.
    Then source these updates (think of this as restarting your terminal) by entering the following command in your terminal:

    ```
    source ~/.zshrc
    ```

    This might seem a little daunting, so you don't need to do it now.
    We will do this with you live in class at the appropriate time.

<!---
  Autocomplete instructions from here  
  https://stackoverflow.com/questions/26462667/git-completion-not-working-in-zsh-on-os-x-yosemite-with-homebrew

--->

## Linux Users

Git should be installed already for you.
To check if it is, enter the following in a terminal:

``` bash
git --version
```

If you get a bunch of numbers (ideally starting with 2.15) or higher - you are good to move on.

If not, install it by entering the following into the command line:

``` bash
sudo apt-get install git
```

Once complete, [verify your install](#verifying-your-install).

## Windows Users

Git will be already installed inside your Ubuntu terminal.
Verify this, by [verifying your installation](#verifying-your-install).

## Verifying your install

<!-- We will need to make Git accessible from the command line. Windows and Mac users will need to follow the steps on the page "Modifying Path Settings." Linux users will already have git accessible from the command line. -->

To verify your installation, type the following command in a terminal and press the return key:

```bash
git --version
```

You should get an output that looks like:

```bash
git version 2.25.1
```

Ensure that you have a version greater than `2.15.0` installed.
