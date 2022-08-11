# Project_2
Project 2 in the First Year Project

## Project Description:

### 1 Overview: image analysis
In this project you will learn to measure features in images of skin lesions,
and predict the diagnosis (for example, melanoma) from these features in
an automatic way. You will likely:
-  Implement methods to measure ”handcrafted” features
-  Explore and transform these features
-  Use the features with a machine learning classifier to predict the
-  lesion diagnosis
-  Perform experiments to evaluate different parts of your method

### 2 Requirements
In addition to the requirements in the course description, you must work on
Github. All Python packages are allowed, but comment your code assuming
the reader has no knowledge of extra packages that were not covered in the
first semester, such as pandas.
You can find starter code here: https://github.com/vcheplygina/
fyp2022-imaging

### 3 Assignment
A dermatologist in your city asks if you can investigate whether some features of skin lesions can be reliably measured by image analysis algorithms.
The dermatologist is especially interested in features like asymmetry, border,
and color.
Your goal is first to measure the asymmetry and color characteristics in
a set of skin lesion images. You can then choose to measure some additional
features of your own choice.
Your second goal is to evaluate how good these features are, by predicting
the diagnosis of the skin lesions based on these features.

#### Task 0: explore the data
The original data is available at https://challenge.isic-archive.com/
landing/2017/. We first only use a subset of this data, available on Github.
Go through the data (images and meta-data) that you have available
to understand what’s available to you, and write a brief description. What
types of diagnoses are there, and how many images are there of each? What
kind of meta-data is available? Is there some missing data? Are there images
of low quality?
As there are quite a few images, you are allowed to resize the images (for
example, to be 300 pixels in width).

#### Task 1: measure the features yourself
Search for related work about the ABC features and how they are measured
by dermatologists. Go through your set and try to rate the images yourself,
with multiple people rating the same image. Document who rates which
image (for example, create a column per feature/rater combination). Save
the ratings in a CSV file and commit it to Github.

#### Task 2: measure the features yourself
Create implementations for the ABC features using related work in image
analysis. There will be multiple (similar) ways to measure each feature, if
this is the case you can motivate which method you choose. You may use
code available online but you need to be able to explain and modify different
steps of the code.
While you are doing this, you might want to create “toy” images where
you already know the results, for example a circle should be less asymmetric
than an ellipse, etc.
Once you are satisfied with your implementations, run them on all your
images and create visualizations to explore the measurements. How do the
features compare to your manual measurements? How do the features compare for each class? Can you see differences between different diagnoses?

#### 7 Task 3: predict the diagnosis
For this task, you can use the entire set of 2000 images if you want. Split
your data so that you are have training data and validation data. Use the
training data to train different classifiers (and/or with different parameters),
and evaluate the performance on the validation data. Analyze the results
by comparing the classifiers on different metrics, inspecting images that are
classified incorrectly, etc. After this, select your best classifier, and create a
script classify groupX.py that takes an image, measures the features, classifies the image and outputs it’s probability of being melanoma, between 0
(healthy) and 1 (melanoma).
This script will be evaluated on a different set of data, which is not given
to you.

#### Task 4: open question
Use the data and your findings so far to formulate, motivate, answer, and
discuss another research question of your choice. For example, you can
study additional types of features, study differences based on age or sex of
the patient (you will need to retrieve this from the ISIC 2017 website), and
so forth. You are also allowed to use data other than ISIC 2017 here.

#### Hand-in
You must hand in:
-  groupX gitlog.txt
-  groupX report.pdf: A project report
-  groupX code.zip: A zip file with your code that can reproduce your results and classify other images.

More specifically the zip file should contain:
-  A .csv file listing your images, and your manual ratings of the images
-  A notebook or script that starts from the raw files, and creates the figures and tables in your report. Do not include the images.
-  A script that takes an image and outputs its probability of being melanoma
-  Any other .py scripts you used

#### Project Report
The project report must be maximum 6 pages long (including figures and
tables, not including references) with 11pt font size, 1.5cm margins. You
can include the following sections:
1. Introduction: context and motivation for the problem. What has been
already studied about this topic? What are your research questions?
2. Data: describe your data, and your analysis of the manual annotations
3. Feature extraction: describe the methods and results of the feature
extraction step
4. Classification: describe the methods and results of the classification
step
5. Discussion and conclusions: limitations of your data and methods,
future work, general (for example ethical) reflections
6. Disclosure statement (optional): here you may state if there were any
serious unequal workloads among group members
Given the nature of the image data, there will be no limit on the number
of figures/tables, but every figure or table you include should be there for a
good reason and discussed in the main text.
