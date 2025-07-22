# Bikini Bottom Domain Adaptation

Can a model trained on real-world images recognize visuals from a cartoon universe like Bikini Bottom?

This project explores **visual domain adaptation** by training a CNN to distinguish between real images (from the STL-10 dataset) and **SpongeBob-inspired cartoonized images**. Using OpenCV filters that simulate bright colors, bold outlines, and underwater-style visuals, we create a stylized dataset that mimics the aesthetic of *SpongeBob SquarePants* — without using any copyrighted content.

---

## Project Overview

- **Objective**: Classify whether an image belongs to the real world or a cartoonized domain.
- **Real Domain**: STL-10 dataset (96×96 images of real-world objects)
- **Cartoon Domain**: Stylized versions of STL-10 images using OpenCV filters
- **Task**: Binary classification (real vs. cartoon)
- **Model**: TinyCNN (or upgrade to ResNet18)
- **Tools**: PyTorch, OpenCV, Matplotlib

---

## How It Works

1. Load 250 images from STL-10
2. Apply a custom cartoonizer (SpongeBob-style):
   - Bright colors
   - High saturation
   - Edge outlines
3. Label real = `0`, cartoon = `1`
4. Train a CNN to classify the style
5. Test accuracy ~70–90%

---

## Results

| Epoch | Training Accuracy | Test Accuracy |
|-------|-------------------|---------------|
| 10    | ~90%              | ~70–85%       |
 Model successfully learned domain shift between real and stylized images.

---
