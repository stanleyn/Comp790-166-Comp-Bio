# Purpose 

Here is a list of publicly available and easy to download datasets that can be used for projects. I also provide an example of the type of question that you could ask for each dataset. They are categorized here generally my modality (e.g. mass cytometry) or by theme (multiomics,images,longitudinal). I am only providing datasets here that are well described and annotated to facilitate prediction, etc with minimal pre-processing. 

The following are only suggestions. Please feel free to come with your own datasets and questions!

# Mass and Flow Cytometry Datasets

## General Pre-Processing Advice
Mass cytometry data comes as a collection of .FCS files, where each file corresponds to an individual sample. For pre-processing, you will need to make sure you are only looking at appropriate markers (phenotypic and functional), and not those that were used to monitor how well the experiment went. 

## Types of Questions
The sky is the limit in the single cell world. Here are some concrete ideas: 

* **Clustering** : For a dataset with hundreds of samples you will have to deal with millions of cells. How do you cluster into coherent cell populations without losing too much information? Clustering on single-cell data has a lot of activity in the literature, so proceed with caution. 
  * How well can you preserve small clusters that might not be found consistently across algorithms?
  * How do you incorporate some notion of 'semi supervision', with regards to the patient outcomes or well-known canonical marker combinations?
  * How can you make existing algorithms faster by doing some smart pre-processing of your dataset? 
  * What do you do with the clusters? Try to come up with something useful to do with your cell populations. 
  * Batch effects and clustering- if there are clear batches in the data, how do we take that into account?
  
* **Predicting Patient Outcomes** : The overarching goal here is to extract information from the heteregenity within a single-cell dataset for downstream tasks. 
  * predict how a patient's immune system will look based on measurements from a previous timepoint
  * can you develop an approach to generate features from single cell data to accurately patients with different clinical outcomes
  * unsupervised questions: if we don't know what the patient labels are, can we extract features from the data 
  * twin studies: how can you use sets of twins to systematically study immune system differences?
  * Which type of immune features are associated with some continuous or ordinal variable (like time, or disease severity) 
 
 # Dataset Examples
 The most popular repositories for mass cytometry and flow cytometry datasets are flow repository (https://flowrepository.org/) and Immport (https://www.immport.org/shared/home) 
 
 * [Mass Cytometry-Longitudinal] : The immune system in healthy vs. preeclamptic women. 
   * FCS Files: https://flowrepository.org/id/FR-FCM-ZYRQ
   * Sample Metadata: https://flowrepository.org/experiments/1914/attachments/4206/download
