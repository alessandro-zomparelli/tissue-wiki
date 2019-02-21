![image](http://alessandrozomparelli.com/tissue/Tissue%20Tools.jpg)

Tessellate Tools
------
### Tessellate
Two objects must be selected. The first object will be the _Component_, while the second one (active object) will be the _Base_ object.
Generate a Tessellated object adapting the Component object to the faces of the Base object.

[Tessellate](https://github.com/alessandro-zomparelli/tissue/wiki/Tessellate)

### Dual Mesh
Automatically generates a special component used for Tessellate the active object. The generated object is a polygonal mesh derived by specific subdivision strategies.

### Refresh
Update the active Tessellated object, reloading the changes to both Base object and Component object.
### Rotate Faces
Shift the vertices order of the selected faces. The order affect the Tessellation rotation. The Tessellated object is automatically updated

Others
------
### Convert to Dual Mesh
Convert the selected meshes to polygonal dual mesh. Differently than [Dual Mesh](https://github.com/alessandro-zomparelli/tissue/wiki/Tissue-Tools#dual-mesh) operator, this operation is destructive. 

### Lattice along Surface
Two object must be selected. The first object is the object to deform, the second object (active object) is the target grid. 

A Lattice object is automatically generated around the first object and then adapted to the shape of the grid object.

The grid object should have a regular number of subdivision and a topology compatible with the structure of a Lattice (a regular grid structure).
(broken)

### UV to Mesh
Convert the active UV-map to mesh trying to preserve the original 3D model total surface area.

![image](http://alessandrozomparelli.com/tissue/UV%20to%20Mesh.png)
