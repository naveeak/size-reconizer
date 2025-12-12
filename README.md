# TailoredAI - Team T-Shirt Size Measurement Tool 👕

**TailoredAI** is a 100% client-side web application designed for **companies and manufacturers** to measure T-shirt sizes for entire teams. Using AI-powered computer vision (MediaPipe BlazePose), it captures employee measurements and exports them to Excel for easy sharing with manufacturers.

## 🚀 Features

### Core Features
*   **Privacy-First**: All processing happens locally in your browser. No video or images are ever uploaded.
*   **Team Batch Mode**: Measure multiple employees in one session with names attached.
*   **Upper Body Detection**: Only requires upper body (head to hips) to be visible.
*   **AI-Powered Calibration**: Uses **Inter-Pupillary Distance (IPD)** (distance between eyes) to calibrate scale automatically. No credit cards or fixed distances required.

### Measurement Accuracy
*   **Multi-Point Measurement**: Tracks **Shoulder Width**, **Hip Width**, and **Torso Length** for precise sizing.
*   **Smart Sizing Logic**: Uses a refined formula `Chest = (Shoulder * 1.8) + (Hip * 0.7)` to account for varying body shapes (e.g., V-taper vs straight).
*   **Rotation Handling**: Detects if user is turned sideways and warns ("⚠️ Slight Turn Detected") but still allows capture to proceed.

### AI & Computer Vision
*   **Real-Time Pose Estimation**: Tracks 33 body keypoints using MediaPipe BlazePose.
*   **Auto-Capture**: Automatically captures measurement when 30 samples are collected.
*   **Dynamic Visual Feedback**:
    *   **Cyan Line**: Valid measurement.
    *   **Orange Line**: Warning (Rotated/Out of perfect range).
    *   **Magenta Line**: Hip width detected.

### Results & Data
*   **3D Visualization**: See a rotating 3D model of the size on a mannequin.
*   **Editable Measurements**: Correct AI-detected values if needed.
*   **Team Dashboard**: View all employee measurements in one place.
*   **Excel Export**: Export the full team list with names, sizes, and measurement details.
*   **Session Management**: IndexedDB storage maintains data across page reloads.

## 🎯 smart Pose Guidance

The app provides real-time visual feedback:
- **"👤 No Person Detected"** - Stand in front of the camera.
- **"👤 Shoulders Not Visible"** - Step back until upper body is in frame.
- **"⚠️ Slight Turn Detected"** - You are turned sideways; try to face forward for best accuracy (but capture continues).
- **"✅ Perfect! Hold Still..."** - Good position, capturing samples.

## 🛠️ Tech Stack

*   **Frontend**: HTML5, Vanilla JavaScript (Single-file app)
*   **Styling**: [Tailwind CSS](https://tailwindcss.com/) (CDN)
*   **ML/CV Libraries**:
    *   [TensorFlow.js](https://www.tensorflow.org/js) - ML runtime
    *   [MediaPipe BlazePose](https://github.com/tensorflow/tfjs-models/tree/master/pose-detection) - Pose estimation
*   **3D Graphics**: [Three.js](https://threejs.org/) - 3D visualization
*   **Utilities**:
    *   [SheetJS](https://sheetjs.com/) - Excel export
    *   IndexedDB - Local data storage

## 📋 Workflow for Manufacturers

1.  **Setup**: Open `index.html` in a modern web browser.
2.  **Read Instructions**: Review the positioning tips (ensure Face is visible!).
3.  **Enter Employee Name**: Type the employee's name or ID.
4.  **Position**: Stand at any comfortable distance where your **Face and Upper Body (to hips)** are visible.
5.  **Pose**: Arms relaxed at sides, looking at camera (for calibration).
6.  **Auto-Capture**: Wait for progress bar to fill (30 samples).
7.  **Review & Edit**: Verify measurements, edit if needed.
8.  **Save**: Click "Save Result" to add to the team list.
9.  **Repeat**: Measure the next employee.
10. **Export**: Click "Export Excel" to download the team measurements file.

## 📊 Excel Export Format

The export includes detailed metrics:

| Employee | Size | Chest (cm) | Shoulder (cm) | Status | Date |
|----------|------|------------|---------------|--------|------|
| John Doe | L    | 105.2      | 46.3          | AI Measured | 12/7/2024 |
| Jane Smith | M  | 98.5       | 43.1          | Manually Edited | 12/7/2024 |

*(Note: Internal data also tracks Hip and Torso measurements for future use)*

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
