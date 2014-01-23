FigureData.py: 
==========

This program allows one to extract quantitative numbers from published 
figures that were not accompanied by tables with the data themselves.  

_Usage:_
```python
>>> import FigureData
>>> FigureData.go(figure_file='Brammer11_Fig7.png', output_file='myfigure.data')
```

The primary input `figure_file` is an image file of the figure (PNG, GIF, JPG).  
The script prompts for the user to mark points on the figure defining the plot regions.  

The steps are as follows:

1. Click two points on the x axis where you know the values from, e.g., the 
   axis labels.  After clicking the points in the plot window, type the _x_
   values of those coordinates on the command line and hit <ENTER>.
   
2. Same as 1) for two points on the _y_ axis.

3. Prompt to click on the lower-left and upper-right corners of the plot 
   window
   
4. After 3) you can then click as many points as you want on the figure.
   To finish, click in the small border outside of the plot window to 
   save the data to a file specified by the `output_file` keyword.
   
   The third column of the output file is a flag for marked data points 
   that fall outside of the defined plot window.
