## Google_Vision_API

To enable the building of a completely automated image processing pipeline, we have included a template for using the Google Vision API to first determine if flood waters are present, and then to determine which of the existing models is better suited to determine water depth (people present? trucks present?).

The google vision api was adapted form this github repository.

https://github.com/cemsaz/google-vision-api-multi-thread

The image folder in the google_vision_api folder must contain those images that are needed to be run through Google Vision.

Start with the **01_Google_Vision_API.ipynb** notebook.  A google API key must be entered on line 4 for the spreadsheet to run. If you wish to run the code, you will need to provide your own Google API key.  The sheet will import the photos from the images file and run those through google vision.

The sheet should run with the packages previously installed with the exception of google cloud vision. Use:

pip install google-cloud-vision

The **01_Google_Vision_API.ipynb** notebook will export data to the labels.csv sheet in the output folder.  

After the labels are exported, open the **02_Parse_Image_Labels.ipynb** notebook. This notebook imports the data from the labels.csv and splits the data into separate dataframes based on the types of labels we are running through the various models.

These dataframes tell the user which images should be run through which model.

Our current model does not finalize this pipeline of taking images from google vision and run them in our model.  It currently stops at splitting them up into different dataframes.  A next step would be to take the images from the api and export them to folders to be used in modeling.
