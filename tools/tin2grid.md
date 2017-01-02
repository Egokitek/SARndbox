# tin2grid

Compile in terminal shell to create a `tin2grid` executable which converts an _Arc ASCII TIN_ file to the Sandbox “grid” format:

`g++ -std=c++11 tin2grid.cpp -o tin2grid`

To get an Arc ASCII Grid format TIN file to work with:

1. Open a browser and go to http://OpenTopography.org
2. Click “Data” in the menus at the top and choose “Lidar Point Cloud”.
3. Select a dataset from the list. The Airborne Lidar sets work nicely.
4. Use the map to zoom in on a relatively small area.
  * The area where the LiDAR data is available will be highlighted in red.
  * Zoom in on a small set of features.
5. Click the “Select a Region” button, then drag a rectangle to select an area.
6. When your rectangle is complete, look in the green highlighted area of the web page below the map. It will show you how many points are in the data for the area you selected. (If you’re using the site as a “guest” you will be limited to 50 million points of data per request. Aim for about 5 million points or less at first).
7. In the “Choose Return Classification” section, turn off “Unclassified”. This will reduce the points somewhat.
8. In the “Point Cloud Data Download” section, select “Point cloud data in ASCII format”. (This selection is not really important, but one of the selections must be chosen. Only the TIN data will be used).
9. In the “DEM Generation (Streaming TIN. section, leave “Calculate TIN” on, and select “Arc ASCII Grid” format in the “Grid Format” menu.
10. Enter a name for the “Job Title” (it only has to be meaningful to you., a description, and your email address.
  * These things are required so that you can get an email with links to download the data if it takes a long time to process. Turning off the “Calculate TIN” feature makes it pretty quick though, like a couple minutes in my tests.
11. Click the Submit button and wait for the process to finish.
12. You need to download the “DEM Results” that will a file named `output.tin.tar.gz`.
  * If you download on a Windows machine, you will need 7-Zip or something equivalent to open GZIP archive, and the TAR file within.
  * Copy the file to your Linux machine where you run the AR Sandbox.
  * Extract the file named “output.tin.asc” and rename it to something meaningful to you.
  * Run the tin2Grid utility to convert this to a “grid” file that the AR Sandbox software can read.
  * Invocation is: `tin2grid <inputfile> <outputfile>`
  
Hope this is helpful to you.

S. Harned

_Adapted from https://arsandbox.ucdavis.edu/forums/topic/terrian-model/#post-102866_
