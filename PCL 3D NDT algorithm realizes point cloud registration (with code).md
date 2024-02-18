#  First, the principle of the algorithm 

##  1. Algorithm overview 

   The basic idea of the NDT algorithm is to construct the normal distribution of multi-latitude variables. If the transformation parameters are the best match of the two point clouds, the probability density of the transformation points is the largest. Therefore, the optimization method is used to obtain the transformation parameters that make the sum of the probability densities the largest. 

##  2. References 

>  Original English: Biber P, Strasser W. The normal distributions transform: a new approach to laser scan matching [C]//Proceedings 2003 IEEE/RSJ International Conference on Intelligent Robots and Systems, 2003, 3:2743-2748. [1] Jing Lu, Wu Bin, Li Xianshuai. Point cloud registration method based on the fusion of SAC-IA and NDT [J]. Geodesy and Geodynamics, 2021, 41 (04): 378-381. [2] Multi-lidar external parameter automatic calibration algorithm and code examples [3] doc: How to use Normal Distributions Transform [4] PCL: pcl :: NormalDistributionsTransform This is a rare and only point cloud registration algorithm based on probabilistic model in PCL.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574113871
  ```  
#  III. Display of results 

>  Red and pink are the initial positions, and pink and green are the registered positions. 

 ![avatar]( 20200428211833407.png) 

