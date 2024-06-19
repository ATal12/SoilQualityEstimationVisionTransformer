# Estimating Soil Quality from Satellite Images Using Vision Transformers.
This repository uses input satellite data on regions in Africa and a dataset from iSDA to train segformer models to map soil quality in a satellite image using segmentation.
##Context
This code accompanies a paper by Ayush Talukder submitted to PGHR about using Vision Transformers in tandem with satellite imaging to measure and map soil degradation. 
**Paper title: Soil Degradation and Its Effects on Human Health: How AI Can Help Detect Estimate Global Soil Quality** 

## Instructions to Run
This is a Python notebook that installs the required libraries and trains segformer models for soil quality analysis in a satellite image, outputting examples for the user to see the accuracy of the models.

If the code has not been run once, run all sections to train the model and import the packages.

To try on your own patches, you can just run the code segment after the one that conducts model fine-tuning.

### Code Info
Uses PyTorch for model fine-tuning, with Adam optimizer with gradient descent.

Input data consists of images of 10 African regions around 277x277km area each from Sentinel-2 (shortwave infrared bands), Landsat-7 (shortwave infrared bands), and MODIS (land surface temperature readings).

Trains on a dataset from iSDAsoil at 30m resolution and measures soil quality using the FCC-4 system of measurement and classes.

Uses garbage collector package to remove data from RAM when it is not needed and reduce computing constraints

### Models Used
The pretrained SegFormers used were the MiT-b0, MiT-b3, and MiT-b5 models. Model sizes range from the smallest MiT-b0 with 3.8M parameters, to the largest MiT-b5 with 82M parameters.
