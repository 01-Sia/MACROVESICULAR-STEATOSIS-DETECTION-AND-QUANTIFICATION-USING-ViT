# MACROVESICULAR STEATOSIS DETETCTION AND QUANTIFICATION IN HUMAN LIVER USING VISION TRANSFORMERS 
## Table of Contents:
- [Introduction](#Introduction)
- [Applications](#applications)
- [Neural Network Architecture](#Neural-Network-Architecture)
- [The Model](#the-model)
- [Results](#results)

## Introduction
- Liver steatosis, the abnormal accumulation of fat within hepatocytes, presents a significant health concern globally, with implications ranging from mild liver dysfunction to severe conditions such as  non-alcoholic steatohepatitis (NASH) and as non-alcoholic fatty liver disease (NAFLD). Macrovesicular steatosis, characterized by large fat vacuoles within hepatocytes, is a particularly important subtype of liver steatosis, often associated with more severe liver damage and disease progression. Accurate detection and quantification of macrovesicular steatosis are critical for diagnosing liver conditions, assessing disease severity, and guiding treatment decisions. However, current methods for evaluating steatosis, such as visual assessment by pathologists or automated image analysis techniques, often lack the precision and efficiency needed for reliable clinical diagnosis and research purposes.Automated image analysis techniques, while offering potential improvements in efficiency and objectivity, often rely on handcrafted features or shallow learning models, limiting their ability to capture complex patterns and variations in histological images accurately. Additionally, existing approaches may struggle to differentiate between different types and degrees of steatosis or may not generalize well to diverse datasets, including samples stained with different techniques or obtained from different imaging modalities.

## Applications 
- The scope of the proposed project encompasses the development and validation of a novel computational framework for the assessment of macrovesicular steatosis in human liver tissue using Vision Transformers (ViTs). This framework will involve pre-processing histological images, extracting relevant features, training ViT models, and evaluating their performance in detecting and quantifying steatosis accurately.
The application of this project spans various domains within hepatology and medical imaging. Firstly, the developed computational tool has the potential to aid pathologists and clinicians in diagnosing liver steatosis more accurately and efficiently. By providing quantitative measures of steatosis severity, the tool can enhance clinical decision-making, treatment planning, and patient monitoring in conditions such as NAFLD and NASH.

## Neural Network Architecture
- ![image](https://github.com/01-Sia/MACROVESICULAR-STEATOSIS-DETETCTION-AND-QUANTIFICATION-/assets/117347998/3b4c5841-620b-4586-8376-993a36841e15)

## Model 
- We employed vision transformers, a state-of-the-art deep learning architecture, for the detection of macrovesicular steatosis in H&E stained histological images of human liver. Vision transformers are known for their ability to capture long-range dependencies in images, making them well-suited for analyzing complex structures such as those found in liver histology.

-The vision transformer model was trained on a dataset of annotated histological images, focusing on identifying regions of interest (ROIs) corresponding to macrovesicular steatosis. The training process involved optimizing the model's parameters using a combination of labeled data and a suitable loss function, such as binary cross-entropy or focal loss.

#### A. DATASET 

- We utilized a large dataset comprising hematoxylin and eosin (H&E) stained liver biopsies for our study. The dataset consisted of histological images obtained from patients with varying degrees of macrovesicular steatosis, as well as samples with other liver pathologies for comprehensive analysis.
The H&E staining provided high contrast images, allowing for the clear visualization of hepatocytes and lipid droplets characteristic of steatosis. The dataset included a diverse range of liver histology samples, ensuring robustness and generalizability of our findings.
The use of this extensive dataset enabled us to train and validate our vision transformer model and Python library for the detection and measurement of macrovesicular steatosis with a high degree of accuracy and reliability.

#### B. DATA PREPROCESSING  

- We employed KMeans clustering as a preprocessing step to remove unnecessary and faulty images from the dataset. KMeans clustering is a popular unsupervised machine learning algorithm used for clustering data points into a specified number of clusters. By applying KMeans clustering to our dataset, we were able to identify and remove images that did not belong to the main clusters, which helped improve the overall quality of the dataset. We extracted features from each image in the dataset using a pre-trained convolutional neural network (CNN). These features represented the unique characteristics of each image.
- We visualized the clusters using a scatter plot, where each point represented an image and its position in the plot was determined by its feature vector. This allowed us to visually inspect the clustering results and identify any outliers or clusters that contained faulty images.

#### C. METHOD 

###### Detection using Vision Transformers
 We employed vision transformers, a state-of-the-art deep learning architecture, for the detection of macrovesicular 
 steatosis in H&E stained histological images of human liver. Vision transformers are known for their ability to capture 
 long-range dependencies in images, making them well-suited for analyzing complex structures such as those found in liver 
 histology.
 The vision transformer model was trained on a dataset of annotated histological images, with a focus on identifying regions 
 of interest (ROIs) corresponding to macrovesicular steatosis. The training process involved optimizing the model's 
 parameters using a combination of labeled data and a suitable loss function, such as binary cross-entropy or focal loss.
 Once trained, the vision transformer was used to predict the presence and location of macrovesicular steatosis in unseen 
 histological images. This detection step served as the initial stage in our methodology, enabling us to isolate and focus 
 on the regions of interest for further analysis.

###### Measurement of Steatosis
 Following the detection of macrovesicular steatosis regions, we utilized a Python library tailored for the measurement of 
 steatosis levels within these regions. The library provides functions for extracting quantitative features from 
 histological images, such as the percentage of hepatocytes containing lipid droplets.
 To measure steatosis, the library analyzes the intensity and distribution of lipid droplets within the detected ROIs. This 
 process involves image processing techniques, including thresholding, segmentation, and morphological operations, to 
 accurately quantify the extent of steatosis. The measurements obtained from the Python library were used to assess the 
 severity of macrovesicular steatosis in the liver samples, providing valuable insights into the disease progression and 
 potential treatment strategies.

###### Measurement of Steatosis
 Following the detection of macrovesicular steatosis regions, we utilized a Python library tailored for the measurement of 
 steatosis levels within these regions. The library provides functions for extracting quantitative features from 
 histological images, such as the percentage of hepatocytes containing lipid droplets.
 To measure steatosis, the library analyzes the intensity and distribution of lipid droplets within the detected ROIs. This 
 process involves image processing techniques, including thresholding, segmentation, and morphological operations, to 
 accurately quantify the extent of steatosis. The measurements obtained from the Python library were used to assess the 
 severity of macrovesicular steatosis in the liver samples, providing valuable insights into the disease progression and 
 potential treatment strategies.

###### Analysis
 In our analysis, we utilized the Kleiner score as a reference standard for assessing the severity of macrovesicular 
 steatosis in human liver histology. The Kleiner score, a widely accepted scoring system in liver pathology, classifies 
 steatosis into four grades based on the percentage of hepatocytes containing lipid droplets.


