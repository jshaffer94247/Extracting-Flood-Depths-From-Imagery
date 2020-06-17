
# Extracting Flood Depths From Imagery

## Problem Statement
---
Flooding is one the most common and most destructive forms of natural disaster.  Current flood detection and measurement systems lack accuracy and expedience to keep people out of danger.  We built a convuluted Neural Network that leverages uploaded personal photos to provide flood detection and depth measurement to expedite alerts and increase safety.

**From assignment** Problem Statement: Floods cause damage to infrastructure and homes. The depth of flood waters is a good indicator of the severity of damage. Floods are incredibly difficult to model, and while model outputs are useful to emergency managers, it is crucial to know the actual depth. Social media and news outlets often present pictures of floods. How can this imagery be used to estimate the depth of water in a given area?

## Executive Summary OR Abstract
---
Teaching a computer to detect water much less a water line is something that has troubled for researcher for years per the attached research library.  As a result, we chose to leverage the Google Vision AI to act as an image preprocessor that would identify prerequisite objects and flooding.  By verifying those conditions, we could train a convulutional neural network(cNN) using VGG16 to identify the level of submersion of those specific objects.  Based on the interpretation of that submersion level we could infer a relative depth of the flood water.

## Data
---
In order to train our neural network we required a large quantity and variety of flood images.  Several research projects had large libraries of training images for their respective model

## Image Processing
---

### Gooogle Vision AI

### VGG16 cNN

<img src="./assets/person_depth_chart.png" alt="drawing" width="400"/> <img src="./assets/truck_depth_chart.png" alt="drawing" width="400"/>

### Person Submersion Detection

### Truck Submersion

## Issues
---
1. People can swim
2. Shortage of training data
3. 


## Future Improvements
---
Extract latitude and longitude from EXIF OR user input
Determine elevation based on location
Project flood level to surrounding area at simliar elevation




## Project Organization
---
```
|__ code
|   |__ google-vision-api
|   |   |__ 01_Google_Vision_API.ipnyb
|   |   |__ 02_Parse_Image_Labels.ipynb
|   |   |__ README.md
|   |   |__ output
|   |   |   |__ labels.csv
|   |__ 03_Image_Augmentation_Trucks.ipnyb
|   |__ 04_Flood_Depth_ModelTraining_Trucks.ipynb
|   |__ 05_Flood_Depth_Prediction_Trucks.ipynb
|   |__ 06_Image_Augmentation_People.ipynb
|   |__ 07_Flood_Depth_ModelTraining_People.ipnyb
|   |__ 08_Flood_Depth_Prediction_People.ipnyb
|   |__ README.md
|__ images (see file tree image below)
|__ Project_presentation.pdf
|__ environment.yml
|__ flood_detection_resources_research_utilities.pdf
|__ README.md
```

<img src="./assets/ImageFolderStructure.png" alt="drawing" width="900"/>

<img src="./assets/image_test_dir_diagram.png" alt="drawing" width="900"/>
