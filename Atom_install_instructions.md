This file explains how to install the text editor `Atom` and some add-on packages to atom that will make your life easier. 

## 1) Text editors - what are they and why do we need them

Text editors are computer programmes that allow you to write and edit very basic text files without all the fancy formatting that programmes like Microsoft Work and Excel add to a document. Microsoft Notepad is an example of a basic text editor you might have come across even if you are new to programming. 

Basic text is important as it allows us to write files that can be easily interpreted by the computer and executed as code to perform computational tasks. 


## 2) Why did we choose Atom 

There are many different text editors available and many people have their own personal favourite that they tend to use. For example you might have come across `emacs`, `vim`, `sublime text`, `nedit`, `gedit` or `nano`. It's very much a matter of personal preference as to which one you choose, some are very basic and easy to use like `nano` or `gedit`, whilst others like `emacs` and `vim` have their own particular syntax that you need to learn but also have the benefit of being really customisable and have lots of additional functionality that can make writing code faster once you get to grips with them. 


We like [Atom](https://atom.io/) as it is simple to get started with and it also has a lot of nice add-on packages that make like a whole lot easier (e.g. it integrates with github excellently, you can edit files remotely on a server and you can run R and python code interactively in the same session etc.)

## 3) Installing Atom on your own computer


- You can find the full install instructions for atom [here](https://flight-manual.atom.io/getting-started/sections/installing-atom/) - basically go to (https://atom.io/) and click the download button. 
- **Note**: If you already have atom installed don't reinstall it - but consider updating it - see [here](https://flight-manual.atom.io/getting-started/sections/installing-atom/) for how to do this and look at the 'updating Atom' section** 

## 4) Opening Atom and getting started

- once installed you should be able to open Atom like you would any other normal software on your computer (From Apps folder for Mac, XXXXX for Windows )
- See Atom documentation for [getting started](https://flight-manual.atom.io/getting-started/sections/atom-basics/): This has a brief guide on changing the colour 'theme' settings to make your atom look pretty - don't worry about this too much but one thing we do want to set is the 'soft tab' option and 'tab length'!
    1) Open Atom
    2) Get to the settings pane  - it might open as a window in Atom when you open it, but if not you can get it to open by going to either `File/Settings` if you are on Windows or `Atom/Preferences` if you are on a mac
    3) In Atom `Settings` window, On the left handside there should be a Tab called `Editor`. Click on the `Editor` Tab and scroll down to the `Soft Tabs` option
    4) Click so `Soft Tabs` has a 'tick' next to the `Soft Tabs` option.
    5) Scroll down a couple of boxes further to `Tab length` and set this to `4` if it's not already. We do this because some programming languages do not like a mix of tabs and spaces when you are writing code.This option means that when you type the 'tab' button on your keyboard 4 space characters will be inserted rather then a tab character, it keeps things consistent in your script and will save you some debugging hassle later. 

## 5) Adding Packages to Atom to add functionality 

- now we should have a fully functioning version of Atom, we can now add additional packages to make our lives easier for working on code on the server. There are loads of packages that you could add on to your Atom program, but these below are particularly useful to have installed and we will go through in more detail on the course. 

- [ftp-remote-edit](https://atom.io/packages/ftp-remote-edit): This is a package that allows you to read and write to files on a remote server, we will use it to read and write code files on the cgat server
- [Tree-view](https://atom.io/packages/tree-view): Allows you to easily explore files in a browser pane
- [platformio-IDE-terminal](https://atom.io/packages/platformio-ide-terminal): Allows you to run a terminal from Atom - we will use this to log onto the server and run our code ins
- [teletype](https://atom.io/packages/teletype): Allows you to collaborate in real time on the same document with other users

1) To install the above packages navigate to the Atom settings pane (If your not already in it in Windows go to `File/Settings` or Mac `Atom/Preferences` 
2) On the left of the settings window click the `+ install` tab.
3) You should now be on the Install Packages Pane and see a search bar at the top.
4) Type the names of the above packages in the search bar (e.g. `ftp-remote-edit`) the package should come up below (tip: copy and paste to make sure you get the right name, there are several very similarly named packages)
5) click the install button for the correct package. Atom should take care of the installation of these add-ons but you might need to restart Atom after installing packages to get them to work properly.


-------------------------
This should be enough to enable us to get started on the course but if your interested in customising your Atom instance even further you can look and find other packages you might want to try out here: https://atom.io/packages. We will go through how to  use these add-ons and Atom itself in the course, so don't worry if it's all a bit confusing at this point. 

Great! Hopefully the above will have gone well, however if there are any installation difficulties please let your OBDS trainers know and they can help you figure things out. 

