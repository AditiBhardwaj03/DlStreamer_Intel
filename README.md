# DlStreamer_Intel

🎥 [Project Video Link](https://drive.google.com/file/d/1kpPGygTYvRxCiVsfyu8S9FC8wlyegLtB/view?usp=drive_link)


#  DL Streamer Pipeline for Object Detection & Classification

This project demonstrates a scalable Deep Learning Streamer (DL Streamer) pipeline using Intel OpenVINO models for object detection and classification. It is designed to run multiple video streams in parallel, measure FPS, and log performance.

---

## Project Structure

├── run_streams.sh # Runs vehicle detection/classification streams
├── run_face_streams.sh # Runs face detection streams
├── intel/models/ # OpenVINO models (downloaded via OMZ)
├── video/ # Input video file(s)
├── stream*.log # Per-stream logs with FPS
└── README.md # Project info


---

## Features

- Runs multiple GStreamer pipelines in parallel
- Performs:
  - **Vehicle Detection** using `person-vehicle-bike-detection-2000`
  - **Vehicle Classification** using `vehicle-attributes-recognition-barrier-0039`
  - **Face Detection** using `face-detection-adas-0001`
- Logs FPS (Max, Min, Avg) for each stream
- Optimized for Intel CPUs with OpenVINO and DL Streamer

---

## Requirements

- Ubuntu 20.04 or later
- Intel® DL Streamer
- OpenVINO Toolkit
- GStreamer with plugins
- Bash

---

##  Model Downloads

Use Open Model Zoo tools:

```bash
omz_downloader --name person-vehicle-bike-detection-2000
omz_downloader --name vehicle-attributes-recognition-barrier-0039
omz_downloader --name face-detection-adas-0001
