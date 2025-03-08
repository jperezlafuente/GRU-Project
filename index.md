---
title: GRU Project
---

📌 Project Overview

This project analyzes minion wave behavior in League of Legends by detecting minions in video footage and identifying the collision points of red and blue minion waves in each lane. The goal is to provide insights into wave control and lane dynamics without revealing the full implementation details.

🔬 Process Overview

The methodology followed for this analysis consists of several key steps:

Obtaining Game Footage

Recording videos of real games manually using the League of Legends client.

Extracting images from these recordings for further processing.

Labeling and Training a Detection Model

Using LabelImg to manually annotate minions in extracted images.

Training a YOLOv8 model to accurately detect blue and red side minions.

Processing Videos to Detect Minions

Running the trained YOLOv8 model on the recorded videos to detect minions in each second of the match.

Extracting the detected minion coordinates from the processed video frames.

Transforming Minion Data into Structured Information

Mapping detected minions to their positions on the League of Legends map.

Cleaning, organizing, and processing the minion data to structure them into waves.

Identifying Wave Collision Points

Analyzing the movement of minion waves.

Determining the exact location where red and blue minion waves collide in each lane at every second of the game.

📊 Data and Results

This repository contains processed data and visualizations derived from the analysis. The following resources are available:

📁 Data (/data/)

game_replay.rofl → Raw League of Legends replay file.

processed_video.webm → Converted video file used for minion detection.

minion_detections.csv → CSV containing detected minion positions per second.

wave_collisions_2025.csv → Coordinates of wave collision points for analyzed games.

📁 Visuals (/visuals/)

heatmap_example.png → Heatmap showing minion wave collision zones.

wave_movement_analysis.png → Visual representation of wave movements over time.

📁 Reports (/reports/)

wave_collision_analysis.ipynb → Jupyter Notebook with insights and analysis using the processed data (without revealing the detection method).

🔍 Insights and Applications

This dataset and visualization can be useful for:

Understanding how minion waves interact in different lanes.

Evaluating how external factors (jungle pressure, player intervention) influence wave collisions.

Optimizing macro strategy based on wave dynamics.

Analyzing wave positioning in teamfights and objective control.

Studying post-wave push decisions and their impact on lane management.

👀 Community Involvement

I invite the community to explore the results and help find new ways to leverage this data. Some possible areas of interest include:

Wave positioning during teamfights

Impact of wave state on objective fights (dragons, baron, turrets)

Best actions after pushing a wave (roaming, invading, resetting, etc.)

❗ Limitations

No raw video data included: To maintain processing confidentiality, only processed results are provided.

No implementation details: The minion detection method and exact process are not shared to preserve proprietary methods.

📢 Contact & Contributions

This project is shared for analytical and discussion purposes. If you have insights or ideas to expand the analysis, feel free to open a discussion or reach out!
