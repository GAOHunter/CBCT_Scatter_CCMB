# Example data 

## The Varian TrueBeam OBI gives the following data:

### CBCT scanning geometry is  given by the following files:

#### Scan.xml file 

- the distance between the source and detector (origin).
- number of pixels
- pixel size 
- total size of the detector
- Offset of Detector
- Offset of image from origin

#### Reconstruction.xml

- total size of the image 
- number of voxels  
- size of each voxel


#### Acquisitions folder

This folder stores the raw projection data, the data was store in \*.xim files. Each paitent have around 895 projections. 

ReadXim function will read the data out according to the xim file names and returns to int32 data. Also, the angle of each projection can also be acquired by reading the header info. 

TIGRE provide 2 methods to retirve the data from xim file:
 1. Using the MATLAB coding "ReadXim.m" function. The code is clear and easy to read, but slow.
 2. Using the C++ complied function "mexReadXim.mexw64". We can't see the code line by line, but this code is super fast!

It's easy to compare the result of these two code, usually, you should be comfort using the mexReadXim function.


#### Calibrations folder

This folder contains the blank scan.

#### Reconstructions folder

This folder contains the reconstructed image by using the Varian Reconstructor.