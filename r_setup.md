# Setting up R

## Installing R

### MacOS

- In your web browser, navigate to <https://cran.r-project.org/bin/macosx/>.
- Click on `R-4.0.2.pkg`.
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `R` by typing `R` in a Terminal.

This should launch an R prompt in the terminal, and the prompt should display a launch message indicating that it is using R version 4.0.2.

### Windows

- In your web browser, navigate to <https://cran.r-project.org/bin/windows/base/>
- Click on `Download R 4.0.2 for Windows`
- Run the installer.
- Test your installation by launching `R x64 4.0.2` from the Start Menu.

This should launch the application `RGui (64-bit)`.
You can close this application.

## Installing RStudio

### MacOS

- In your web browser, navigate to <https://rstudio.com/products/rstudio/download/>
- Click on the `DOWNLOAD` button under "RStudio Desktop, Open Source License"
- On the next web page, click on `DOWNLOAD RSTUDIO FOR MAC`.
  The button should mention a version number 1.3.1073 or higher.
- Open the downloaded file.
- In the window that opens, drag and drop the `RStudio` icon into the `Applications` folder.
- Test your installation by launching `RStudio` from the `Applications` folder.

This should launch the application `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.2.

### Windows

- In your web browser, navigate to <https://rstudio.com/products/rstudio/download/>
- Click on the `DOWNLOAD` button under "RStudio Desktop, Open Source License"
- On the next web page, click on `DOWNLOAD RSTUDIO FOR WINDOWS`.
  The button should mention a version number 1.3.1073 or higher.
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `RStudio` from the Start Menu.

This should launch the application `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.2.

## Managing multiple version of R

We ask that you use R version 4.0.2 for this course.
Installing R 4.0.2 will not delete the other version(s) of R installed on you computer.
It is possible to switch between multiple versions of R.

### MacOS

- In your web browser, navigate to <https://rud.is/rswitch/>.
- Click on the `Download RSwitch` button.
  The button should mention a version number v1.7.0 or higher.
- Double click on the downloaded archive to decompress it.
  A file named `RSwitch` should appear in the same folder.
- Drag and drop the `RSwitch` file into your `Applications` folder.
- Launch the `RSwitch` app from the `Applications` folder.

The `RSwitch` icon should appear in the Apple menu bar at the top of your screen.

- Click on the `RSwitch` icon in the Apple menu bar.
- Select `4.0 (4.0.2)`
- If you had any `RStudio` application open with another version of R, you should close them.

Any new `RStudio` application that you open now will use R version 4.0.2.

### Windows

- Launch `RStudio`.
- In the RStudio menu, click on `Tools`.
- Click on `Global Options...`.
- In the `General` panel, in the `Basic` sub-panel, next to the `R version:` field, click on the `Change...` button.
- Select `Choose a specific version of R:`.
- Select `[64-bit] C:\Program Files\R\R-4.0.2`.
- Click on `OK`
- Restart `RStudio` when prompted.

This should relaunch `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.2.

## Git integration with RStudio

After following the instructions for [Setting up git](git_setup.md) and [Creating an SSH key pair](create_ssh_keypair.md), check that RStudio detects your `git` installation and your private SSH key.

- Launch `RStudio`.
- In the RStudio menu, click on `Tools`.
- Click on `Global Options...`.
- In the `Git/SVN` panel:
  + The `Git executable:` field should indicate the path to the `git` executable, e.g.
    * `C:\Program Files\Git\bin\git.exe` on Windows.
    * `/usr/bin/git` on MacOS.
  + The `SSH RSA key:` field should indicate the path to your private SSH key, e.g.
    * `C:\Users\Username\.ssh\id_rsa` on Windows.
    * `/Users/username/.ssh/id_rsa` on MacOS.

Any field that displays `(Not found)` means that `RStudio` did not detect a working installation at any of the standard locations on your system.
Either relaunch `RStudio`, or try repeating the relevant instructions for [Setting up git](git_setup.md) or [Creating an SSH key pair](create_ssh_keypair.md), and relaunch `RStudio` again to apply the changes.

## Installing Rtools (Windows only)

You may see the following warning message when installing R packages on Windows.

```r
WARNING: Rtools is required to build R packages, but is not currently installed.
```

- In your web browser, navigate to <https://cran.rstudio.com/bin/windows/Rtools/>
- Click on `rtools40-x86_64.exe`
- Run the installer
  + Use all the default options, unless you have specific reasons not to.
