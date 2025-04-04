# 3D Models and Virtual Tours on the Web

This repository provides examples of using 3D models and virtual tours on the web. First, we explore technologies that can be used to generate and display 3D models of spaces and objects. Then we demonstrate techniques for creating virtual tours. Documentation summarizes technologies and applications used to create these examples.

## Creating 3D Models

An object or space can be converted into a 3D mesh using LiDAR scanning or photogrammetry. The former requires a device with a LiDAR sensor, whereas the latter relies on capturing multiple overlapping images from different angles to make a 3D geometry.

Applications for LiDAR scanning and photogrammetry:

1. [Scaniverse](3DModels/creating/scaniverse.md)
2. [Polycam](3DModels/creating/polycam.md)
3. [3D Scanner App](3DModels/creating/3d-scanner-app.md)
4. [Photogrammetry with Meshroom](3DModels/creating/meshroom.md)

## Displaying 3D Models

Three.js is one of the most widely used libraries for creating and rendering 3D content on the web. Additionally, model viewers can be used to display, inspect, and embed models in applications.

Here are some examples of how to add 3D content on the webpage or application:

1. [Three.js](3DModels/viewing/threejs.md)
2. [Sketchfab](3DModels/viewing/sketchfab.md)
3. [Clara.io](3DModels/viewing/clara-io.md)
4. [Model Viewer](3DModels/viewing/model-viewer.md)

## Virtual Tours

Some example virtual tours:

1. [Matterport](virtualTours/matterport.md)
2. [Pannellum](virtualTours/pannellum.md)
3. [Metareal](virtualTours/metareal-virtual-tour.md)

There are also many other platforms for creating virtual tours, for example [Koala360](https://koala360.com/).

## Documentation

###3D Models

<details>

  <summary>Mobile Apps</summary>

**Photogrammetry**

- **Qlone**
  - Mobile app for Android/iOS, free with limits
  - Can generate animations and has AR functionality
  - Needs right size printed Qlone mat under the object

**LiDAR scanning**

- **Scaniverse**

  - Mobile scanner app for iOS and Android, free
  - AR view
  - Can scan little details

- **3D Scanner App**

  - Mobile scanner app for iOS, free with limits
  - In-app editor for trimming the model
  - AR view

- **Sitescape**
  - Mobile scan app for iOS, free with limits
  - Handles large files (although slow)
  - Allows adjustments in quality and point size
  - _Point-cloud data only_

**Both Photogrammetry and LiDAR**

- **Polycam**
  - Mobile app for iOS and Android, free with limits
  - Very good LiDAR scan results with large objects
  - Cuts out small elements on LiDAR scans (helpful to remove “noise”)
  - Can get good results with photogrammetry when photos are taken around the object

</details>

<details>
  <summary>Common File Formats</summary>

- **FBX**

  - Developed by Autodesk
  - Supports meshes, materials, textures, and animation
  - Common in game development, animation, and visual effects
  - Supported by most software and game engines
  - Proprietary format, large file size

- **glTF** (Graphics Library Transmission Format)

  - Open standard developed by Khronos Group
  - Standard file format for 3D scenes and models
  - Two file extensions: .glTF (JSON/ASCII) and .glb (binary)
  - Widely used on the web
  - Small size, optimized for fast transmission
  - Supports physically-based rendering (PBR)
  - Extensible for animations, scenes, metadata

- **LAS**

  - Developed by ASPRS (American Society for Photogrammetry and Remote Sensing)
  - Standard format for storing LiDAR point-cloud data
  - Includes geospatial coordinates, intensity, color, classification info
  - Used in mapping, surveying, and remote sensing

- **OBJ** (Wavefront Object)

  - Text-based format for 3D geometry
  - Stores vertices, normals, texture coordinates, and faces
  - Uses .mtl files for materials
  - Widely supported
  - Large file size

- **PLY**

  - Stores 3D data as a list of vertices and faces, with optional properties like color
  - Can be ASCII (readable) or binary (compact)
  - Used for 3D scanning and point-clouds
  - Supports mesh and point-cloud data

- **STL**

  - Standard format for 3D printing
  - Contains only geometry (no textures or colors)
  - Common in prototyping and manufacturing workflows

- **USDZ** (Universal Scene Description Zip)
  - Developed by Apple and Pixar
  - Compressed format including geometry, materials, textures, animations
  - Optimized for AR on iOS devices (ARKit)
  - Supports PBR and easy sharing across platforms

</details>

<details>
  <summary>Model Viewers</summary>

- **Gltf Viewer**

  - Open-source web tool for inspecting glTF/glb models

- **3D Viewer**

  - Accepts a wide range of 3D file formats
  - Useful for quick previews

- **Model Viewer**
  - Web editor based on `<model-viewer>`
  - _Accepts only glTF/GLB formats_

</details>

<details>
  <summary>Libraries & Frameworks</summary>

- **Three.js**

  - JavaScript library for creating and rendering 3D graphics in the browser using WebGL
  - Widely used for 3D experiences, games, and visualisations
  - Supports scenes, lighting, cameras, animation, physics, and more
  - Requires JavaScript knowledge and manual setup

-- **Babylon.js**

- JavaScript engine for building 3D games and interactive web applications
- Supports advanced features like physics, animations, and PBR materials
- Comes with a visual editor and extensive documentation
- Great for developers focused on game-like experiences

- **Model-viewer**
  - Lightweight library for displaying 3D models in the browser
  - Simple to set up and ideal for non-developers
  - Supports AR on compatible devices
  - Includes a web-based editor for customizing settings and generating embed code

</details>

### Virtual Tours

<details>
<summary>Lightweight Virtual Tour Web Tools</summary>

- **Koala360**

  - Platform for creating and sharing interactive 360° virtual tours
  - Used for example in real estate, tourism, education
  - Tours can include hotspots, info panels, and media
  - No coding required

- **Momento360**  
  -A web-based platform for displaying and embedding 360° photos
  -Great for making panoramic content quickly, or building simple virtual tours
  -No coding required

</details>

<details>
<summary>Lightweight Virtual Tour Libraries</summary>

- **Pannellum**  
  -Open source panorama viewer for the web  
  -Easy to use

- **Marzipano**  
  -Open source panorama viewer for the web  
  -Easy to use  
  -Includes a web editor  
  -Automatically converts spherical panoramas to cube format

</details>

<details>
<summary>Professional Virtual Tours</summary>

- **Matterport**  
  -Professional platform for creating immersive 3D virtual tours and spatial models
  -Automatically generates high-quality tours and mesh models from 360° scans  
  -Requires a compatible Matterport camera and cloud processing
  -Offers features like MatterTags, floor plans, and measurement tools
  -Expensive! (Exporting models or using developer tools (API, SDK) requires additional licenses or fees)

- **Metareal**  
  -A browser-based platform for building 3D virtual tours and models using 360° images
  -Can use any camera
  -Supports creation of 3D models from depth maps and offers editing environment
  -Includes an SDK for custom feature development.  
  -Has a learning curve, especially for advanced editing tools
  _Note: During testing, the editor was not fully working in Safari._

- **Krpano**  
  A powerful tool for building virtual tours from 360° images and depth maps.  
  Supports advanced features like 3D transitions and integration with custom plugins.  
  Requires some coding knowledge for customization and more complex setups.

</details>

### Converters

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

### Photo Stitching Software

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

### Cameras

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
