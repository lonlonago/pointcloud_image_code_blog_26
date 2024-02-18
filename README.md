PCL_common classes: (1) class pcl :: BivariatePolynomialT < real > This represents a binary polynomial and provides some functional interfaces to it. (4) class pcl :: Feature Histogram A histogram type used to calculate the mean and variance of some floating-point numbers. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 5) class pcl :: Gaussian Kernel The Gaussian Kernel class brings together all methods for computing images using Gaussian kernels, convolution, smoothing, and layer. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (6) class pcl :: PCA < PointT > Principal Component Analysis (PCA) class. The principal components are extracted by performing singular value decomposition on the covariance matrix of the center points of the input point cluster. The available data after the pca calculation are the average of the input data, the eigenvalues (in descending order) and the corresponding eigenvectors. Other methods allow projection in the feature space, reconstruction from the feature space, and updating the feature space with new data. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 Class PCL :: PiecewiseLinearFunction provides the ability to return the value of a valid piecewise linear function. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (8) class pcl :: PolynomialCalculationsT < real > provides some functionality for polynomials, such as finding roots or approximating binary polynomials. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (9) class pcl :: Poses From Matches Compute three-dimensional space transformations between points based on their corresponding relationships 

 Class PCL :: TransformationFromCorrespondences compute transformations based on corresponding 3D points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (15) class pcl :: Vector Average < real, dimension > Class for computing the weighted average and covariance matrix of a set of vectors for a given weight 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (16) struct pcl :: Correspondence Represents a match between two entities (e.g., points, descriptors, etc.). Represented by the distance between the source point cloud and the target point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  
 (17) struct pcl :: PointCorrespondence3D represents a (possible) correspondence between two 3D points in two different coordinate systems (e.g. from feature matching) (18) struct pcl :: PointCorrespondence6D represents a (possible) correspondence between two points (e.g. from feature matching) and is a 6DOF transformation. 

 ![avatar]( 2020080511193913.png) 

 These three classes are inherited relationships.  

 < 10 > struct pcl :: Interest Point represents a point set structure type with Euclidean xyz coordinates and interest values. Here is an example of this particular type: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574147483
  ```  


--------------------------------------------------------------------------------

#  I. Overview 

   The production process of the Qt dialog box interface is built by manual drag and drop, and the point cloud area growth algorithm in PCL is taken as an example to make it. 

#  Plug-in production 

 ![avatar]( 442ebfa2a8034ef69818b54e84cef7c9.png) 

 1. Copy the ExamplePlugin under the....\ plugins\ example path and modify the name to CCPointCloudProcess.  

 2. Create a window UI file, use any Qt project to create a new dialog box window, and try to set the name to be the same as the plug-in name to facilitate the unification of code specifications. 

 ![avatar]( 3f67b45adcda4fc686cdae3b14759ab0.png) 

 After creating, create a new ui folder in the CCPointCloudProcess folder and place the .ui file in the ui folder. 3. Configure the CMakeLists.txt of the ui folder 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 Note: This CMakeLists configuration is valid in CloudCompare version 2.11.2, other versions have not been tried 

 ![avatar]( 8745b00b0d9447bf87ac9f1ce61610ff.png) 

 4. Create a new src folder, and configure CMakeLists.txt CCPointCloudDlg.h and CCPointCloudDlg.cpp to compile and add code to the VS project. 

 CMakeLists.txt 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 ![avatar]( 36dadfd5d4db4be99879bcb19b5194a6.png) 

 5. Configure CMakeLists.txt CCPointCloudProcess.h and CCPointCloudProcess.cpp in the CCPointCloudProcess folder and add code in the VS project after compilation. 

 CMakeLists.txt 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 ![avatar]( 2033233635f64856b1c434a208063592.png) 

 5. To configure CMakeLists.txt in the example folder, just add new plugins on the original basis. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
#  III. Cmake compilation 

 Reference: CloudCompare secondary development (1) - get all points of the specified elevation 

>  Note: The ui file needs to be clicked to compile before it can be recognized in the code. If it is not recognized, compile it a few more times or restart VS. 

#  IV. Plug-in code 

 CCPointCloudDlg.h 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 CCPointCloudDlg.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 CCPointCloudProcess.h 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
 CCPointCloudProcess.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574168568
  ```  
#  V. Display of results 

 ![avatar]( bb1bc03575be47bbb8b7fa77c6d09e3b.gif) 



--------------------------------------------------------------------------------

 1. Quaternion and rotation matrix Quaternion to rotation matrix Rotation matrix to quaternion

 2. Euler angle and quaternion Euler angle to quaternion quaternion to Euler angle

 3. Euler angle and rotation matrix

#  First, the principle description 

##   1. Quaternions and rotation matrices 

#  II. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574129242
  ```  
#  III. Display of results 

 ![avatar]( 20210205131744162.png) 

 1. The result of the conversion tool calculation 2. The result of the code calculation  



--------------------------------------------------------------------------------

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


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm flow 

 ![avatar]( 20210522212717363.png) 

 (1) Set the maximum recursion depth. (2) Find the maximum size of the scene and build the first cube with this size. (3) Throw the unit elements into the cube that can be contained without sub-nodes in sequence. (4) If the maximum recursion depth is not reached, subdivide it into eight equal parts, and then divide all the unit elements contained in the cube into eight sub-cubes. (5) If it is found that the number of unit elements assigned to the child cube is not zero and is the same as the parent cube, then the child cube stops being subdivided, because according to the space division theory, the subdivided space must be allocated less. If the number is the same, then no matter how the number is cut, it will cause infinite cuts. (6) Repeat 3 until the maximum recursion depth is reached. (7) Get the center points of all occupied voxels. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574212342
  ```  
#  III. Display of results 

 ![avatar]( 817c98fa2d9b417ea1aef986200c00ad.png) 



--------------------------------------------------------------------------------

#  I. Introduction 

##  1. Overview 

    PCL pcl :: Point XY ZI is a data structure used to store coordinates and intensity information. When using CloudCompare to convert the point cloud in las format to pcd format, using PCL to read the point cloud in pcd format cannot obtain the intensity information (using open3d and matlab can read the intensity information). The specific reason is not yet in depth. This article gives how to use PCL to obtain the .pcd format point cloud with intensity information. 

#  Obtain from the LAS file 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252331
  ```  
#  III. Obtain a pcd point cloud with intensity from txt 

 ![avatar]( 094fcee1070b4d08b6c47e48c3dad899.png) 

 The efficiency of this method is very low. The implementation and code are also given here. First, use CloudCompare software to save the las point cloud in txt format. After saving it as txt, the last column is strength  

 Use the following code to obtain xyz and intensity: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252331
  ```  
 1482821 points in debug mode, code running time 58397.1 milliseconds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252331
  ```  
 1482821 points are directly converted with las in debug mode, code running time: 422.23 milliseconds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252331
  ```  
#  IV. Display of results 

 ![avatar]( eea78a30d5454641afb74a7c7afbfbd5.png) 

 The following is the display result of directly reading the point cloud in pcd format converted by the above code  



--------------------------------------------------------------------------------

![avatar]( 20210205122557633.png) 

 Common expressions: 1, rotation matrix (3X3): Eigen :: Matrix 3d 2, rotation vector (3X1): Eigen :: Angle Axisd rotation vector is the so-called axis angle, defined as follows:  

 3, quaternion (4X1): Eigen :: Quaternion d 4, translation vector (3X1): Eigen :: Vector 3 d 5, transformation matrix (4X4): Eigen :: Isometry 3 d 6, about the axis counterclockwise rotation angle (rad): AngleAxis (angle, axis) angle (rad) indicates that the rotation angle The default is: radian system 7, transformation matrix: Eigen :: Isometry 3 d T; T.matrix () is the transformation matrix, and the matrix () suffix is added when doing the operation; T.pretranslate () and T.rotate () can assign values to the translation part and rotation matrix, but if used in the loop, if the transformation matrix is not reset at the end, this setting will be accumulated, not overwritten. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574112247
  ```  


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

>  1. The algorithm comes from the latest paper "Symmetric Objective Function for ICP" published in 2019. 2. PCL1.11.1 version has the integration of the algorithm pcl :: registration :: TransformationEstimationSymmetricPointToPlaneLLS

##  1. Algorithm description 

   Point-to-plane ICP has a distance residue of 0 at the best alignment only when the local surface is a plane. Therefore, a symmetric version for point-to-plane ICP is proposed, combining two key ideas. First, the plane where the error is minimized is based on the surface normals of the two points in the corresponding point pair. Second, the optimization is performed in a stable coordinate system with two meshes moving in opposite directions simultaneously. These improvements make it almost impossible to increase the amount of computation per iteration, but improve the convergence of ICP. The reason for this improvement is that the symmetric objective function is minimized whenever a pair of point pairs are located on a second-order (constant curvature) surface, rather than only when these points are on the plane. Therefore, without having to explicitly calculate the second-order surface properties and Euclidean distance, some of the same benefits as the second-order distance function minimization method can be obtained. In addition to the new symmetric objective function, an alternative method of rotational linearization is introduced to simplify the optimization to a linear least squares problem, which can still solve the exact transformation when the correspondence is exact. The error reduction is greater with each iteration, and the convergence domain is increased. 

##  2. Symmetric objective function 

 ![avatar]( 20210430205836188.png) 

##  2. References 

>  [1] Rusinkiewicz S . A symmetric objective function for ICP[J]. ACM Transactions on Graphics, 2019, 38(4):1-7. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574175715
  ```  
#  III. Display of results 

 ![avatar]( 20210130191759803.png) 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

>  PCL :: SAC Segmentation core principle is RANSAC fitting plane, change a code writing method to achieve model extraction. Specific principle reference: PCL uses RANSAC fitting plane 

##  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095741245
  ```  
##  III. Display of results 

 ![avatar]( 20200702102545380.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

##  Function prototype 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225115
  ```  
   Calculate the normalized 3x3 covariance matrix and centroid for a given set of points. Normalization means that each item in the matrix is divided by the number of valid points in the point cloud. For a small number of points, or if you need to explicitly calculate the sample variance, use the scaled covariance matrix, which is the number of points used to calculate the covariance matrix. The calculation formula is:  

##  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225115
  ```  
##  III. Display of results 

 ![avatar]( 20210317203925412.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 See: PCL 3D-SIFT keypoint detection (Z-direction layer constraint) This example shows how to estimate SIFT feature points based on RGB color features, i.e. using RGB instead of the intensity layer. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574119093
  ```  
#  III. Display of results 

 ![avatar]( d52102c6ee024145884b08b05d7a585e.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##   1. Overview of the principle 

    This part of the PCL uses the alpha-shape algorithm to obtain the point cloud concave package. At the three-dimensional level, the algorithm can be imagined as a ball rolling in a pile of points, and the three points that meet the conditions will form a polygon. This condition is a "empty sphere rule" (similar to the empty circle rule), which means that the ball will not contain other points except three basic points. And the alpha value is the radius of the ball, because only three points cannot form a sphere, and this parameter needs to be matched. 

##   2. References 

>  [1] H.Edelsbrunner and D. G. Kirkpatrick and R. Seidel: On the shape of a set of points in the plane, IEEE Transactions on Information Theory, 29 (4): 551–559, 1983 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574137876
  ```  
#  III. Display of results 

 ![avatar]( f8df73b9066241339b3a3764d99e6b8f.png) 



--------------------------------------------------------------------------------

#  Overview of the method 

>  Draw lines between points using viewer- > addLine < pcl :: Point XYZ > in PCL 

 1. In order to see the nearest neighbor points more intuitively, connect all the points with the query points. Each connection needs to have its own independent ID and cannot be duplicated. Therefore, a character stream is defined to create different IDs. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574186373
  ```  
 2. The connection between the add point and the query point, the number indicates the RGB coloring of the add line 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574186373
  ```  
#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574186373
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574186373
  ```  
 ![avatar]( aa6e48f7861d40e18b4b9dd301344378.png) 



--------------------------------------------------------------------------------

#  Custom point type 

##  1. Preface 

   The PCL library itself defines many point cloud types, but if you want to use your own defined point cloud types when using it, you can implement it through a specific class/algorithm template file. 

##  2. Definition method 

   1. To add a new point type, you must first define it. For example, define a point type named MyPointType: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
   2. Then, you need to ensure that the code includes the template header implementation of the specific class/algorithm in the PCL used by the new point type MyPointType. For example, if you want to use pcl :: Pass Through. All you have to do is: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
   3. If the implementation code used is part of the PCL library, and the custom point type can be directly based on the PCL library, it is best to use explicit instantiation when defining the MyPointType type. 

>  Note: As of PCL-1.7, when customizing point types, you need to define PCL_NO_PRECOMPILE to include templating algorithms before including any PCL header files. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
 ![avatar]( f92f681a85cb40a193f3a9d46d1fda24.png) 

 Or add directly to the preprocessor: PCL_NO_PRECOMPILE  

   4. Use the macro definition of the PCL library PCL_ADD_POINT4D (there are,, and an alignment variable in it) to add the coordinates of the point cloud. 5. Use the macro definition of PCL PCL_MAKE_ALIGNED_OPERATOR_NEW ensure that the new operator is memory aligned. 6. Use the macro definition of PCL POINT_CLOUD_REGISTER_POINT_STRUCT to register the point type. 

##  3. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
#  Merge existing types 

 Packaged into std :: uint32_t rgba values, you need to use the following code: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
 To unpack the package, you need to use: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574260226
  ```  
#  Point clouds are rendered in time 

##  1. CloudCompare rendering 

 ![avatar]( c3fa2a96535e4fef94b7d199e248e349.png) 

##  2. PCL rendering 

 ![avatar]( 4841d157cddc418cafa8deeb09dc8692.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 ![avatar]( 20210516201610418.png) 

   Affine transformation is a special case of projective transformation, which is an important class of linear ensemble transformation. When the projective center plane becomes infinity, the projective transformation becomes an affine transformation.  

   The 3-latitude affine transformation has 12 degrees of freedom. Unlike the Euclidean transformation, the affine transformation only requires the rotation matrix to be an invertible matrix, not an orthogonal matrix. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574151038
  ```  
#  III. Display of results 

 ![avatar]( 20210205185617905.png) 



--------------------------------------------------------------------------------

#  I. Overview of algorithms 

   This is a template matching tutorial given on the PCL official website to illustrate how to combine some of the tools introduced in other tutorials to solve a higher-level problem of aligning a previously captured object model with some newly captured data. In this specific example, we will take a depth image containing a person and try to fit some previously captured face templates; this will allow us to determine the position and orientation of the face in the scene. 

>  The code of the official website is too long and cannot run normally. This article modifies the code of the official website to make it suitable for the mainstream version of the PCL library. https://pcl.readthedocs.io/projects/tutorials/en/latest/template_alignment.html#template-alignment 

#  Code implementation 

 AligningObjectTemplate.h 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574120712
  ```  
 AligningObjectTemplate.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574120712
  ```  
 main.cpp 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574120712
  ```  
#  III. Display of results 

 ![avatar]( 71c1b26b4c1347ec939266d16a21b59d.jpeg) 

#  IV. Relevant links 

 [1] PCL 读取、保存点云 [2] PCL 直通滤波器 [3] PCL体素滤波器 [4] PCL SAC-IA 初始配准算法 [5] PCL 计算FPFH并可视化 [6] PCL点云处理算法汇总（C++长期更新版） 

#  V. Experimental data 

 Template Matching Test Point Cloud in PCL Point Cloud Library 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview of the principle 

 ![avatar]( 20210324113107628.png) 

   In the experiment of extracting boundary points from planar point clouds, the alpha shapes algorithm proposed by Edelsbrunner H is a simple and effective algorithm for extracting boundary points quickly. It overcomes the shortcomings of the influence of the shape of point cloud boundary points, and can quickly and accurately extract boundary points. Its principle is as follows: As shown in the figure below, for a plane point cloud of any shape, if a circle of radius is, roll around it. If the radius of the rolling circle is small enough, each point in the point cloud is a boundary point; if it is appropriately increased to a certain extent, it only rolls on the boundary point, and its rolling track is the point cloud boundary.  

##  2. Detailed process 

 ![avatar]( 20210324113442723.png) 

   The specific algorithm steps are as follows: (1) For any point, the radius of the rolling circle is searched for all points within the distance point in the point cloud, which is recorded as the point set; (2) Select any point, and calculate the coordinates of the center of the circle according to the coordinates of these two points.  

 The center of the circle is the coordinate of the center of the circle in two cases where the radius is equal to two points. The coordinate calculation formula is shown in (1):     

 among them 

   (3) After removing the points in the point set, calculate the distance from the remaining points to the points respectively. If the distance from all points to or points is greater than that, it indicates that the point is a boundary point. (4) If the remaining point-to-point or point-to-point distances are all greater than that, then all points in the point set are rotated as points. If there is a point that satisfies the conditions (2) (3), it indicates that the point is a boundary point, terminates the judgment of the point, and determines the next point. If there is no such point in all the nearest neighbors, it indicates that the point is a non-boundary point. 

##  3. References 

>  [1] LIU Ke. Research on boundary extraction algorithm of planar point cloud [D]. Changsha University of Science and Technology, 2017.P51-53 [2] PCL :: Concave Hull < PointInT > class realizes alphashapese to extract the boundary of planar point cloud. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574190336
  ```  
#  III. Display of results 

 ![avatar]( 20210325091050983.png) 



--------------------------------------------------------------------------------

