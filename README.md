# CRiSp use cases

<!-- badges: start -->

<!-- badges: end -->

This repository is an inventory of use cases for the CRiSp software.
Each use case is stored in a dedicated directory comprising of one or
more Quarto notebooks documenting the analytical workflow addressed in
that specific use case. To enable reproducibility, an environment is set
up for each use case with the `renv` package.

## List of use cases

| Use case | Description |
|--------------------------|----------------------------------------------|
| [01-Dresden-streams](https://CityRiverSpaces.github.io/01-Dresden-streams/notebook.html) | Corridor and segment delineation along the stream network of Dresden |

## How to run a use case

To run a use case, you need to have the `renv` package installed. If you
don't have it, you can install it by running:

``` r
install.packages("renv")
```

After installing `renv`, make sure that the working directory is set to
the root directory of the use case and run:

``` r
renv::restore()
```

This will install all the necessary packages and set up the environment
for the use case. You can then run the code in the Quarto notebook(s).

## How to add a use case

1.  Fork the repository and clone it locally.

2.  In the local clone, copy the template use case directory
    [00-use-case-template/](00-use-case-template/) and rename it with a
    short descriptive name using dashes between words.

3.  Create an RStudio project in the new directory and open it. This
    will set the working directory to the new use case directory.

4.  Write the narrative and code of the use case in Quarto notebook(s)
    using the template `notebook.qmd`. Feel free to split your workflow
    into multiple notebooks and rename them accordingly.

5.  Create a snapshot of the packages used in the notebooks by running:

``` r
renv::snapshot()
```

6.  Add the new use case to the list of use cases in the README.md file.

7.  Commit the new use case directory to the repository and push your
    changes to your fork.

8.  Open a Pull Request to the main repository.
