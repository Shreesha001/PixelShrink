# Image Compression with K-Means Clustering

This project demonstrates **image compression using K-Means clustering** implemented in two ways:  

1. **From Scratch (NumPy implementation)** – Implements the K-Means algorithm manually without external ML libraries.  
2. **Using scikit-learn** – Leverages the `KMeans` class from `scikit-learn` for efficient clustering.  

The goal is to reduce the number of colors in an image (color quantization), thereby compressing its size while retaining visual quality.  

---

## Features

- Compress images to a reduced color palette (e.g., 20 colors instead of thousands).  
- Compare original and compressed images side by side.  
- Evaluate compression effectiveness by computing:  
  - Original file size  
  - Compressed file size  
  - Compression ratio  
- Two different implementations for better understanding:  
  - **Manual K-Means (NumPy)**  
  - **scikit-learn KMeans**  

---

## Installation

### Prerequisites
Ensure you have Python **3.8+** installed along with the required libraries.

Install dependencies:

```bash
pip install numpy matplotlib pillow scikit-learn scikit-image
```

---

## Usage

### 1. NumPy Implementation (Manual K-Means)

Run:

```bash
python kmeans_numpy.py
```

Default values inside the script:
- `image_path = "image.jpg"`
- `K = 20`

This script:
- Loads the image
- Runs a custom K-Means algorithm
- Displays the compressed image
- Saves it as `compressed_image_python.jpg`
- Prints file sizes and compression ratio

---

### 2. scikit-learn Implementation

Run:

```bash
python kmeans_sklearn.py
```

Default values inside the script:
- `image_path = "image.jpg"`
- `K = 14`

This script:
- Loads the image
- Uses `sklearn.cluster.KMeans` for clustering
- Displays the compressed image
- Saves it as `compressed_image.jpg`
- Prints file sizes and compression ratio

---

## Example Results

For an input image of size **203.89 KB**:

- **NumPy Implementation**  
  - Compressed size: 24.87 KB  
  - Compression ratio: ~8.20x  

- **scikit-learn Implementation**  
  - Compressed size: 25.04 KB  
  - Compression ratio: ~8.14x  

---