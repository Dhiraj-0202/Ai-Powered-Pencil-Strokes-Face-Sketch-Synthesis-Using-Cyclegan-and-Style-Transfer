# 🎨 Image to Pencil Sketch Using CycleGAN

> AI-powered Image-to-Pencil Sketch Generation using CycleGAN and Style Transfer

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![License](https://img.shields.io/badge/License-MIT-brightgreen)

---

# 📖 Overview

This project presents an AI-based approach for converting real-world images into realistic pencil sketches using **CycleGAN (Cycle-Consistent Generative Adversarial Network)**.

Unlike traditional sketch generation methods that rely on edge detection or handcrafted filters, CycleGAN learns the mapping between photographs and sketches without requiring paired datasets.

The generated sketches are further enhanced using **Style Transfer** to produce more natural pencil stroke effects while preserving important facial features, textures, and shading.

This project was developed as part of our Final Year Engineering Project.

---

# 🚀 Features

- Convert real images into realistic pencil sketches
- Uses unpaired datasets (No paired training images required)
- CycleGAN-based image-to-image translation
- Style Transfer enhancement
- Preserves facial structure and fine details
- Supports different image categories
- High-quality sketch generation
- SSIM evaluation metric
- GPU supported training

---

# 📂 Project Structure

```
Image-to-Pencil-Sketch-Using-CycleGAN/
│
├── Dataset/
│   ├── trainA/
│   ├── trainB/
│   ├── testA/
│   └── testB/
│
├── Models/
│   ├── Generator.py
│   ├── Discriminator.py
│   └── CycleGAN.py
│
├── Images/
│
├── Results/
│
├── Notebook/
│   └── CYCLEGAN_IMAGE_TO_SKETCH.ipynb
│
├── requirements.txt
│
├── README.md
│
└── LICENSE
```

---

# 🧠 How CycleGAN Works

CycleGAN performs image-to-image translation using two Generators and two Discriminators.

```
Real Image
      │
      ▼
Generator G
(Photo → Sketch)
      │
      ▼
Generated Sketch
      │
      ▼
Discriminator DSketch
      │
      ▼
Generator F
(Sketch → Photo)
      │
      ▼
Reconstructed Image
```

The model learns by minimizing:

- Adversarial Loss
- Cycle Consistency Loss
- Identity Loss

---

# ⚙️ Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- PIL
- Google Colab
- Jupyter Notebook

---

# 📊 Dataset

The model is trained using **unpaired datasets**.

### Domain A

Real Images

Examples:

- Human Faces
- Landscapes
- Buildings
- Objects

### Domain B

Pencil Sketches

Examples:

- Hand-drawn sketches
- Digital pencil sketches

Image Size

```
256 × 256
```

---

# 🔄 Data Preprocessing

Before training the model:

- Resize images to 256×256 pixels
- Normalize pixel values
- Remove duplicate images
- Data augmentation
- Image hashing
- Convert to tensors

---

# 🏗️ Model Architecture

## Generator

- Convolution Layer
- Instance Normalization
- ReLU Activation
- 9 Residual Blocks
- Upsampling Layers
- Tanh Activation

## Discriminator

PatchGAN Discriminator

- Convolution
- Instance Normalization
- LeakyReLU
- Patch Classification

---

# 📉 Loss Functions

### Adversarial Loss

Helps the Generator create realistic sketches that fool the Discriminator.

---

### Cycle Consistency Loss

Ensures:

```
Photo → Sketch → Photo
```

returns back to the original image.

---

### Identity Loss

Preserves the original image characteristics while generating sketches.

---

# 🖥️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Image-to-Pencil-Sketch-Using-CycleGAN.git
```

Move into the project

```bash
cd Image-to-Pencil-Sketch-Using-CycleGAN
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Running the Project

Open the notebook

```bash
jupyter notebook
```

Run

```
CYCLEGAN_IMAGE_TO_SKETCH.ipynb
```

or

Upload the notebook into **Google Colab** and execute all cells.

---

# 📈 Hyperparameters

| Parameter | Value |
|------------|--------|
| Image Size | 256 × 256 |
| Optimizer | Adam |
| Learning Rate | 0.0002 |
| Batch Size | 1 |
| Cycle Loss λ | 10 |
| Identity Loss | 0.5 λ |

---

# 📊 Performance Evaluation

Evaluation Metric

- Structural Similarity Index (SSIM)

Obtained Result

| Metric | Value |
|----------|--------|
| SSIM | **0.56** |

The generated sketches preserve facial structures while improving artistic quality using style transfer.

---

# 📷 Sample Results

```
Original Image

        ↓

CycleGAN

        ↓

Generated Pencil Sketch
```

*(Add screenshots of your outputs inside the Results folder.)*

---

# 💡 Applications

- Digital Art
- Pencil Sketch Generation
- Face Sketch Synthesis
- Animation
- Graphic Design
- Mobile Photo Editing Apps
- Forensic Sketch Generation
- AI Art Generation

---

# 🚧 Limitations

- Requires a large dataset
- Training is computationally expensive
- Performance depends on dataset quality
- Fine details may sometimes be lost
- GPU is recommended

---

# 🔮 Future Scope

- Real-time video sketch generation
- Mobile application deployment
- Multiple artistic styles
- Higher resolution image generation
- Diffusion model integration
- Attention-based CycleGAN
- Transformer-based image translation

---

# 📚 Research Paper

This project is based on our IEEE conference publication:

**AI-Powered Pencil Strokes: Face Sketch Synthesis Using CycleGAN and Style Transfer**

Published in:

**2025 International Conference on Inventive Computation Technologies (ICICT)**

DOI:

https://doi.org/10.1109/ICICT64420.2025.11005149

---

# 👨‍💻 Team Members

- Peddi Deekshith
- S. Dheeraj
- Simma Sathwik
- S. V. Dhiraj

Guide

- Dr. C. R. Lekshmi

School of Artificial Intelligence

Amrita Vishwa Vidyapeetham

---

# 🙏 Acknowledgements

We sincerely thank:

- Amrita Vishwa Vidyapeetham
- School of Artificial Intelligence
- Our Project Guide
- TensorFlow Community
- OpenCV Community
- CycleGAN Authors

---

# ⭐ If you like this project

Please consider giving it a ⭐ on GitHub!

---

# 📧 Contact

For any queries or collaborations:

📩 Create an Issue on this repository.

---

## License

This project is intended for **academic and educational purposes**. If you reuse or extend this work, please provide appropriate attribution to the original authors and cite the associated IEEE publication where applicable.
