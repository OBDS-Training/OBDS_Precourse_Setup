# Setting up Atom

This page explains how to install the text editor `Atom` and some add-on packages to atom that we will use during the course, and generally make life easier for daily bioinformatics work.

## Text editors - what they are and why we need them

Text editors are computer programs that allow you to write and edit simple text files without the additional text formatting that programs like [Microsoft Word](https://www.microsoft.com/en-gb/microsoft-365/word) and [Microsoft Excel](https://www.microsoft.com/en-gb/microsoft-365/excel) add to a document.
For instance, [Notepad](https://www.microsoft.com/en-us/p/notepad-for-windows-10/9nblggh4w20k) is an example of a basic text editor you might have come across on Microsoft Windows.

Basic text is important as it allows us to write files that can be easily interpreted by the computer and executed as code to perform computational tasks.
Text files are also easy to share, as they do not require any proprietary program to open and edit them.

## Why we chose Atom

There are many different text editors available and many people have their own personal favourite that they tend to use.
For example you might have come across some of these editors...
- [GNU Emacs](https://www.gnu.org/software/emacs/)
- [Vim](https://www.vim.org/)
- [GNU nano](https://www.nano-editor.org/)
- [Sublime Text](https://www.sublimetext.com/)
- [nedit](https://sourceforge.net/projects/nedit/)
- [gedit](https://wiki.gnome.org/Apps/Gedit)

It's very much a matter of personal preference as to which one you choose, some are very basic and easy to use like [GNU nano](https://www.nano-editor.org/) and [gedit](https://wiki.gnome.org/Apps/Gedit), whilst others like [GNU Emacs](https://www.gnu.org/software/emacs/) and [Vim](https://www.vim.org/) offer more advanced functionality which comes at the cost of a steeper learning curve.For instance, some editors are customizable, with lots of additional functionality that can make writing code faster once you get to grips with their keyboard shortcuts and syntax.

We like [Atom](https://atom.io/) as it is simple to get started with, while it also has a lot of nice add-on packages that make life a whole lot easier (e.g. it integrates with GitHub seamlessly and it can edit files remotely on a server).

## Installing Atom on your own computer

- You can find the full install instructions in the [Installing Atom](https://flight-manual.atom.io/getting-started/sections/installing-atom/) section of the <https://atom.io/> website.

**Note**: If you already have Atom installed, you don't need to reinstall it.
That said, consider following the instruction in the [Updating Atom](https://flight-manual.atom.io/getting-started/sections/installing-atom/#updating-atom) section.

## Launching Atom and getting started

Once installed you should be able to open Atom like you would any other normal software on your computer (From the `Applications` folder for Mac, from the `Start menu` for Windows).
See Atom documentation for [getting started](https://flight-manual.atom.io/getting-started/sections/atom-basics/). This has a brief guide on [Changing the theme](https://flight-manual.atom.io/getting-started/sections/atom-basics/#changing-the-theme) settings to make the Atom window look pretty.
Don't worry too much about this, but one thing we do want to set is the 'soft tab' option and 'tab length':

    1) Open Atom
    2) Get to the settings pane. It might immediately open as a tab in the editor window when you launch Atom, but if not you can open it by navigating the Atom menu to either `File/Settings` if you are using Windows or `Atom/Preferences` if you are using Mac.
    3) In the Atom `Settings` pane, on the left handside there should be a tab called `Editor`. Click on the `Editor` Tab and scroll down to the `Soft Tabs` option.
    4) Click so `Soft Tabs` has a 'tick' next to the `Soft Tabs` option.
    5) Scroll down a couple of boxes further to `Tab length` and set this to `4` if it's not already.
       We do this because some programming languages do not like a mix of tabs and spaces when you are writing code.
       This option means that when you type the 'tab' key on your keyboard 4 space characters will be inserted rather then a tabulation character.
       This keeps things consistent in your script and will save you some debugging hassle later.


## Adding Packages to Atom to add functionality

Now that we have a fully functioning version of Atom, we can add additional packages to make our lives easier for working on code on the server. There are loads of packages that you could add on to your copy of the Atom program, but those below are particularly useful to have installed and we will go through in more detail on the course.

    - [ftp-remote-edit](https://atom.io/packages/ftp-remote-edit): This is a package that allows you to read and write files on a remote server.
      We will use this package to read and write files on the CGAT server.
    - [platformio-IDE-terminal](https://atom.io/packages/platformio-ide-terminal): This package allows you to run a terminal from Atom.
      We will use this package to log onto the server and run our code in the terminal on the server.
    - [teletype](https://atom.io/packages/teletype): Allows you to collaborate in real time on the same document with other users.
    - [script](https://atom.io/packages/script): Enables you to run python scripts in Atom.
    - [tool-bar](https://atom.io/packages/tool-bar): Adds a customisable tool bar.
    - [tool-bar-atom](https://atom.io/packages/tool-bar-atom): Adds a tool bar for common atom shortcuts (based on tool-bar).
    - [python-debugger](https://atom.io/packages/python-debugger): A tool for debugging Python code.
    - [python-autopep8](https://atom.io/packages/python-autopep8): A tool for formatting Python code.
    - [ide-python](https://atom.io/packages/ide-python): A suite of tools for adding syntax checking and code auto-completion for Python code.
    - [atom-ide-ui](https://atom.io/packages/atom-ide-ui): Additions to te Atom user interface for linters and debuggers.
    
1) To install the above packages navigate to the Atom settings pane, like we did above.
2) On the left of the settings window click the `Install` tab.
3) You should now be in a pane called `Install Packages` and see a search bar at the top.
4) Type the names of the above packages in the search bar (e.g. `ftp-remote-edit`).
   The package should be shortlisted below (tip: copy and paste to make sure you get the right name, there are several packages with very similarly names)
5) Click the `Install` button for the correct package.
   Atom should take care of the installation of these add-ons but you might need to restart Atom after installing packages to get them to work properly.

We will go through how to use these add-ons and Atom itself during the course, so don't worry if it's all a bit confusing at this point.

Great! Hopefully the above will have gone well, however if there are any installation difficulties please let your OBDS trainers know and they can help you figure things out.
