# Setting up git

## Installing git

### Windows

- In your web browser, navigate to <https://git-scm.com/download/win>.
- Click on `Click here to download manually`
- Run the installer
  + In the screen `Choosing the default editor used by Git`, choose `Use Atom as Git's default editor`.
  + Leave all other options to their default choice, unless you have specific reasons not to.

## Git configuration

Before you can make your first commit using `git`, you need to configure your user profile with two key pieces of information: your email address and your username.

If `git` is unable to find that information, you may be prompted with the following error message:

```
*** Please tell me who you are.
Run
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```

### Windows

- Launch the Windows PowerShell from the Start Menu.
- Type the following commands after editing as needed:

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
