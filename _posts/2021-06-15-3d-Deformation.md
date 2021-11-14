---
layout: post
title: Shape Deformation
---
Shape deformation has been a well-studied problem over the decades. It provides easy modeling by deforming existing shapes for many applications (e.g., character posing for animation, deformation transfer, shape interpolation, shape editing, simulation).

Traditional Shape Deformation

Deforming objects by preserving geometric details is a challenging task. There are broadly three main approaches for traditional shape deformation: surface deformation, space deformation, and skeleton skinning. Surface deformation methods move the control points on the surface of the mesh by constraining surrounding vertices to move naturally towards deformation to preserve the local surface geometry for a given vertex position.  (i.e., preserving mean curvature). Those methods benefit from regularization methods such as Laplacian \cite{sorkine2004laplacian, sorkine2005laplacian} or ARAP  \cite{sorkine2007rigid}. Unlike moving the vertices directly on the mesh, space deformation (a.k.a free-form deformation, cage-based) encloses the object within a cage. When the control points of the cage are deformed, the object deformed as well. Cage coordinates can be calculated in different ways such as barycentric coordinates, mean value coordinates \cite{ju2005mean}, harmonic coordinates \cite{joshi2007harmonic}, or green coordinates \cite{lipman2008green}.

In skeleton skinning, deformation is rigidly (e.g., rotation, translation) defined on the first bones assuming that many objects have bones inside \cite{lewis2000pose, kavan2014direct}. Then the surface of the body deforms according to the bone. Similar to surface deformations, our method also deforms the surface of the initial parts by moving vertex points with a smooth regularization. \\


Free form approaches
- These methods use the voxel grids of the volume enclosing the surface as control points and define a smooth deformation function interpolating weights from the control points to the mesh vertices.
- 
cage-based approaches
- take the control points not from voxel grids but from a coarse scaffold mesh surrounding the input.
- 
vertex-based
- In these methods, the objective function for the optimization is directly defined with the mesh vertex positions, which describe geometric properties that should be preserved, such as mesh Laplacian [58,41] or local rigidity [43,33,57].
- 

Learning 3D Deformations - In recent years, surface deformations, space deformations, and skeleton skinning methods are combined with the learning-based methods. DeepMetaHandles \cite{liu2021deepmetahandles} uses key points as control points and uses a neural network to learn a basis function from the data. Neural Cages \cite{yifan2020neuralcage} is a cage-based method where the source shape is deformed by interpolating the new positions of its cage vertices. 3DN \cite{wang20193dn}, Groueix et al. \cite{groueix2019unsupervised} are the surface deformation (i.e. vertex-based) methods that are also based on neural networks. The neural networks also help us to handle different modalities (i.e., partial scan, image) as an input, computing features in an unsupervised way \cite{uy2020deformation}. Our method also addresses learning mesh deformations from partial scans; however, it leverages part-based geometry to capture the geometric details.


- 

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

### References
[1] Yifan, W., Aigerman, N., Kim, V., Chaudhuri, S., Sorkine-Hornung, O.: Neural
cages for detail-preserving 3d deformations (2019) 

[2] http://graphics.stanford.edu/courses/cs468-10-fall/LectureSlides/18_Deformation_1.pdf
