---
layout: post
title: 3D Deformation
---
Free form approaches
- These methods use the voxel grids of the volume enclosing the surface as control points and define a smooth deformation function interpolating weights from the control points to the mesh vertices.
- 
cage-based approaches
- take the control points not from voxel grids but from a coarse scaffold mesh surrounding the input.
- 
vertex-based
- In these methods, the objective function for the optimization is directly defined with the mesh vertex positions, which describe geometric properties that should be preserved, such as mesh Laplacian [58,41] or local rigidity [43,33,57].
- 

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

### References
[1] Yifan, W., Aigerman, N., Kim, V., Chaudhuri, S., Sorkine-Hornung, O.: Neural
cages for detail-preserving 3d deformations (2019) 
