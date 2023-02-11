# Principal-Componet-Analysis
The idea behind the project is to implement Principle Component Analysis (PCA) to a medical data (of liver patients)and give the key variables with the help of eigen value decomposition and covariance relations.
1.Introduction

1.Background
“Principal components are the key to PCA; they represent what's underneath the hood of your data.”
Principal Component Analysis or PCA is a dimensionality reduction technique. Many non-linear dimensionality reduction techniques exist out there (Sammons Mapping) but linear methods are more mature, if more limited. 
1.	Principal Component Analysis
2.	Multidimensional Scaling
PCA minimizes low-dimensional reconstruction error, but another sensible objective is to maximize the scatter of the projection, under the rationale that doing so would yield the most informative projection (this choice is sometimes called classical scaling).
There are other methods too for linear dimensionality reduction. We have included Multidimensional scaling as it is connected with PCA. This project focuses on obtaining the principal components of a matrix. The Principal Component Analysis helps find the component of the matrix that contribute most significantly. It is used for compression of data without losing any significant information. This project uses many concepts of linear algebra thus increasing our grasp and understanding of the concepts. It also helps us in seeing how these concepts are used in the real life and how it changes our lives in ways we can’t imagine. Our group has tried to reduce the dimensions of a medical data set thus focusing on the components that really matter and even combining different components to form one singular variable. 

2.Motivation and Overview
With the ongoing situation in the world medical reports and precision of medical reports have become increasingly important. One minor mistake can cost a person’s life. For this project we decide to work on a dataset of a liver cancer victims. There are several critical variables which determine the life of the patient. In the third stage there are simply too many variables to be considered. Keeping in mind all these variables is simply not possible. This is where Principal Component Analysis comes in. It helps in reducing the dimensionality of the data set while keeping in mind that there is no significant loss of information. These cancer data set proves to be the perfect set for performing PCA. While each and every variable is equally important there are some which play a bigger role in the outcome of the health of a patient. The relation between different factors is based on a form of matrix. It analyses the data and tells us what can be clubbed together or in a crucial time even rejected for then.
Our dataset contains 584 x 11 data points to work on. With each row representing a different patient and each column representing a different factor contributing to the lung cancer.

Keywords
•	PCA (Principal Component Analysis) and data reduction
•	Eigen vectors and Eigen values
--------------------------------------------------------------------------------------------


3.Approach	
1.Description and the Approach used
The whole idea behind the project is to implement PCA to a medical data and give the key variables with the help of eigen value decomposition and covariance relations. Overall, we have taken into consideration how to find out the eigen values and the eigen vectors using the power method. Finding the covariance matrix of the given matrix. Using the covariance matrix and finding its eigen values and vectors. Applying PCA on those eigen vectors and finding the principal components. Which then finally gives us our results.

2.Explanation of the concepts used.
1.Covariance Matrix
Firstly, we create a covariance matrix with the help of the given matrix. The covariance matrix tells us about the relation between the different variables.
 
xi – Value of a data field 
yi – Value of the data field to be compared to
 x̅ – Mean of the column
 y̅ – Mean of the column

 We can use excel to help us develop the covariance matrix. The output of which is provided below. 
 

Positive numbers indicate that the two variables are positively co-dependent on each other. It means that with the increase in the value of one variable the other increases and vice versa. 

2.Eigen vectors: -
In layman’s term an eigenvector or characteristic vector of a linear transformation is a nonzero vector that changes by a scalar factor when that linear transformation is applied to it.
The scalar by which it changes is known as the eigen value.







	Here lambda denotes the eigen value of the given Eigen vector.


3.Power simulation
Next, we use the power method to find the eigen vectors and the eigen values. It returns the eigen vectors and values of the covariance matrix. It is also known as the Von Mises Iteration.
After finding the eigen vectors and the eigen values our task is to find the eigen vectors and the values which affect the data the most i.e. finding the principal components. Sorting of the eigen vectors take place then with respect to the eigen values in decreasing order. 
Last but not the least we divide each of the eigen values by the sum of eigen values and we get the weightage of each eigen values which give us our principal components.
 
If we assume  has an eigenvalue that is strictly greater in magnitude than its other eigenvalues and the starting vector has a nonzero component in the direction of an eigenvector associated with the dominant eigenvalue, then a subsequence converges to an eigenvector associated with the dominant eigenvalue.
 
Repeat the process for all the eigen values and sort them is descending order. 
	

4.Coding and Simulation
Description: - 
About the dataset: -
	The data we have taken is that of a liver patient (Indian). The purpose we are trying to achieve is to predict whether the patient has cancer or not. So, we will be using PCA on the given data set for predictive analysis.

Context: -
	Patients with Liver disease have been continuously increasing because of excessive consumption of alcohol, inhale of harmful gases, intake of contaminated food, pickles and drugs. This dataset was used to evaluate prediction algorithms in an effort to reduce burden on doctors.  
Content: -
	This data set contains 416 liver patient records and 167 non liver patient records collected from North East of Andhra Pradesh, India. The "Dataset" column is a class label used to divide groups into liver patient (liver disease) or not (no disease). This data set contains 441 male patient records and 142 female patient records. Any patient whose age exceeded 89 is listed as being of age "90". While the other columns represent the factors affecting the liver cancer patient the last column i.e. the dataset column is used to split the data into 2 halves (patient with liver disease, or no disease).



Approach of coding strategy: - 
1.	Filtering the data
The first thing to do while working with any data this big is to analyse it. While analysing the data we get to know about any null values in the data or improper values. On getting these values we can either set it to 0 or any other combination of the values in that row. We cleared the column with the string values.

2.	Forming the covariance matrix
Say for instance we have a data with ‘n’ predictor variables. Here n represents the number of columns in the data set. Here n = 9. We centre the predictors to their respective means and then get an n*n covariance matrix. This covariance matrix is then decomposed into the eigen values and eigen vectors. 
