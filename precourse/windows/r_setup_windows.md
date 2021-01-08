# Setting up R & Rstudio on Windows 10

## Installing R

- In your web browser, navigate to <https://cran.r-project.org/bin/windows/base/>
- Click on `Download R 4.0.3 for Windows`
- Run the installer.
- Test your installation by launching `R x64 4.0.3` from the Start Menu.

This should launch the application `RGui (64-bit)`.
You can close this application.

## Installing RStudio

- In your web browser, navigate to <https://rstudio.com/products/rstudio/download/>
- Click on the `DOWNLOAD` button under "RStudio Desktop, Open Source License"
- On the next web page, click on `DOWNLOAD RSTUDIO FOR WINDOWS`.
  The button should mention a version number 1.3.1073 or higher.
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `RStudio` from the Start Menu.

This should launch the application `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.3.

## Managing multiple versions of R

We ask that you use R version 4.0.3 for this course.
Installing R 4.0.3 will not delete the other version(s) of R installed on you computer.
It is possible to switch between multiple versions of R.

- Launch `RStudio`.
- In the RStudio menu, click on `Tools`.
- Click on `Global Options...`.
- In the `General` panel, in the `Basic` sub-panel, next to the `R version:` field, click on the `Change...` button.
- Select `Choose a specific version of R:`.
- Select `[64-bit] C:\Program Files\R\R-4.0.3`.
- Click on `OK`
- Restart `RStudio` when prompted.

This should relaunch `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.3.

## Installing Rtools

You may see the following warning message when installing R packages on Windows.

```r
WARNING: Rtools is required to build R packages, but is not currently installed.
```

- In your web browser, navigate to <https://cran.rstudio.com/bin/windows/Rtools/>
- Click on `rtools40-x86_64.exe`
- Run the installer
  + Use all the default options, unless you have specific reasons not to.
