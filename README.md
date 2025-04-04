# ASL-Alphabet-Education-Tool: AI-Powered Educational Tool for American Sign Language

## Overview

The ASL Alphabet Education Tool is an innovative, AI-powered educational tool designed to empower the Deaf and Hard-of-Hearing community while teaching American Sign Language (ASL) to children. Our system translates ASL alphabets into English text in real-time (ASL-to-text). The project features a simple, kid-friendly interface with three interactive modes: **Learn**, **Freemode**, and **Play**. This initiative aligns with our commitment to accessibility and inclusivity and is built with a robust technology stack to ensure high performance and scalability.

## Features

- **Real-Time ASL Detection:**  
  Utilises computer vision and deep learning to recognise hand gestures.
  
- **Interactive Modes:**  
  - **Learn Mode:** Displays an ASL word using alphabet images; the user is prompted to input the correct English spelling.
  - **Freemode:** Provides an open, free practice environment for signing.
  - **Play Mode:** A game-like mode that challenges the user with a time limit and awards points based on accuracy.

- **Autocomplete Functionality:**  
  Suggests possible words based on the letters the user has signed so far.

- **Data Augmentation:**  
  Builds a robust, diverse dataset by augmenting each image with a variety of transformations, ensuring the model generalises well to different hand positions, angles, and lighting conditions.

- **Model Comparison:**  
  Offers two model training options:
  - A classical **Random Forest classifier** (baseline).
  - A CNN-based model (using MobileNetV2) that is recommended for improved accuracy on image data.

## Technology Stack

- **Operating System:** Ubuntu 24.04 (Linux)
- **Programming Language:** Python 3.12+
- **Machine Learning Frameworks:**  
  - **Scikit-learn:** For the Random Forest classifier.  
  - **TensorFlow/Keras:** For the CNN-based model using MobileNetV2.
- **Computer Vision:** OpenCV for image processing and display.
- **Hand Detection:** MediaPipe for robust hand landmark extraction.
- **Data Augmentation:** Albumentations for diverse image transformations.
- **GUI Framework:** Tkinter for a kid-friendly interactive interface.
- **Version Control:** Git and GitHub

## Dataset

- **Raw Data:**  
  201 unaltered images per alphabet (A–Z) captured manually.
  
- **Merged & Augmented Data:**  
  The raw images are standardised (resised to 224×224 pixels, converted to grayscale, and saved as JPEG at 90% quality). Data augmentation is then applied to each image (e.g., rotation, affine transformations, brightness/contrast adjustments, noise, etc.) to generate 10 additional variations per image. The final dataset is stored in the folder `asl_processed`, and hand landmarks are extracted and saved in the pickle file `data_final.pickle`.
