# voxel.jscad
OpenJSCAD scripts to create and use voxel volumes

INTRO

Voxel is a 3D pixel, I made this little project to create and manipulate voxel with OpenJSCAD.


1) VOXEL_CREATE

creates voxel data (.json) from a CSG. On this example the CSG is taken from a SVG file imported to OpenJSCAD and put into a function and is used to populate volume variable.
The only parameter is Largeur (size) that is the size of the voxel unit, note that if it is too small the voxel data will become huge and the creation will take longer to complet.
When the creation is complete, the voxel data will be available on the javascript console so that it can be saved to a text file (I use .voxel extension for such files).

2) VOXEL_DISPLAY

creates a CSG from a voxel data pasted to parameter "source". To display a voxel model just paste its data to this parameter and also the size used to create it. From there it is possible to save the model as STL file and use it as any other 3D file.

3) VOXEL_SLICE

To make use of a voxel model, one can also slice it. a voxel grid is very easy to slice on any axis; it is just a matter of gathering voxels with same X or Y or Z.
To slice a voxel model, the same data that is used to display it is needed (source and size) and some more too :
- tranche (chunk size)
- hull ? (if yes render each chunk as the hull of all its voxels instead of just unioning them)

The result can be saved as SVG (or DXF).

4) VOXEL_DISPLAY_CHUNK

This little script display only the chunk corresponding to the parameter and the one before it, in order to ease the assembly chunk by chunk.

