# RayTracer
Ray Tracer written in C++ with only GLM lib (No OpenGL or other libraries). <br/>
(GLM lib is used for matrix operations) <br/>
Program Last modified: 2019-03-18 <br/>

# Authors
[Vince Li](https://github.com/vince1114) <br/>
[Rix Lai](https://github.com/rixktl)

# How it works
This program reads an input file that contains details of each objects. <br/>
For instance, material property (specular, shininess, ambient, diffuse), <br/>
location of the objects (before trasnformation), transformation (scale, rotate, translate), <br/>
light sources, image dimension and eye location. <br/>

The program perform ray tracing by shooting ray from eye, and compute color based on <br/>
object intersection. In our implementation, each pixel on the image is computed by <br/>
one corresponding ray. We have also implemented recursive ray tracing for computing <br/>
reflections. <br/>

To accelerate our computation, we have implemented a basic uniform grid acceleration <br/>
structure. We partition the space by uniform grids and maintain a list of object that <br/>
intersects with each of the grids. We have used unordered map to enable quick lookup from <br/>
coordinate(grid) to the the corresponding list of objects. As the rays progress through space, <br/>
we check for the intersecting grid and its objects. This provides significant speed up for scene 7. <br/>
Scene 7's render time reduces from 1 hour to 15 minutes.

# Where is the code
We do not have the permission to publish our code because of course policy. <br>
However, we are able to publish the images we have rendered. The input files <br/>
are given from CSE 167 course at UCSD.

# Images
![scene4](https://github.com/rixktl/RayTracer/blob/master/scene4-specular.png)
![scene5](https://github.com/rixktl/RayTracer/blob/master/scene5.png)
![scene6](https://github.com/rixktl/RayTracer/blob/master/scene6.png)
![scene7](https://github.com/rixktl/RayTracer/blob/master/scene7.png)
