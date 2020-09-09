# Setting up R

## Windows

- In your web browser, navigate to <https://cran.r-project.org/bin/windows/base/>
- Click on `Download R 4.0.2 for Windows`
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `R x64 4.0.2` from the Start Menu.

This should launch the application `RGui (64-bit)`.
You can close this application.

# Setting up RStudio

Please make sure you have already installed R 4.0.2 as indicated above.

## Windows

- In your web browser, navigate to <https://rstudio.com/products/rstudio/download/>
- Click on the `DOWNLOAD` button under "RStudio Desktop, Open Source License"
- On the next web page, click on `DOWNLOAD RSTUDIO FOR WINDOWS`.
  The button should mention a version number 1.3.1073 of higher (last checked on 09/09/2020).
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `RStudio` from the Start Menu.

This should launch the application `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.2.

# Managing multiple version of R

We ask that you use R version 4.0.2 for this course.
Installing R 4.0.2 will not delete the other version(s) of R installed on you computer.
It is possible to switch between multiple versions of R.

## Windows

- Launch `RStudio`.
- In the RStudio menu, click on `Tools`.
- Click on `Global Options...`.
- In the `General` panel, in the `Basic` sub-panel, next to the `R version:` field, click on the `Change...` button.
- Select `Choose a specific version of R:`.
- Select `[64-bit] C:\Program Files\R\R-4.0.2`.
- Click on `OK`
- Restart `RStudio` when prompted.

This should relaunch `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.2.
