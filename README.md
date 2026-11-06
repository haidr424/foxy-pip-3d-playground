# Foxy & Pip — 3D Motion Playground

A small, browser-based Three.js demo featuring original low-poly Foxy and Pip characters, a simple garden scene, and selectable walk, dance, and play animations.
The WebGL scene uses warm key and cool fill/rim lighting, soft shadows, subtle depth of field, and a restrained bloom highlight.

## Run locally

Open this folder with a static web server, such as the VS Code **Live Server** extension. The page imports Three.js and its post-processing modules from jsDelivr, so an internet connection is required.

## Controls

- Choose **Walk**, **Dance**, or **Play**.
- Drag the scene to orbit the camera.
- Scroll to zoom.
- Choose **Export 1080p video** to record a 12-second, 1920×1080 canvas video at a requested 30 fps.

The export uses the browser's `MediaRecorder` and saves MP4 only when the browser supports MP4 recording; otherwise it saves WebM. It records the rendered 3D scene, including the logo and selected motion label, but not the surrounding page controls. To avoid exhausting GPU memory, the scene is rendered at 1280×720 and upscaled to a 1920×1080 video; lighting and shadows are retained, while depth-of-field and bloom remain enabled in the interactive preview. The export file is Full HD in dimensions, but it is not natively rendered at 1080p. Actual frame rate and export support depend on the browser and device.

This is a stylized procedural prototype, not a production-ready or cinematic 3D character model. Character geometry and motion are built directly in `index.html`; no source images or generated video files are needed.
