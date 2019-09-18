# OSL Text Shader
This shader allow for procedural render of text without the need of a bitmap.  
The text is attached to the mesh UVs.

![example](https://raw.githubusercontent.com/qmasingarbe/osl-shaders/master/TextShader/TextShader_example.jpg)

### Original use case
I originally wanted a procedural weight/size text on the side of containers.
Doing it procedurally allow random text to be generated for each instance of a container in the image.

### In depth explanation
First I used a houdini graph and a python script to export each character polygon to an xml file.  
You can see the houdini graph in the hip file if you want to use another font or other characters.  
The shader looks for the right letter at the UV position in the xml file and uses a simple raytracing algorithm to display the letter.  
Simple control like offset and scale are provided.

### Software and versions
The project was developed using Houdini 17.5 and Arnold HtoA 4.0.2

### Ressoures
Ray tracing part is adapted from Leander post :
https://blender.stackexchange.com/questions/105748/can-i-map-a-vector-image-on-a-mesh

Xml loading mecanism is inspired by matrixdisplay.osl from Michel J. Anders :
https://github.com/varkenvarken/osl-shaders