![avatar]( 20210205122557633.png) 

 Common expressions: 1, rotation matrix (3X3): Eigen :: Matrix 3d 2, rotation vector (3X1): Eigen :: Angle Axisd rotation vector is the so-called axis angle, defined as follows:  

 3, quaternion (4X1): Eigen :: Quaternion d 4, translation vector (3X1): Eigen :: Vector 3 d 5, transformation matrix (4X4): Eigen :: Isometry 3 d 6, about the axis counterclockwise rotation angle (rad): AngleAxis (angle, axis) angle (rad) indicates that the rotation angle The default is: radian system 7, transformation matrix: Eigen :: Isometry 3 d T; T.matrix () is the transformation matrix, and the matrix () suffix is added when doing the operation; T.pretranslate () and T.rotate () can assign values to the translation part and rotation matrix, but if used in the loop, if the transformation matrix is not reset at the end, this setting will be accumulated, not overwritten. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574112247
  ```  
