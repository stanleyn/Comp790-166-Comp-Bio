# Comp790-166: Computational Biology

## Details
Instructor: Natalie Stanley

Email: stanleyn@stanford.edu

Time: Tuesday/Thursday 9:30am-10:45am, Spring Semester 2021

Office Hours: TBD

Location: Zoom link TBD

## Description
Moden high-throughput assays allow us to efficiently profile a variety biological processes at a systems-level across a set of patient samples. As a result, these technologies generate an abundance of detailed information that needs to be extracted, analyzed and interpreted. In this course we will discuss the methodology used to analyze (process, engineer features from, combine, etc.) data generated by some of the most cutting-edge technologies, such as proteomics, single-cell assays, and imaging in biomedicine.  We will further discuss how numerical linear algebra techniques and modern machine learning approaches can be applied to effectively extract information from these assays for an improved understanding of human health and disease. **While computational biology is a very broad field, we will focus here on the analysis of data generated by single-cell technologies (e.g. mass cytometry), multiomics/multi-modality analysis, systems immunology, and benchmarking.** For each class of algorithms introduced for some task on biological data, we will also go over necessary theory and mathematical intuition. 

## Prerequistes
Strong programming. Comfortable with linear algebra and basic probabilty. Please do not worry if you don't have any background in biology. Any relevant concepts will be introduced. Please feel free to talk to me about any of these prerequistes. 

## Course Structure
This course will be mostly lecture-based with two homework assignments and a course project. I will provide ideas for several publicly available biological datasets and open problems for you to work on for these projects. Overall, the project is intended to give you an opportunity to implement/apply methodology discussed in the papers that we will discuss together. The final project writeup will also give you practice writing up results and communicating ideas. You are welcome to work on teams for this project.

Most of the lectures will be based around several papers. To benefit your own understanding, I will provide a set of questions that should be answered for one of the papers discussed in each lecture.

# Schedule

Note that this is preliminary. Some topics may take (on average) 1 day longer than planned. 

| Date | Topic | Reading | Notes | Code |
|------|-------|---------|-------|------|
| Week 1-1    | Intro, bioinformatics vs comp bio, big picture challenges, bio primer     | [[Systems Immunology, Just Getting Started](https://pubmed.ncbi.nlm.nih.gov/28632713/)] | [Lecture 1 Notes](https://github.com/stanleyn/Comp790-166-Comp-Bio/blob/main/Lecture_Notes/Lecture1_intro.pdf) | | |
| Week 1-2    | Building graphs from data, graph laplacian, matrix decomposition, low rank appropximations | [[SLMP. pages 10-22](https://arxiv.org/abs/2004.07984)], [[LargeVis](https://arxiv.org/abs/1602.00370)] **reading summary on LargeVis** |  | [[LargeVis](https://github.com/lferry007/LargeVis)][[graph tools for python](https://github.com/stanleyn/graphtools)] |
| Week 2-1 | Partitioning Graphs, Ranking Nodes | [[Louvain](https://iopscience.iop.org/article/10.1088/1742-5468/2008/10/P10008/meta)], [[Neighborhood PageRank and Link Prediction](https://www.cs.purdue.edu/homes/dgleich/publications/Nassar%202020%20-%20pairwise%20prediction.pdf)] **no reading summary** |  | [[Louvain](https://github.com/vtraag/louvain-igraph)] |
| Week 2-2 | Random walks on graphs, Graph Embeddings, Graph Diffusion --> Embedding Nodes and Embedding Edges | [[Node2Vec](https://dl.acm.org/doi/pdf/10.1145/2939672.2939754?casa_token=vQTboPUL6qIAAAAA:XQsAUtXd4MyWfj1ClUBw8FKhuPbpqO-aE2d7EDs5iX9-jJZP9BuxDbKUjg3CM69YKHALjCAKJtJx)], [[Edge2Vec](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-019-2914-2)] | | [[node2vec](https://github.com/aditya-grover/node2vec)], [[edge2vec](https://github.com/RoyZhengGao/edge2vec)] |
| Week 3-1| Graph Signal Processing | [[Review on GSP](https://arxiv.org/abs/1211.0053)], [[PHATE](https://www.nature.com/articles/s41587-019-0336-3)] **reading summary on PHATE** | | [[PHATE](https://github.com/KrishnaswamyLab/PHATE)] | 
| Week 3-2 | Single Cell Day 1: Intro to single-cell profiling, normalization, batch effect correction, imputation in single-cell analysis, automated cell-population discovery, visualization | [[Spade](https://www.nature.com/articles/nbt.1991)], [[MAGIC](https://www.biorxiv.org/content/10.1101/111591v1)] | | [[FCS file tutorial](https://github.com/stanleyn/fcs_tutorial)], [[MAGIC](https://github.com/KrishnaswamyLab/MAGIC)] |
|Week 4-1 | Single Cell Day 2: Graph-based analysis of single-cell data | [[phenograph](https://www.sciencedirect.com/science/article/pii/S0092867415006376)] | | [[phenograph](https://github.com/JinmiaoChenLab/Rphenograph)], [[FastPG](https://github.com/sararselitsky/FastPG)] |
| Week 4-2 | Single Cell Day 3: Feature Engineering from single-cell data and linking to external variables | Citrus, VoPo, MELD | 
| Week 5-1 | Single Cell Day 4: Differential Analysis of Cell-Populations | Diffcyt, Cydar |
| Week 5-2 | Single Cell Day 5: Graph-based matching of single-cell data | Conos, LIGER
| Week 6-2 | Single Cell Day 6: Deep Learning for Single Cell Tasks | SAUCIE, CellCNN |
| Week 6-2 | Single Cell Day 7: Semi-Supervised Automated Cell-Population Discovery | MARS| 
| Week 7-1 | Single Cell Day 7: Trajectory Inference | |
| Week 7-2 | Single Cell Day 8: Benchmarking in Trajectory Inference | |
| Week 8-1 : **Project Proposals Due** | Presentations of Project Propsals Day 1 | |
| Week 8-2 | Project Proposal Presentation Day 2 | |
| Week 9-1 : **Homework 1 Due** | Single Cell Day 9: Benchmarking in Single-Cell Analysis | Aghaeepour et al |
| Week 9-2 | Single Cell Day 10: Imaging Proteomics + Spatial Regularization : computational challeneges in combining tissue images and protein expression | |
| Week 10-1 | Multiomics Day 1: Constructing a joint embedding of samples according to multiple modalities, subspace merging | SNF, grassmann embed |  
| Week 10-2 | Multiomics Day 2: MOFA-1 and MOFA-2: Multiomics Factor Analysis | MOFA-1, MOFA-2 | 
| Week 11-1 | Multiomics Day 3: Uncovering Relationships Between Modalities | mmvec| 
| Week 11-2 | Multiomics Day 4: Stacked Generalization and CCA in multiomics studies | Ghaemi |
| Week 12-1 | Multiomics Day 5: Benchmarking in multiomics studies | |
|Week 12-2  | Incorporating Prior Biological Knowledge into Analysis | |
|Week 13-1 : **Homework 2 Due** |  Systems Immunology Topic: TCR/BCR (T and B cell receptor reperotire analysis) | | 
|Week 13-2 | Partial Correlation, Thresholding etc for Identifying Meaningful Interactions | | 
|Week 14-1 | Enrichment Analysis, writing for an interdiscplinary audience | | 
|Week 14-2 | Project Presentations Day 1 | |
|Week 15-1 | Project Presentations Day 2 | |
|Final Exam Day | Project papers due | |

# Homework, Project, Reading, Grading, Etc

## Homework
There will be two homework assignments to practice implementing particular concepts. Often, things can become a bit easier to understand and use when they are implemented by you. I will be happy to read/run code written in Python, R, Julia, or Matlab. Please submit your homework writeup as a PDF. 

## Background Resources
Most of what we discuss in class will come from papers. However, I suggest the following textbooks as background references. Conveniently, they are also available for free.

* [PRML] Pattern Recognition and Machine Learning-- Chris Bishop [[Link](http://users.isr.ist.utl.pt/~wurmd/Livros/school/Bishop%20-%20Pattern%20Recognition%20And%20Machine%20Learning%20-%20Springer%20%202006.pdf)]

* [SLMP] Spectral Learning on Matrices and Tensors -- Majid Janzamin et al. [[Link](https://arxiv.org/abs/2004.07984)]

* The Matrix Cookbook [[Link](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf)]

## Readings
For each class, I will update the papers that we will go over in above table. You will only be required to write a summary of one of the potentially multiple papers assigned for that day.

### Reading Questions

1) Please explain in 2 sentences or less what the problem being solved is.

2) What were the main contributions of the authors in this work? (You can answer in a few bullet points). 

3) Please describe 1-2 computational experiments that the authors implemented to test their method.

4) Were the authors the first to attempt this particular problem? If not, did they compare their results to other baselines? Do you think that their evaluation was objective?

5) Do you think that the authors provided enough evidence for why their developed method is an important contribution? If yes, please describe their reasoning here. If you do not think they adequately justified why they worked on this particular problem, please describe your thoughts on that here. 

6) What is one follow-up idea or extension from this work? 

## Final Project
I will provide you with several examples of publicly available biological datasets and problems (https://github.com/stanleyn/Comp790-166-Comp-Bio/blob/main/Datasets.md). Half-way through the semester, you will submit your project proposal and present your idea to the class.  The proposal will be a short document describing 1) The problem 2) A background on other people's attempts to solve this problem and 3) A background on your idea of a solution and 4) the data you will use to test your method. At the end of the semester you will write a short paper explaining your method and results and present your results.

## Grading
 Grading will be based on the following

1) Reading Questions : 20% over the entire semester
2) Homework 1: 20%
3) Homework 2: 20%
4) Project Proposal : 10%
5) Project final writeup: 30%

