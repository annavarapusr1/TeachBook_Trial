(vsc)=
# Visual Studio Code (VSC)

Visual Studio Code (VSC) is and _Integrated Development Environment_ (IDE): a software that helps users program more effectively, as it combines different workflows in one place. For our purpose VSC is very useful because allows us to do things in one place, for example:
- manage files and sub-directories within our working directory
- execute Python code (and any other programming language!), including Jupyter notebooks
- manage Python environments
- use Git and version control
- many other things, especially with Extensions!

Although Jupyter Lab and Jupyter Notebook are also IDE's, they don't provide as many features as VSC, or maintenance and improvement of tools is slower because the Jupyter development community is smaller. The availability of extensions in VSC, in particular, is exceptional. 

## VSC Installation

The primary steps are:
- download the installer from [code.visualstudio.com/download](https://code.visualstudio.com/download)
- install on your computer (default settings are fine)
- get familiar with the interface
- install a few useful Extensions (see {ref}`overview page <extensions-vsc>`)
- use it!

## Command Palette

VSC is very easy to customize, and you can spend hours optimizing it for your own personal use and projects. We recommend skipping this for now if you are just getting started. However, it is useful to know about the _Command Palette,_ which governs all functionality of VSC, and can be accessed with `CTRL+SHIFT+P` for Windows or `SHIFT+CMD+P` for Mac. _This is the single most important VSC command to remember._

## Using a CLI (a VSC "Terminal")

VSC refers to a Command Line Interface (CLI) with the term "Terminal."

You can open a new Terminal with the menu bar at the top. Once a Terminal is active you can open additional Terminal instances, choosing amongst the various CLI's available on your computer. It can be useful to have more than one CLI open at a time and keep them collected together with your project files!

To have a specific CLI open by default when you open a Terminal in VSC, open the Command Palette (`CTRL+SHIFT+P`, `SHIFT+CMD+P`), select the option `Terminal: Select Default Profile` and select your preferred CLI from the list.

## Activating a Python Environment

The easiest way to do this is to make sure you have the Python extension installed, then try to run the cells of a notebook or execute a `*.py` file (look for the play button icon once you have either of these file types open). Upon clicking the run button you will see that VSC asks you to choose a Python kernel. You can choose a Python virtual environment (`venv`) if you have one, but you should also be able to see your `conda` environments as well.

Remember that if you need to install more packages, you should open a CLI (this is called a "terminal" in VSC) and use `pip`, which you can do directly from VSC.