# Predicting_promotions
Testing different classification methods to predicts promotions using a HR features
Data caveats and main results
Binary classification model comparison using synthetic data acquired here (https://www.kaggle.com/datasets/bhrt97/hr-analytics-classification). The dataset was incomplete, missing the ground truth values for the test set. Therefore, I divided the train set into chunks to create my own test set. Additionally, none of the features present in the dataset contained much information (i.e., were correlated with) the target feature: a binary feature about company promotions.

Instead of abandoning the project, I took it as a challenge to see how much I could improve classification scores with different techniques using the validation dataset. Scaling and under/oversampling were used to improve 
these scores due to the minority class status of the target feature. These approaches yielded limited results. With the non preprocessed features having equal or better results than the preprocessed ones. At the same time, 
the results serve as a good example of the well-known trade-off present in classification metrics (e.g., 'accuracy' and 'recall'), undersampling the training data resulted in a lower F1 score, with very high recall values 
(0.796) as a consequence of lowering accuracy. In this scenario, companies would face a choice between potentially overlooking 70% of future promotees, while having confidence in the suitability of the remaining 30%, or 
accurately identifying 93% of true promotees, even if it means that 3 out of 4 model predictions are incorrect. Incorporating additional features that contribute valuable information to the model could offer a viable and 
obvious solution to effectively address this classification challenge.
