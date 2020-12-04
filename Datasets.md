# Purpose 

Here is a list of publicly available and easy to download datasets that can be used for projects. They are categorized here generally by modality (e.g. mass cytometry) or by theme (multiomics,images,longitudinal). I am only providing datasets here that are well described and annotated to facilitate prediction, with very minimal pre-processing. 

The following are only suggestions. Please feel free to come with your own datasets and questions!

# Mass and Flow Cytometry Datasets

## General Pre-Processing Advice
Mass cytometry data comes as a collection of .FCS files, where each file corresponds to an individual sample. For pre-processing, you will need to make sure you are only looking at appropriate markers (phenotypic and functional), and not those that were used to monitor how well the experiment went. Usually the paper corresponding to each dataset will have a table of the antibodies that were used. You should keep only columns that correspond to these. 

## Dataset Examples
 The most popular repositories for mass cytometry and flow cytometry datasets are flow repository (https://flowrepository.org/) and Immport (https://www.immport.org/shared/home) 
 
 * [Mass Cytometry-Longitudinal] : **The immune system in healthy vs. preeclamptic women during pregnancy**. 
   * FCS Files: https://flowrepository.org/id/FR-FCM-ZYRQ
   * Sample Metadata: https://flowrepository.org/experiments/1914/attachments/4206/download
   * Paper: https://www.frontiersin.org/articles/10.3389/fimmu.2019.01305/full?source=post_page---------------------------
   
 * [Mass Cytometry- Longitudinal] : **Looking at the effects of Dengue Virus on dendritic cells**
   * FCS Files: https://flowrepository.org/id/FR-FCM-ZY87
   * Sample Metadata: https://flowrepository.org/id/FR-FCM-ZY87 (see experiment variables in the experimental overview section. Explains samples according to individual, timepoint and condition).
   * Paper: https://pubmed.ncbi.nlm.nih.gov/28679950/ 
  
 * [Mass Cytometry- Bechmarking Datasets]: **Labeled Cell-Populations for Benchmarking Clustering Approaches**
   * FCS Files: https://flowrepository.org/id/FR-FCM-ZZPH
   * Metadata: https://flowrepository.org/id/FR-FCM-ZZPH. See `attachments` in the experiment overview section
   * Paper: https://pubmed.ncbi.nlm.nih.gov/27992111/ 
 
 * [Flow Cytometry- Healthy vs AML] : **FlowCAP Challenge Dataset** 
   * FCS files: https://flowrepository.org/id/FR-FCM-ZZYA
   * Sample Metadata: https://flowrepository.org/id/FR-FCM-ZZYA (see experiment variables in the experiment overview section)
   * Paper : https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3906045/
   
* [Mass Cytometry- Longitudinal] : **Predicting Covid-19 Severity**
  * FCS Files: https://ki.app.box.com/s/sby0jesyu23a65cbgv51vpbzqjdmipr1?page=1
  * Sample Metadata: https://www.sciencedirect.com/science/article/pii/S2666379120300999 (see Figure 2)
  * Paper : https://www.sciencedirect.com/science/article/pii/S2666379120300999
  
* [Mass Cytometry-Longitudinal] : **Longitduinal Recovery of Patients from Stroke**
  * FCS Files : https://flowrepository.org/id/FR-FCM-ZYSB
  * Sample Metadata : https://flowrepository.org/experiments/1931/attachments/4257/download
  * Paper : https://academic.oup.com/brain/article-abstract/142/4/978/5373058 
  
* [Mass Cytometry- Cross-Species Immune Atlas] : **Immunophenotyping Across Multiple Species**
  * FCS Files: https://flowrepository.org/id/FR-FCM-Z2ZY
  * Sample Metadata: https://flowrepository.org/id/FR-FCM-Z2ZY (see Download Attachments in Experiment Overview Section)
  * Paper : https://www.biorxiv.org/content/10.1101/574160v1 
  
* [Mass Cytometry- Patient Survival Analysis] : **Predicting Survival from Glioblastoma**
  * FCS Files : https://flowrepository.org/id/FR-FCM-Z24K
  * Sample Metadata : https://cdn.elifesciences.org/articles/56879/elife-56879-supp3-v2.docx
  * Paper: https://elifesciences.org/articles/56879.pdf 
  
* [Mass Cytometry- Longitudinal] : **An Immune Clock of Healthy Human Pregnacy**
  * FCS: https://flowrepository.org/id/FR-FCM-ZY3Q
  * Sample Metadata: Not given, but I can help you :)
  * Paper: https://pubmed.ncbi.nlm.nih.gov/28864494/
  
 * [Mass Cytometry- Differential Abundance, Patient Classification] **3 datasets from diffcyt paper (differential abundance analysis)**
   * FCS Files: https://flowrepository.org/id/FR-FCM-ZYL8
   * Sample Metadata: https://github.com/lmweber/diffcyt-evaluations (check depending on which sub dataset)
   * Paper: https://www.nature.com/articles/s42003-019-0415-5 
  
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
  
# Multiomics Datasets
How can we successfully integrate multiple biological modalities measured in a common set of patients.

* [TCGA Data (in an easy-to-use format)]: **Processed TCGA Data for Multiple Cancer Tyes**
  * Data: http://www.linkedomics.org/login.php
  * Paper: https://academic.oup.com/nar/article/46/D1/D956/4607804
  
* [Multiple Datasets in Term Pregnancy]: **7 Modalities Profiled for a Cohort of Healthy Women**
  * Data: https://nalab.stanford.edu/multiomics-pregnancy/
  * Paper: https://academic.oup.com/bioinformatics/article/35/1/95/5047759
  
 # Biological Networks, Examining Correlation Structure.

Here are examples of data that is inherently a graph, or data that we could build a graph from. 

 ## Dataset Examples
 
 * [Graph Partitioning] : **Disease Modeling DREAM Challenge on Graph Clustering**
   * Data: https://www.synapse.org/#!Synapse:syn6156761/wiki/400645
   * Paper : https://www.nature.com/articles/s41592-019-0509-5
   
 * [Inter-modality between-feature correlation] : **Genetic Dependency and LargeScale Screens**
   * Data: https://depmap.org/portal/download/
   * Paper : https://depmap.org/portal/
  
* [Microbiome Networks] : **Interspecies Microbial Correlation**
   * Data : https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002687#s5 (see supporting information)
   * Paper : https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002687#s5
   
## Types of Questions
 * **Graph partitioning** : Evaluating a partition, linking to external information, incoporating extra information into the problem (rather than just connectivity), speeding up existing methods through pre-processing. 
 * **Graph Representation** : What is the best way to represent the graph? How can your method to construct a graph scale to situations where there are portentially a very large number of nodes? 
 * **Ranking** : What are the most important parts of the graph, how do we identify them?
   
   
 # Imaging Mass Cytometry (Images of tissue + protein expression)
 
 On top of the regular challenges associated with studying image data, here you need to incorporate another source of information, which is the expression of multiple proteins. 
 
 * [Imaging Cytometry] : **histocat**
   * Data : https://github.com/BodenmillerGroup/histoCAT (see tutorials for examples)
   * Paper : https://www.nature.com/articles/nmeth.4391
   
 * [Imaging Cytometry] : **IMCTools** (see tutorials for examples)
   * Data : https://github.com/BodenmillerGroup/imctools
   * Paper : https://www.nature.com/articles/s43018-020-0026-6#data-availability
   
 * [General Microscopy Data] : https://idr.openmicroscopy.org/ 
   
  
