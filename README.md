tidyverse course
================

<!-- README.md is generated from README.Rmd. Please edit that file -->
Building the docs folder
------------------------

To create the html files for the docs folder, use the Build -&gt; Build All button in RStudio. This button will use the rules defined in `Makefiles` to produce the HTML files. `make` will use the `rmarkdown::render_site()` function to create the files in the `docs` folder.

-   Source files for the gh-pages doc folder are oranized as follows:
    -   `lectures` folder for ioslides lectures with Rmd files supposed to start with "lecture\*".
    -   `practicals` folder for the tutorials rendered using `unilur::tutorial_html()`. Rmd files should start with "TD\*".
    -   `site` folder for the global webpages
    -   Every file in these folders not starting with an underscore ("\_") and not being a used source will be copied to the docs folder (this is a `rmardkown::render_site()` behaviour).
-   Altering `_site.yml` should reconstruct the site.
-   You can use the clean or clean & rebuild in Rstudio: it will erase the content of the doc folder and rebuild the site.
