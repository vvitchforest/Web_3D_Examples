# Model-viewer + AR

[![Model-viewer + AR](../../images/elephant.jpg)]

[Model-viewer viewer](https://modelviewer.dev/)

## Info

**Model Viewer** is an open-source web component (primarily developed by Google) that makes it easy to display and interact with 3D models on a web page using just a few lines of HTML. It’s built on top of WebGL and the `<model-viewer>` tag handles a lot of the complexity that normally goes into rendering 3D on the web—things like lighting, controls, and AR support on compatible devices. This allows developers to integrate 3D content without needing knowledge of Three.js or Babylon.js.

[Model-viewer Editor](https://modelviewer.dev/editor) is a web-based tool that lets you visually customize and preview 3D models before embedding them into your website. It allows you to adjust settings like camera controls, lighting, and AR options, and then generates the code needed to display the model using the `<model-viewer>` component. This makes it easier for developers to integrate interactive 3D content without extensive coding.

### Technologies

- **Photogrammetry:**  
  Qlone mobile app for Android/iOS (free with limits)
- **Materials:**  
  Printed Qlone mat, size A4
- **Viewer:**  
  Google Model-viewer library with AR support (free)

### Working Process

- A 3D elephant figure was created with the Qlone mobile app on an Android phone.
- The model was exported as a `.glb` file.
- The model was uploaded to the Model-viewer editor, which generated the necessary code along with a poster image.
- That code was then integrated into a website to enable AR features.

### Where to Use

- E-commerce and product showcases on teh web
- Adding 3D and AR elements to a webpage, for example art or design portfolio without the need to learn Three.js
- Show an object in AR

### Webpages

- [qlone.pro](https://www.qlone.pro)
- [modelviewer.dev](https://modelviewer.dev)
- [modelviewer.dev/editor](https://modelviewer.dev/editor)
