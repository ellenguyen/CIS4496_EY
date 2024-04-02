# Project Charter

## 1. Introduction
Natural disasters pose significant challenges to affected communities, requiring prompt and accurate damage assessment to direct resources effectively. Traditional assessment methods are often slow and resource-intensive. This project proposes a machine learning solution to improve the speed and accuracy of these assessments.

## 2. Problem Description:
The main challenge addressed by this project is the need for a quick and reliable method to assess infrastructure damaged by natural disasters. This capability is crucial for disaster response organizations, insurance companies, and government agencies. These entities operate within domains critically reliant on immediate and precise damage evaluation to expedite recovery, insurance claim processing, and optimize resource allocation. 

By leveraging machine learning to analyze satellite images, this initiative promises to enhance the speed and accuracy of damage evaluation. This approach not only ensures consistent, data-driven decision-making across the affected region but also provides insights for long-term planning and risk assessment, supporting the clients’ goals of ensuring public safety, managing financial risk, and aiding communities in disaster recovery.

## 3. Project Scope:
* Data Science solution: Develop a machine learning model to identify and detect “damaged” and “undamaged” coastal infrastructure (residential and commercial buildings), which have been impacted by natural calamities such as hurricanes, cyclones, etc.
* Objectives: Detect 4 different objects in a satellite image of a cyclone impacted area (Undamaged residential building, Damaged residential building, Undamaged commercial building, Damaged commercial building) using bounding boxes with various object detection models.
* Consumption: The model’s predictions will be integrated into the client’s processing system to prioritize areas for immediate response, resource allocation, and damage estimates.

## 4. Personnel:
* Team:
  * Project Lead: Will Schenk
  * Data Scientists: Mary Le, Elle Nguyen
* Client:
  * Business Contact: Dr. Stephen McNeil
  * Technology Consultant: Jovan Andjelkovic

## 5. Metrics:
* Qualitative Objectives: Improve accuracy and effectiveness in storm damage assessment.
* Quantifiable Metric: Reduce the time for initial damage assessment by 50%.
* Desired Improvement: Decrease the time taken for storm damage assessment by 50% compared to the current manual process.
* Baseline Value: The current time taken for storm damage assessment is 2 days.
* Measurement: Time taken for storm damage assessment before and after model optimization will be compared.

## 6. Plan:
* Phase 1: Data Collection and Preprocessing (2 weeks)

    This phase involves gathering high-resolution panchromatic satellite images given by EY Open Science Data Challenge Platform, including pre- and post-event images of affected areas, along with building footprints. The data is then preprocessed for analysis, which includes cleaning, feature extraction, footprint overlay, and ensuring compatibility between datasets.

* Phase 2: Annotation (2 weeks)

    Annotation phase involves manual annotating and a pre-trained model to automate the labeling process. 

* Phase 3: Model Development (2 weeks)

    The team employs a machine learning model to detect objects (Damaged residential buildings, Undamaged residential buildings, Damaged commercial buildings, and Undamaged commercial buildings)

* Phase 4: Model Evaluation and Improvement (3 weeks)

    The model’s accuracy and effectiveness are evaluated using a separate set of images. Refinements will be made to improve the model’s predictive capabilities. Anticipated areas of model improvement include: 
  * Create training data
  * Optimize class imbalance
  * Explore object detection algorithms
  * Leverage moderate resolution satellite data (Sentinel-1, Sentinet-2)
  * Optimize training approach
 
## 7. Architecture:
* Tools: 
  * The final deliverable to EY must be able to fully run on a 4 core 32 GB memory compute resource. This requirement will motivate our team to build a memory/computationally efficient model.
  * Access to Microsoft Planetary Hub, a Jupyter compute environment tailored for satellite image processing, is provided to our team by EY for the duration of the project. 

* Data analytics resources:
  * Labelme, Labelbox, etc. for annotation tools.
  * Geopositioning and Image Processing Libraries include GDAL, Rasterio, Ultralytics, and GeoPandas

* Data: 
  * Raw pre- and post-cyclone satellite images as TIFF (Tag Image File Format) files will be used for data training step.

![image](https://github.com/ellenguyen/CIS4496_EY/assets/93592445/be60dffc-0f69-4d98-91e0-da4ecd4cf881)
    Figure 1: A sample pre-event image with dark region clouds in RBG bands.

![image](https://github.com/ellenguyen/CIS4496_EY/assets/93592445/8fad7c5b-2f9f-4167-9cc2-6eae25614fc2)
    Figure 2: A sample post-event image with dark region clouds in RBG bands.

  * Results from the model detection from each of the validation images (class, confidence score, bounding box coordinates) are saved in a .txt file, which are later compressed into a single .zip file.
  * Other data sources, external, and data provided by EY such as the Landsat and Sentinel-2 satellite imagery, and building footprints.

  * // more to add

## 8. Communication:
* Meetings:
  * Two in-person weekly meetings to discuss progress and address any concerns with external mentors.
  * Dedicated internal communication channels on Discord and joint review sessions at key milestones (e.g., after model selection, before evaluation) with external mentors. 

* Workflow management:
  * Utilizing GitHub as the central platform for code management and documentation.
  * Kanban principles to improve productivity (To-do, In progress, Done)

![image](https://github.com/ellenguyen/CIS4496_EY/assets/93592445/a1ff2b87-afe5-4a46-bb19-2c025e556ed3)

* Contacts: 
  * Project Lead: Will Schenk
  * Business Contact: Dr. Stephen McNeil
