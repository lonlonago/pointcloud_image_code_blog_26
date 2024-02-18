#  First, the principle of the algorithm 

##  1. Algorithm flow 

   The 4PCS algorithm is a popular registration tool in computer graphics. Given two point sets, three points are randomly selected in the point set, and then the fourth coplanar point that is far enough away from the other three points is selected according to the overlap ratio of the point set to form a coplanar four-point base; then all the four-point sets that may conform to b within a certain distance are extracted from the point set according to the affine invariant ratio, and the rigid transformation is calculated through the relationship between a and b; according to the overlap ratio test, when there are enough corresponding points in a constant number of random sampling points, the best rigid transformation matrix for completing coarse registration is obtained. 

##  2. References 

>  WANG Fei, LIU Rufei, Ren Hongwei, Chai Yongning. Multi-phase on-board laser point cloud registration using road target features [J]. Journal of Surveying and Mapping Science and Technology, 2020, 37 (05): 496-502. [2] Homepage B T.4-Conpoints gruent Sets for Robust Surface Registration [J]. [3] PCL: pcl :: registration :: FPCSInitialAlignment 

#  Code implementation 

##  1. Main parameters 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574117425
  ```  
 The maximum distance between corresponding points after registration = the average density of the point cloud 

##  2. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574117425
  ```  
#  III. Display of results 

 ![avatar]( 20201108184843190.png) 

#  IV. Relevant links 

>  The 4PCS registration algorithm is based on the RANSAC algorithm framework, which reduces the spatial matching operation by constructing and matching congruent four-point pairs, thereby speeding up the registration process. Construct a coplanar four-point set in the input point clouds P and Q of arbitrary poses, use affine invariance constraints to match the corresponding pairs that meet the conditions in the coplanar four-point set, and use LCP (Largest Common Pointset) strategy to find the four-point pair with the maximum overlap after registration to obtain the optimal matching result and complete the coarse matching of the point cloud. Related links:

Introduction to 4PCS Point Cloud Coarse Registration Algorithm 4PCS Reading Notes 4PCS 

