# Emotion Analysis using DeepFace

## Overview

This simple Python script uses OpenCV, DeepFace, and Matplotlib to analyze and display emotions in an image. The script reads an image, uses DeepFace to detect emotions, and then displays the image with emotion annotations using Matplotlib.

## Prerequisites

- Python 3
- OpenCV (`pip install opencv-python`)
- DeepFace (`pip install deepface`)
- Matplotlib (`pip install matplotlib`)

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/emotion-analysis.git
    cd emotion-analysis
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Run the script:

    ```bash
    python emotion_analysis.py --image_path path/to/your/image.jpg
    ```

Replace `path/to/your/image.jpg` with the path to the image you want to analyze.

## Script Details

- **emotion_analysis.py**: The main script that reads an image, detects emotions using DeepFace, and displays the annotated image using Matplotlib.

## Example

```python
import cv2
from deepface import DeepFace
import matplotlib.pyplot as plt

# Read image
img = cv2.imread('happyboy1.jpg')

# Use DeepFace to detect emotions
result = DeepFace.analyze(img, actions=['emotion'])

# Display the image with emotion annotations
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title(f"Emotion: {result['dominant_emotion']}")
plt.axis('off')
plt.show()
```
All these code can written using opencv ,deep face and other algos and emotion detection can easily be done using different libraries and by implementing and training the data easily we can run this one.
