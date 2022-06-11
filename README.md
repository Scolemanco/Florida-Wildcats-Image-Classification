# Executive Summary
## Problem statement

**The Challenge:** Binary Image Classification for Florida Bobcats and Panthers from camera traps.


## Description of data
**Florida Wildlife Camera Trap Dataset:**

- Bobcat (2463 Images)
- Panther (2558 Images)

**Source:** 

https://www.crcv.ucf.edu/research/projects/florida-wildlife-camera-trap-dataset/


## EDA and Modeling

**Notebooks**
1. Florida Wildcats Image EDA

2. Florida Wildcats Binary Classification Models 


**Task:**
`Binary Image Classification`


**Model Performance on Validation Set:**

#### Comparison Table: Evaluated Metrics on Test Set

|Model|Evaluated Accuracy|Evaluated Precision|Evaluated Loss|
|----|----|----|----|
|Base Model|0.6538|0.6150|1.3390|
|Model 1|0.6804|0.6715|3.1976|
|Model 2 |0.5093|0.5093|0.6949|
|ResNet50V2|0.8143|0.8065|0.4788|

The best model of the four is definitely the ResNet50V2 model, because it had the best scores for accuracy, precision, and loss, even though its predictions weren't as good as the predictions from model 1.


## Conclusions

The three built models showed a lot of underfitting and in some models there were signs showing a lack of sufficient data to properly train the model. 

The pretrained ResNet502V model did significantly better than the other three when evaluated on the test set. 

The ResNet502V model outperformed the others.


## Recommendations and Next steps

None of the models are ready for production. In the future I would increase the sample size and test out other pre-trained models. I would also train for longer epochs and probably utilize AWS or a similar service that would be better able to quickly train these models, since my system struggled with training the models without interruption.  





