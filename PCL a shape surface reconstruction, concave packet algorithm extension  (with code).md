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

