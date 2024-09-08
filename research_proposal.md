# Image Analysis for Flea Beetle Damage Assessment in Canola Plants: A Machine Learning Approach

### Supervisor: Dr. Christopher Henry
### Created By: Jesse Shen


## Introduction
Canola is a crucial crop globally, valued for its oil and meal products, In Canada, canola is one of the Canada’s most profitable crops, contributing $19.3 billion to Canadian economy and providing more than 225,000 jobs to Canadians. However, it is highly susceptible to various pest insects, with flea beetles being the most damaging. Currently, the primary method of controlling these pests involves the use of broad-spectrum insecticides. These insecticides pose significant risks, including the inadvertent killing of non-target beneficial insects and potential adverse effects on vertebrate species. Moreover, there is a growing public concern regarding the long-term adverse impact of these chemicals and the escalating risk of developing insecticide-resistant pest populations. Consequently, there is an urgent need to develop safer and more targeted pest control methods.

Dr. Steve Whyard, professor of Biological Sciences at University of Manitoba and his team are developing a solution utilizing RNA interference (RNAi) technology. This method aims to silence specific genes essential for pest insect growth and development by applying double-stranded RNA (dsRNA) to the organism's cells. “Inside the cell, the dsRNA induces the destruction of any mRNAs that are complementary to the dsRNA’s nucleotide sequence, thereby reducing or silencing the targeted gene’s expression.”

## Project Idea
The project aims to assist Dr. Whyard’s research by investigating different machine learning (ML) algorithms that could solve the problem, potentially proposing new adaptations of existing ML techniques (if necessary), and, finally, developing an ML tool to automate the analysis of plant damage caused by flea beetles – based on the method(s) identified in the investigation. This overarching goal of this work is to enhance the throughput and accuracy of evaluating plant resistance. The current method involves taking photographs of test plants every few days over a two-week period and manually scoring the extent of damage based on the number of holes in the leaves. This process is labor-intensive, requiring manual adjustments of hue, saturation, and brightness to select all plant material in the images, followed by additional image manipulation to remove white speckles and outlying pixels. Each photograph takes 2 to 5 minutes to analyze, making the process time-consuming.

By leveraging machine learning, the proposed tool will automate the image analysis process. The tool will be trained to recognize and quantify leaf damage accurately, reducing the need for manual adjustments and significantly speeding up the analysis. This will involve developing and implementing ML models capable of detecting and counting the number of holes in the leaves, filtering out noise, and recording the adjusted color threshold values and white pixel count for statistical analysis. The automation of this process will enable higher throughput analyses, facilitating the identification of plants that exhibit greater resistance to flea beetle damage. 
Machine Learning Theory/Approach

The ML development process always begins with a literary search (LS) to ensure the most up-to-date approaches and methods are considered. This is a field that is rapidly evolving, and new developments are published with high frequency. This will ensure we are using the best architectures or architecture components for the proposed problem. For this project, we will start by identifying state-of-the-art approaches in semantic segmentation [1], which is necessary to solve Dr. Whyard’s problem. We will start by assessing the suitability of Meta's Segment Anything Model (SAM) [2] but will also explore all of the latest developments in semantic segmentation models. 

Next, we will attempt to implement the methods we identify in the LS to solve Dr. Whyard’s problem. Typically, the first step in the ML development process is to use existing architectures, and solutions built with these models can achieve the desired results. We will start with the architectures identified in the LS. However, it is often the case that custom adjustments or architectures are necessary to gain the extra accuracy or performance required for practical applications. Producing the best model in this case requires the following general iterative ML development approach. First, the network architecture is defined (either off-the-self or custom architectures). This is followed by training of models, hyper parameter tuning, testing, and validation. This is a cyclic process, which can include incremental network architecture redesign based on intermediate model results.

Finally, the project will end with a comparison between the method we have developed, and other tools available in the Plant and Biological Sciences. An example framework we can use for comparison is PlantCV , a plant-specific image processing library based on Open CV  that contains methods for plant segmentation. 

## Dataset
The dataset for this project will be provided by Dr. Whyard's team which consists of photographs of canola plants subjected to flea beetle attacks. As part of this project, we will be responsible for analyzing and processing the given dataset to ensure compatibility and effectiveness with the chosen ML model [2].

## Development Environment:
-	Programming Language: Python
-	Libraries and Frameworks: NumPy, Pandas, Scikit-learn, PyTorch
-	Integrated Development Environment (IDE): VS Code, Jupyter Notebook


[1]	Cheng, B., et al, Per-Pixel Classification is Not All You Need for Semantic Segmentation. arXiv:2107.06278, 2021 

[2]	Kirillov, A., et al. Segment Anything. arXiv: 2304.02643, 2023
