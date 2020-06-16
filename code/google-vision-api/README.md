# Google_Vision_API

The google vision api was adapted form this github repository.
https://github.com/cemsaz/google-vision-api-multi-thread

The image folder must contain those images that are needed to run through Google Vision.

Start with the Google_Vision_API notebook.  A google API key must be entered on line 4 for the spreadsheet to run.

The sheet should run with the packages previously installed with the exception of google cloud vision. Use:

pip install google-cloud-vision

The Google_Vision_API notebook will export data to the labels.csv sheet in the output folder.  

# Parse_Image_Labels

The Parse_Image_Labels notebook imports the data from the lebels.csv. and splits the data into separate dataframes.
