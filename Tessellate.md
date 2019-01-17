The settings for the Tessellation can be defined at beginning:

![Tessellate](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20basic%20command.png)

Or also in a second moment from the panle in the _Object Data_ section of the _Properties_ frame:

![Tessellate](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20settings%20panel.png)

The main settings are:

### Animatable

The Tessellation is automatically recomputed each time that the frame changes. If you want to easily refresh, once _Animatable_ is active you can use Left and Right key in order to change the current frame.

### Refresh

Manually refresh the Tessellation reloading the changes to both Base and Component objects.

### BASE

Base object that will be tessellated. 
(Object supported are Mesh, Curve, Surface, Text)

### COMPONENT

Component object that will be multiplied and adapted to the Base object.
(Object supported are Mesh, Curve, Surface, Text)

### Use Modifiers

Apply Modifiers and Shape Keys, otherwise just the original mesh data is used.

### Fill Mode

You can chose from three different Fill strategies:

#### Quad
This is the default setting and will consider the first 4 vertices of each face as boundary for the component. This means that is the Base mesh contains triangles, then it will considered as a quad face with two coincident vertices.
On the other hand, if the Base mesh have NGon, then part of the face will be ignored.

#### Fan
This is the recommended setting for NGons. In order to make possible to Tessellate any generic polygon a triangle fan is generated connecting each side with the center. The generated triangles will be considered as special quad faces with two coincident vertices.

#### Patch
This mode works only with a mesh with quad faces and a _Subdivision Surface_ (or _Multiresolution_) modifier. The generated Tessellation will use the size of the original faces, but the smoothness of the subdivided one.
If the object have more subdivision modifiers, then only the last one is considered for the deformation. The previous modifiers will make the component smaller.
After the last Subdivision Surface other modifiers can be used, but only those modifiers that doesn't change the topology of the mesh. 

![quad-patch](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20quad%20patch%20comparison.jpg)
