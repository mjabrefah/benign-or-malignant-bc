# benign-or-malignant-bc
A K-Nearest Neighbors (KNN) machine learning model to predict breast cancer.
***
Accurate and early diagnosis is crucial for effective treatment planning and patient outcomes, especially when it comes to a disease such as breast cancer. Diagnosis begins with determining whether a breast **tumor** also known as [**neoplasm**](https://en.wikipedia.org/wiki/Neoplasm) (mass of abnormal cells) is benign or malignant.

[**Benign**](https://my.clevelandclinic.org/health/diseases/22121-benign-tumor) breast tumors may continue to grow, but they are not aggressive toward the tissue around them. They remain contained, and often doctors advise leaving them alone. In contrast, [**malignant**](https://my.clevelandclinic.org/health/diseases/22319-malignant-neoplasm) breast tumors are cancerous. As they grow, they actively invade and damage the surrounding tissue. Over time they may become [**metastatic**](https://my.clevelandclinic.org/health/diseases/22213-metastasis-metastatic-cancer), which means that the cancerous cells have spread through the lymphatic system or blood and created secondary tumors in other parts of the body.

One of the methods used to diagnose whether a breast tumor is benign or malignant involves having a pathologist (a specialized doctor) look at biopsies (tissue samples) taken from the tumor using a fine needle.

The pathologist examines the tissue sample under a microscope, looking for physical changes in the cells' nuclei that indicate that the cells are cancerous. The pathologist may take measurements and make counts of what they see. Ultimately, they use their data to make a calculated diagnosis of benign or malignant.

As you can probably tell, this process takes time and must be done by a highly trained expert. What if we could use technology to make it faster and easier?

In this project, you will explore whether AI and machine learning can help accurately diagnose breast cancer. If so, their use could speed up the diagnosis process and bring diagnostic capabilities to geographic areas where cancer pathologists are not available. You will then optimize the model to achieve the best accuracy you can and evaluate how useful you think the model is.

The **K-Nearest Neighbors (KNN)** algorithm, involves making predictions based on the characteristics of nearby data points. KNN exemplifies how machine learning algorithms harness data to make informed decisions and refine their performance over time.

KNN can save time and effort compared to analyzing data manually. It is great at finding complex patterns that might be hard for people to see. KNN is consistent and works well with both small and large datasets. It can adjust to changes quickly and make decisions automatically. It is also good at handling data with many details.

KNN has some limits, too. For example, it might not work as well with data with a lot of noise—random or irrelevant information that can hide true patterns. And because it makes complex calculations, it can be slow to use with large datasets. It is important to decide if KNN is the right fit based on what you need to do with the data.

KNN is a straightforward machine-learning technique used for classification and regression tasks. It predicts by comparing a new data point to a certain number (k) of its nearest neighbors. The algorithm then makes predictions based on how the majority of its neighbors are categorized (for classification) or by averaging its neighbors' values (for regression).

## Dataset
The dataset used comes from Dr. William H. Wolberg from the University of Wisconsin Hospital in Madison. It is commonly called the Wisconsin Diagnostic Breast Cancer (WDBC) dataset. It contains data about the nuclei of cells found in breast tumor samples.

Cancer involves abnormal cell growth. Cancerous cells divide rapidly, even when the cells are not fully ready. This can lead to changes in the number of chromosomes as well as other physical changes that can be seen in the nuclei of the cells (where the DNA is stored).

![Normal cells and Cancer cells](https://www.sciencebuddies.org/lsxwirljlcGjZW2SImJX0FeY7Ho=/975x548/-/https/www.sciencebuddies.org/cdn/Files/19874/5/cancer-cells-versus-normal-cells.jpg)
**Figure 1.** Normal breast tissue cells each have a single uniformly shaped and sized nucleus. In contrast, cancerous cells often have abnormally shaped and sized nuclei.

The WDBC dataset contains information about 10 features of the nuclei in the samples:

_Radius_: the distance from the center of a nucleus to points on the perimeter of the nucleus  
_Texture_: the standard deviation of grayscale values of nuclei. The grayscale values can be used as a proxy for whether the nucleus has an abnormal distribution of features like chromatin, ribosomes, and nuclear pores  
_Perimeter_: the measurement around the outside of the nucleus  
_Area_: the area of the nucleus  
_Smoothness_: the variation in the radius lengths of nearby nuclei (local variation in radius lengths)  
_Compactness_: the perimeter squared, divided by the area of the nucleus  
_Concavity_: the severity of concave portions of the contour of the nucleus  
_Concave points_: the number of concave portions of the contour of the nucleus  
_Symmetry_: a measure of how uniform the nuclei are across the midpoint  
_Fractal dimension_: a measure of how misshapen the outline of the nucleus is

Taken together, these 10 features are intended to capture the regular, uniform shape of nuclei in normal breast tissue compared to the chaotic and irregular shapes of cancerous nuclei. The WBCD dataset includes a computed mean, standard error, and "worst" or "largest" (mean of the three largest values) for each feature for each image.
