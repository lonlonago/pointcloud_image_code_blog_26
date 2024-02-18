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

