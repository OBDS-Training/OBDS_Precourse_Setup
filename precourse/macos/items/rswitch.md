# Managing multiple version of R using RSwitch

We ask that you use R version 4.0.3 for this course. Installing R 4.0.3 will not delete the other version(s) of R installed on you computer. It is possible to switch between multiple versions of R.

- In your web browser, navigate to <https://rud.is/rswitch/>.

- Click on the `Download RSwitch` button.

The button should mention a version number v1.7.0 or higher.

- Double click on the downloaded archive to decompress it.

A file named `RSwitch` should appear in the same folder.

- Drag and drop the `RSwitch` file into your `Applications` folder.

- Launch the `RSwitch` app from the `Applications` folder.

- The `RSwitch` icon should appear in the Apple menu bar at the top of your screen.

- Click on the `RSwitch` icon in the Apple menu bar.

- Select `4.0 (4.0.3)`.

- If you had any `RStudio` application open with another version of R, you should close them.

- Any new `RStudio` application that you open now will use R version `4.0.3`.

When you launch a new instance of the `RStudio` application, the startup message printed in the console should display the version of R that is used.

Alternatively, you can type `R.version` in the console, and you should see

```r
...
major          4
minor          0.3
...
```
