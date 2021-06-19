### --------------------------------------------------------------------------------------------------------
# K-Means Clustering – Private vs. Public Universities
### --------------------------------------------------------------------------------------------------------
### K-Means Clustering:
- an **algorithm**:
    - based on **Unsupervised Learning**
    - to solve **Clustering problems**
    - where machines **learn without supervision**
    - **input data are unlabeled** and **output data is unknown**
    - with key **objective**:									
        - **to find structure in inputs by understanding hidden patterns** -> divide input data into distinct groups such that observations within each group are similar	
        - **to cluster unlabeled data based on their similarity** -> try to find patterns in the data, no outcome to be predicted
- **how K-Means Clustering algorithm works**:
    1. Choose a number of clusters (K) -> specify in how many clusters want to group the data or expect or want to explore
    2. Randomly assign each data point (observation) to a specific cluster
    3. Until clusters stop changing (no new clusters), repeat (iterate) the following steps:
        - 3.1 Calculate each cluster centroid by taking the mean vector of points in the cluster
        - 3.2 Iterate through these two steps:
            - 3.2.1 Re-assign each data point (observation) to the cluster whose cluster centroid is closest, using distance metric
            - 3.2.2 Re-calculate each cluster centroid
        - 3.3 Repeat steps 3.2.1 and 3.2.2 until within cluster variation cannot be reduced -> repeat until reach convergence
            - within cluster variation is calculated as the sum of the Euclidean distance between the data points (observations) in the cluster and their respective cluster centroids
- how to **choose a K value**: 
    - **K is the number of clusters** -> no easy way to choose a “best” K value
    - use the **Elbow method to choose a K value**:
        - Compute the Sum of Squared Error (SSE) for some values of K
            - SSE is the sum of the squared distance between the data points (observations) in the cluster and their respective cluster centroids
        - Choose the K value at which the SSE decreases abruptly
            - SSE decreases as K value gets larger
            - when K value increases, clusters are smaller and distortion is also smaller

### --------------------------------------------------------------------------------------------------------
### Project Objective: Clustering Universities into Private or Public
Create a model that allows to put in a few features of Universities and clusters them into two groups, Private and Public. Information about the children who have had corrective spine surgery is in the dataset 'College_Data'. The College dataset has 777 rows and 18 columns.

**Remark:** There are labels of the input data for this dataset. In this case we will use the labels to try to get an idea of how well the algorithm performed. But under normal circumstances, since K-Means clustering algorithm is an Unsupervised learning algorithm and we do not have labels, the Classification report and Confusion matrix don't truly make sense in a real world setting!

The College dataset contains the following columns:
- **Private** - A factor with levels Yes and No indicating Private or Public University (Yes=565, No=212)
- **Apps** - Number of applications received
- **Accept** - Number of applications accepted
- **Enroll** - Number of new students enrolled
- **Top10perc** - Pct. new students from top 10% of H.S. class
- **Top25perc** - Pct. new students from top 25% of H.S. class
- **F.Undergrad** - Number of full-time undergraduates
- **P.Undergrad** - Number of part-time undergraduates
- **Outstate** - Out-of-state tuition
- **Room.Board** - Room and board costs
- **Books** - Estimated book costs
- **Personal** - Estimated personal spending
- **PhD** - Pct. of faculty with Ph.D.’s
- **Terminal** - Pct. of faculty with terminal degree
- **S.F.Ratio** - Student/faculty ratio
- **perc.alumni** - Pct. alumni who donate
- **Expend** - Instructional expenditure per student
- **Grad.Rate** - Graduation rate

### --------------------------------------------------------------------------------------------------------
### Table of Contents:
1. File Descriptions
2. Technologies Used
3. Structure of Notebook
4. Executive Summary

#### 1. File Descriptions
- K-Means Clustering - Private_vs._Public_Universities.ipynb
- College_Data.csv
- README.md

#### 2. Technologies Used
- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-Learn

#### 3. Structure of Notebook
1. Import the Libraries
2. Load the Data
3. Exploratory Data Analysis
    - 3.1 Check out the Data
    - 3.2 Data Visualization
4. Data Preprocessing and Feature Engineering
    - 4.1 Identify the variables
    - 4.2 Dealing with the Non-numerical features
    - 4.3 Dealing with Outliers
    - 4.4 Cleaning the data
    - 4.5 Standardize (Scale) the values of variables
5. Create the K-Means Clustering model
    - 5.1 Create the K-Means Clustering model
    - 5.2 Choose the best K value
    - 5.3 Fit the K-Means Clustering model
    - 5.4 Plotting of clustered data
    - 5.5 Evaluate the model
        - 5.5.1 Classification report
	    - 5.5.2 Confusion matrix
    - 5.6 GridSearchCV
        - 5.6.1 Create the Grid of parameters
	    - 5.6.2 Create the GridSearchCV model (Re-create the K-Means Clustering model)
	    - 5.6.3 Train / fit the GridSearchCV model (Re-train / Re-fit the K-Means Clustering model)
	    - 5.6.4 Predictions from the GridSearchCV model (Re-predictions from the K-Means Clustering model)
	    - 5.6.5 Evaluate the GridSearchCV model (Re-evaluate the K-Means Clustering model)
	        - 1. Classification report
	        - 2. Confusion matrix

#### 4. Executive Summary
TBA
