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

