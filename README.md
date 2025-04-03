# 3D Models and Virtual Tours on the Web

This repository provides examples of using 3D models and virtual tours on the web. First, we explore technologies that can be used to generate and display 3D models of spaces and objects. Then we demonstrate techniques for creating virtual tours. Documentation summarizes technologies and applications used to create these examples.

## Creating 3D Models

An object or space can be converted into a 3D mesh using LiDAR scanning or photogrammetry. The former requires a device with a LiDAR sensor, whereas the latter relies on capturing multiple overlapping images from various angles to reconstruct the 3D geometry.

Here are some example applications for LiDAR scanning and photogrammetry.

1. [Scaniverse](3DModels/creating/scaniverse.md)
2. [Polycam](3DModels/creating/polycam.md)
3. [3D Scanner App](3DModels/creating/3d-scanner-app.md)
4. [Photogrammetry with Meshroom](3DModels/creating/meshroom.md)

## Displaying 3D Models

Three.js is one of the most widely used libraries for creating and rendering 3D content on the web. Additionally, model viewers can be used to display, inspect, and embed models in applications.

Here are some examples of how to add 3D content on the webpage or application.

1. [Three.js](3DModels/viewing/threejs.md)
2. [Sketchfab](3DModels/viewing/sketchfab.md)
3. [Clara.io](3DModels/viewing/clara-io.md)
4. [Model Viewer](3DModels/viewing/model-viewer.md)

## Virtual Tours

Here are some technologies for creating virtual tours. There are also many other platforms for creating virtual tours, for example [Koala360](https://koala360.com/).

1. [Matterport](virtualTours/matterport.md)
2. [Pannellum](virtualTours/pannellum.md)
3. [Metareal](virtualTours/metareal-virtual-tour.md)

## Documentation

Here are some notes we made during the project.

### Apps for Mobile and 3D Scanning

<details>
  <summary>Photogrammetry</summary>

- **Qlone**

  - Mobile app for Android/iOS for free with limits
  - Can make good looking 3D models around and under
  - Can generate animations and has AR functionality
  - _Needs right size printed Qlone mat under the object_

- **3D Live Scanner**
  - Mobile app for Android for free with advertisements, early access
  - Quite promising application; result depends on the phone camera features (better with a ToF sensor)
  - _VR view_
  </details>

<details>
  <summary>LiDAR</summary>

- **Scaniverse**

  - Mobile scanner app for iOS, free
  - AR view
  - _Can scan little details, but not completely_

- **3D Scanner App**

  - Mobile scanner app for iOS, free with limits
  - Can get good results with larger objects
  - Good in-app editor for trimming the model
  - _AR view_

- **Sitescape**
  - Mobile scan app for iOS, free with limits
  - Handles big files (though slow) and allows adjustments in quality and point-size to minimize file size
  - _Point-cloud data only_
  </details>

<details>
  <summary>Both Photogrammetry and LiDAR</summary>

- **Polycam**

  - Mobile app for iOS for free with limits
  - Very good LiDAR scan results with big objects
  - Cuts out small elements on LiDAR scans (helpful to remove “noise”)
  - Can get good results with photogrammetry when photos are taken around the object (good for AR)
  - Can continue scan later by extending it
  - _Result can be unexpected when trying to have a wholesome model (around and down parts)_

- **Metascan**
  - Mobile scan app for iOS free with limits
  - Can capture smaller details, though not very clearly
  - Offers a good in-app trimming editor for LiDAR scans
  - Good results with photogrammetry—but more suitable for AR
  - _AR view_
  </details>

<details>
  <summary>TrueDepth</summary>

- **Capture: 3D Scan Anything**

  - Mobile app for iOS, free
  - Very good results with small and detailed objects
  - Exports point-cloud data
  - _USDZ file data comes without colors/textures_
  - _Hard to scan objects with only the front camera_
  - _AR view, but not very useful_

- **EM3D: Ethan Makes 3D Scanner**
  - Mobile app for iOS, free with limits
  - Good results with small and detailed objects
  - Generates point-cloud data automatically into mesh data
  - Can export different file types
  - _Hard to scan objects with only the front camera; solution: use the EM3D: Mirror Saver app with a second phone as a second screen while scanning_
  </details>

<details>
  <summary>Augmented Reality</summary>

- **MyWebAR**
  - Web-app, free with limits
  - Easy interface to use 3D models to create AR content with QR codes
  - Comes with ready-to-use templates
  - _Has easy-to-follow tutorials_
  </details>

#### Common File Formats

<details>
  <summary>Mesh Data Formats</summary>

- **glTB**

  - Open 3D format for the web (JSON/ASCII)
  - Standard for web 3D models
  - Small size

- **GLB**

  - Open 3D format for the web (binary glTF)
  - Standard for web 3D models
  - Small size

- **USDZ**

  - Best for ARKit and sharing on iPhones

- **STL**
  - Untextured file used in 3D printing
  </details>

<details>
  <summary>Point-cloud Data Formats</summary>

- **XYZ**

  - Chemical file format

- **LAS**

  - Georeferenced color point-cloud, designed for the interchange and archiving of LiDAR data
  - _Open binary format_

- **E57**
  - Vendor-neutral file format for storing and exchanging three-dimensional imaging data
  </details>

<details>
  <summary>Both Mesh and Point-cloud Data Formats</summary>

- **PLY**

  - High-density color point-cloud

- **OBJ**

  - Text-based 3D model format
  - Well supported
  - _Large file size_

- **FBX**
  - Supported by most software and game engines
  - _Large file size_
  </details>

#### Model Viewers

<details>
  <summary>3D Model Viewer Web‑apps</summary>

- **Sketchfab**

  - Easy to use
  - Can sell your models on their webpage

- **clara.io**
  - Advanced editor
  - Offers many functionalities
  - _Not so easy to understand interface_
  - _Viewer won’t show hotspots with embed iframe_
  - _Viewer navigation may not work well in different browsers_
  </details>

<details>
  <summary>3D Model Viewer Libraries</summary>

- **Three.js**

  - Advanced level; build from scratch
  - Used as a base for other panorama and model viewer libraries
  - _Hard to learn; requires writing a lot of code_

- **babylon.js**

  - Advanced level; build from scratch

- **Model-viewer**
  - Easy to use
  - Comes with a web editor
  </details>

<details>
  <summary>Online 3D Model Viewers for Testing</summary>

- **Gltf-viewer**

  - With Git repository
  - Offers many control parameters for testing
  - _Accepts only glTF/GLB file format_

- **3dviewer**

  - Accepts a wide range of formats

- **Model-viewer editor**
  - More useful for a quick view
  - _Accepts only glTF/GLB file format_
  </details>

<details>
  <summary>3D Model Viewer Apps/File Converters</summary>

- **Blender**

  - Can import and export formats like OBJ, DAE, PLY, GLB, etc.
  - Cleans up virtual models
  - Can create complex 3D sculptures and animations
  - Free to use
  - _Hard to learn_

- **Meshlab**

  - Can import and export formats like OBJ, DAE, PLY, etc.
  - Cleans up virtual models
  - Can generate mesh data from point-clouds
  - Free to use
  - _Cannot export GLB_

- **Xcode**
  - Can open USDZ files (developed by Apple and Pixar Animation Studios)
  - Can export formats like OBJ, DAE, etc.
  - Free to use
  - _Only available for Mac; cannot export GLBT/GLD file format_
  </details>

#### Virtual Tours

<details>
  <summary>Professional Virtual Tour Web‑apps</summary>

- **Cupix**

  - Can generate 3D models (alternative to Matterport)

- **Metareal**

  - Can create 3D models from depth maps (alternative to Matterport)
  - Can use any 360° images to create virtual tours
  - Can customize content through an SDK
  - _Takes time to learn how to use the editor_
  - _Not always working in Safari_

- **Matterport**
  - Easy to use
  - Automatically generates high-quality 3D models and virtual tours
  - _Only works with certain cameras_
  - _Expensive (subscription plan; exports purchased separately; Showcase SDK requires production license)_
  - _Free plan is practically useless (does not allow uploading scans created with a Matterport camera to the Matterport cloud)_
  </details>

<details>
  <summary>Lightweight Virtual Tour Web‑apps</summary>

- **RoundMe**

  - Simple and easy to use

- **Momento360**
  - _Details not provided_
  </details>

<details>
  <summary>Lightweight Virtual Tour Libraries</summary>

- **Pannellum**

  - Open source panorama viewer for the web
  - Easy to use

- **Marzipano**

  - Open source panorama viewer for the web
  - Easy to use and fast
  - Includes a web editor
  - Automatically converts sphere panorama pictures to cube pictures

- **Panolens.js**
  - _Details not provided_
  </details>

<details>
  <summary>Lightweight Virtual Tour App + Depth Map</summary>

- **Krpano**
  - Can create a virtual tour from depth maps
    - _Use Everpano first to create depth maps_
    - _Use the PanocamAdder plugin with Blender to create 3D models from equirectangular panoramas (generates OBJ files)_
  - _Requires understanding of code and some coding skills for advanced customization_
  </details>

#### Converters

<details>
  <summary>Sphere to Cube Converters</summary>

- **Nadirpatch**

  - Easy to use
  - _Erases uploaded pictures after 1 hour_

- **jaxry.github.io**

  - _Details not provided_

- **Matheowis**
  - Open source
  - Can choose picture quality
  - _Pictures won’t be loaded on someone else’s server_
  </details>

#### Photo Stitching Software

<details>
  <summary>Panorama Stitching Apps</summary>

- **PTGui**

  - Easy to use, automatic
  - _Not free_

- **Easypano**

  - _Not free_

- **Hugin**
  - Free
  - _Hard to use; requires a deeper understanding of photography_
  </details>

<details>
  <summary>Photogrammetry Software</summary>

- **Meshroom**

  - High quality results
  - Easy to start with, yet fully customizable for advanced users
  - Provides extensive information about the photogrammetry pipeline
  - _Requires an NVIDIA CUDA-enabled GPU and is only available for Windows and Linux_

- **Capturingreality**
  - _Details not provided_
  </details>

#### Cameras

<details>
  <summary>Popular 3D Auto Stitching Cameras</summary>

- **Yi**
- **Insta360 One**
- **Mi Sphere**
- **Qoocam**
- **Fusion**
</details>

<details>
  <summary>360 Cameras We Used</summary>

- **Garmin Virb**

  - Auto stitching

- **Matterport Pro2**

  - Auto stitching
  - Really simple and fast to use
  - Outcome is professional
  - Automatic model and virtual tour generation
  - _Works only with the Matterport mobile app and requires a Matterport subscription_
  - _Matterport cameras are supported only with the Matterport cloud professional plan_
  - _Cannot get high-quality 360° pictures out from the cloud_
  - _In-app purchases for each virtual tour separately, even for the 3D model_
    </details>

       </details>
