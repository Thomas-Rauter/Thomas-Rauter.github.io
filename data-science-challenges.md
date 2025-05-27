---
layout: default
title: Data Science Challenges
---
# Data Science Challenges

Data science challenges are competitive events where individuals or teams work on real-world 
problems using data analysis and machine learning techniques. Below are challenges I participated in
together with a team:


---
<br>

## **BIRDCLEF+ 2025**  
> **by Cornell Lab of Ornithology, USA**  
> *May 2025*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-%23013243.svg?style=flat&logo=numpy&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C?style=flat&logo=pytorch&logoColor=white)

[Learn more about the challenge](https://www.imageclef.org/BirdCLEF2025) 

**Overview**  
The task was to develop a sound classification model that determines which of 
206 different 
animal species are present in a soundclip, taken in a wild life reservoir. 
Such models are used to quantifiy the success of environmental restoration 
programs. The idea is that a high biodiversity and the presence of certain 
key species indicates a healthy environment and therefore the success of the 
restoration program. 

**Approach**  
I used the PANN audio model, which was pretrained on 5000 hours of sound and 
predicts 527 sound classes. With the help of this model, I created 
embeddings of the sound training data from the BIRDCLEF challenge. The idea 
is that this pretrained model is already capable of finding useful features 
in sound data, and can therefore be used as a feature extractor. To achieve 
this, I removed the output layer of the PANN, and used the output of the 
layer before as the embeddings. Then I trained another neural network model 
with far fewer parameters than PANN to map from those embeddings to the 
probabilities of the 206 animal classes of the BIRDCLEF challenge. 
Unfortunately, the challenge hosts required a minimal runtime of the 
approach in their cloud environment, which I could not meet with my approach,
which is why I was unable to submit and achieve a ranking. 



---
<br>

## **Richter's Predictor: Modeling Earthquake Damage**  
> **by Driven Data, USA**  
> *March – May 2025*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-%23013243.svg?style=flat&logo=numpy&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-%230072C6?style=flat&logo=xgboost&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-%23FF4081?style=flat&logoColor=white)


### 🏆 **1007th Place / 2487 Submissions**

[Learn more about the challenge](https://www.drivendata.org/competitions/57/nepal-earthquake/) 

**Overview**  
The task was to develop a model that predicts the earthquake damage (low, 
medium, almost complete destruction) from features such as the geo location, 
and construction engineering features, such as the height of the building 
and the type of superstructure material. The data consisted of about 260,000 
houses damaged in the Gorkha earthquake that hit Nepal in 2015. Note that 
this was a practice challenge with no price pool.

**Approach**  
We used one-hot encoding and target encoding for the categorical 
features, and predicted the damage with an XGBoost model by threating this 
ordinal problem as a classification. As the objective function, we used 
multi-class classification – soft probability output. The final score was 
reported with the micro-averaged F1 score. Finally, we used SHAP to extract 
feature importances to find insights about how to build houses so that they 
get less earthquake damage. Our SHAP feature importance analysis showed that 
building age is the most important predictor of earthquake damage (besides 
proximity to the earthquake epicenter): newer buildings tend to suffer less, 
while older ones are more likely to be heavily damaged. Structural materials 
play a major role too. Buildings made of mud mortar stone, mud mortar brick, or
adobe mud are associated with higher damage, which matches engineering
knowledge—they are brittle, lack reinforcement, and perform poorly under 
lateral  seismic forces. In contrast, cement mortar brick offers better 
protection due to its higher strength and cohesion. 


---
<br>

## **Watt's up? Synthetic Data for Buildings**  
> **by TU Vienna, Austria**  
> *22 – 23 February 2025*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-%23013243.svg?style=flat&logo=numpy&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-%230072C6?style=flat&logo=xgboost&logoColor=white)

### 🏆 **3rd Place / 8 Teams – 80€ Prize**

[Learn more about the challenge](https://events.vsc.ac.at/event/173/) 

**Overview**  
The task was to develop a model that can input timecourse data of electricity
consumption and output a synthetic version of this dataset that ensures the
privacy of the individuals. This is important because electricity consumption
data are sensitive and cannot be easily shared. However, widespread availability
of such datasets could be very beneficial for model development, allowing insights
that help save energy.

**Approach**  
We chose an approach that samples pieces from the actual data, reassembles them,
and adds Gaussian noise on top. This produced instances that closely resembled
the real data in terms of statistical properties but were different enough to
ensure they cannot be linked to individual examples of the real data.


---
<br>

## **Autoimmune Disease Machine Learning Challenge**  
> **by Eric and Wendy Schmidt Center at the Broad Institute, USA**  
> *Part 1: Oktober 2024 – February 2025*
> 
> *Part 2: November 2024 – March 2025*
> 
> *Part 3: December 2024 – April 2025*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white) 
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9AB00?style=flat&logo=googlecolab&logoColor=white)

### Part 1: 🏆 **2th Place / 75 submissions / 7800 participants – 2400$ Prize**
### Part 2: 🏆 **6th Place / 11 submissions / 8200 participants – 700$ Prize**
### Part 3: 🏆 still ongoing

[Learn more about the challenge](https://drive.google.com/file/d/1h5Z6euEbMD-8r0hSZsMEYEG-pb_nyiiH/view?usp=sharing)

**Overview**  
Autoimmune diseases occur when the immune system mistakenly attacks healthy 
cells, disrupting the body’s natural defense mechanisms. These diseases affect 
50 million people in the U.S., with cases rising globally.
One of the most prevalent autoimmune diseases is inflammatory bowel disease 
(IBD). To better understand and treat IBD, researchers sequence the RNA 
(transcriptome) of individual affected cells. However, this process is highly 
complex and expensive, making a predictive model for transcriptomics a valuable
tool in advancing research.
This challenge consisted of three independent sub-challenges, each addressing a
distinct aspect of this broader research problem:
- The task of Part 1 of this challenge was to 
  create a model that can deliver this expensive and hard to obtain 
  information from readily available pathology images.
- The task of Part 2 was to predict all genes of a cell from a (predicted) 
  subpart.
- The task of Part 3 was to rank all genes based on their ability to 
  distinguish between normal cells and ones showing dysplasia. 

**Approach**  
For task 1, we used the ResNet50 model implemented in PyTorch to directly  
map from the input images to the 460 genes (end-to-end deep learning approach).

For task 2, we took our trained ResNet50 model and its predictions, which 
served as the input to a standard neural network, which mapped from the 460 
predicted genes to all genes of the cell.

For task 3, we submitted many different approaches. Notable examples include
(i) determining the AUC value for all features, and sorting them according to 
that, and (ii) predicting the cells with dysplasia with the help of a neural 
network model, for which we extracted feature importances with the 
Integrated Gradients method from the Captum library. Integrated Gradients is 
a feature importance algorithm for neural networks.


---
<br>

## **LEC Data Challenge 2023**  
> **by LEC Gmbh, Austria**  
> *July – August 2023*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white) 
![Perl](https://img.shields.io/badge/Perl-%2339457E?style=flat&logo=perl&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-%230072C6?style=flat&logo=xgboost&logoColor=white)
![GMMs](https://img.shields.io/badge/GMMs-orange?style=flat)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikitlearn&logoColor=white)

### 🏆 **1st Place / 46 Teams – 4,000€ Prize**

[Learn more about the challenge](https://www.lec.at/research-area/lec-data-challenge-2023-neu/) | [See the winners on LinkedIn](https://www.linkedin.com/posts/lec%2Eat_theresadoppelhofer-danielhebenstreit-thomasrauter-activity-7120656589488861186-S9zy?utm_source=share&utm_medium=member_desktop)

**Overview**  
The task was to develop a machine learning solution to identify 
cylinder-specific events in time-series data from large combustion engines.

**Approach**  
We trained an XGBoost algorithm to produce a model that predicted, for each  
time point, which type of issue was present, if any. As input, we used slices  
of the time course (nearest values in time). Because issues always covered  
larger continuous time windows in the training data, we afterward  
algorithmically identified regions in the XGBoost predictions where many 
issues were detected and unified them into a continuous stretch with one 
issue type.


---
<br>

## **Trigger Detection Challenge 2023**  
> **by Bauhaus-University Weimar, Germany**  
> *April – May 2023*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white) 
![Perl](https://img.shields.io/badge/Perl-%2339457E?style=flat&logo=perl&logoColor=white)
![LLMs](https://img.shields.io/badge/Transformers-green?style=flat)

[Learn more about the challenge](https://pan.webis.de/clef23/pan23-web/trigger-detection.html)

**Overview**  
A multi-label classification challenge to assign trigger warning
labels (such as violence and blood) to fanfiction documents based on their 
content.  
As I still was a beginner, I honestly was a bit overwhelmed and left the 
challenge before it ended. However, I learned a lot about the workflow on how 
to tackle such tasks.
