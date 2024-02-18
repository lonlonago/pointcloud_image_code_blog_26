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

