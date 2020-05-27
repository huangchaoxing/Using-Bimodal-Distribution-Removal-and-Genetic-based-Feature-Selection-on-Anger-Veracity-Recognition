# Using-Bimodal-Distribution-Removal-and-Genetic-based-Feature-Selection-on-Anger-Veracity-Recognition
# **Readme**

# Prerequisite 

Pytorch 1.0

Python 3.x (with Anaconda package)

Windows 10 environment

I have transformed the original dataset into a csv file by using online converter.

I have also included the train and test split data as npy array files.

# Guidence for version-1 dataset

Most of the code file has almost identical code but with little difference in the plot code. I separate them into different files for convenience.

**Baseline experiment:**

Use pre\_bdr.py, set _bdr_ and _early\_stop_ as zero. You can change the activation function type in the model class. You can also assign different hidden unit number to _hidden\_size_

**BDR error function experiment:**

Use the bdr\_err.py, you need to go to line 123-line 130 to comment/uncomment different choice of error. You will see the plotting then.



**BDR hyperparameter experiment:**

Go back to pre\_bdr.py, set _bdr_ and _early\_stop_ as 1. Assign different value to _alpha_ and _stop\_thresh._

**BDR curve comparison:**

Go to bdr\_curve.py. First comment the plot block:&quot;PLOT ACCURACY CURVE OF BDR AND NORMAL&quot;. Set _bdr_ and _early\_stop_ as zero to run the baseline. Then uncomment the plot block and set _bdr_ and _early\_stop_ as 1, run the BDR case and you will get the final plot.

**BDR artificial outlier experiment:**

Go back to pre\_bdr.py, set _bdr_ and _early\_stop_ as 1, assign different value to _npattern_

**BDR as pre-processing:**

Run bdr\_split.py, you will get the new dataset. Then go back to pre\_bdr.py to run the baseline again. Do not forget to change the data file name in pre\_bdr.py to the new one.
# Guidence for version-2 dataset
**Two-stream model**  
Run time_train.py to see the effect of two-stream model. When dealing with the time-differences input, the input of one of the stream need to be modified to one neurons less than the other stream, because time-differences is one frame less.  
**GA algorithm**  
Run ea_nn.py to see the effect. You can play around with the hyperparameters. 
