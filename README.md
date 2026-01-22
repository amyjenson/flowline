# flowline
Simple set of script to get flow line on a glacier using an annual mosaic of velocity. 

1. Download a velocity mosaic from NSIDC (netcdf). You can do this through the the NSIDC webpage (https://nsidc.org/data/data-access-tool/NSIDC-0776/versions/2) or by running the python script . If you run 'nsidc-download_NSIDC-0776.002_2026-01-22.py', you will get a set velocity maps of Sit' Tlien (Hubbard Glacier) for a few different years.  

2. Next you can run either flowlines.py to get a single flow line if you know the coordinate of where you would like your flow line to start. 

This script reads in the velocity map to get the vx and vy. It then solves an ODE to determine the positions along flow using the velocity field and the initial point you choose. 

3. If you are unsure and want to look at many options of where to start, you can read in a set of starting coordinates and run 'multiple_flowlines.py'. I have a file I created in QGIS called, 'points_across_glacier.csv' that I use for that. 

4. You can plot your flow line on a map like I did on Sit Tlien to see which one you like best. ('map_flowlines.py'). 