# Pandoc

Pandoc is an extremely useful 'swiss army knife' for converting between different types of markup languages from the command line.
For example, it readily builds PDFs with latex, and markdown - both of which are heavily used in academic research.

!!! Note "Department Managed Laptops"
        Admin User rights are required to install Pandoc. Unfortunately, only IT has those. Hence Pandoc can't be installed.


!!! tip "Note"
        We do not actively teach how to use Pandoc in the course - but we will utilize it in some lessons where we produce PDF, Word or HTML output from plain text files.

## Pandoc Install for Mac

In a terminal window and type:

```bash
brew install pandoc
```

Now [verify your install](verify-pandoc-install).

## Pandoc Install for Linux

Open a terminal window and type

```bash
sudo apt install pandoc
```

to install pandoc from the command line. Now [verify your install](verify-pandoc-install).

## Pandoc Install for Windows

Open the terminal an run:
```bash
winget install -e --id JohnMacFarlane.Pandoc
```
Now [verify your install](verify-pandoc-install).

## Verify Pandoc Install

Verify your install by typing the following into a command line:

```bash
pandoc --version
```

The expected output starts with the following information:

```bash
pandoc 2.x

```

Ensure you have at least version 2.1.1 installed.