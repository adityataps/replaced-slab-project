# Instructions on use
1. To collect files from UCPRC dataset, run data collection script from the Data folder
   1. Files will be downloaded to Data/collected
   2. Alternatively, UCPRC data can be found at https://gatech.box.com/s/o92vej8sd2uhmxoems58ijf4tu2oqsbz
      1. Extract and copy the files in the zip file to Data/downloaded
2. Run feature extraction script
   1. Specify whether code will be run on collected or downloaded data
   2. Alternatively, CSV files have been provided. Use caution - running feature extraction code will overwrite existing CSV files
3. When CSV files have been generated, run Models.ipynb which will read in respective CSV files and train models
___

# Folder Structure
```angular2html
UCPRC
│   README.md
│
└───Data                            # After unzipping and moving from GDOT_Data zip file
│   │   data_collection.ipynb       # Notebook for aggregating data from UCPRC Box drive using UC Davis's file data (CSV file)
│   │   ucdavis-data.csv            # UC Davis's file data including Box filepaths and replaced/unreplaced ground truth annotations
│   └───collected                   # Images that are downloaded from the data_collection notebook script
│   └───downloaded                  # Images that are copied from extracted zip file from GaTech Box drive
│   
└───Feature Extraction
│   │   Processing.ipynb            # Feature extraction on Slab images in Data/collected or Data/downloaded
│   │   .csv files                  # CSV files for each feature set and configuration
│
└───Models
│   │   Models.ipynb                # Notebook to run models on CSV files from Feature Extraction folder
```

___
##### Note
Length and Length_2 csv files represent the collected length using the GDOT processing code and the specified slab length as denoted in UCPRC CSV data file, respectively. 