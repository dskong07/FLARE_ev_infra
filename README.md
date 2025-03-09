# Explore [FLARE on our website](https://jingchenggu.github.io/FLARE-website/)!

This repository contains work by **Daniel Kong, Ethan Deng, Jason Gu, and Irving Zhao** as part of the **DSC 180B UCSD Capstone Project**.

## Overview  

The FLARE project aims to automate fault detection in EV charging stations using Semantic Segmentation and Vision-Transformer-based Classification models.
- **Semantic Segmentation**: SegFormer models for detecting charger components.  
- **Classification Models**: Binary classifiers for assessing damage and operational status in charger components.

## Semantic Segmentation  

The **`semantic_segmentation_models`** folder includes: 

- `seg_test.py` – Binary segmentation testing (contours & edges).  
- `trial_model` – Initial trial segmentation model using **NVIDIA's mit-b0** on the Hugging Face Semantic Sidewalk dataset.  
- `custom_segformer_training` – Creation of public dataset repositories, along with the development, training, and deployment of our custom semantic segmentation model on the gathered dataset. 
- `custom_segformer_b3_training` – Fine-tuned **Mit-B3** on our dataset for improved accuracy.  
- `upgraded_model_template` – Template for testing alternative transformer-based segmentation models.

## Classification  

The **`classifier_models`** folder includes: 

- **Binary inference models** for detecting cable damage, service availability, screen condition, and plug functionality.  
- Public dataset cleaning & preparation for model training.  

## Final Model  

- **Semantic Segmentation Model**: [SegFormer-B3 Fine-tuned](https://huggingface.co/irvingz/segformer-b3-finetuned-segments-chargers-full-v3.1)
- **Plug Classification Model**: [Plug Classification Model](https://huggingface.co/dskong07/plug-classif-model)  
- **Screen Classification Model**: [Screen Classification Model](https://huggingface.co/dskong07/screen-classif-model)  
- **OOS Classification Model**: [OOS Classification Model](https://huggingface.co/dskong07/charger-classif-model)  
- **Cord Classification Model**: [Cord Classification Model](https://huggingface.co/dskong07/cord-classif-model)
- **Dataset**: [Segments.ai Chargers Dataset](https://app.segments.ai/dskong07/chargers-full)  
- **Training Repository**: [Hugging Face Dataset](https://huggingface.co/dskong07)

### Example Outputs  

| Preliminary Model Output | Final Model Output |  
|-------------------------|--------------------|  
| <img src="https://github.com/user-attachments/assets/a6ca6746-69df-44d6-8b82-a374d9bdc66a" width="350"> | <img src="https://github.com/user-attachments/assets/f2842610-d117-4ca0-a9fc-1bcbca10af60" width="350"> |

## Setup  

### Requirements  

- **Hugging Face Account** – Required for accessing models via API.  
- **Segments.ai Account** – Required for accessing datasets via API.

### Installation  

Clone the repository and set up the environment:  

```bash
git clone https://github.com/dskong07/FLARE_ev_infra.git
cd FLARE_ev_infra
conda env create -f environment.yml
conda activate compvision
