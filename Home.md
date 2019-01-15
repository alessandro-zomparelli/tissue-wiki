Welcome to the Tissue wiki!
Tissue add-on for Blender is developed by [Co-de-iT](http://www.co-de-it.com) for promote the use of Blender in Computational Design.


**For the complete Wiki, please visit [Tissue (Blender add-on)](http://wiki.blender.org/index.php/Extensions:2.6/Py/Scripts/Mesh/Tissue)**

For news, updates or for share your works, please follow us on [Blender for Computational Design](https://www.facebook.com/groups/1396995897211561)


![tissue_graphics](https://cloud.githubusercontent.com/assets/6708848/8459408/467b74a0-201d-11e5-923c-e542bfad8ba7.jpg)

**Intallation**

For installing Tissue Add-on in Blender read <i>Installation of a 3rd party Add-on</i> on [Blender's Manual](http://www.blender.org/manual/extensions/python/add_ons.html).
After installation, you should find _Tissue_ Tab in the 3D Viewport Toolshelf.

## Tissue Tools

![image](http://alessandrozomparelli.com/tissue/Tissue%20Tools.jpg)

## Tissue Tools - Weight Paint

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


## Tissue Tools - Vertex Paint

![image](http://alessandrozomparelli.com/tissue/Tissue%20Tools%20-%20Verte%20Paint.jpg)

#### Convert to Weight
Convert Vertex Color to Vertex Group (Red Channel, Green Channel, Blue Channel, Value Channel, Invert)

![image](http://alessandrozomparelli.com/tissue/Convert%20to%20Weight.jpg)

