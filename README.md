# Temporal Performance Evaluation on Collaborative Filtering Algorithms
This project is a Master Thesis project and partial fulfillment of the requirements for the degree of Master of Science in Data Science and Society, Tilburg University. In this project, we evaluate 4 collaborative filtering algorithms (User-based _k_-NN, Item-based _k_-NN, Singular Value Decomposition (SVD) and SVD++ algorithms) by incorporating a sequence of training and evaluation process on expanding and dynamic dataset. The dataset we are using is the Netflix prize dataset that publicly available on [Kaggle](https://www.kaggle.com/netflix-inc/netflix-prize-data "Netflix Prize data | Kaggle"). The result of this project is dependent to this dataset. The insights from this project benefit the businesses to design and/or improve their existing Recommender Systems to provide better recommendation to the customer, thus reduce our exposure to information overload and, on a greater extent, improve our overall quality of life. We also provide the full thesis text in the [root](https://github.com/miftahulridwan/Temporal-Performance-Evaluation-CF-algorithms/blob/master/2040778_M.Ridwan_Thesis%20Submit%20FINAL.pdf) folder

## Table of Directory
1. [Dataset](https://github.com/miftahulridwan/Temporal-Performance-Evaluation-CF-algorithms/tree/master/Dataset)
2. [Figures](https://github.com/miftahulridwan/Temporal-Performance-Evaluation-CF-algorithms/tree/master/Figures)

## Abstract
In previous work on CF, researchers are mainly focused on comparing algorithms as well as proposing new and/or enhanced state-of-the-art algorithms claiming to outperform the existing ones. Experiment setting often started with splitting the data into training and test set, the algorithms are then trained and evaluated against the unseen test set. However, CF algorithms operate in a rather different setting once it is deployed in the production stage. As the number of user and the business grow over time, the algorithms should be trained periodically using all the available data to provide the user with up-to-date recommendation.
<br>

In this work, we evaluate CF algorithms on Netflix Prize dataset, by mimicking how they are deployed in production stage: incrementally updating the training and test set, as well as iteratively training and measuring the performances over the course of observation period. The algorithms are User-based _k_-NN, Item-based _k_-NN, SVD and SVD++ algorithms. By setting the update interval to monthly system update, we found that neither User-based _k_-NN nor Item-based _k_-NN algorithms' performances overlap with SVD and SVD++ algorithms. However, we found that SVD++ algorithm does not consistently outperformed SVD algorithm as previously suggested in the literature. Thus, our work indicate the urge to always perform temporal evaluation before claiming one algorithms to outperform the others.
<br>


## Environment and Library
We initially plan to deploy our code in Google Collaboratory environment. However, due to technical limitation and long processing hours needed by some algorithm, we partially run our experiment on Macbook Pro with 2.3 GHz 8-Core Intel Core i9 and 16GB of RAM. The [code](https://github.com/miftahulridwan/Temporal-Performance-Evaluation-CF-algorithms/blob/master/Thesis%20-%20Clean.ipynb) is written in Python using several libraries, namely:
1. Pandas
2. Numpy
3. Matplotlib
4. [Tqdm](https://github.com/tqdm/tqdm)
5. [Surprise](https://github.com/NicolasHug/Surprise)
