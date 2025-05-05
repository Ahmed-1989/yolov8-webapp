
# YOLOv8 Real-Time Object Detection Web App

This is a browser-based web app that performs **real-time object detection using a YOLOv8 ONNX model**, directly from your webcam — including iPhone Safari.

## 🚀 How It Works

- Loads a trained `best.onnx` model using [ONNX.js](https://github.com/microsoft/onnxjs)
- Captures webcam video and processes it in real-time
- Displays bounding boxes and class labels over detected objects

## 📁 Files Included

| File         | Description                                |
|--------------|--------------------------------------------|
| `index.html` | Main web interface                         |
| `script.js`  | Inference logic and canvas drawing         |
| `style.css`  | Basic styling for layout                   |
| `best.onnx`  | Trained YOLOv8 ONNX model                  |

## 📦 Deployment via GitHub Pages

1. Create a **public GitHub repository**
2. Upload all files to the **root** of the repo
3. Go to `Settings → Pages` and:
   - Set **Source** to `main` branch, `/ (root)`
4. GitHub will give you a live URL like:
   ```
   https://yourusername.github.io/yolov8-webapp/
   ```

## 📱 Usage (iPhone or Laptop)

1. Open the link in Safari or Chrome
2. **Grant camera access**
3. Point your camera at objects — bounding boxes should appear!

## 🛠 Customization

- To change class labels, update the array in `script.js`:
  ```js
  const classNames = ['Class1', 'Class2', 'Class3'];
  ```

- Confidence threshold is adjustable inside `script.js`:
  ```js
  const confThreshold = 0.3;
  ```

## 🧠 Notes

- YOLOv8 ONNX exports must use `opset=11` and `dynamic=False` for browser compatibility
- Tested on mobile Safari and Chrome

---

Created for educational, research, and lightweight deployment use-cases.
