# Setting up R & Rstudio on MacOS

## Installing R

- In your web browser, navigate to <https://cran.r-project.org/bin/macosx/>.
- Click on `R-4.0.3.pkg`.
- Run the installer.
  + Use all the default options, unless you have specific reasons not to.
- Test your installation by launching `R` by typing `R` in a Terminal.

This should launch an R prompt in the terminal, and the prompt should display a launch message indicating that it is using R version 4.0.3.

## Installing RStudio

- In your web browser, navigate to <https://rstudio.com/products/rstudio/download/>
- Click on the `DOWNLOAD` button under "RStudio Desktop, Open Source License"
- On the next web page, click on `DOWNLOAD RSTUDIO FOR MAC`.
  + The button should mention a version number 1.3.1073 or higher.
- Open the downloaded file.
- In the window that opens, drag and drop the `RStudio` icon into the `Applications` folder.
- Test your installation by launching `RStudio` from the `Applications` folder.
- This should launch the application `RStudio`, and the prompt should display a launch message indicating that it is using R version 4.0.3.


## Managing multiple version of R

We ask that you use R version 4.0.3 for this course. Installing R 4.0.3 will not delete the other version(s) of R installed on you computer. It is possible to switch between multiple versions of R.

- In your web browser, navigate to <https://rud.is/rswitch/>.
- Click on the `Download RSwitch` button.
   + The button should mention a version number v1.7.0 or higher.
- Double click on the downloaded archive to decompress it.
  + A file named `RSwitch` should appear in the same folder.
- Drag and drop the `RSwitch` file into your `Applications` folder.
- Launch the `RSwitch` app from the `Applications` folder.
- The `RSwitch` icon should appear in the Apple menu bar at the top of your screen.
- Click on the `RSwitch` icon in the Apple menu bar.
- Select `4.0 (4.0.3)`
- If you had any `RStudio` application open with another version of R, you should close them.
- Any new `RStudio` application that you open now will use R version 4.0.3.
