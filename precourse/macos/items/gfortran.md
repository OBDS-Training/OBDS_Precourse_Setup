# Setting up the gfortran compiler on MacOS

Some R packages are distributed as source code that needs to be compiled on your computer during installation.
The GGC compilers (including gfortran) are necessary to compile those packages.

- In your web browser, navigate to <https://github.com/fxcoudert/gfortran-for-macOS/releases>.

- Identify the latest version that is not labelled as 'experimental'.

On June, 3rd 2021, this is 'gfortran 10.2 for Catalina (macOS 10.15)', released on 30 Sep 2020.

- Click on the `*.dmg` file listed in the assets for that release.

For the version mentioned above, this is `gfortran-10.2-Catalina.dmg`.

- Open the downloaded file.

- In the window that opens, open the file `gfortran.pkg`.

Use all the default options, unless you have specific reasons not to.

## Source

To give you an idea 

- When you install a new version of R for macOS, you would usually navigate to <https://cran.r-project.org/bin/macosx/>.

- In the `Subdirectories` section, the `tools` link would take you to <https://cran.r-project.org/bin/macosx/tools/>.

- At the top of that page, you would be encouraged to navigate to <https://github.com/fxcoudert/gfortran-for-macOS/releases>.
