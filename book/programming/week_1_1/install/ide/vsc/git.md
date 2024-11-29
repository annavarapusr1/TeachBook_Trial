(vsc-git)=
# Using Git with VS Code

Git (a version control software) is very nicely integrated within VSC. If you are working on code and text-based projects, the use of Git is strongly encouraged (although if you are a student, we recommend you wait until it is introduced in class before proceeding further).

Git and VS Code (VSC) work together very well, regardless of how you use Git. For example, you can:
- use the "Source Control" GUI interface provided by VS Code (the branch diagram in the left toolbar)
- use any number of extensions that extend the default VS Code features
- invoke Git commands directly via a VS Code Terminal (i.e., a CLI)
- using GitHub Desktop application in parallel with VSC, which can be easier to use for some workflows, depending on your familiarity with VSC

These tools work seamlessly together because of the way VS Code is designed to work with text-based files, as well as the way Git functions by working primarily from the hidden `.git` folder in a Git repository.

## Adding a Git Repository

There are many ways to do this, and the internet is a better source of information that this book. However, to illustrate the key steps, we describe an approach here that uses the HTTPS protocol for cloning repositories, since VSC allows you to authenticate yourself by logging in to your GitHub account via the application (this avoids setting up SSH authentication). To complete these steps you should already have the extension GitHub Pull Requests installed, which will allow you to authenticate your GitHub account. Once this is done, it is very easy to clone a repository and start working on a project:

- In a web browser, copy the HTTPS clone link from the online repository
- In VSC, open a new window (File >>> New Window)
- Under the "Start" menu, select "Clone Git Repository"
- Paste the link, then choose the location where you would like to store the repository (i.e., identify the location for your working directory)s

You can now use the various Git workflows in the "Source Control" toolbar on the left side of VSC, which provides an easy way to carry out common Git workflows such as `commit`, `fetch`, `pull` and `push`, although one should note that the terminology may be altered slightly, and some commands are combined (for example, "Sync" combines `push` and `pull`).
