# TailoredAI - Team T-Shirt Size Measurement Tool 👕

**TailoredAI** is a 100% client-side web application designed for **companies and manufacturers** to measure T-shirt sizes for entire teams. Using AI-powered computer vision, it captures employee measurements and exports them to Excel for easy sharing with manufacturers.

## 🚀 Features

### Core Features
*   **Privacy-First**: All processing happens locally in your browser. No video or images are ever uploaded.
*   **Team Batch Mode**: Measure multiple employees in one session with names attached.
*   **Upper Body Detection**: Only requires upper body (head to hips) to be visible - no need to show full body.

### Calibration Modes
*   💳 **Card Mode**: Uses a standard credit card (ISO/IEC 7810) as a reference.
*   📏 **Height Mode**: Uses body height to estimate scale via torso length.

### AI & Computer Vision
*   **Real-Time Pose Estimation**: Tracks 33 body keypoints using MediaPipe BlazePose.
*   **Auto-Capture**: Automatically captures measurement when 30 samples are collected.
*   **Real-Time Pose Guidance**: Visual feedback tells users to step closer/back for optimal positioning.
*   **Progress Indicator**: Shows sample collection progress (0/30 samples).

### Results & Data
*   **3D Visualization**: See a rotating 3D model of the size in the results panel.
*   **Editable Measurements**: Correct AI-detected values if needed.
*   **Team Dashboard**: View all employee measurements in one place.
*   **Excel Export**: Export the full team list with names, sizes, and measurements for manufacturers.
*   **Session Management**: Clear all data to start a new measurement session.

## 🎯 Pose Guidance System

The app provides real-time visual feedback:
- **"👤 No Person Detected"** - Stand in front of the camera
- **"👤 Shoulders Not Visible"** - Step back until shoulders are visible
- **"📍 Show Upper Body"** - Make sure head and hips are visible
- **"⬅️ Step Back"** - You're too close to the camera
- **"➡️ Step Closer"** - You're too far from the camera
- **"✅ Perfect! Hold Still..."** - Good position, capturing samples

## 🛠️ Tech Stack

*   **Frontend**: HTML5, Vanilla JavaScript (Single-file app)
*   **Styling**: [Tailwind CSS](https://tailwindcss.com/) (CDN)
*   **ML/CV Libraries**:
    *   [TensorFlow.js](https://www.tensorflow.org/js) - ML runtime
    *   [MediaPipe BlazePose](https://github.com/tensorflow/tfjs-models/tree/master/pose-detection) - Pose estimation
    *   [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) - Card detection
*   **3D Graphics**: [Three.js](https://threejs.org/) - 3D visualization
*   **Utilities**:
    *   [SheetJS](https://sheetjs.com/) - Excel export
    *   IndexedDB - Local data storage

## 📋 Workflow for Manufacturers

1.  **Setup**: Open `index.html` in a modern web browser.
2.  **Enter Employee Name**: Type the employee's name or ID.
3.  **Calibrate**: Use Card or Height method.
4.  **Pose**: Have the employee show upper body (head to hips), arms relaxed.
5.  **Auto-Capture**: Wait for progress bar to fill (30 samples) - or click the red button for manual capture.
6.  **Review & Edit**: Verify measurements, edit if needed.
7.  **Save**: Click "Save Result" to add to the team list.
8.  **Repeat**: Measure the next employee.
9.  **Export**: Click "Export Excel" to download the team measurements file.
10. **Share**: Send the Excel file to your manufacturer.

## 📊 Excel Export Format

| Employee | Size | Chest (cm) | Shoulder (cm) | Status | Date |
|----------|------|------------|---------------|--------|------|
| John Doe | L    | 105.2      | 46.3          | AI Measured | 12/7/2024 |
| Jane Smith | M  | 98.5       | 43.1          | Manually Edited | 12/7/2024 |

## 🔧 Installation

No build process required! This is a standalone single-file application.

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/tailored-ai.git
    ```
2.  Open `index.html` in your browser.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - see the [LICENSE](LICENSE) file for details.
