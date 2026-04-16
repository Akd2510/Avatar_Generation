IPL Avatar Pipeline
A computer vision pipeline that performs high-fidelity face swaps onto IPL player templates. This project uses MediaPipe for landmark detection and OpenCV for advanced seamless blending and color harmonization.

Features
Hybrid Poisson Blending: Combines NORMAL_CLONE and MIXED_CLONE to maintain sharp facial details (like glasses) while matching skin tones perfectly.

Histogram Matching: Dynamically aligns the color and luminance of the input face to the stadium lighting of the template.

Geometric Gating: Automatically rejects side-profile photos to ensure optimal front-facing results.

Delaunay Triangulation: Precise face warping to match the underlying head geometry.

Installation
Clone the repository:

Bash
git clone git@github.com:your-username/IPL-Avatar-Pipeline.git
cd IPL-Avatar-Pipeline
Install dependencies:

Bash
pip install opencv-python mediapipe numpy scikit-image
Download Model:
Download the Face Landmarker Model (.task file) and place it in the root directory.

Usage
Place your input photo as input.jpg.

Place your player template as ipl_template.jpg.

Run the pipeline:

Bash
python main.py

Project Structure
main.py: The entry point and skin tone matching logic.

detector.py: MediaPipe landmark detection and pose validation.

masking.py: Generates smooth, rounded masks for the facial features.

transform.py: Handles Delaunay triangulation and warping.

blender.py: Advanced multi-pass Poisson blending logic.

License
MIT License. Feel free to use and modify for personal or commercial projects.
