(env-vars-windows)=
# Environment Variables

```{note}
This is for Windows Operating Systems only. It is often required when installing command line tools, for example `conda`.
```

Your computer has _environment variables_ which define the behavior of your operating system. For example, one commonly used variable is `PATH`, which helps your computer locate key files, especially when using a CLI.

````{tip}
Keep in mind that the Windows OS allows you to set environment variables for a specific _user_ as well as for the _system_ (all users). It is important to note which environment variable you should set for a given activity, as choosing the wrong one can have unintended consequences (or lead to much frustration!). The difference can be seen in the example here:

```{figure} figures/environment_var_system_user.png
---
width: 60%
name: environment_var_system_user
---
Environment variables, highlighting the difference between those for the user and system (all users).
```

````

## The `PATH` Variable

The `PATH` variable is like an address book for your computer: it lists various folders (directories) where the computer should look when executing commands. Updating the `PATH` variable is often required when installing software that is to be used with a CLI. In addition, updating this variable is often the solution to the problem of trying to execute a command and getting a "not found" message in response. For example, the following Windows Command Prompt illustrates what happens when (first) a command is executed that cannot be found by the CLI and (second) `conda` is called:

```none
C:\Users\YOUR_USERNAME>software_that_is_not_on_path --version
'software_that_is_not_on_path' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\YOUR_USERNAME>conda --version
conda 23.11.0
```

```{tip}
Note the two dashes used with `--version`, not one, `-`!
```

The message that is returned with the `conda` version number indicates not only that `conda` is installed _and_ that it is findable via the Windows `PATH` environment variable.

### Setting the `PATH` Variable

Setting the `PATH` variable is as simple as giving the path to the folder (directory) where the file or program of interest is located. All that is needed is to explain where the variable needs to be updated.

````{admonition} Before you start, find your desired path!
:class: tip, dropdown
These instructions assume that you have _already_ identified the path of the folder (directory) which needs to be added to the `PATH` variable. On windows, the easiest way to do this is to navigate to the folder using the File Explorer, then click in the address bar near the top and copy the text, which should look something like this:

```none
C:\Users\<your user name>\miniconda3\Scripts
```

In this case, the folder (directory) contains the executable files `conda.exe`, which is what makes the command `conda` possible to use on the CLI. Thus, the full path to `conda.exe` is this:

```none
C:\Users\<your user name>\miniconda3\Scripts\conda.exe
```
Note also that depending on your system settings, or if you are copying the path from a CLI, you may need to adjust the separators from a forward slash `/` to a backward slash `\`; the `PATH` variable on Windows requires a backward slash `\`.
````

The easiest way to find the appropriate setting window is by typing the first letters of "environment" in the Windows toolbar. The first three letters are usually enough to cause several relevant options to appear; select _Edit environment variables for your account_ and see the figure below for an illustration:

```{figure} figures/environment_var_search.png
---
width: 60%
name: environment_var_search
---
Search for environment variable settings; note the description "for your account"!
```

As a general rule you should only adjust the `PATH` variable for the _user_, **not** the _system._ Failing to do this is a common mistake and leads to frustration when installing applications like Anaconda and Miniconda.

To set the right variable, pay particular attention to the descriptions provided in the environment variable window, as it is easy to miss; the right location is illustrated clearly in the following figure:

```{figure} figures/environment_var_miniconda_not_system.png
---
width: 60%
name: environment_var_miniconda_not_system
---
Unless specified otherwise, don't set an environment variable for the _system_, only your account!
```

Once you have identified the proper (user) window, look for the `PATH` variable, select it, then click the "Edit..." button. If the variable value is empty, you will probably see a window similar to that in the following figure; enter (paste) the path of the folder (directory) you wish to add to the path in the field "Variable value" then click "OK." Note that you can browse for the file and folder of interest via the settings window if you did not already copy the path via the File Explorer or a CLI. 

```{figure} figures/environment_var_miniconda.png
---
width: 60%
name: environment_var_miniconda
---
How to add a folder (directory) location to the `PATH` variable. The example here is for Miniconda.
```

If there are already values set for the `PATH` variable then the "Edit..." button will probably show a window like that in the following figure. In this case, you can add a new path via the "New" button; paste the path in an open row of the list. Note that you can browse for the file and folder of interest via the settings window if you did not already copy the path via the File Explorer or a CLI. 

```{figure} figures/environment_var_PATH_examples.png
---
width: 60%
name: environment_var_PATH_examples
---
Example showing folders (directories) that have already been added to the `PATH` variable. Note the "New" and "Edit" buttons.
```

The following figure illustrates exactly where you should paste your desired folder (directory) path after clicking the "New" button:

```{figure} figures/environment_var_PATH_new.png
---
width: 60%
name: environment_var_PATH_new
---
How to add a folder (directory) location to the `PATH` variable using the "New" button.
```

### Checking `PATH` Configuration

To check that your `PATH` variable was properly configured you should use a CLI to see whether your program of interest is now findable. For example, if you added the location of `conda.exe` to `PATH` you should now be able to execute `conda --version` (note the two dashes, `--`, not one, `-`!), which will return the following:

```none
C:\Users\YOUR_USERNAME>conda --version
conda 23.11.0
```

```{tip}
You usually need to restart a CLI for changes to the variables to take effect. Simply closing and reopening the CLI is usually enough. If you are completely sure that the setup was done properly, it may also be prudent to restart your computer.
```
