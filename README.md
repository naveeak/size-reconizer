# SizeAI - Client-Side T-Shirt Size Predictor 👕

**SizeAI** is a 100% client-side web application that uses computer vision to predict T-shirt sizes in real-time. By using either a standard credit card or your height for calibration, it provides accurate size recommendations without sending any images to a server.

## 🚀 Features

*   **Privacy-First**: All processing happens locally in your browser. No video or images are ever uploaded.
*   **Dual Calibration Modes**:
    *   💳 **Card Mode**: Uses a standard credit card (ISO/IEC 7810) as a reference.
    *   📏 **Height Mode**: Uses your body height to estimate scale.
*   **Real-Time Computer Vision**: Utilizes TensorFlow.js and OpenCV.js for instant feedback.
*   **Pose Estimation**: Tracks 33 body keypoints using MediaPipe BlazePose to measure shoulder width.
*   **Dashboard & History**: Built-in dashboard to view past measurements and captured images.
*   **Data Persistence**: Automatically saves results to your browser's local storage (IndexedDB).
*   **Excel Export**: Export your measurement history to `.xlsx` format.
*   **Responsive Design**: Works on desktop and mobile devices with a sleek, dark-mode UI.

## 🛠️ Tech Stack

*   **Frontend**: HTML5, Vanilla JavaScript
*   **Styling**: Tailwind CSS
*   **ML/CV Libraries**:
    *   [TensorFlow.js](https://www.tensorflow.org/js)
    *   [MediaPipe BlazePose](https://github.com/tensorflow/tfjs-models/tree/master/pose-detection)
    *   [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html)
*   **Utilities**:
    *   [SheetJS](https://sheetjs.com/) (for Excel export)
    *   IndexedDB (for local storage)

## 📋 Usage

1.  **Open the App**: Simply open `index.html` in a modern web browser.
2.  **Calibrate**:
    *   **Card**: Hold a credit card against your chest.
    *   **Height**: Enter your height and step back until your full body is visible.
3.  **Pose**: Step back until your upper body is visible. The app will measure your shoulder width.
4.  **Get Results**: Receive your estimated chest circumference and recommended T-shirt size.
5.  **Save & Track**: Save your results to the dashboard, view history, and export data.

## 🔧 Installation

No build process required! This is a standalone single-file application.

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/size-ai.git
    ```
2.  Open `index.html` in your browser.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - see the [LICENSE](LICENSE) file for details.
