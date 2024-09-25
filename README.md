# replaced-slab-detection
Fall 2021 - Spring 2022 Project on Replaced Slab Detection
___
Instructions: 

1. (Optional) Download GDOT and UCPRC Data (further instructions found in GDOT and UCPRC folders)
   1. GDOT: https://gatech.box.com/s/zi4tqj1ttjim7abt8tkxsqr8uo3nyc5z
   2. UCPRC: https://gatech.box.com/s/o92vej8sd2uhmxoems58ijf4tu2oqsbz
2. (Optional) for raw LCMS range/intensity images, follow instructions for running `crop-slab.ipynb` in the GDOT folder
3. Run `Processing.ipynb` for GDOT and UCPRC data in respective Feature Extraction folders; or use existing CSV files
4. Run `Models.ipynb` on CSV files for respective GDOT and UCPRC datasets
___
CSV formats:
- `master_df`: slab label/filepath and ground truth
- `length_df`/`length_df_2`: length data for each slab, either collected using processing code or gathered from UCPRC data
- `lbp_<config>`/`lbp_<config>_10`: LBP data for each configuration, either using the maximum number of bins or 10 bins
  - for `ror` LBP, bins with zero values are culled
- `color_<bin count>` / `smoothed_<bin count>`: grayscale intensity histogram values with the specified number of bins. 
`smoothed` corresponds to grayscale intensity distribution on Gaussian blurred images