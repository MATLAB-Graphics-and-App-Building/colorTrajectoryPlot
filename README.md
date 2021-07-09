# Colored Trajectory Plot

Version: 1.0

This chart creates a multi-color line based on a 2D trajectory with
corresponding color data.

## Syntax
* `colorTrajectoryPlot(x,y)` create a multi-color line plot following the 2D path specified by the coordinates x and y using the index of each coordinate to determine the color of the line. x and y must be numeric vectors of equal length.
* `colorTrajectoryPlot(x,y,c)` create a multi-color line plot following the 2D path specified by the coordinates x and y using values from c to determine the color of the line at each coordinate. x, y, and c must be numeric vectors of equal length.
* `colorTrajectoryPlot()` create a multi-color line plot using only name-value pairs.
* `colorTrajectoryPlot(___,Name,Value)` specifies additional options for the multi-color line plot using one or more name-value pair arguments. Specify the options after all other input arguments.
* `colorTrajectoryPlot(parent,___)` creates the multi-color line plot in the specified parent.
* `h = colorTrajectoryPlot(___)` returns the colorTrajectoryPlot object. Use h to modify properties of the plot after creating it.

## Name-Value Pair Arguments/Properties
* `XData` (n x 1 numeric vector) x-coordinates of the trajectory.
* `YData` (n x 1 numeric vector) y-coordintaes of the trajectory.
* `ColorData` (n x 1 numeric vector) data used to determine the color of the line.
* `Colormap` (m x 3 matrix of RGB triplets) colormap used to convert `ColorData` into colors.
* `ColorLimits` (1 x 2 numeric vector) limits used to convert `ColorData` into colors.
* `ColorLimitsMode` (`'auto'` or '`manual'`) mode for the color limits.
* `ColorbarVisible` (scalar `matlab.lang.OnOffSwitchState`) display the colorbar or not.
* `LineWidth` (scalar positive double) line width of the trajectory.
* `TitleText` (n x 1 string vector) title of the plot.
* `SubtitleText` (n x 1 string vector) subtitle of the plot.
* `ColorbarLabel` (n x 1 string vector) label on the colorbar.

## Example
Create a multi-color trajectory plot using x, y, and color data generated by the helper script `randomWalk`.
```
[x,y,c] = randomWalk;
c = colorTrajectoryPlot(x,y,c);
c.ColorbarLabel = "Firing Rate (Hz)";
colormap(hot(256))
```
