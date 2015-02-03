# README
# Project def
This project is a [proof of concept (POC)](http://en.wikipedia.org/wiki/Proof_of_concept). This project builds up a testing framework in matlab as a prileminary study for classifying different types of wood for barrel construction using an image retraible scheme:
1. Each sample corresponds to a single image that is described with a set of features
2. Classify this sample to determine the wood class in the picture

## Objectives
The project has two main objectives: 
* determine if its possible to differenciate between wood types.
* the framework should allow to explore the following items without need of recoding. So that if the project moves forward, the framework can be used to take a decission in which is the optimal system configuration. 
  * features
  * feature-configurations
  * classification strategies
  * classifier configurations


## Code structure
```
.# here is some code for specific tasks and dirty coding
|____histogramsSignature.m
|____dummyCode.m
|____meeting.m
|
|____datasets
| |# Here are placed the datasets used to experiment with.
| |# those datasets are nothing but links to images which
| |# are located within the images folder. There's a script
| |# to generate those randomized datasets. Bare that the
| |# class subfolders are needed.
| |
| |____1004BalancedRandomDataset
| | |____F
| | |____M
| | |____GG
| | |____TF
| |____relinkImages.sh
|
|____outputFigures
| |# folder cotaining the image results.
| |# This folder should remain empty in the remote repo in
| |# in exception of specific results communication which should
| |# be manually added to the repo in specific branches
|
|____images
| |# This folder contain images adquisitions and manipulations.
| |
| |____1004
| | |# Those are the imadges aquired 10/04/2014 from the second
| | |# set of samples available.
| | |
| | |____1M009BX.png
| | |__   ...
| | |____1M002BX.png
| | 
| |____1004Crop
| | |# Pre-processed images from 1004 image dataset.
| | |# Some scripts to generate images for the report can be
| | |# also found here. (Maybe they should be realocated)
| | |
| | |____imAdjust
| | | |____1M009BX.png
| | | |__   ...
| | | |____1M002BX.png
| | |____histEq
| | | |____1M009BX.png
| | | |__   ...
| | | |____1M002BX.png
| | |____generateWaveLetImages.m
| | |____generateAllwaveletImages.m
| | |____wavelet_1TF001_04.png
|
|____patternRecognitionApproach
| |# Thats the approach that we are using to classify wood samples
| |
| |____woodtest2.m
| |
| |____code
| | |# Here are the core functions
| | |
| | |____checkCalculation.m
| | |____calcGLCMStatistics.m
| | |____woodTestConfigure2.m
| | |____woodTestGenerateDescriptors.m
| | |____calcGLCM.m
| | |____calcWaveletTransform.m
| | |____woodTestClassificationTest.m
| | |____getRelativePath.m
| | |____waveletFeatures.m
| | |____featureDescription2struct.m
| | |____woodTestReportResults.m
| | |____calcWaveletEnergy.m
| | |____woodTestEnsureFeatures.m
| | |____adaptivethreshold
| |
| |____calculations
| | |# This folder contains calculations (so, keep it local)
| |
| |__ Dependencies
| | |# Please change your own path for dataset.
| | |# Add allcomb.m to path __ Ecternal libraray
| | |# Add DataHash.m to path__ External Library
| | |# Add EnsureDir.m to path and external library
| | |# Include Vlfeat library
```
