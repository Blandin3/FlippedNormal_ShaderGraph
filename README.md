# Simulating Flipped Normals on an Object using Shader Graph

## Overview

This project demonstrates how to simulate flipped normals on a 3D object using Unity's Shader Graph. Instead of modifying the mesh geometry, the shader manipulates the normal vectors to create the appearance of inverted surface normals, allowing observation of how lighting and rendering are affected.

## Objectives

* Create a custom Shader Graph.
* Sample and apply a texture to an object.
* Manipulate the object's normal vectors.
* Simulate flipped normals through shader operations.
* Apply the shader to a material and observe the visual result.

## Technologies Used

* Unity 6 (6000.3.16f1)
* Universal Render Pipeline (URP)
* Shader Graph

## Project Structure

```
Assets/
├── Materials/
├── Shaders/
│   └── FlippedNormals.shadergraph
├── Textures/
└── Scenes/
```

## Shader Graph Components

### Texture

* PanoramaTexture (Texture2D Property)
* Sample Texture 2D

### Normal Manipulation

* Normal Vector
* Multiply Node
* Float (-1)

### Material Output

* Base Color
* Smoothness (0.8)
* Metallic (Default)

## Implementation Steps

1. Created a new URP Lit Shader Graph.
2. Added a Texture2D property named **PanoramaTexture**.
3. Sampled the texture using the Sample Texture 2D node.
4. Connected the RGBA output to the Base Color input.
5. Added a Normal Vector node.
6. Used a Multiply node to invert the normal direction.
7. Applied a Smoothness value of 0.8.
8. Saved the shader and created a material using it.
9. Assigned the material to a 3D object.
10. Tested the lighting response to verify the flipped normal effect.

## Expected Result

The object displays the applied texture while the manipulated normals alter the way lighting interacts with the surface, creating the appearance of flipped normals.

## Author

Blandine Iradukunda
