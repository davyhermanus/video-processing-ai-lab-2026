# Video Processing AI Lab 2026

Teaching materials for **Session 07 – Video Processing**: traffic monitoring, aerial person detection, and CCTV pedestrian analysis using Python, OpenCV, YOLO, and ByteTrack.

## Open the notebooks in Google Colab

| Lab | Open directly | Source file |
|---|---|---|
| Traffic Monitoring | [Open in Colab](https://colab.research.google.com/github/davyhermanus/video-processing-ai-lab-2026/blob/main/notebooks/01_Traffic_Monitoring.ipynb) | [Notebook](notebooks/01_Traffic_Monitoring.ipynb) |
| Drone HOG (baseline) | [Open in Colab](https://colab.research.google.com/github/davyhermanus/video-processing-ai-lab-2026/blob/main/notebooks/02_Drone_HOG_Baseline.ipynb) | [Notebook](notebooks/02_Drone_HOG_Baseline.ipynb) |
| Drone YOLO + ByteTrack | [Open in Colab](https://colab.research.google.com/github/davyhermanus/video-processing-ai-lab-2026/blob/main/notebooks/03_Drone_YOLO_ByteTrack.ipynb) | [Notebook](notebooks/03_Drone_YOLO_ByteTrack.ipynb) |
| Smart CCTV + ByteTrack (event log) | [Open in Colab](https://colab.research.google.com/github/davyhermanus/video-processing-ai-lab-2026/blob/main/notebooks/04_Smart_CCTV_YOLO_ByteTrack.ipynb) | [Notebook](notebooks/04_Smart_CCTV_YOLO_ByteTrack.ipynb) |
| Three-demos overview | [Open in Colab](https://colab.research.google.com/github/davyhermanus/video-processing-ai-lab-2026/blob/main/notebooks/05_Three_Demos_Overview.ipynb) | [Notebook](notebooks/05_Three_Demos_Overview.ipynb) |

**Usage:** Open a notebook, select **Runtime → Run all**, and provide a video when asked. In notebook settings, select a GPU for YOLO if available. For self-contained demonstrations use the videos in `videos/source/`.

## Project structure

- `slides/` — Session 07 lecture slides (PowerPoint)
- `notebooks/` — runnable Google Colab notebooks including classical HOG and deep learning
- `videos/source/` — source clips (traffic, aerial gathering, pedestrian CCTV)
- `videos/results/` — recorded outputs from the practical sessions
- `screenshots/` — sample result figures

## Methods and important limitations

- **HOG** is a classical person detector that can miss small people in overhead drone footage.
- **YOLO** detects `person` objects; **ByteTrack** assigns temporary tracking IDs, which are **not** reliable unique-person counts.
- **Virtual-line crossings** are estimated events, not independently verified attendance or occupancy.
- Compare approaches on identical footage and annotate reference frames before making accuracy claims.

## Video file mapping

| Use case | Source | Recorded result |
|---|---|---|
| Traffic | `videos/source/traffic.mp4` | `videos/results/traffic_result.mp4` |
| Drone HOG | `videos/source/test_video.mp4` | `videos/results/drone_hog_result.mp4` |
| Drone YOLO | `videos/source/test_video.mp4` | `videos/results/deobw_yolo_result.mp4` |
| CCTV | `videos/source/vtest.avi` | `videos/results/smartcity-yolo-byte-track_result.mp4` |

## Credits, data rights, and privacy

Please review the reuse permissions of the **source videos** and any embedded figures before making this repository public. Uploading a video for classroom analysis does not automatically grant permission to redistribute it. The included results may contain recognizable people, so consider privacy and consent. If rights are uncertain, keep videos out of the public repository and distribute them only where authorized.

The packages used in notebooks are subject to their own licenses. In particular, review Ultralytics licensing for your intended use.
