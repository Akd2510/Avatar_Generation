````markdown
# IPL Avatar Pipeline

A professional-grade computer vision pipeline for high-fidelity face swaps onto IPL player templates. This project utilizes **MediaPipe** for landmark detection and **OpenCV** for advanced seamless blending and color harmonization.

---

## 🚀 Key Features

* **Hybrid Poisson Blending**: Merges `NORMAL_CLONE` (for color) and `MIXED_CLONE` (for texture) to preserve sharp features like glasses while matching skin tones.
* **Histogram Matching**: Dynamically aligns the color and luminance of the input face to match the stadium lighting of the template.
* **Geometric Gating**: Automatically detects and rejects side-profile photos to ensure optimal front-facing results.
* **Delaunay Triangulation**: Precise mesh warping to align facial features with the template geometry.

---

## 🛠️ Installation

1. **Clone the repository:**
   ```bash
   git clone git@github.com:your-username/IPL-Avatar-Pipeline.git
   cd IPL-Avatar-Pipeline
````

2.  **Install dependencies:**

    ```bash
    pip install opencv-python mediapipe numpy scikit-image
    ```

3.  **Download Model:**
    Download the `face_landmarker.task` file from [MediaPipe Solutions](https://www.google.com/search?q=https://developers.google.com/mediapipe/solutions/vision/face_landmarker%23models) and place it in the project root.

-----

## 💻 Usage

1.  Place your selfie as `input.jpg`.
2.  Place the player template as `ipl_template.jpg`.
3.  Run the pipeline:
    ```bash
    python main.py
    ```

-----

## 📂 Project Structure

  * `main.py`: Pipeline entry point and statistical color matching.
  * `detector.py`: Landmark detection and pose validation.
  * `masking.py`: Generates smoothed binary masks for facial features.
  * `transform.py`: Handles Delaunay-based warping and mesh alignment.
  * `blender.py`: Advanced multi-pass Poisson blending logic.

-----

## ⚖️ License

MIT License. Created for the love of the game and computer vision.

```

