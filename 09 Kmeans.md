# K- Means
Clustering is the process of grouping elements or objects in a set, based on certain similarity. Several algorithms are available for clustering process. We discuss below one such algorithm named K- means clustering.

K- means is one among the simplest and popular clustering algorithm. K- means proceeds in such a way that the elements are assigned randomly to k clusters and the centroid (mean) is calculated for each cluster.In the next step, the elements are reassigned in such a manner that it belongs to the cluster with closest centroid. The process is iterated until two consecutive steps end up in the same assignment of elements. In R package, k-means clustering is done using the function kmeans(). Its syntax is 
kmeans(x, centers, iter.max = 10, nstart = 1, algorithm = c("Hartigan-Wong", "Lloyd", "Forgy","MacQueen"), trace=FALSE)


Here x is the data matrix. The attribute centers gives the number of clusters. If the value is a number, then a random set of distinct rows in x is chosen as the initial center. ieter.max determines the maximum number of permitted iterations. nstart gives the number of random sets to be chosen and algorithm determines the algorithm to be used.  Trace will be a logical value which produce the tracing information on the progress of the algorithm, if TRUE and vice versa.

Let us illustrate this with the help of an example. We shall calculate the k- means of the height and weight of fourteen students
Lets Create Data first
```R
RollNo<-c(1,2,3,4,5,6,7,8,9,10,11,12,13,14)
Height<-c (173,160,150,161,155,172,165,170,150,163,164,166,169,171)
Weight<-c(70,66,45,60,47,68,66,77,46,69,67,69,70,80)
dfkmeans<-data.frame(RollNo,Height,Weight)
```

Since the data lies in different range, we have to normalize it. The functionscale( )is used for this purpose. 
```R
scaled_data<-scale(datak[,2:3], center = TRUE, scale = TRUE)
```
scale( ) centers and/or scales the columns of a numeric matrix. The attribute center determines whether centering should be done for the data. If center is TRUE then centering is done and vice versa. Similarly if the attribute scale determines whether scaling should be done for the centered data. If TRUE then scaling should be done for after centering and if FALSE, no scaling is done.

The function k-means( )will return an object of class kmeans with the following components:
cluster                : A vector of integers indicating the cluster to which each point is allocated.
centers               : A matrix of cluster centers.
cluster means:Coordinates of the centroid (centre) for each cluster.
whithnss:The measure of the total variance in our data set explained by the clustering. This is the difference between the squared distances of each data point to the centroid and the sum of squared distances of each cluster to the centroid. 
size: The number of points in each cluster.

Now we can apply the k-means( ) function to our scaled data. See the below statements.

```R
cluster1<-kmeans(scaled_data,2)
cluster2<-kmeans(scaled_data,3)
```

The first statement generates two clusters while the second generates three. 
We can generate plots for visualizing the result of k- means( ). 
See the following script to generate plots for the two variables cluster1 and cluster2and the obtained plot. 
In the script, function par( )enables to combine the plots of cluster1 and cluster2 in one single graph. 
The function points( ) will indicate the location of the centroid in the plot. The attribute pch of the points() function denotes
the plotting character to be used. Its value will be an integer code indicating the symbol. col attribute is meant for the color of the symbol.

```R
par(mfrow=c(2,1))
plot(scaled_data, col= cluster1$cluster, main="Plot with two clusters")
points(cluster1$centers, col = "blue", pch = 8)
plot(scaled_data, col= cluster2$cluster, main="Plot with three clusters")
points(cluster2$centers, col = "blue", pch = 8)
```
