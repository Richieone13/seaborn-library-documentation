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
 * [sns.FacetGrid](https://seaborn.pydata.org/generated/seaborn.FacetGrid.html) - subplot for plotting conditional relationship (this is very useful!), can use col_order, col_wrap=n
 * [sns.catplot](https://seaborn.pydata.org/generated/seaborn.catplot.html) - draw a categorical plot onto a Facetgrid, represent relationshop on a facet grid (in a way to represent the same relationshop with different conditions) it can be 3D, default is a point plot, can be kind="bar", "box", "swarn" 
 * [sns.lmplot](https://seaborn.pydata.org/generated/seaborn.lmplot.html) - plot data and regression model fits across a FacetGrid
 * [sns.pairgrid](https://seaborn.pydata.org/generated/seaborn.PairGrid.html) - subplot grid that allows to quickly summarize the different relationships with the different pairs of data - look at documentation
 * [sns.pairplot](https://seaborn.pydata.org/generated/seaborn.pairplot.html) - plot pairwise bivariate distributions
 * [sns.jointgrid](https://seaborn.pydata.org/generated/seaborn.JointGrid.html) - grid for birvariate plot with marginal univariate plots
 * [sns.jointplot](http://seaborn.pydata.org/generated/seaborn.jointplot.html) - plot bivariate distribution, this can be kind='hex' this can be Hexbin
 * [sns.kdeplot](https://seaborn.pydata.org/generated/seaborn.kdeplot.html) - plot univariate or bivariate distributions using kernel density estimation

### Regression Plots:
 * [sns.regplot](https://seaborn.pydata.org/generated/seaborn.regplot.html) - plot data and a linear regression model fit

### Distribution Plots
 * [sns.displot](https://seaborn.pydata.org/generated/seaborn.displot.html) - plot univariate distribution
 * [sns.histplot](https://seaborn.pydata.org/generated/seaborn.histplot.html) - plot univariate or bivariate histograms to show distributions of datasets
 
### Matrix Plots:
 * [sns.heapmap](https://seaborn.pydata.org/generated/seaborn.heatmap.html) - heatmap
 
### Categorical Plots:
 * [sns.countplot](https://seaborn.pydata.org/generated/seaborn.countplot.html) - shows count of observations
 * [sns.boxplot](https://seaborn.pydata.org/generated/seaborn.boxplot.html) - boxplot Q1/Q3 -/+  1.5 * interquartile range (IQR): 25th to the 75th percentile) outside is the outliers, boxplot with wide-form data this can be horiztonally displayed
 * [sns.volionplot](https://seaborn.pydata.org/generated/seaborn.violinplot.html) - violin plot (Curved are a KDE of all possible points, thickness is how common the point is at the value, probability density, whiskers distance 1.5 IQR, thickest is the mode of the data, customise into count, and combine into swarm plot)
 * [sns.stripplot](https://seaborn.pydata.org/generated/seaborn.stripplot.html) - scatterplot with one categorical variable
 * [sns.swarmplot](https://seaborn.pydata.org/generated/seaborn.swarmplot.html) - swarmplot an extension of stripplot without need to specify jitter = True, all points are definitely going to be visible, whereas jitter might hide points, categorical scatterplot with non-overlapping points
 * [sns.barplot](https://seaborn.pydata.org/generated/seaborn.barplot.html) - Show point estimates and confidence intervals with scatterplot glyphs (can represent 3 variables)
 * [sns.pointplot](https://seaborn.pydata.org/generated/seaborn.pointplot.html) - shows point estimates and confidence intervats as rectangular bars, they are connected

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

## FactetGrid
g=sns.FacetGrid(data, col='column_a', hue="column_b")

g.map(plt.scatter, "x axis title", "y axis title", alpha = 0.7)

g.add_legend()

g=sns.FacetGrid(data, row='column_a' col='column_b', hue="column_c")

___

g.map(sns.regplot, "x axis title", "y axis title", fit_reg=False) #remove regression

g.add_legend()

plt.ylim(0,1000)
