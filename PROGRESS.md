# Progress Towards Completing Project 
#### `Paths Taken - Organization - Goals`

#### Goal: *To identify residential and commercial buildings, and determine whether they are damaged. We specifically focus on San Juan, PR immediately following hurricane Maria in 2017.* 

## Part 1: Import and Organize Data: 
##### There are two primary satellite images $(~ 1 \space GB)$ of before and after the hurricane event. EY provides these $2$ images of $1$ large region in San Juan, PR. 
##### Goal: Create python code that seamlessly completes the following: 
1. Import the large images 
2. Take these images, split them into tiles of a predetermined size $(~ 512 \space x \space 512 \space \text{pixels})$ 
3. Ensure a one-to-one correspondence of pre and post event images. 
	- e.g. pre_tile_4.tif and post_tile_4.tif span over the exact same geographic coordinates 
	- Create a function that generates random but equivalent pre and post images. This will provide us the ability to sample tiles of varying geographic features. 
1. Convert images from TIFF to JPEG format 
2. Square images with respect to coordinate positions of the image to ensure the before and after image sets are **exactly one-to-one** 

## Part 2: Expand Training Data 
- These alternate open-source online datasets can assist in model training. For example, bounding boxes or segmentation features already created by similar projects could aid our models.  
### Rio de Janeiro Dataset - Spacenet 
> [Link to data imported from AWS S3 Bucket](https://spacenet.ai/rio-de-janeiro/) 
- This dataset consists of already generated tiles $[(200 \space m \space x \space 200)$, $(3.1 \space GB), (\text{year } 2018)]$ of the coastal city of Rio De Janeiro, Brazil. The regions geographic features, consisting of dense urban streets situated among steep forested mountain terrain perfectly matches that of San Juan, PR. A folder of polygons in geojson format identify all buildings in the Rio region is also included. 
- This dataset is simple (single label)  
- We converted the geojson dataset to the annotation formats of COCO, YOLO, MASK, and Pixel Coordinates to [allow for the convenient training of various potential ML models](https://drive.google.com/drive/folders/1GoOg6lXnZKLkdUBzkEeXa4DhqUVbEqw6?usp=sharing).
- Also converted to regular bounding boxes 
### EY Open Data Science Projects  - Other participants publicly posted labels on Roboflow 
- Since many there are many other people completing the same project whose instructions were originally set by EY, there are many recently created annotation datasets of San Juan online. Roboflow is free resource that allows for quick annotation of features, and simultaneously posts these annotations online for the public to see. 
- By identifying high quality and unique annotation datasets of San Juan posted on Roboflow, we can quickly expand our training data. 
- By taking these images and completing image augmentation, the data can be grown even further. 

> Add information about this process here 

### Priming Dataset with Feature Recognition Using Segment Anything 
Resource: https://samgeo.gishub.org/examples/satellite/ 
> Does anyone remember what this is called again? I've already asked our teacher like 3 times, I just forget. 
- Create annotations that will allow our ML model to better parse image features. These polygon annotations provide "context" to how ground truth is related to other general features in the image. 
- Example: Four long, $90$ degree polygons forming a cross +. This shape feature will train our neural network to recognize standard + intersections as likely residential streets. 
	- The neural network doesn't need to know what the polygons are. It's task is to only identify correlations between shapes on the image and ground truths (building / building type annotations). 

> Add information about this process here 
## Part 3: Create Functionality for the Quick Visualization of Images and Annotations 
- Code that goes in and visualizes bounding boxes and polygons over tile images. 

> Add information here as progress is made 
## Part 4: Model Creation 
- There are many routes and iterations that can be completed in this process. 
- Model Type: YOLO, SegmentAnything, Detectron2 
	- Currently working with YOLOV8 
#### Potential Iterations in Model Creation: 
- Consider what data we train the model on first, and subsequently train the model on. 
- Do we train the model on one massive dataset? 
- Do we use bounding boxes or polygons? Is it a detect or segment model? 
	- We start with higher complexity "segmentation data" and then re-train the same model on bounding boxes 
- Need code to be able to quickly convert data into to the format that is needed for the model. 

> Add information here as progress is made  
###### Select a Model: 
- By selecting a model, like YOLOv8, our code can be created to always serve this model type. For example, the YOLOv8 model must be placed into the following format prior to training: 
	- `dataset`
	    - `dataset.yaml`
	    - `images`
	        - `train`
	        - `val`
	    - `labels`
	        - `train`
	        - `val` 

 > Add information here as progress is made 
## Part 5: Model Testing: 

> Add information here as progress is made 
