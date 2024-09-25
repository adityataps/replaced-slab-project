# Instructions on use
1. Extract and copy files in the [GDOT_Data.zip](https://gatech.box.com/s/zi4tqj1ttjim7abt8tkxsqr8uo3nyc5z) file to the Data folder
2. If slabs need to be extracted, copy raw LCMS range/intensity image files to Data/Range or Data/Intensity
   1. Copy XML files to Data/XML
   2. Run crop-slab ipynb script
   3. Run feature extraction ipynb script using cropped slab images in Data folder
      1. Use caution - CSV files from previous feature extraction also made available; running feature extraction code will overwrite these files
3. Run Models.ipynb in the Models folder using CSV files from feature extraction folder
___
# Folder Structure
```angular2html
GDOT
│   README.md
│
└───Crop Slab
│   │   continuous_range.py         # Helper file for slab isolation
│   │   crop-slab.ipynb             # Script for isolating slabs from LCMS images 
│
└───Data                            # After unzipping and moving from GDOT_Data zip file
│   └───MP18-17/MP22/MP22-12_19
│       │   debug.txt               # Debugging output from slab isolation
│       │   slabs.csv               # Slab info
│       │   slabs_and_gts.csv       # Slab info and ground truth assignments 
│       │
│       └───Range                   # Original range (or intensity) image files
│       └───Slabs                   # Cropped slab images
│       └───XML                     # XML metadata from LCMS
│
└───Feature Extraction
│   │   Processing.ipynb            # Feature extraction on Slab images in Data folder
│   │   Slab Analysis.ipynb         # Qualitative survey of slab images and extracted features
│   │   .csv files                  # CSV files for each feature set and configuration
│
└───Models
│   │   Models.ipynb                # Notebook to run models on CSV files from Feature Extraction folder
```