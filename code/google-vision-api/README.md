## Google_Vision_API

To enable the building of a completely automated image processing pipeline, we have included a template for using the Google Vision API to first determine if flood waters are present, and then to determine which of the exiting models is better suited to determine water depth (people present? trucks present?).

The google vision api was adapted form this github repository.

https://github.com/cemsaz/google-vision-api-multi-thread

The image folder must contain those images that are needed to run through Google Vision.

Start with the Google_Vision_API notebook.  A google API key must be entered on line 4 for the spreadsheet to run. If you wish to run the code, you will need to provide your own Google API key.  The sheet will import the photos from the images file and run those through google vision.

The sheet should run with the packages previously installed with the exception of google cloud vision. Use:

pip install google-cloud-vision

The Google_Vision_API notebook will export data to the labels.csv sheet in the output folder.  

## Parse_Image_Labels

The Parse_Image_Labels notebook imports the data from the labels.csv. and splits the data into separate dataframes.
