### Ensemble Learning

- Random Forests uses bagging (bootstrap aggregating) to implement ensemble learning
    - Many models are built by training on randomly-drawn subsets of data
- Boosting is an alternate technique where each subsequent model in the ensemble boosts attributes that address data mis-classified by the previous model
- A bucket of models trains several different models using training data, and picks the one that works best with the test data
- Stacking runs multiple models at once on the data, and combines the results together.


#### Advanced Ensemble Learning: Ways to Sound Smart

- Bayes Optimal Classifier
    - Theoretically the best - but almost always impractival
- Bayesian Parameter Averaging
    - Attempts to make BOC practical - but it is still misunderstood, susceptible to overfitting, and often outperformed by the simpler bagging approach
- Bayesian Model Combination:
    - Tries to address all of those problems
    - But in the end, it's about the same as using cross-validation to find the best combination of model.