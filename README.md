# Pokemon-Object-Detection-Model

## Pokémon and Pokéball Object Detection with YOLOv5

This repository contains the code, data, and artifacts for an object detection project focused on identifying Pokémon and Pokéballs in images and videos using the YOLOv5 model. The project was developed as part of the ITI107 assignment.

---

**Table of Contents**

- Project Overview
- Data Collection & Annotation
- Model Training
- Results & Evaluation
- Deployment
- Recommendations for Improvement
- Repository Structure

---

## Project Overview

The goal of this project is to train a YOLOv5 model to detect Pokémon and Pokéballs in images and videos. The project covers the full pipeline, including data collection, annotation, model training, evaluation, and deployment via a Gradio demo on Hugging Face Space.

---

## Data Collection & Annotation

- **Pokémon Images:** Sourced from the public Kaggle Pokémon Image Dataset.
- **Pokéball Images:** Manually collected from various online resources.
- **Annotation:** All images were annotated using [Roboflow](https://roboflow.com/), labeling each image as containing either a Pokémon or a Pokéball.
- **Dataset Size:** 2,564 annotated images.

---

## Model Training

- **Framework:** YOLOv5 repository.
- **Batch Size:** 8 (reduced from 16 due to hardware constraints).
- **Epochs:** 5 (limited due to computational and time constraints).
- **Logging:** Initial attempts to use Weights & Biases (wandb) were abandoned due to API errors causing significant delays.
- **Fine-Tuning:** Not performed due to time limitations.
- **Artifacts:** Training code, model weights, and results are located in `code/YOLO/yolov5/runs`.

---

## Results & Evaluation

- **Detection Performance:** The trained model detects Pokémon and Pokéballs with reasonable accuracy on test images and videos, considering the limited training.
- **Inference Speed:** The exported model runs efficiently on both images and a 1-minute video sample.
- **Metrics:** Evaluated using mean average precision (mAP) and qualitative assessment.

---

## Deployment

- **Demo Application:** Deployed on Hugging Face Space using Gradio.
- **Functionality:** Users can upload images or videos to visualize detection results in real-time.

---

## Recommendations for Improvement

- **Fine-Tuning:** Allocate more time for hyperparameter tuning and additional training epochs.
- **Experiment Logging:** Resolve wandb issues for seamless experiment tracking.
- **Data Augmentation:** Apply advanced augmentation techniques to improve model generalization.
- **Hardware:** Utilize more powerful hardware or cloud GPUs to enable larger batch sizes and longer training.

## Acknowledgements

- [Kaggle Pokémon Image Dataset](https://www.kaggle.com/)
- [Roboflow Annotation Tool](https://roboflow.com/)
- [YOLOv5](https://github.com/ultralytics/yolov5)
- [Gradio](https://gradio.app/)
- [Hugging Face Spaces](https://huggingface.co/spaces)