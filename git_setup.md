# Setting up git

## Windows

After completing the instructions for [Setting up Atom](atom_installation_instructions.md):

- Launch Atom from the Start Menu.
- Open a new file.
  + In the Atom menu, click on `File`.
  + Click on `New File`.
  + In the new file, add the following lines, and edit as needed:

```bash
[user]
	email = you@example.com
	name = "Firstname Lastname"
```

- Save the file as `.gitconfig` in your home folder.
  + In the Atom menu, click on `File`.
  + Click on `Save As...`.
  + Navigate to your home folder, e.g. `C:\Users\Username`
  + In the `File name:` field, type `gitconfig`
  + Click on the `Save` button.

If you already have a file called `.gitignore` in your home folder, simply make sure that it contains at least the lines above.
