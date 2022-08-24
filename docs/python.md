# Anaconda Python

Anaconda is a pre-packaged Python distribution for scientific users.
Unlike other Python distributions, this means that most additional functionality that we need to do numerical computing, statistics, plotting and the like come already installed - which saves us a lot of time.

## Installing Miniforge Python for Mac

Install using Homebrew.
In your terminal type the following and press return:

``` bash
brew install --cask miniforge
```

During the installation process you might be the following output asking you to review the license agreement:

``` bash
Welcome to Anaconda3

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
>>>
...
Do you approve the license terms? [yes|no]
```

Press `Return` until you reach the end, and type 'yes'.

<!--
### Making Anaconda Python Accessible from the Terminal

By default, Mac uses a default install of Python inside the terminal.
We want to change that.

Enter the following in the terminal and press `Return`:

``` bash
echo 'export PATH="/usr/local/anaconda3/bin:$PATH"' >> ~/.zshrc
```

Then, reload the terminal environment:

``` bash
source .zshrc
```
-->

Now proceed to [verify your install](#verifying-your-installation)

## Installing Miniforge Python for Linux and Windows

First, we need to download the Anaconda Bash Script (a file that will install things for us). Enter the following into the terminal:

``` bash
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

Run the Anaconda Script by entering the following into the terminal:

``` bash
bash Miniforge3-$(uname)-$(uname -m).sh
```

As this script runs through, review and accept the license agreement.
To do this press `Return` until you reach the end, and type 'yes'.

After you agree to the license, you will be prompted to choose the location of the installation:

``` bash
Miniforge3 will now be installed into this location:
/home/lachlan/miniforge3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/lachlan/miniforge3] >>>

```

Use the default.

The installation will continue - it does take some time, so be patient.

Once the installation is complete, you will get the following output, which asks a question of us:

``` bash
...
Preparing transaction: done
Executing transaction: done
installation finished.
Do you wish the installer to initialize Miniforge3
by running conda init? [yes|no]
```

Type 'yes'.

Now we need to refresh our terminal settings, so type the following and press return:

``` bash
source ~/.bashrc
```

Now proceed to [verify your install](#verifying-your-installation).

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
!!! tip "Updating the Anaconda Install"
    The above procedure will always install the latest available Miiforge distribution for your platform. If you want to update an existing installation, you can generally do that using the command `conda updade --all`, which updates all packages in a given environment (including conda itself).
<!-- markdownlint-restore -->

## Verifying Your Installation

In order to activate Miniforge's environment, we have to start with

```
conda activate
```

Then, to verify that the correct version of Python has been installed, usually we would follow the `programName --version` logic from before.

``` bash
python --version
```

which yields:

``` bash
Python 3.9.13
```

which tells us that Python is installed.
But, because most operating systems these days have some additional version of Python installed, this doesn't guarantee that the Miniforge version is available for us to use from the terminal.

To check, initiate Python by entering the following into a terminal and pressing `Return`:

``` bash
python
```

You should now see something like:

``` bash
Python 3.9.13 | packaged by conda-forge | (main, May 27 2022, 16:56:21)
[GCC 10.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
```

where the operating system name should be different for Mac users.

Now we see that the terminal is using the Miniforge (conda-forge) version as we wanted.
To quit the Python session we just opened, type the following at the `>>>`:

``` python
>>> quit()
```

and you will return to your terminal.
This was successful if you now see a `$` rather than the `>>>`.

If you want to deactivate the Miniforge environment (e.g. so that you can use the system's Python interpreter), you simply have to type

```bash
conda deactivate
```

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
<!-- !!! tip "Python 2 vs Python 3"
    Python 2 and 3 are incompatible in syntax. If you had Python 2 previously installed on your machine, you might have seen `Python 2.x.x` above. In that case try typing

    ```python3 --version```

    instead. Now you should see a message like the one above and are good to go for the course. -->
<!-- markdownlint-restore -->
