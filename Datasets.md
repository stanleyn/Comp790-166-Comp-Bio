# Purpose 

Here is a list of publicly available and easy to download datasets that can be used for projects. I also provide an example of the type of question that you could ask for each dataset. They are categorized here generally my modality (e.g. mass cytometry) or by theme (multiomics,images,longitudinal). 

# Mass Cytometry Datasets

## General Pre-Processing Advice
Mass cytometry data comes as a collection of .FCS files, where each file corresponds to an individual sample. For pre-processing, you will need to make sure you are only looking at appropriate markers (phenotypic and functional), and not those that were used to monitor how well the experiment went. 

## Types of Questions
The sky is the limit in the single cell world. Here are some concrete ideas: 
* Clustering : For a dataset with hundreds of samples you will have to deal with millions of cells. How do you cluster into coherent cell populations without losing too much information? Clustering on single-cell data has a lot of activity in the literature, so proceed with caution. 
  * How well can you preserve small clusters that might not be found consistently across algorithms?
  * How do you incorporate some notion of 'semi supervision', with regards to the patient outcomes or well-known canonical marker combinations?
  * How can you make existing algorithms faster by doing some smart pre-processing of your dataset? 
  * What do you do with the clusters? Try to come up with something useful to do with your cell populations. 
  * Batch effects and clustering- if there are clear batches in the data, how do we take that into account?  
