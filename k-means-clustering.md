# K-means clustering { use sklearn }

- Give the number of clusters you want to fix in X (data)
- For errors use "inertia" (from sklearn)
- Find random point (to be centroid)
- Calculate (Euclidean) distance of all other points - done by
kmeans itself (data visulaization)
- It automatically generate the number of clusters you wanted.
- For intertia, no. of data points = no. of clusters inertia = 0

Thus, we calculate it by finding distance from the nearest
cluster centroids, in order to determine if it was supposed
to be in another (nearer ones) cluster and not the one in which
it has currently been placed.

# Random-forest clustering
- Visualize the daa points based on attributes
- then select subsets from attributes to form decision tree

e.g. # attributes = 500
  we need to select atleast 200 attributes to form a tree
- we give the depth of the tree and the no. of tress we want
- based on this it gives us the best decision tree as the response

# Supervised Learning
- Linear Regression
- Logistic Regression
- Naive Baye's Classification
- LDA
- QDA
- SVM (Support Vector Machine)
- Neural Network Classification - Supervised/Unsupervised

---

- SVM
- PCA - Prnicipal Component Analysis
- K means-clustering (Unsupervised)
- ICA - Independent Component Analysis

### **SVM**
- Make x_0 and x_1
- Choose hyper plane randomly
- Find x_0 and x_1 that are at minimum distance from it
- Find the max out of all these mins (KKT)
- Put all points in hyperplane's equation and classify
according to > 0, < 0

### **PCA**
- Dimension Reduction
- Considering many attributes of same kind i.e correlated
- Find correlation b/w attributes and remove the ones which
are correlated
- Now you're left with principal components

