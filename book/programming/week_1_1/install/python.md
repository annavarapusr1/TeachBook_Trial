# Python Installation

There are many ways to get Python, a few of which are listed here. If you are new to Python and related open-source software, we recommend using Miniconda or Anaconda. Choose Miniconda if you are comfortable using the command line interface.

Direct installation of Python is a good option if you want to build environments quickly, your project is limited to Python and/or you don't mind installing and troubleshooting software installation for your particular copmputer operating system (for example, using tools like LaTeX, Pandoc, or non-Python programming languages).

```{note}
The installation instructions here use `conda-forge` as the default channel for creating and managing environments with `conda`, for example, environments are created with the optional argument `create -c conda-forge`. This is primarily to avoid license issues, as the default channel has more restrictive terms of use, and has a negligible impact on the installation of Python.

When installing Python packages, `conda-forge` generally has higher package versions, so it is common to use this as the default channel.
```

## Quick Start

One of the easiest ways to get Python is via Miniconda. Here are the minimum steps required to get started on Windows (Python is installed on Mac OS by default); see the associated pages if you need a more detailed guide.

1. Execute the following in the Windows Command Prompt:

```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o miniconda.exe
start /wait "" miniconda.exe /S
del miniconda.exe
```

2. Add `./miniconda/Scripts` to the Path environment variable for your user account (_not_ the system)
3. Confirm the installation works by using `conda --version` in the Windows Command Prompt
4. Create an environment by executing the following, replacing the `<...>` as needed:
```
conda create -c conda-forge -n <environment name> python=<3.XX>
```