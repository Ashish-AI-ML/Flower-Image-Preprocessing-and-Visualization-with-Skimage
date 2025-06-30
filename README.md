# 🌸 Flower Image Preprocessing and Visualization with Skimage

This project focuses on **image preprocessing** and **morphological operations** for flower classification using the `scikit-image` and `matplotlib` libraries. It demonstrates techniques used to prepare images for tasks such as image segmentation, feature extraction, and input normalization for machine learning models (like CNNs).

---

## ✅ What This Code Does

### 📂 1. Load and Visualize Flower Images
- Loads flower images from specific folders (`daisy`, `rose`).
- Uses `glob` and `os.path` to read images from directory.
- Displays full-color images and individual RGB channels using `matplotlib`.

### 🧼 2. Thresholding and Binarization
- Uses **Otsu’s Thresholding** (from `skimage.filters`) to automatically determine a good threshold for converting grayscale images to binary (black & white).
- Applies manual thresholding to a specific color channel for segmentation.

### 🔄 3. Morphological Transformations
Performs classical image operations to enhance structural features in the binary images:

| Transformation   | Purpose                                |
|------------------|----------------------------------------|
| **Erosion**      | Shrinks bright regions (enhances dark) |
| **Dilation**     | Expands bright regions (enhances light)|
| **Opening**      | Removes small bright noise             |
| **Closing**      | Fills small dark holes                 |

These are applied using structural elements like disks to isolate flower shapes more clearly.

### 🔧 4. Image Normalization
- Normalizes image pixel values using three methods:
  - **Min-max normalization**
  - **0-255 scaling**
  - **Percentile-based contrast stretching**
- Prepares images for deep learning pipelines (e.g., CNN input).

---

## 🛠️ Libraries & Tools Used

| Library           | Purpose                                  |
|-------------------|------------------------------------------|
| **scikit-image**  | Image preprocessing, morphology, filters |
| **matplotlib**    | Image visualization                      |
| **NumPy**         | Matrix and pixel-level operations        |
| **os / glob**     | Directory and file handling              |
| **random**        | Random image selection for display       |

---

## 🔍 Use Cases

- Preprocessing pipeline for **image classification** tasks (e.g., with CNNs)
- Data preparation for **flower species recognition**
- Demonstration of classical image operations for **educational or research use**

---

## 📋 Requirements

Install the required Python packages:

```bash
pip install scikit-image matplotlib numpy
