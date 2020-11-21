# Seaborn Library

## What is seaborn?
Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

## How it works?
Built on top of matplotlib and tightly integrated with the PyData stack, including support for numpy and pandas data structures and statistical routines from scipy and statsmodels.

Built on top of matplotlib and tightly integrates with Pydata
High level, easy-to-use abstractions for common use cases

## seaborn cheatsheet
https://python-graph-gallery.com/cheat-sheets/

## seaborn documentation
https://seaborn.pydata.org/

### The basic steps to creating plots with Seaborn are:
 1. Prepare some data (importing the data)
 2. Control figure aesthetics (seaborn styles, context functions, colour palette)
 3. Plot with Seaborn
 4. Further customize your plot

## Plot with Seaborn
### Axis Grids: 
 * sns.FacetGrid - subplot for plotting conditional relationship
 * sns.factorplot - draw a categorical plot onto a Facetgrid
 * sns.lmplot - plot data and regression model fits across a FacetGrid
 * sns.pairgrid - subplot grid for plotting pairwise relationship
 * sns.pairplot - plot pairwise bivariate distributions
 * sns.jointgrid - grid for birvariate plot with marginal univariate plots
 * sns.jointplot - plot bivariate distribution
 
### Regression Plots:
 * sns.regplot - plot data and a linear regression model fit

### Distribution Plots
 * sns.displot - plot univariate distribution
 
### Matrix Plots:
 * sns.heapmap - heatmap
 
### Categorical Plots:
 * sns.stripplot - scatterplot with one categorical variable
 * sns.swarmplot - categorical scatterplot with non-overlapping points
 * sns.contplot - shows count of observations
 * sns.barplot - Show point estimates and confidence intervals with scatterplot glyphs
 * sns.countplot - show count of observations
 * sns.pointplot - shows point estimates and confidence intervats as rectangular bars
 * sns.boxplot - boxplot / boxplot with wide-form data
 * sns.volionplot - violin plot
 
## Plot
 * plt.title("Add plot title")
 * plt.ylabel("adjust the label of the y-axis")
 * plt.xlabel("adjust the label of the x-axis")
 * plt.ylim(0,100) - adjust the label of the y-limit
 * plt.xlim(0,10) - adjust the label of the x-limit
 * plt.tight_layout() - ajdjust subplot param
 * plt.show() - show the plot
 * plt.savefig("save-the-plot-as-figure.png")
 * plt.savefig("figure.png",transparent = True)
 * plt.cla() - clear an axis
 * plt.clf() - clear an entire figure
 * plt.close() - close a window
