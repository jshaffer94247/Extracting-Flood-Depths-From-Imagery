
# Extracting Flood Depths From Imagery

## Problem Statement
---
Flooding is one the most common and most destructive forms of natural disaster.  Current flood detection and measurement systems lack accuracy and expedience to keep people out of danger.  We built a convuluted Neural Network that leverages uploaded personal photos to provide flood detection and depth measurement to expedite alerts and increase safety.

**From assignment** Problem Statement: Floods cause damage to infrastructure and homes. The depth of flood waters is a good indicator of the severity of damage. Floods are incredibly difficult to model, and while model outputs are useful to emergency managers, it is crucial to know the actual depth. Social media and news outlets often present pictures of floods. How can this imagery be used to estimate the depth of water in a given area?

## Executive Summary OR Abstract
---


## Data
---
https://docs.google.com/document/d/1p74Q2P8alsDMn7t_SStoAjlu6nj5iP8MUyruClTQPMs/edit?usp=sharing - Resource doc

## Image Processing
---

<img src="./assets/person_depth_chart.png" alt="drawing" width="400"/> <img src="./assets/truck_depth_chart.png" alt="drawing" width="400"/>


## Issues
---



## Future Improvements
---
Extract latitude and longitude from EXIF OR user input
Determine elevation based on location
Project flood level to surrounding area at simliar elevation




## Project Organization
---
```
|__ code
|   |__ 01_Google_Vision_API.ipnyb
|   |__ 02_Parse_Image_Labels.ipynb   
|   |__ 03_Image_Augmentation_Trucks.ipnyb
|   |__ 04_Flood_Depth_ModelTraining_Trucks.ipynb
|   |__ 05_Flood_Depth_Prediction_Trucks.ipynb
|   |__ 06_Image_Augmentation_People.ipynb
|   |__ 07_Flood_Depth_ModelTraining_People.ipnyb
|   |__ 08_Flood_Depth_Prediction_People.ipnyb
|   |__ output
|   |   |__ labels.csv
|   |__ README.md
|__ images (see file tree image below)
|__ Project_presentation.pdf
|__ environment.yml
|__ README.md
```

<img src="./assets/ImageFolderStructure.png" alt="drawing" width="900"/>