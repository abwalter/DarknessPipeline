# DarknessPipeline
Data reduction pipeline for DARKNESS, an MKID IFU for high contrast imaging

Installation
============

Install anaconda with python 3.6.  You will also need the packages pyintervals, astropy, pytables

IMPORTANT: FIXING PYQT4 BACKEND PROBLEMS
Upon re-installing python, the Qt backend is automatically set to PySide, which breaks Matt’s array pop-up gui (and possibly other GUIs that have not been tested yet). To fix this, the matplotlib rcParams file can be permanently edited to make PyQt4 your backend. Do the following. (instructions borrowed from matplotlib site: http://matplotlib.org/users/customizing.html#the-matplotlibrc-file)
 
To find your rcParams file, try:

ipython> import matplotlib

ipython> matplotlib.matplotlib_fname()

'/home/foo/.config/matplotlib/matplotlibrc'
 
Then find the line in your rc file that looks like:

#backend.qt4 : PyQt4        # PyQt4 | PySide
 
And make sure it is uncommented and set to PyQt4. With Canopy’s default install it will likely be PySide.


Pipeline Quick Start Guide
==========================

Selecting the .bin files you want to work with
______________________________________________



Creating HDF5 files from the .bin files
_______________________________________



Wavelength Calibrating
______________________



Flatfielding
____________



Creating Image Cubes
____________________



Making Speckle Statistics Maps
______________________________
