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

`Evaluated Metrics on Test Set`

Comparison Table:

|Model|Evaluated Accuracy|Evaluated Precision|Evaluated Recall|Evaluated Loss (BCE)|
|----|----|----|----|----|
|Base Model|0.6340|0.6093|0.7839|1.0687|
|Model 1|0.6711|0.5104|0.4805|3.0071|
|Model 2 |0.6804|0.6757|0.7161|0.6804|
|ResNet50V2|0.8170|0.8060|0.8438|0.4729|

`Evaluated Metrics on Validation Set`

Comparison Table: 

|Model|Evaluated Accuracy|Evaluated Precision|Evaluated Recall|Evaluated Loss (BCE)|
|----|----|----|----|----|
|Base Model|0.5368|0.5302|0.7891|1.1466|
|Model 1|0.5010|0.5104|0.4805|3.0071|
|Model 2 |0.6024|0.5833|0.7656|2.0314|
|ResNet50V2|0.6839|0.7156|0.6289|0.7747|

The best model of the four is definitely the ResNet50V2 model, because it scored highest in accuracy, precision, recall and loss on the test set, and in accuracy, precision, and loss on unseen data. 

Its scores on the validation set are still very low, and it was not able to beat the baseline model on recall, so there is a lot of room for improvement with this model.


## Conclusions

The models showed a lot of underfitting and in some models there were signs showing a lack of sufficient data to properly train the model. 

The pretrained ResNet502V model did significantly better than the other three when evaluated on the test set, but its scores dropped when evaluated on unseen data. 

The ResNet502V model was the better model amoung the four.


## Recommendations and Next steps

None of the models are ready for production. In the future I would increase the sample size and test out other pre-trained models. I would also train for longer epochs and probably utilize AWS or a similar service that would be better able to quickly train these models, since my system struggled with training the models without interruption.  





