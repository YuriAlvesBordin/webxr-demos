🌐 **[Live Demo](https://yuriAlvesbordin.github.io/webxr-demos/)**

---

Interactive demos of the [A-Frame](https://aframe.io) library for building 3D scenes in the browser via WebXR. Developed as an academic project for the Computer Graphics course.

<img width="1069" height="624" alt="image" src="https://github.com/user-attachments/assets/440e4cf8-cecd-4682-aaca-70ff51e62035" />

## Project Structure

```
webxr-demos/
|
+-- index.html              # Landing page with navigation between demos
|
+-- cenas/
|   +-- demo1.html          # Demo 1 - Geometric primitives with morphing
|   +-- demo2.html          # Demo 2 - Atomic model with dynamic lighting
|   +-- demo3.html          # Demo 3 - External 3D model import
|   +-- demo1-ar.html       # Demo 1 in AR (Hiro marker)
|   +-- demo2-ar.html       # Demo 2 in AR (Hiro marker)
|   +-- demo3-ar.html       # Demo 3 in AR (Hiro marker)
|
+-- docs/
|   +-- roteiro.md          # Presentation script
|
+-- .gitignore
```

---

## Running Locally

No dependencies or build steps required. Just serve the files locally:

```bash
# Python
python -m http.server 8080

# Node.js
npx serve .
```

Then open `http://localhost:8080` in your browser.

> **Note:** opening via `file://` may cause CORS errors in some browsers. A local server is recommended.

---

## Demos

### Demo 1 - Primitives Morphing

Displays native A-Frame geometric primitives (`<a-box>`, `<a-sphere>`, `<a-cylinder>`, `<a-cone>`, `<a-torus>`, `<a-torus-knot>`, `<a-icosahedron>`, and others) with automatic shape transitions every 2.8 seconds. Each swap applies a random PBR material, varying `roughness`, `metalness`, `opacity`, `emissive` and `wireframe`.

![Demo 1 - Primitives Morphing](demo_gifs/demo1.gif)

### Demo 2 - Atomic Model

Simulation of an atom with a central nucleus and electrons orbiting in three-dimensionally distributed planes. The number of electrons is configurable in real time via a slider (1 to 10). Each electron emits a colored point light and continuously transitions between colors via HSL interpolation, illuminating the nucleus and neighboring electrons.

![Demo 2 - Atomic Model](demo_gifs/demo2.gif)

### Demo 3 - 3D Model Viewer

Allows loading a `.glb`, `.gltf` or `.obj` file from the local filesystem via drag-and-drop or file picker. The model is automatically centered and scaled. The scene provides Blender-style orbit controls: drag to orbit, scroll to zoom, right-click to pan. Full touch support on mobile devices.

<img width="1069" height="624" alt="image" src="https://github.com/user-attachments/assets/fd97c5be-6ed0-4449-85db-4983722de5d0" />

---

## AR Mode

Each demo has an Augmented Reality version accessible via the **AR Mode** button inside the scene. AR is powered by the [AR.js](https://ar-js-org.github.io/AR.js/) library using **Hiro** marker tracking.

Print or display the marker below to use AR mode:

<p align="center">
  <img
    src="https://raw.githubusercontent.com/AR-js-org/AR.js/master/data/images/hiro.png"
    alt="Hiro Marker - AR.js"
    width="220"
    height="220"
  />
  <br>
  <em>Hiro Marker - point your camera at this pattern to activate AR</em>
</p>
