# 3Dscene2Dimage
EC601 Placement Exam Demonstrations
Zachary Halvorson
August 29, 2020

In researching and experimenting with various 3D reconstruction programs I tested Alicevision Meshroom for static object reconstruction, WebODM and OpenHeritage for aerial photogrammetry, and a free-trial of professional software from GreenValley International (LiDAR360, LiMapper, LiPowerline)

### Static Objects

I selected two objects; an antique lever press and an antique Mickey Mouse figurine to explore the challenges with recontructing different objects. The antique level press has a matte surface with some texture form old green paint, with some difficult geometries due to shadows and smooth surfaces lacking in texture. The Mickey Mouse figurine is glossy and was extremely reflective and had many glares apparent on the surface while imaging.

The results of these reconstructions can be found within the sub-folders for each object, with varying results. The lever was generally reconstructed well, although the main central piston appears to be missing, likely due to shadows and a smooth texture on that part, lacking in any available features that could be detected accross multiple angles. Similarly the smooth, dark rod connecting the green handle was poorly reconstructed, likely due to the same reasons as the center piston. The Mickey Mouse figure faired much worse, with a majority of the images being ignored in the process. Analyzing these now, I should have taken these images much closer to the object, so as to fill more of the field of view with the object of interest, and less of the background. Some techniques to improve these reconstructions would mostly focus on improving the quality of the images, through more diffuse lighting, as well as possible spray painting texture onto the objects with light coats of black and white over a gray basecoat to provide features to match accross the various views.

### WebODM and OpenHeritage

First I downloaded various datasets from OpenHeritage on Mesa Verde National Park, as well as one dataset on Pompeii, Italy (citations at end of README). I also downloaded a test dataset from WebODM itself.


### GreenValley Interational



### Data Sources

CyArk 2018: Mesa Verde National Park- Balcony House - LiDAR - Terrestrial , Photogrammetry . Collected by CyArk . Distrubuted by Open Heritage. https://doi.org/10.26301/az9d-mx47

2020: Fire Temple - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/e22j-4c22

2020: Square Tower House - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/cbtd-5b18

2020: Spruce Tree House - Mesa Verde National Park - LiDAR - Terrestrial . Collected by CyArk , Texas Tech University , University of California at Berkeley , INSIGHT . Distrubuted by Open Heritage. https://doi.org/10.26301/5vwp-yh91

CyArk 2018: Pompeii - LiDAR - Terrestrial . Collected by DIAPReM University of Ferrara . Distrubuted by Open Heritage. https://doi.org/10.26301/88jt-yz94

2020: Kastro Apalirou - LiDAR - Terrestrial . Collected by CyArk . Distributed by Open Heritage 3D. https://doi.org/10.26301/d998-rd62

https://github.com/OpenDroneMap/odm_data_waterbury.git
