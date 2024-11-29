(extensions-vsc)=
# VS Code Extensions

This page gives an overview of useful extensions in VS Code, with short tips on how to install them or what they could be used for. It is organized by various user types.

To install an extension, select the "Extensions" box on the left side of the application (the symbol is four boxes), then search for and install the following (entering the ID in the search box turns up the right result).

As VS Code and its extensions are actively developed by a large international community, we don't include exhaustive instructions and troubleshooting help in this book; instead, you should search for up-to-date solutions on the internet. For example, the [Extension Marketplace page from VS Code](https://code.visualstudio.com/docs/editor/extension-marketplace) is already quite thorough.

## First Time User

New to VS Code? New to programming in general? If you are using Python, we recommend starting with the following extensions:

- Python (Extension ID: `ms-python.python`)
- Jupyter (Extension ID: `ms-toolsai.jupyter`)

```{tip}
Note that if you are using the Jupyter extension it is good to include `ipykernel` in your Python environments (but VS Code will add this automatically for you if you don't - isn't VS Code great?!).
```

## Markdown All-in-One

Extension ID: `yzhang.markdown-all-in-one`

This is a useful tool for rendering Markdown files in real time. Once installed, open a `*.md` file and use the shortcut `CTRL+SHIFT+V` to open a preview page. It is useful to arrange the preview side-by-side with the source code so you can see the marked up version as you edit. This is extremely useful for checking figures, equations and other Markdown formats before pushing files to other locations (e.g., a Git repository).

```{tip}
As Markdown is implemented in a wide array of different software, it has many different variants (called "flavors"). For example, see the [Wikipedia Summary of Markdown Variants](https://en.wikipedia.org/wiki/Markdown#Variants). This means that what you see when your Markdown text is rendered may appear differently on other platforms. For example, the appearance of your file on GitHub maybe different than what you see in VSC. The takeaway? _Always check your Markdown file on the platform where it will be shared!_
```

## Code Spell Checker

Extension ID: `streetsidesoftware.code-spell-checker`

This extension is useful for catching typos in your work. Read the extension documentation page for instructions on how it can be customized.

## Git

For general use with Git**Hub** use the following:

- GitHub Pull Requests (Extension ID: `GitHub.vscode-pull-request-github`)