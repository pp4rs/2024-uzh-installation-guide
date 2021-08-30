# RStudio

RStudio provides an easy to work with graphical interface to R, and its format should feel familiar to Stata and Matlab users.

## Installing RStudio for Mac Users

We can install RStudio with Homebrew:

``` bash
brew install --cask rstudio
```

To see if it installed correctly, try and open RStudio from spotlight - there's not simple verification from the terminal.

## Installing RStudio for Linux Users

Download the Latest Version of RStudio:

``` bash
wget https://download1.rstudio.org/desktop/bionic/amd64/rstudio-1.2.5033-amd64.deb
```

Install it:

```bash
sudo gdebi rstudio-1.2.5033-amd64.deb
```

To see if it installed correctly, try and open RStudio from the GNOME menu - there's not simple verification from the terminal.

## Installing RStudio for Windows Users

Download the most recent version of RStudio Server for Ubuntu 18 (see [here](https://rstudio.com/products/rstudio/download-server/debian-ubuntu/)).
Enter the following into your terminal and press `Return`:

```bash
wget https://download2.rstudio.org/server/bionic/amd64/rstudio-server-1.4.1717-amd64.deb
```

Now install it by entering this command and hitting `Return`:

``` bash
sudo gdebi rstudio-server-1.4.1717-amd64.deb
```

Now that we have RStudio installed on our subsystem, how can we use it?

In the Ubuntu terminal enter the following text and press `Return`:

```bash
sudo rstudio-server start
```

Now open a web browser, and go to the following address:

```bash
http://localhost:8787/
```

which will take you to a log in page.

Log in using the username and password for your Ubuntu terminal that we set up at the beginning.

After logging in successfully you have access to the RStudio that you installed in your Ubuntu subsystem.

To log out, click on the log out button in the top right corner.

To stop the RStudio server from running (logging out doesn't stop it), enter `rstudio stop` into your terminal.

!!! tip "Why RStudio Server?"
    We are using RStudio server rather then the desktop version of RStudio because we have found it the easiest way to interact with the R installation inside the WSL system.
