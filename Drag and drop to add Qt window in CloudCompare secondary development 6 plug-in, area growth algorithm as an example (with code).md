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

