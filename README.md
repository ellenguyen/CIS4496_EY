## CIS 4496 - Projects in Data Science - Spring 2024 - EY Project 
## [Progress on Course Project](https://github.com/ellenguyen/CIS4496_EY/blob/main/PROGRESS.md) 
## *Tropical Storm Damage Detection Model* 
## Mary Le, Will Schenk, & Elle Nguyen 
## [EY Launch Page](https://challenge.ey.com/challenges/tropical-cyclone-damage-assessment-lrrno2xm) 
## [Microsoft Planetary Hub](https://pccompute.westeurope.cloudapp.azure.com/compute/hub/spawn) 

### Resources: 
- https://github.com/satellite-image-deep-learning 
- https://github.com/labelmeai/labelme
- Segment Anything
- YOLOV8
- Spacenet 




# Data Description & Phase Details 
#### Objective: 
- Create a machine learning model to evaluate storm damage from satellite imagery 
- Compete in the [EY Open Science Data Challenge Program](https://challenge.ey.com/) 
**Detect four different objects** in a satellite image of a cyclone impacted area:
	- Undamaged residential building 
	- Damaged residential building 
	- Undamaged commercial building 
	- Damaged commercial building 

### Primary Data: 
- **Mandatory datasets:** *High-resolution* satellite images before and after tropical cyclone Maria 
- **Optional datasets:** 
	- *Moderate-resolution* satellite data: 
		- [Landsat and Sentinel-2 "Supplementary Notebooks 2024"](./given/Supplementary_Notebooks_2024)
	- [Buildins Footprint ROI](./given/Buildins%20Footprint%20ROI) - Identifies residential versus commercial  
	- [Other datasets provided by Microsoft](https://planetarycomputer.microsoft.com/catalog)
- *Other data permitted* 

### EY Recommendation: 
- Development environment: **Microsoft's Planetary Computer's Hub**). 
	
### EY Project Steps: 
- Understand example Jupyter notebook (sample model) which has a preliminary mAP (Mean Average Precision) score of 0.34. Pre- and post-cyclone satellite images of a site impacted by a tropical cyclone 
- Build the ML model 
- Detect objects in the [Submission Data (Validation Images)](./given/Submission%20data) 
	- Save Class, confidence score, and bounding box coordinates in a .txt file 
	- Save all .txt files in a single .zip file 
- [Upload the .zip file to get a score](https://challenge.ey.com/challenges/tropical-cyclone-damage-assessment-lrrno2xm)  

### Recommended Model Improvement Methods 
- Create training data 
- Optimize class imbalance 
- Explore object detection algorithms 
- Leverage moderate resolution satellite data (Sentinel-1, Sentinet-2) 
- Optimize training approach 

# Other EY Support 
**How to Get Started?**
-  [Tutorial video](https://challenge.ey.com/challenge-2024-phase-1-get-started/help) 
- Support: [datachallenge@ey.com](mailto:datachallenge@ey.com) 
- PDF Below 
#### [Guidance and Suggestions for Participants of the 2024 EY Open Science Data Challenge](https://challenge.ey.com/api/v1/storage/admin-files/2513955341204317-65bb9169868dc8fadbfc9728-2024%20EY%20Open%20Science%20Data%20Challenge%20Participant%20Guidance.pdf) 
##### Notes on the above pdf: 
##### Recommended References from EY: 
> 1. Transformation and Innovation in the Wake of Devastation – An Economic and Disaster Recovery https://prsciencetrust.org/
> 2. National Hurricane Center Tropical Cyclone Report, Hurricane Maria https://www.nhc.noaa.gov/data/tcr/AL152017_Maria.pdf
> 3. Jean et.al., Combining satellite imagery and machine learning to predict poverty. Science 353, 790–794, 2016.
> 4. Kim et.al., Disaster assessment using computer vision and satellite imagery: Applications in detecting water-related building damages, Front. Environ. Sci. 10:969758, 2022.
> 5. Polina Berezina and Desheng Liu, Hurricane damage assessment using coupled convolutional neural networks: a case study of hurricane Michael, Geomatics, Natural Hazards and Risk, 2022.
> 6. Quoc Dung Cao and Youngjun Choe, Post-Hurricane Damage Assessment Using Satellite Imagery and Geolocation Features, 2020. 

##### How we’ll be Evaluated 
> An **out-of-sample [validation dataset (Submission data)](./given/Submission%20data)** will be provided to participants. Your **submission/prediction (.zip file)**, will be **compared** with the ground **truth file and a metric mAP (Mean Average Precision)** will be generated to evaluate the performance of the model. 
> Refer to the sample notebook to understand the needed format of annotations 
#### Key Recommendations:  
- **Use small grids** e.g. found in sample notebook 
- Use more data (of course, including the pre-event imagery) 
- Annotate data 
#### Annotate Data: 
- Enables successful object detection 
- **Recommended Annotation Tools:** 
	- LabelMe 
	- VGG Image 
	- LabelImg 
- **Note:** Annotation tools $\to$ generate *image annotation files* unique to the application. 


