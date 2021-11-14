---
layout: post
title: Shape Deformation
---
Shape deformation has been a well-studied problem over the decades. It provides easy modeling by deforming existing shapes for many applications (e.g., character posing for animation, deformation transfer, shape interpolation, shape editing, simulation).

Challenges - “Intuitive deformation” how to? global change + local detail preservation

Traditional Shape Deformation - three main approaches for traditional shape deformation: surface deformation, space deformation, and skeleton skinning. 

1 - Surface deformation -  methods move the control points on the surface of the mesh by constraining surrounding vertices to move naturally towards deformation to preserve the local surface geometry for a given vertex position.  (i.e., preserving mean curvature). Those methods benefit from regularization methods such as Laplacian \cite{sorkine2004laplacian, sorkine2005laplacian} or ARAP  \cite{sorkine2007rigid}. 

- Shape is empty shell. Curve for 2D Deformation, surface for 3D Deformation.
- 

![_config.yml]({{ site.baseurl }}/images/config.png)

### References

[1] http://graphics.stanford.edu/courses/cs468-10-fall/LectureSlides/18_Deformation_1.pdf
