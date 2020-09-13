# Setting up git

## Installing git

### MacOS

`git` should be available after following the instructions for [Installing XCode](xcode_setup.md).

You can test your installation as follows:

- In a Terminal, type `git`.

This should display a message indicating the main `git` subcommands.

### Windows

- In your web browser, navigate to <https://git-scm.com/download/win>.
- Click on `Click here to download manually`
- Run the installer
  + In the screen `Choosing the default editor used by Git`, choose `Use Atom as Git's default editor`.
  + Leave all other options to their default choice, unless you have specific reasons not to.

  You can test your installation as follows:

  - Launch the Windows PowerShell from the Start Menu.
  - Type `git`

  This should display a message indicating the main `git` subcommands.

## Git configuration

Before you can make your first commit using `git`, you need to configure your user profile with two key pieces of information: your email address and your username.

If `git` is unable to find that information, you may be prompted with the following error message:

```
*** Please tell me who you are.
Run
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```

### Windows / MacOS

- Launch a command line console
    + On Windows, launch the `Windows PowerShell` from the `Start Menu`.
    + On MacOS, launch a new `Terminal`.

- To check whether `git` is already configured, type the following commands:

```bash
git config --global user.email
git config --global user.name
```

If both commands display information in the console, then everything is set and you can ignore the instructions below.

If any of those commands does not display a result, use the commands below to set the relevant pieces of information.

- Type the following commands after editing as needed:

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

You can then run the commands above again to check your configuration.
