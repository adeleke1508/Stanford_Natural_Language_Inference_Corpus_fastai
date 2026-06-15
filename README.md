Carvana Image Segmentation using ResNet (U-Net)
Overview
This project implements semantic image segmentation to accurately mask car images from their backgrounds, using the Carvana Image Masking Challenge dataset from Kaggle. A U-Net architecture with a ResNet encoder is used as the backbone, leveraging transfer learning for strong performance on this pixel-level classification task.
Dataset
Source: Carvana Image Masking Challenge – Kaggle
Task: Binary pixel-level segmentation — classify each pixel as either car or background
Images: High-resolution car photographs taken from 16 different angles per vehicle
Tech Stack
Python, PyTorch / fastai
ResNet (pretrained encoder backbone)
U-Net architecture (encoder-decoder with skip connections)
Jupyter Notebook
Approach
Data Loading — loaded image-mask pairs and built a segmentation DataLoader
Architecture — used a U-Net with a pretrained ResNet encoder; the encoder captures rich visual features while the decoder reconstructs pixel-level masks
Training — fine-tuned with fastai's fit_one_cycle policy; applied data augmentation (flipping, zoom, lighting transforms)
Loss Function — used a combination of Binary Cross-Entropy and Dice loss for robust segmentation training
Evaluation — assessed quality using the Dice coefficient (F1 score at pixel level)
Results
Produced visually accurate car masks with clean boundary detection
Transfer learning from ResNet significantly improved convergence speed and mask quality compared to training from scratch
Key Learnings
U-Net encoder-decoder architecture with skip connections
Transfer learning for pixel-level tasks using pretrained CNNs
Dice loss and its advantages over pure cross-entropy for imbalanced segmentation masks
Data augmentation strategies specific to segmentation tasks (applying same transforms to image and mask)
How to Run
# Clone the repo
git clone https://github.com/adeleke1508/carvana_segmentation_task_using_resnet.git
cd carvana_segmentation_task_using_resnet

# Install dependencies
pip install fastai torch jupyter

# Download the dataset from Kaggle:
# https://www.kaggle.com/c/carvana-image-masking-challenge/data

# Launch the notebook
jupyter notebook carvana-segmentation-task-using-resnet.ipynb
Note: This task requires significant GPU memory. Google Colab Pro or Kaggle Notebooks (free GPU) are recommended.
Author
Ismail Khaleed Ayobami — 300-Level Software engineering Student, FUTA
LinkedIn | GitHub
