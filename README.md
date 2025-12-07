# SizeAI - Client-Side T-Shirt Size Predictor 👕

**SizeAI** is a 100% client-side web application that uses computer vision to predict T-shirt sizes in real-time. By using a standard credit card for calibration and pose detection for body measurements, it provides accurate size recommendations without sending any images to a server.

## 🚀 Features

*   **Privacy-First**: All processing happens locally in your browser. No video or images are ever uploaded.
*   **Real-Time Computer Vision**: Utilizes TensorFlow.js and OpenCV.js for instant feedback.
*   **Smart Calibration**: Uses a standard credit card (ISO/IEC 7810) as a physical reference object.
*   **Pose Estimation**: Tracks 33 body keypoints using MediaPipe BlazePose to measure shoulder width.
*   **Responsive Design**: Works on desktop and mobile devices with a sleek, dark-mode UI.

## 🛠️ Tech Stack

*   **Frontend**: HTML5, Vanilla JavaScript
*   **Styling**: Tailwind CSS
*   **ML/CV Libraries**:
    *   [TensorFlow.js](https://www.tensorflow.org/js)
    *   [MediaPipe BlazePose](https://github.com/tensorflow/tfjs-models/tree/master/pose-detection)
    *   [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html)

## 📋 Usage

1.  **Open the App**: Simply open `index.html` in a modern web browser.
2.  **Calibrate**: Hold a standard credit card vertically against your chest. The app will detect it to calculate the scale.
3.  **Pose**: Step back until your upper body is visible. The app will measure your shoulder width.
4.  **Get Results**: Receive your estimated chest circumference and recommended T-shirt size (XS - 3XL).

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
