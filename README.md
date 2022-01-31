# steam-predictions
### Task 1: Would Play 
For the would play task, various different methods were attempted including creating a classifier combining popularity and the Jaccard similarity, and iterating through multiple types of classifiers, such as Logistic Regression and SVM. Additionally, the actual game counts were used features rather than whether they were popular or not. Lastly, the minimum and maximum achieved Jaccard similarity scores were looked at.

The method achieving the highest accuracy was to use a collaborative filtering strategy where the delineator was the average Jaccard similarity rating. The threshold value was optimized to find the best accuracy, with the best value being 9.0×10^(-3). Final accuracy: 0.72050

### Task 2: Time Played 
Multiple methods were again tested for this prediction task. A simple latent factor baseline model was expanded to a complete latent factor model, but it found overfit to the training data by quite a lot and was also rather slow to train. Additionally, the Cosine and Pearson similarities were found to be unsuccessful as well. Lastly, a multitude of different regression models were tested, such as Linear Regression, Bayesian Ridge, and Elastic-Net.

In the end, a Ridge regression model using the parameters from simple latent factor model as features as well as the average time played for the specific item and the average time playing any game for that specific user. Multiple regression terms for the latent factor model were iterated through to find the one that minimized MSE, which was 3.2×10^(-5). Upon testing multiple alphas for the actual ridge regression model, it was found that an alpha of 10 was the best. Final MSE: 3.06613
