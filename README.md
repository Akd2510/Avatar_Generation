-----

# IPL Avatar Pipeline

A computer vision pipeline that performs high-fidelity face swaps onto IPL player templates. This project uses **MediaPipe** for landmark detection and **OpenCV** for advanced seamless blending and color harmonization.

## 🚀 Features

  * **Hybrid Poisson Blending**: Combines `NORMAL_CLONE` and `MIXED_CLONE` to maintain sharp facial details (like glasses) while matching skin tones perfectly.
  * **Histogram Matching**: Dynamically aligns the color and luminance of the input face to the stadium lighting of the template.
  * **Geometric Gating**: Automatically rejects side-profile photos to ensure optimal front-facing results.
  * **Delaunay Triangulation**: Precise face warping to match the underlying head geometry.

## 🛠️ Installation

1.  **Clone the repository:**

    ```bash
    git clone git@github.com:your-username/IPL-Avatar-Pipeline.git
    cd IPL-Avatar-Pipeline
    ```

2.  **Install dependencies:**

    ```bash
    pip install opencv-python mediapipe numpy scikit-image
    ```

3.  **Download Model:**
    Download the [Face Landmarker Model](https://www.google.com/search?q=https://developers.google.com/mediapipe/solutions/vision/face_landmarker%23models) (`.task` file) and place it in the root directory.

## 💻 Usage

1.  Place your input photo as `input.jpg`.
2.  Place your player template as `ipl_template.jpg`.
3.  Run the pipeline:
    ```bash
    python main.py
    ```

## 📂 Project Structure

  * `main.py`: The entry point and skin tone matching logic.
  * `detector.py`: MediaPipe landmark detection and pose validation.
  * `masking.py`: Generates smooth, rounded masks for the facial features.
  * `transform.py`: Handles Delaunay triangulation and warping.
  * `blender.py`: Advanced multi-pass Poisson blending logic.

## ⚖️ License

MIT License. Feel free to use and modify for personal or commercial projects.

-----
