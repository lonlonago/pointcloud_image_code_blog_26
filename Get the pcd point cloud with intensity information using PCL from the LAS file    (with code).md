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

