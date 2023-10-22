---
title:       Autonome und Mobile Roboter
subtitle:    3 - Control, Locomotion, and Actuation
author:      Prof. Dr. Malte Schilling
affiliation: Autonomous Intelligent Systems Group
feedback:
  deck-id:  'mschilli-arob_03'
---



## Overview Approaches {.right}

[:include](src/reference_driving.md)

# Homogeneous Coordinates:
Homogeneous coordinates are commonly used in computer graphics and computer vision to represent points in a projective space, where points at infinity can be represented as finite points. The homogeneous coordinates for a point in 2D are typically represented as a 3-dimensional vector, denoted as 

$$\mathbf{p} = 
\begin{bmatrix} x \\ y \\ w \end{bmatrix}
$$

, where $x$ and $y$ are the Cartesian coordinates of the point, and $w$ is a scaling factor.

# Translation:

Translation is a transformation that shifts an object in a particular direction by a given distance. In homogeneous coordinates, translation can be represented as a matrix multiplication. The LaTeX equation for translation in 2D is:

$$
T = \begin{bmatrix} 1 & 0 & dx \\ 0 & 1 & dy \\ 0 & 0 & 1 \end{bmatrix}
$$

where $dx$ and $dy$ are the amounts of translation in the x-axis and y-axis respectively.

# Scaling:

Scaling is a transformation that changes the size of an object along each axis by a certain scale factor. In homogeneous coordinates, scaling can be represented as a matrix multiplication. The LaTeX equation for scaling in 2D is:

$$ 
S = \begin{bmatrix} sx & 0 & 0 \\ 0 & sy & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

where $sx$ and $sy$ are the scale factors along the x-axis and y-axis respectively.

# Rotation:

Rotation is a transformation that rotates an object about a given point or the origin by a certain angle. In homogeneous coordinates, rotation can be represented as a matrix multiplication. The LaTeX equation for rotation in 2D about the origin is:

$$ 
R = \begin{bmatrix} \cos(\theta) & -\sin(\theta) & 0 \\ \sin(\theta) & \cos(\theta) & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

where $\theta$ is the angle of rotation.

Note: These are basic equations for homogeneous coordinates and main transformation types in 2D. In practice, more complex transformations such as shearing, reflection, and perspective projection may also be used in computer graphics and computer vision.

# Rotation in 3D

Orientation in computer graphics and computer vision is often described using rotation matrices or Euler angles. In the context of homogeneous coordinates, rotation matrices are commonly used to represent orientation transformations.

A rotation matrix is a 3x3 matrix that describes a rotation transformation in 3D space. In homogeneous coordinates, a rotation matrix can be extended to a 4x4 matrix, where the upper left 3x3 sub-matrix represents the rotation transformation, and the last row and column are typically set to [0 0 0 1] to maintain homogeneous coordinates.

$$
R = \begin{bmatrix} r_{11} & r_{12} & r_{13} & 0 \\ r_{21} & r_{22} & r_{23} & 0 \\ r_{31} & r_{32} & r_{33} & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix}
$$

where $r_{ij}$ represent the elements of the $3x3$ rotation sub-matrix.

# Euler angles

Alternatively, orientation can also be represented using Euler angles, which are a set of three angles that describe a rotation around each of the three axes (typically, x-axis, y-axis, and z-axis) in a specific order. Euler angles can be converted to rotation matrices or quaternion representations for further use in transformations.

Note: It's important to keep in mind that there are different conventions for rotation order and axis order in Euler angles, which can affect the resulting orientation. Care should be taken to use the appropriate convention for a specific application or context.

# References{ .biblio}