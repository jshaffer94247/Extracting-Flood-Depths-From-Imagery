Technical Users Guide
---------------------------

### Download the data

 1. Clone this repo to your computer and cd into the top of the folder    
 
 `cd Extracting-Flood-Depths-From-Imagery`
 
 1. Create a virtual environment called 'flood_depths' with     
 
  `conda env create -f environment.yml`

 1. Activate your environment with 

  `conda activate flood_depths`

### Augment the training data

One of the challenges with this project has been acquiring sufficient training data. In lieu of delaying the project, we have opted to augment the data by creating horizontally flipped, cropped, black & white, and slightly rotated versions of the original data. 
Advantages of this approach include   
 - Less space is required in the repo
 - These images can be quickly regenerated with a tool we've provided
 - Users can add images to the collection and augment those, too

This also means that you can retarget the model to train on an expanded flood depth dataset or even another dataset of your own choosing, and you can then also augment your own images.

 1. Start jupyter-notebook from the flood_depths conda environment
 
   `jupyter-notebook`
   
 1. Open the notebook and follow the instructions to expand the dataset of your choice
 
    03_Image_Augmentation.ipynb. **TODO: update name, add link**
 
### Build the model(s)

Our original plan was to include the finished model(s) in this repo, but file size is problematic (1.5G+). The same was true of the model weight files (512M). This leaves the option of building the model yourself. We have put in the hooks to save the model weight file after it is built, so you will be able to run the predictions notebook after building the model just once. If we are able to compress the weight file(s) and add it to the repo, we will do that later.

 1. Open a model file
 
    04_Flood_Depth_ModelTraining_Trucks.ipynb
    05_Flood_Depth_ModelTraining_People.ipynb
    **TODO: update names, add links**
    
 1. Run all
    Caution: the model may run for an hour or so depending on your computer's capabilities. The models were originally build on MacBook Pro computers with CPU-only support.
    
 1. Confirm that the model weights were saved as a *.h5 file
 
     Examples:
         `model_weights_trucks.h5`
 
### Predict on new images

To predict on new images, you will need to place the images into folders according to the structure the tools are expecting. A set of starter folders have been made called "user_images". We suggest that you run the prediction tools on those images first as this will be quick and will show you the pattern.

 1. Confirm that the model weight file was saved in the previous step
 1. Open the predictions notebook (name includes 'Prediction')
    06_Flood_Depth_Prediction_Trucks.ipynb
    07_Flood_Depth_Prediction_People.ipynb
    **TODO: update names, add links**
 1. Change the User Configurable Items if you needed
 1. Run all

Caution: Due to various resource constraints (time, people, training data), the results of this model are not suitable for making life-changing decisions. Using the model to explore machine learning, to making non-binding estimations of flood depths, or for entertainment (Can it predict the depth of the water a horse is standing in?) is acceptable and encouraged.

### Build an image processing pipeline

To enable the building of a completely automated image processing pipeline, we have included a template for using the Google Vision API to first determine if flood waters are present, and then to determine which of the exiting models is better suited to determine water depth (people present? trucks present?).

 1. ...**Clint: can you add a note on how to get an API key**
 1. ...and then whatever else you need to do