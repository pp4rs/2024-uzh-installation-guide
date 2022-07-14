# Additional Python packages

Miniforge is a very streamlined Python Distribution containing only the most necessary packages. In addition to these, there are many other packages we need to do scientific computing. We will install those in this section of the guide.

!!! note
    Miniforge (also Mambaforge, Miniconda) is based on the Anaconda Python Distribution, which includes a large number of packages related to scientific computing by default. However, it also means, that it is rather large, and many of those packages are of no interest to most economists. (If you're interested in all the packages included, click [here](https://docs.continuum.io/anaconda/packages/pkg-docs) and go to the Python 3.9 tab.) For this reason, start from a barebones distribution and only install what we require instead.

<!-- However, you may come across packages that are not installed by default.
In this case we recommend you use the `pip` package management tool to install them. -->
The following recipe works for *all* operating systems.

There are a multitude of package management tools that work with Python packages. In this course, we use `conda`, which is the default one for Anaconda-based Python distributions. It combines dependency management and virtual environments in one program. Furthermore, it is designed with the scientific workflow in mind. For those packages that are not available in the conda repositories, we fall back to `pip`, Python's standard package manager.

!!! note
    Mixing `conda` and `pip` is generally advised against, but sometimes it cannot be avoided. However, by using `conda` first and `pip` second, and utilizing virtual environments, you are mostly safe. You can find more info [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#using-pip-in-an-environment).

<!-- !!! note
    If your python 3 was accessed via `python3` rather than `python` on the previous page, then type `pip3` instead of `pip` for all of the following python packages. -->

First let us update `conda` by typing the following into the terminal

```bash
conda update conda --yes
```

Next, install a handful of packages using the following command
```bash
conda install jupyter jupyterlab nb_conda_kernels
```

Press enter to accept the proposed package plan.

This command installs those four packages into the default (base) environment. It is fine, as we would like those to be shared across all environments we later create. However, it is generally not the case, as we want dependencies for our different projects well separated. For example, packages for this course should be wholly independent from packages you are using to write a paper. The next command creates a `conda` environment called `pp4rs` and installs all the packages required for the course.

```bash
    conda env create -f https://pp4rs.github.io/2022-uzh-installation-guide/assets/pp4rs-env.yml
```

Generally, you should have such a file for each of your projects in order to easily reproduce the environment it was built in any time in the future.

!!! note
    You can find more info on how to create such environment specifications [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#create-env-file-manually)


Now it is time to test your Python installation. Type into your shell the following
```bash
    conda activate pp4rs
    conda list
```

It should return a list will all of the packages that are installed in the `pp4rs` environment. In order to use them, you will need to activate this environment in the beginning of every new shell session.


!!! note
    If you are using a computer with an Intel processor and want every ounce of performance for linear algebra operations, you might want to tell conda to use Intel's matrix algebra algorithms instead of the default open source ones. In order to do that, you simply have to install a quasi-package the following way

    ```
        conda install blas=*=*mkl --name pp4rs
    ```
    
    The performance boost is not huge, though.