#  First, the principle of the algorithm 

>  For more details, please refer to the paper: Curvature Estimation of 3D Point Cloud Surfaces Through the Fitting of Normal Section Curvature PCL for PCL :: PrincipalCurvaturesEstimation This is also the method. 

##  1. Overview of the principle 

    All adjacent points of a specific point on the surface of a point cloud determine the local shape. If the curvature is estimated by surface fitting, a large error may be generated. Therefore, the contribution of the normal vector should be considered. To estimate the curvature of a point, we will only consider the contribution of one adjacent point, which is converted into the construction of a positive section curve. We will construct a normal section circle and estimate the normal curvature based on the positions and normal vectors of two points (the target point and one of its neighbors). 

##  2. Local fitting of normal curvature 

 ![avatar]( 20210430171738193.png) 

This method uses strings, adjacent normal vectors and dense circles, so we call it string normal vector method. The advantage of this method is that the normal vector of adjacent points is used to estimate the principal curvature of a point. 

##  3. Euler equation least squares fitting 

##  4. References 

>  [1] ZHANG Xiaopeng, LI Hongjun, CHENG Zhanglin. Curvature estimation of 3D point cloud surfaces through the fitting of normal section curvatures[C]. Proceedings of AsiaGraph, Tokyo, Japan, 2008:72-79. 

#  Code implementation 

 principal_curvatures_can.h 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574281563
  ```  
 principal_curvatures_can.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574281563
  ```  
 example.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574281563
  ```  
