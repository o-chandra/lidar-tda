# lidar-tda
Topological Data Analysis for Lidar Forestry Data
This repository contains Jupyter notebooks for performing topological data analysis (TDA) on LIDAR-generated point cloud data using the alpha complex class of the GUDHI library: https://gudhi.inria.fr/. 

The primary notebook is the "read-process-data" notebook. Here, you can:
 -read in .las or .laz files using laspy (https://laspy.readthedocs.io/en/latest/)
 -format the data in a numpy array so you can process it
 -construct simplicial complexes and store them in a data structure called a simplex tree
 -report various information about the resulting simplicial complexes
 -create and display persistance diagrams
 -generate betti numbers as a function of the alpha radius, plot this data and write it to a .cvs file
 
 The "visualization" notebook allows you to visualize the construction of the alpha complexes for different values of alpha_max, which is the alpha radius at which you stop the filtration.
 
 The "distance-metrics" notebook allows you to calculate the bottleneck distance for a given homology group, which gives you an idea of how "far apart" two persistence diagrams are. 
 
 The "k-means" notebook uses output from the "read-process-data" notebook (in particular, the betti numbers) and runs a k means clustering algorithm to cluster data by relative betti number.
 
 


 
 






This code was developed for a summer internship with the Center for Forest Disturbance Science in Athens, GA and was supported by funds from the NSF MSGI internship program: https://orise.orau.gov/nsf-msgi/, which is administered through the Oak Ridge Center for Education and Science (ORISE).
