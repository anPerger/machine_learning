#machine_learning

This project utilizes data from NASAs Kepler Objects of Interest table identifying potential exoplanets. The dataset is made up of potential exoplanets divided into 
'Confirmed', 'False Positive', and 'Candidate' classifications along with 40 columns of readings taken by the NASA Exoplanet Science Institute. The goal of this project was to 
train a machine learning model that can predict if an exoplanet observation will turn out to be confirmed or a false positive. The first step of this was to drop all the 
'Candidates' from the dataset in order to have a good training and testing sample.

After dropping the candidates the next step was to do some feature analysis with a decision tree and random forest model. Looking at the different features in order of
importance it was clear that no individual variable was all the important and many of the variables had less than 1% of the feature importance in the random forest iteration.
Despite many of these features ranking very low in importance to the model, dropping all the features below that 1% threshold yielded virtually identical results to all
features, and further narrowing of the features only made preformance worse and worse. Because of this, I decided to include all the features in the dataset for future models.

 After the random forest analysis I experimented with various types of models such as Logistic regression, K-nearest neighbors, svc, but the most effective model was a neural
 network model that was able to predict whether an observation turned out to be confirmed or a false positive with a high degree of accuracy and very little loss.

