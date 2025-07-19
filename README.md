# ⚽ Football In-Depth Video Analysis 📊

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()
[![Made with Python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

This application provides advanced video analysis tools tailored for football analysts and developers. 👨‍💻 It enhances raw football footage, providing insights through automated processing and visualization. ⚙️ This allows for detailed examination of player movements, tactical formations, and key moments within a game. 🔍

## Table of Contents
- [Directory Structure](#directory-structure)
- [Key Findings](#key-findings)
- [Data Sources](#data-sources)
- [Features](#features)
- [Installation](#installation)
- [Setup and Execution](#setup-and-execution)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Contribution Guidelines](#contribution-guidelines)
- [Troubleshooting](#troubleshooting)
- [License](#license)
- [Contact](#contact)

## Directory Structure📁

<pre>
└── daxgupta-football_in-depth_video_analysis/
    ├── README.md
    ├── main.py
    ├── yolo_custom.ipynb
    ├── yolo_inference.ipynb
    ├── camera_movement_estimator/
    │   ├── __init__.py
    │   └── camera_movement_estimator.py
    ├── development_and_analysis/
    │   └── color_assignement.ipynb
    ├── models/
    │   └── Link to download file under moodels.txt
    ├── output_video/
    │   └── Link to download files under output_video.txt
    ├── player_ball_assigner/
    │   ├── __init__.py
    │   └── player_ball_assigner.py
    ├── runs/
    │   └── Link to download all the files and folders under runs.txt
    ├── speed_and_distance_estimator/
    │   ├── __init__.py
    │   └── speed_and_distance_estimator.py
    ├── stubs/
    │   ├── camera_movement_stub.pkl
    │   └── track_stubs.pkl
    ├── team_assigner/
    │   ├── __init__.py
    │   └── team_assigner.py
    ├── trackers/
    │   ├── __init__.py
    │   └── tracker.py
    ├── training/
    │   └── Football_video_analysis.ipynb
    ├── utils/
    │   ├── __init__.py
    │   ├── bbox_utils.py
    │   └── video_utils.py
    └── view_transformer/
        ├── __init__.py
        └── view_transformer.py
   </pre>

## Project Overview

**This project automates football match analysis using computer vision. It reads video, detects and tracks players, balls, and referees via a pre-trained model `(models/best.pt)`, then generates annotated output video. The system also extracts player positions and calculates their speeds for each frame, providing a foundation for advanced tactical and performance insights. The goal is to streamline video review, saving time, and enhancing game understanding. It leverages Python, OpenCV, and a custom tracking system for efficient and accurate analysis.**

## Key Findings🕵

**Provide a summary of the key findings or insights derived from the video analysis.  This section should highlight the most important results that the application helps uncover. For example:**

  *   Improved understanding of team formations and player positioning.
  *   Quantifiable metrics for player speed, distance covered, and tactical efficiency.
  *   Identification of critical moments and patterns in the game.

## Data Sources🗄

**Describe the data sources used for the video analysis.  This should include the type of video footage, any external data sources used (e.g., player statistics), and how the data is preprocessed. For example:**

  *   Input video footage: `Describe the source and characteristics of the video footage, e.g., resolution, frame rate, camera angles.`
  *   Player statistics: `If applicable, describe the source of player statistics and how it's integrated.`
  *   Preprocessing steps: `Outline any preprocessing steps applied to the video or external data.`

## Features✨

*   **Automated Player Tracking:** 🏃‍♂️ Identifies and tracks players throughout the video.
*   **Tactical Formation Analysis:** 📐 Analyzes and visualizes team formations.
*   **Event Detection:** 💥 Automatically detects key events like passes, shots, and tackles.
*   **Enhanced Visualization:** 📈 Overlays data and visualizations onto the original video to highlight important information.
*   **Before-and-After Comparison:** 🖼️ Demonstrates the enhancement achieved through video processing.

This is the input video file pic before processing:
![Before Processing](https://github.com/user-attachments/assets/4c15cb70-a9ab-4294-b16b-d368e23993d6)

This is the output video file pic after processing:
![After Processing](https://github.com/user-attachments/assets/f8cae508-d46c-4a93-b7c7-a827e90ff0b2)

## Installation💻

1.  **Clone the repository:**
> `git clone [repository_url]`
2.  **Navigate to the project directory:**
> `cd daxgupta-football_in-depth_video_analysis`
3.  **Install the required dependencies:**
> `pip install -r requirements.txt` (if a requirements file is available) or install dependencies manually.

## Setup and Execution

**Provide detailed instructions on setting up the project and executing the main script. Include steps for configuring the environment and running the analysis. For example:**

   1.  **Environment Configuration:**
        *   Set up a virtual environment (recommended): `python -m venv venv`
        *   Activate the virtual environment: `source venv/bin/activate` (Linux/macOS) or `venv\Scripts\activate` (Windows)
   2.  **Configuration File:**
        *   Ensure the `config.ini` file is properly configured with the correct paths to the input video, output video, and model files.
   3.  **Model Download:**
        *   Download the model file from the link provided in `models/models.txt` and place it in the appropriate directory.
   4.  **Execution:**
        *   Run the main script with the necessary arguments: `python main.py --input_video [path_to_input_video] --output_video [path_to_output_video] --config [path_to_config_file]`

## Dependencies🧩

*   Python 3.7+ 🐍
*   OpenCV 📸
*   TensorFlow or PyTorch (depending on the model) 🧠
*   NumPy 🔢
*   [List any other specific Python packages]

> List any specific versions of the dependencies if required for compatibility.

Model file is linked in `models/models.txt`. 🔗

## Usage🚀

*   `--input_video`: Path to the input video file. 📹
*   `--output_video`: Path to the output video file. 🎬
*   `--config`: Path to the configuration file (optional, defaults to `config.ini`). ⚙️

    Example:

*   **Input:** The application primarily supports `.mp4` video files. Other common formats like `.mov` and `.avi` might work but are not guaranteed. 🎥
*   **Output:** The processed video is output as an `.avi` file by default. This can be configured in the `config.ini` file. 📤

> Note that using other video formats might require installing additional codecs.

## Contribution Guidelines🤝

1.  Fork the repository. 🍴
2.  Create a new branch for your feature or bug fix. 🌿
3.  Make your changes and commit them with descriptive messages. ✍️
4.  Submit a pull request. 📤

> Please follow the coding style and conventions used in the project.

## Troubleshooting⚙

*   **Issue:** "ModuleNotFoundError: No module named 'cv2'"
    **Solution:** Install OpenCV: `pip install opencv-python`
    
*   **Issue:** "Error: Model file not found"
    **Solution:** Ensure the model file is downloaded and the `model_path` in `config.ini` is correct.
    
*   **Issue:** "Video processing is slow"
    **Solution:** Try reducing the resolution of the input video or using a more powerful machine. Also, ensure that you are using GPU acceleration if available.

## License🪪

## Contact📞
