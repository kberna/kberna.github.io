---
layout: post
title: Shape Deformation
---
Shape deformation has been a well-studied problem over the decades. It provides easy modeling by deforming existing shapes for many applications (e.g., character posing for animation, deformation transfer, shape interpolation, shape editing, simulation).

Challenges - “Intuitive deformation” how to? global change + local detail preservation

Traditional Shape Deformation - three main approaches for traditional shape deformation: surface deformation, space deformation, and skeleton skinning. 

1 - Surface deformation -  methods move the control points on the surface of the mesh by constraining surrounding vertices to move naturally towards deformation to preserve the local surface geometry for a given vertex position.  (i.e., preserving mean curvature). Those methods benefit from regularization methods such as Laplacian \cite{sorkine2004laplacian, sorkine2005laplacian} or ARAP  \cite{sorkine2007rigid}. 

- Shape is empty shell. Curve for 2D Deformation, surface for 3D Deformation

2 - Space deformation - Unlike moving the vertices directly on the mesh, space deformation (a.k.a free-form deformation, cage-based) encloses the object within a cage. When the control points of the cage are deformed, the object deformed as well. Cage coordinates can be calculated in different ways such as barycentric coordinates, mean value coordinates \cite{ju2005mean}, harmonic coordinates \cite{joshi2007harmonic}, or green coordinates \cite{lipman2008green}.

- Shape is volumetric, planar domain in 2D, Polyhedral domain in 3D

3 - In skeleton skinning, deformation is rigidly (e.g., rotation, translation) defined on the first bones assuming that many objects have bones inside \cite{lewis2000pose, kavan2014direct}. Then the surface of the body deforms according to the bone. Similar to surface deformations, our method also deforms the surface of the initial parts by moving vertex points with a smooth regularization. \\

![_config.yml]({{ site.baseurl }}/images/config.png)

### References

[1] http://graphics.stanford.edu/courses/cs468-10-fall/LectureSlides/18_Deformation_1.pdf
