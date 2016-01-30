webvis is an R (http://www.r-project.org) package designed to provide a common framework for creating web visualizations (now available on  [CRAN](http://cran.r-project.org/web/packages/webvis/)).  It is currently a wrapper for protovis (http://vis.stanford.edu/protovis/), although it will ultimately provide access to other visualization libraries including the Google Visualization API (http://code.google.com/apis/visualization/).  More resources can be found here: http://www.insideria.com/2009/12/28-rich-data-visualization-too.html.

Webvis can be installed in R by calling `install.packages("webvis")`.  You can test the installation by running the primary demo: `demo(playfairs.wheat)`.

# Roadmap #

Here is a rough outline of the project plan.  More details can be found on the "Issues" tab.

  * Version 0.0.1 - Wrap all the major components of protovis. (This version is now available on [CRAN](http://cran.r-project.org/web/packages/webvis/)).  This version provides all the basic functionality although it is not in a final form.  Ideally the package will ultimately mirror ggplot2's functionality as much as possible.  The `demo(playfairs.wheat)` is available, although the scaling of the x-axis is slightly off.
  * Version 0.1 ([item list](http://code.google.com/p/rwebvis/issues/list?can=1&q=label:Release0.1)) - Complete the basic Protovis integration with basic examples. Should also include more functionality around scaling.  And provide a legend on the standard charts.  Will provide RUnit test cases of important functions. (April 2010)
  * Version 0.2 - Provide latticing and layering functionality, as well as some extended examples. (April 2010)
  * Version 0.3 - Provide client side JavaScript execution through http://code.google.com/p/rjscript/ package  Enable multiple output formats (e.g. PNG, JPG, GIF) for images, instead of just SVG.  Also, provide visualizations of graphics themselves to help explain graphical structure (with layers).  This may be achieved by using the rbatik package: http://code.google.com/p/rbatik/. (June 2010)
  * Version 1.0 - Provide some basic animations and interactivity. (September 2010)
  * Version 2.0 - Include Google API.

# Current Status #

I have placed a pre-Alpha release on CRAN.

I'm looking for collaborators on this project.  Are you a strong developer who's passionate about R and graphics?  Send me a note (shane.conway at gmail dot com) and let's build a simple yet powerful R web visualization package.

# Examples #

## High Level ##

The S3 `plot.webvis` function is the most basic high-level function in the package.  See each function help file for more examples.

This command `plot.webvis(x=10*rnorm(20), y=10*rnorm(20), width=500, height=300, type="dot")` produces the following image (as javascript).

![http://i43.tinypic.com/2zxmgdf.gif](http://i43.tinypic.com/2zxmgdf.gif)