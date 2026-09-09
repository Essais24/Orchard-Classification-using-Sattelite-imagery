# Orchard-Classification-using-Sattelite-imagery
This project uses USDA NAIP imagery to classify three major canopy systems: V-trellis, vertical, and freestanding. The workflow includes geospatial data preprocessing, image tiling, class-balanced segmentation, and deep learning model development using U-Net and Mask R-CNN. Model performance is evaluated using pixel and instance level metrics.

# Overview
This project develops a deep learning-based approach for large-scale
mapping and classification of apple orchard canopy architectures using
high-resolution aerial imagery.

<img width="1371" height="652" alt="image" src="https://github.com/user-attachments/assets/ad2fd13a-f8de-4e69-9bfb-0026e992dbe9" />

Apple orchards use different canopy systems, including V-trellis,
vertical, and freestanding architectures. Accurately identifying these
systems at regional scale can support orchard inventory, agricultural
planning, and precision agriculture.

The project combines remote sensing, geospatial data processing,
semantic segmentation, and instance segmentation to automate orchard
canopy architecture classification.

# Objective
Develop and evaluate deep learning models for accurate orchard canopy
architecture mapping and classification using annotated aerial
imagery.

# Canopy Classes
V-Trellis

Vertical

Freestanding

# Data Acquisition
The imagery was obtained from USDA NAIP (National Agriculture Imagery
Program) through USGS Earth Explorer.

Study region: Yakima Valley, Washington, USA

<img width="1939" height="710" alt="image" src="https://github.com/user-attachments/assets/aa43a864-2322-4b81-86a4-bb400a35b6c6" />


Years covered: 2018--2023

Spatial resolution: Approximately 60 cm

Data type: High-resolution aerial imagery

# Dataset Preparation
The preprocessing workflow includes:

Identifying orchard regions using the USDA Cropland Data Layer.

![Uploading image.png…]()


Manually surveying and labeling orchard polygons.

Georeferencing polygons to NAIP imagery.

Converting polygons into training-ready labels.

Clipping imagery into smaller image patches.

Applying image preprocessing and normalization.

Applying class-specific augmentation to reduce class imbalance.

The final dataset contains 1,249 orchard instances:

# Canopy Architecture Instances

Freestanding 315

V-Trellis 568

Vertical 366

Total 1,249

# Model Development
U-Net
U-Net was used for semantic segmentation and pixel-level
classification of canopy architecture.

Mask R-CNN
Mask R-CNN was used for instance segmentation, allowing individual
orchard structures to be detected and segmented separately.

The dataset was divided into a 70/30 train-test split.

# Evaluation
Models were evaluated using pixel-level and instance-level metrics:

<img width="1022" height="766" alt="image" src="https://github.com/user-attachments/assets/00cb03db-b5f9-48ed-83f9-c195fb0c0df6" />

<img width="1022" height="766" alt="image" src="https://github.com/user-attachments/assets/fb86f656-b706-410a-83b8-c629d2b09f44" />

The results showed that U-Net provided stronger overall pixel-level
classification performance for this application, while Mask R-CNN
provided instance-level segmentation capabilities.
