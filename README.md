# FROID

FROID is a pre-processing framework. It takes a $X$ dataset as input and returns an enriched version ($X_a$) of itself as output. This pre-processed dataset contains a new set of features, in addition to the original ones, computed through outlier detection and feature reduction techniques. 
The returned output can then be used as training for classification models. 
The main purpose of FROID is to solve cases of unbalanced learning, not employing any rebalancing techniques and so not changing the original number of available data. Through FROID, the aim is to increase data dimensionality by including useful scores and projections for distinguishing between classes, allowing models to compute more accurate hypotheses.

![image](https://user-images.githubusercontent.com/52006312/178043583-df04fd70-12e9-4b3f-8429-7bf8a88b8a45.png)

FROID has the structure of a black box: taken as input a dataset, several generation workflows are applied to it. Each of them computes a set of supporting features, following different strategies that sequentially combine outlier detection and feature reduction algorithms. 
The output of this extraction phase is represented by ten datasets. each of them describes the original instances from different perspectives, intending to bring as much information as possible to the subsequently trained models.
Some datasets, as mentioned earlier, are in the form of vectors of real numbers, representing outlierness scores. The higher the score is, the more the algorithm has associated with the single instance a significant chance of being an outlier via its decision function. 

In addition, these algorithms also allow the binary prediction to be output: thus, also totally binary datasets are generated. Their presence might seem redundant within the numeric ones, but their binary nature allows for further arrangement of instances in the hyperplane, resulting in different results obtained by applying, for example, features reduction algorithms.

#DETAILS

All theoretical and implementation details can be found in the attached dissertation [Thesis_Lusito.pdf](https://github.com/SalvatoreLusito/FROID/files/9074137/Thesis_Lusito.pdf)
