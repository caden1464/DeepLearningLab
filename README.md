#Temporal fMRI Denoising with Deep Learning Trained on Synthetic Data

## Problem Definition:
- Fmri is a 4d data where one axis is time. Normally, this data is used to figure out blood flow in our brain. This blood flow refers to hemodynamic response function(HRF).
- Since fmri has limited time to get one 3D data in 1 repertition time(TR), we only get noisy data under experimental conditions.
- This means we can't get a clean data as a label for deep learning model.
- Below picture is raw fmri data which shows too much noisy.(3D and temporal data each)

![image](https://github.com/caden1464/MILAB-project/assets/67831416/363eadfb-f867-4783-8412-3f184dd078fe)
![image](https://github.com/caden1464/MILAB-project/assets/67831416/d63078c5-2d56-4819-b375-7acd7029dbda)

## Suggestion:
- The purpose of this project is to denois
e the temporal fmri data using deep learning.
- I made 'sythetic HRF' as a label and 'sythetic HRF + noise' as a training data.
- In the first experiment, I used U-net as a backbone architecture.

## Experiment
### making synthetic data
![image](https://github.com/caden1464/MILAB-project/assets/67831416/d63078c5-2d56-4819-b375-7acd7029dbda)

### putting noise
![image](https://github.com/caden1464/MILAB-project/assets/67831416/d1aae536-fb0f-48f7-b206-516bef6a5023)

### Training (Green = label, Blue=Training data)
![image](https://github.com/caden1464/MILAB-project/assets/67831416/17719d8c-7b75-42f7-938f-80116185b087)


## Result
### GLM score map difference
- original one
  
![image](https://github.com/caden1464/MILAB-project/assets/67831416/4b112e3e-b259-4f06-bf30-c562cac3560e)

- denoised one
  
![image](https://github.com/caden1464/MILAB-project/assets/67831416/dab8f3c2-9cb5-4dad-bbad-3c9c4ca7e069)

### Temporally denoised results
- original one
![image](https://github.com/caden1464/MILAB-project/assets/67831416/d63078c5-2d56-4819-b375-7acd7029dbda)
- denoised one
![image](https://github.com/caden1464/MILAB-project/assets/67831416/493247a0-44ca-4925-b324-53323d23eb72)
