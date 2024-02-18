#  First, the principle of the algorithm 

##  1. Algorithm overview 

   IterativeClosestPointNonLinear is an ICP variant that uses Levenberg-Marquardt to optimize the backend.  

   Introduction to Levenberg-Marquardt algorithm: [Optimization] Levenberg-Marquardt least squares optimization 

##  2. Overview of the LM model 

   The main idea of the Levenberg-Marquardt model is as follows: The objective function of the nonlinear optimal problem is defined as: where, is the nonlinear function. The first-order Taylor expansion will be performed on the previous, resulting in: where, is the derivative of about, is the amount of decline. To solve the amount of decline, a linear least squares problem needs to be constructed: To expand the square term of equation (3), in order to ensure that it does not fall too fast, a suitable damping factor is added at each iteration,

   The Leavenberg-Marquardt model has local convergence, can correctly deal with indefinite and singular matrices, and has global search characteristics. The selection of the initial position of the point cloud is not harsh, which can effectively improve the flexibility of feature point cloud extraction. 

##  3. References 

>  [1] Fitzgibbon A W. Robust registration of 2D and 3D point sets [J]. Image and Vision Computing, 2003. [2] Zeng Junfei, Yang Haiqing, Wu Hao. Adaptive Levenberg-Marquardt point cloud registration method for 3D reconstruction [J]. Computer Science, 2020, 47 (03): 137-142. [3] Liu Yi. 3D reconstruction of binocular vision scenes combined with Kinect [D]. University of Electronic Science and Technology of China, 2016. 

#  Code implementation 

 lmicp.h 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574128862
  ```  
 lmicp.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574128862
  ```  
 main.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574128862
  ```  
#  III. Display of results 

 ![avatar]( 20210305162059193.png) 

