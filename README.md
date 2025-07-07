# Facial‑Expression‑Recognition

A clean, modular web app for detecting emotions from facial images using modern frontend and ML pipelines. Ideal for developers building interactive computer vision experiences.

## 🔍 Description

This repo processes webcam or uploaded images to identify facial expressions like happy, sad, surprised, etc. It's built with real‑time observation and uses Intersection Observer and CSS Scroll Snap for smooth UI. The ML logic runs in-browser leveraging pre-trained models.

## 🛠️ Techniques

- **[Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)** for lazy‑loading and smooth section transitions.
- **[CSS Scroll Snap](https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-snap)** for seamless gallery scrolling.
- **Web Workers** offload model inference to avoid blocking the UI.
- **WebGL / Canvas2D** for real‑time video frame handling in [`src/script.js`](src/script.js).

## 📦 Technologies & Libraries

- [TensorFlow.js](https://www.tensorflow.org/js) – runs facial‑expression model in-browser.
- [Face API JS](https://github.com/justadudewhohacks/face-api.js) – pre‑trained face landmark detection and expression classification.
- [Bootstrap 5](https://getbootstrap.com/) – responsive UI components.
- Google Fonts: [Roboto](https://fonts.google.com/specimen/Roboto) and [Montserrat](https://fonts.google.com/specimen/Montserrat) — included in CSS.

## 🗂️ Project Structure

```
/
├── assets/
├── models/
├── src/
└── README.md
```

- **assets/** – images and icons used in the UI.
- **models/** – pre-trained TensorFlow.js model JSON and weights.
- **src/** – main application code:
  - `index.html` – UI layout and camera/video elements.
  - `styles.css` – styling including Scroll Snap and responsive design.
  - `script.js` – webcam setup, model loading, inference loop.
  - `worker.js` – Web Worker for background model execution.
