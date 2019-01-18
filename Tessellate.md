The settings for the Tessellation can be defined at beginning:

![Tessellate](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20basic%20command.png)

Or in a second moment from the panle in the _Object Data_ section of the _Properties_ frame:

![Tessellate](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20settings%20panel.png)

## Base Settings

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

### Rotation

Different strategies can be used in order to define the rotation of the components:

#### Default

By default the rotation depends of the indexes of the vertices. If you want to manually change them you can use [Rotate Faces](https://github.com/alessandro-zomparelli/tissue/wiki/Tissue-Tools#rotate-faces)

#### Active UV

The orientation of the faces in the UV spaces will be used in order to determine the desired rotation for the component. This is the recommended strategy for controlling the orientation of the components on complex geometries.

#### Random

The rotation of the components is randomized. An additional _Seed_ parameter can be changed.

### Component Coordinates

Different coordinates can be used in order to adapting the component each face:

#### Bounds

(Default) Automatically check the size of the componet and adapt it automatically in order to fit the faces size

#### Local

Local coordinates of the component will be used. Only the vertices with coordinates within a range from 0 to 1 (in both local X and Y) will be inside the faces, the other vertices will continue outside of the face boundaries.

#### Global

As for the _Local_, but this allow to use also rotation, scale and position of the component. When Global is active it replace the _Offset_ setting because the global Z coordinates will be used instead.

### Thickness

#### Constant

The same thickness will be used for all the components.

#### Proportional

The thickness changes accordinagly to the area of the faces, tryng to keep the proportions of the component similar to the original ones.

#### Scale

Scale multiplier for the components thickness

#### Offset

Similar to the offset parameter of the _Solidify Modifier_. It can be used in order to change the position of the components according to the original surface. It doesn't work if _Global_ coordinates are used.

### Direction

#### Along normals 

(Default) The Tessellation is consistent with the vertices normal.

#### Individual Faces

The components follow an individual normal direction depending on the faces orientation. (This can generate openings if the components are designed to be connected with the neighbors) 

### Merge

Automatically merge non manifold vertices in order to have a continuous geometry.

#### Distance

Merge distance

#### Dissolve Seams

Automatically try to dissolve seams edges after the Tessellation. This allows to make the generated topology more indipendent for the original faces.

![dissolve-seams](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20Dissolve%20Seams.png)
![patterns](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20patterns.png)

### Smooth Shading

Smooth the generated geometry 

## Advanced Settings

### Limited Tessellation

It is possible to apply the tessellation only some particular faces:

#### On Selected Faces

Perform the tessellation only on the selected faces. 

#### Material ID

Perform the tessellation only on the faces with a specific Material, according to the chosen Material ID.

_If both options are used, then only faces that are both selected and have the correct Material ID will be used (AND condition)_

#### Combine unused

If the tessellation is performed only on some faces, then it combine the result with all the Base faces that have not been used.
Can be used for making decoration or holes on some part of the Base mesh.

### Data

Some additional data can be mapped from the source objects:

#### Map Vertex Groups

Automatically project all the Vertex Groups of the Base object to the generated object

#### Use Shape Keys

Keeps the component's Shape Keys with their original value. 

_If the Shape Keys from the Component object have the same name of the Vertex Groups of the Base object, then they will be automatically combined. If you don't see any effect, make sure that the Shape Keys value is set to the desired value._

![weight-shapekeys](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20Weight%20Shape%20Keys.png)

### Reiterate Tessellation

It's possible to automatically repeat the tessellation using the result of the tessellation as Base object for the next one. 
This setting can be used for generating _Branching Systems_ of _Iterative_ geometries.

#### Repeat

Set the number of iteration. Be carefull, This can generate a lot of polygons!

![branching-systems](http://www.alessandrozomparelli.com/tissue/Tessellate%20-%20branching%20systems.jpg)
