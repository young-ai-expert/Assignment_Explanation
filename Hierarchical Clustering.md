# Hierarchical Clustering

  - It is a part of unsupervised learning and has 3 types.
  
  1. Complete Link Clustering
  2. Single Link CLustering
  3. Agglomerative Clustering

### Complete Link Clustering

        This makes clusters with minimum distance, then merges the cluster by calculating the distance and finding the farthest  
        point in the clusters then it selects the minimum distance of the farthest data point which results in the creation of a 
        clusters needed, and some clusters will be removed accordingly. Complete Link Clustering is better than Single Link Clustering.
        
### Agglomerative Clustering

   #### Average Link Clustering
   
         It is going to calculate the distances between data points in two clusters by taking the average of the distances which 
         will be the distance measure.Then, it selects the cluster which has the lowest average.
        
   #### Ward's Method
   
         This is the default one in sklearn and it's the best. This tries to minimize the variance while merging the clusters which 
         calculates the central point by taking the average of all the points. The average will be the central point which then 
         calculates the distance from the central point to the other data points.
        
- Distance from the central point to the datapoints of two clusters is given by:
         
   C<sub>1</sub><sup>2</sup>+C<sub>2</sub><sup>2</sup>+C<sub>3</sub><sup>2</sup>+C<sub>4</sub><sup>2</sup>+......+C<sub>n</sub><sup>2</sup>
   
- Calculate the variance of the cluster and the distance of the points from the clusters.

   ![image](https://user-images.githubusercontent.com/78351203/123639338-b4a13300-d83d-11eb-8968-6f108d1ca26b.png)
   
    This can be done for hundreds of datapoints.

   
  
  ![image](https://user-images.githubusercontent.com/78351203/123637575-ce417b00-d83b-11eb-8e5a-96333e1f83c1.png)

         
         
