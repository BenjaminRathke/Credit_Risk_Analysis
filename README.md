# Supervised Machine Learning and Credit Risk

## Overview of the analysis
The analysis is intended to determine which sampling method would be the most useful in predicting peer-to-peer credit lending risk.

* Naive Random Oversampling
  * Balanced Accuracy Score:  .6515  
  * Precision Score: .99
  * Recall Score:  .69  
  * ![NRO](NRO.PNG)  
  
* SMOTE Oversampling
  * Balanced Accuracy Score:  .6250  
  * Precision Score:  .99
  * Recall Score:  .66
  * ![SMOTE](SMOTE.PNG)  

* Cluster Centroids Resampler
  * Balanced Accuracy Score:  .5160  
  * Precision Score:  .99
  * Recall Score:  .44
  * ![ClusterCentroids](ClusterCentroids.PNG)

* SMOTEEN
  * Balanced Accuracy Score:  .6191  
  * Precision Score: .99
  * Recall Score: .54
  * ![SMOTEEN](SMOTEEN.PNG)  

* Balanced Random Forest Classifier
  * Balanced Accuracy Score:  .7836  
  * Precision Score:  .99
  * Recall Score:  .89
  * ![BRFC](BRFC.PNG)  

* Easy Ensemble AdaBoost Classifier
  * Balanced Accuracy Score:  .9250  
  * Precision Score:  .99
  * Recall Score:  .94
  * ![EEC](EEC.PNG)  

##  Summary and Model Recommendation
Ensemble models tend to have a higher accuracy score, with EasyEnsemble AdaBoost being the most accurate.
Precision scores for all models are misleading.  The models are reliable in identifying low risk (this make sense as most loans are low-risk), but not particularly good at identifying high risk.  Based on high recall scores for both high and low risk, the ensemble models work well, while the four others do not.  As illustrated by the screen shots, both Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier have high recall scores meaning that there is a higher likelihood of a correct classication as either high or low risk.

Ultimately, the Ensemble AdaBoost Classifier model has the highest (>.9) recall scores, accuracy scores, and precision scores for high risk loans.  I would recommend using this model.
