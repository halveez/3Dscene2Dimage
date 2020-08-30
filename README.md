# 3Dscene2Dimage
EC601 Placement Exam Demonstrations
Zachary Halvorson
August 30, 2020

In researching and experimenting with various 3D reconstruction programs I tested Alicevision Meshroom for static object reconstruction, WebODM and OpenHeritage for aerial photogrammetry, and a free-trial of professional software from GreenValley International (LiDAR360, LiMapper, LiPowerline) as well as Zephyr3D.

### Static Objects

I selected two objects; an antique lever press and an antique Mickey Mouse figurine to explore the challenges with recontructing different objects. The antique level press has a matte surface with some texture form old green paint, with some difficult geometries due to shadows and smooth surfaces lacking in texture. The Mickey Mouse figurine is glossy and was extremely reflective and had many glares apparent on the surface while imaging.

The results of these reconstructions can be found within the sub-folders for each object, with varying results. The lever was generally reconstructed well, although the main central piston appears to be missing, likely due to shadows and a smooth texture on that part, lacking in any available features that could be detected accross multiple angles. Similarly the smooth, dark rod connecting the green handle was poorly reconstructed, likely due to the same reasons as the center piston. The Mickey Mouse figure faired much worse, with a majority of the images being ignored in the process. Analyzing these now, I should have taken these images much closer to the object, so as to fill more of the field of view with the object of interest, and less of the background. Some techniques to improve these reconstructions would mostly focus on improving the quality of the images, through more diffuse lighting, as well as possible spray painting texture onto the objects with light coats of black and white over a gray basecoat to provide features to match accross the various views.

### WebODM and OpenHeritage

First I downloaded various datasets from OpenHeritage on Mesa Verde National Park, as well as one dataset on Pompeii, Italy (citations at end of README). I also downloaded a test dataset from WebODM itself. 

The files from OpenHeritage are .e57, which I opened in CloudCompare and was able to open and view the point cloud data, take approximate measurements, and export screenshots. Importing the Spruce Tree House LIDAR data, I was able to interact with the general structure of the dataset, which includes the caves and manmade structures inside, as well as many surrounding trees and some of the contour. Using CloudCompare, I was able to extract measurements of tripod lights that were present in the capture, as well as for a window and a room's floor to ceiling height. While the data may have been calibrated to a known scale, I was unable to confirm this, so the measurements do not have any unit or relevant scale. In order to map them to a known scale, if the tripod has known physicial measurements, this could be used to convert the additional measurements. However, there likely is corresponding scale calibration data included with the available data, something that could be explored in the future. 

Next, I loaded the Pompeii, Italy dataset in CloudCompare and took similar measurements with corresponding screenshots in the same folder. In fact, the high quality of the dataset allowed for detecting a gate at the base of a set of stairs beneath some columns to be detected, which were easily found in a corresponding google search and image from the following website - https://juliasalbum.com/things-to-do-in-pompeii/. I again took some measurements of the gate, the column heights, and the column diameter from an overhead view.

The test dataset from WebODM of aerial Waterbury photos was processed through both WebODM and Meshroom to compare results.

While proccessing the Waterbury dataset through WebODM, I downsized the images and first reconstructed a model using every other image in order to ensure I would have enough time for the submission. This reconstruction took approximately 90 minutes, and is generally accurate, but quite rough, and would be difficult to extract dimensionally accurate measurements from. The reconstruction can be found here: 

https://github.com/halveez/3Dscene2Dimage/tree/master/AerialTests/WebODM/EveryOtherPhoto/all/odm_texturing

I then ran the same setting including all of the images, and with an estimated run time of 10+ hours, I was not able to reconstruct the scene at a second, higher resolution before the deadline.

Similarly for Meshroom after running a default setting reconstruction with approximately 2000 photos, I was forced to restart the reconstruction after it stalled approximately 20 hours in. I attempted to shorten the processing time by downscaling the Depth Map and the final Texturing in order to attempt to complete the reconstruction in a timely manner. The reconstruction failed however in the texturing step, and I was unable to produce an interactive object with all of the photos at a high resolution.

For WebODM, I allocated 2.5GB (default) of RAM out of a total 16GB available on my device, and in future tests when not performing multiple concurrent reconstructions, I would likely allocate closer to 8GB RAM, or more.

While these processes were running, I ran the same set of photos through a free trial of Zephyr3D, and similarly used low resolution and "fast" settings to perform a reconstruction. It failed after producing a dense point cloud, results included in PDF form.

### GreenValley Interational

While I intended to describe some results from GreenValley software, as it is not open source I will not upload any results, and only experimented briefly with their tools.

However, the LIDAR sample data on their site was very enjoyable to interact with here - https://greenvalleyintl.com/sample-data/

### Data Sources

CyArk 2018: Mesa Verde National Park- Balcony House - LiDAR - Terrestrial , Photogrammetry . Collected by CyArk . Distrubuted by Open Heritage. https://doi.org/10.26301/az9d-mx47

2020: Fire Temple - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/e22j-4c22

2020: Square Tower House - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/cbtd-5b18

2020: Spruce Tree House - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/5vwp-yh91

CyArk 2018: Pompeii - LiDAR - Terrestrial . Collected by DIAPReM University of Ferrara . Distrubuted by Open Heritage. https://doi.org/10.26301/88jt-yz94

2020: Kastro Apalirou - LiDAR - Terrestrial . Collected by CyArk . Distributed by Open Heritage 3D. https://doi.org/10.26301/d998-rd62

https://github.com/OpenDroneMap/odm_data_waterbury.git
