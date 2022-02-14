### Materials 

Materials are definitions of how a surface should be rendered, including references to textures used, tiling information, colour tints and more. The available options for a material depend on which shader the material is using.

### Shaders 

Shadersare small scripts that contain the mathematical calculations and algorithms for calculating the colour of each pixel rendered, based on the lighting input and the Material configuration.

### Textures 

Textures are bitmap images. A Material may contain references to textures, so that the Material’s shader can use the textures while calculating the surface colour of an object. 
In addition to basic colour (albedo) of an obejct’s surface, textures can represent many other aspects of a material’s surface such as its reflectivity or roughness.

### Vertext Shaders

Script that runs for each vertex of mesh and allow developer to apply transformations, where vertex in 3D space.


### Pixel Shaders

Script that runs for each fragment (three vertex) of mesh triangle that allows to apply UV / Texture coords and sample textures in order to control final color.

https://www.raywenderlich.com/5671826-introduction-to-shaders-in-unity
