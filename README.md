#Temporal fMRI Denoising with Deep Learning Trained on Synthetic Data

# Problem Definition:
- Fmri is a 4d data where one axis is time. Normally, this data is used to figure out blood flow in our brain. This blood flow refers to hemodynamic response function(HRF).
- Since fmri has limited time to get one 3D data in 1 repertition time(TR), we only get noisy data under experimental conditions.
- This means we can't get a clean data as a label for deep learning model.
- 
# Suggestion:
- The purpose of this project is to denoise the temporal fmri data using deep learning.
- I made 'sythetic HRF' as a label and 'sythetic HRF + noise' as a training data.
- In the first experiment, I used U-net as a backbone architecture.
