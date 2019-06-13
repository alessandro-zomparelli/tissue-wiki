![image](http://alessandrozomparelli.com/tissue/Tissue%20Tools%20-%20Weight%20Paint.jpg)

### Weight Generate

#### Area
Weight from Faces area (Automatic Bounds, Manual Bounds)

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Area.jpg)

#### Curvature
Weight from Curvature (Based on *Dirty Vertex Colors*)

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Curvature.jpg)

#### Weight Formula
Weight based on Vertices parameters.
Allows to use vertices coordinates and normals direction. Integer and Float sliders can be created in order to find the proper parameters more easily.

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Formula.jpg)

Inside the _Weight Formula_, the following parameters can be used. Each parameter is referred to individual vertices.

_lx, ly, lz_: Local Coordinates

_gx, gy, gz_: Global Coordinates

_rx, ry, rz_: Local Coordinates (from 0 to 1)

_nx, ny, nz_: Normal Coordinates

_w[0], w[1], w[2], ..._: Vertex Groups Values

_f1, f2, f3, f4, f5_: Float Sliders

_i1, i2, i3, i4, i5_: Integer Slider

All [Numpy mathematical functions](https://docs.scipy.org/doc/numpy-1.13.0/reference/routines.math.html) van be used in the formula.

#### Harmonic
Harmonic function based on active Weight

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Harmonic.jpg)

#### Convert to Colors
Convert active Weight to Vertex Colors

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Colors.jpg)

### Deformation Analysis

#### Edges Deformation
Generate a Vertex Group based on Edges Deformation evaluated on the Modifiers result (Deformation Modifiers and Simulations)

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Edges%20Deformation.jpg)

#### Edges Bending
Generate a Vertex Group based on Edges Bending evaluated on the Modifiers result (Deformation Modifiers and Simulations)

![image](http://alessandrozomparelli.com/tissue/Weight%20-%20Edges%20Bending.jpg)

### Weight Contour

#### Contour Curves
Generates isocurves based on Avtive Weight.

![image](http://alessandrozomparelli.com/tissue/Contour%20-%20Curves.jpg)

#### Contour Displace
Cut the mesh according to active Weight in a variable number of isocurves and automatically add a Displace Modifier.

![image](http://alessandrozomparelli.com/tissue/Contour%20-%20Displace.jpg)

#### Contour Mask
Trim the mesh according to active Weight. 

![image](http://alessandrozomparelli.com/tissue/Contour%20-%20Mask.jpg)

### Simulations

#### Reaction Diffusion
*Work in Progress* 