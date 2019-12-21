# Configuring the Workshop Environment
These directions walk through downloading the NAVO workshop material, installing miniconda, a lightweight distribution of the python package installer conda, then creating and testing the custom environment for the  workshop. 

## 1. Clone This Repository

Download the workshop folder using
[git](https://help.github.com/articles/set-up-git/):

    % git clone https://github.com/NASA-NAVO/aas_workshop_2020_winter.git

If you don't have git installed, you can download the ZIP file by pressing the
green *Clone or download* button at
https://github.com/NASA-NAVO/aas_workshop_2020_winter and selecting *Download ZIP*.
However, this option is not recommended because it impedes the ability to
update your copy of the repository if updates are made.

## 2. Install Miniconda (if needed)

*Miniconda is a free minimal installer for conda. It is a small, bootstrap
version of Anaconda that includes only conda, Python, the packages they depend
on, and a small number of other useful packages, including pip, zlib and a few
others. Note, though, that if you have either Miniconda or the full Anaconda
already installed, you can skip to the next step.*

Check if Miniconda is already installed.

    % conda info

If Miniconda is not already installed, follow these instructions for your
operating system: https://docs.conda.io/en/latest/miniconda.html

On Windows, you might also need
[additional compilers](https://github.com/conda/conda-build/wiki/Windows-Compilers).

## 3. Create a conda environment for the workshop

*Miniconda includes an environment manager called conda. Environments
allow you to have multiple sets of Python packages installed at the same
time, making reproducibility and upgrades easier. You can create,
export, list, remove, and update environments that have different versions of
Python and/or packages installed in them. For this workshop, the python version 
and all needed packages are listed in the
[environment.yml](https://github.com/NASA-NAVO/aas_workshop_2020_winter/blob/master/environment.yml) file.*

On Mac or Linux, open your terminal and verify your shell environment:

    % echo $SHELL

If the output text does not contain `bash`, switch to the bash shell before
being able to run anything related to conda.

On Windows, open the `Anaconda Prompt` terminal app.

Now navigate to this directory in the terminal. For example, if you installed
the navo-workshop directory in your home directory, you could type the
following.

    % cd aas_workshop_2020_winter

And finally, on any platform, to install and activate the aas_workshop_2020_winter
environment, type:

    % conda env create -n navo-workshop --file environment.yml
    % conda activate navo-workshop

## 4. Check Installation

The name of the new conda environment created above should be displayed next
to the terminal prompt:

    (navo-workshop) %

Run the `check_env.py` script to check the Python environment and some of the
required dependencies:

    (navo-workshop) % python check_env.py

## 5. Starting Jupyterlab
From the directory containing the notebooks:

    (navo-workshop) % jupyter lab

## Additional Resources

- [Set up git](https://help.github.com/articles/set-up-git/)
- [Conda Users Guide](https://docs.conda.io/projects/conda/en/latest/user-guide/)