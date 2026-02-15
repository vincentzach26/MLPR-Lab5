# Lab 5: Distance-Based Classification & Face Clustering

## Course
**Machine Learning and Pattern Recognition**  
**Spring Semester 2026**

---

## Objective
The aim of this lab is to understand and implement **distance-based classification concepts** using real image data. The lab focuses on:

- Face detection using Haar Cascade classifiers  
- Feature extraction using **color space transformation (HSV)**  
- Unsupervised clustering using **K-Means**  
- Classifying a new (template) image based on learned clusters  
- Visualizing clusters and interpreting results  

This lab demonstrates how distance metrics operate in practical machine learning pipelines involving image data.

---

## Methodology

### 1. Image Preprocessing
- The input image (`plaksha_Faculty.jpg`) is read using OpenCV.
- It is converted from **BGR to grayscale** for face detection.
- Haar Cascade (`haarcascade_frontalface_default.xml`) is used to detect faces.

### 2. Feature Extraction
- The original image is converted from **BGR to HSV color space**.
- For each detected face:
  - Mean **Hue** and **Saturation** values are extracted.
- These values form a 2D feature vector for each face.

### 3. Clustering using K-Means
- K-Means clustering is applied with:
  - `k = 2`
  - Feature space: (Hue, Saturation)
- Faces are grouped into two clusters based on color similarity.

### 4. Template Image Classification
- A separate template image (`Dr_Shashi_Tharoor.jpg`) is processed similarly.
- Hue and Saturation features are extracted.
- The trained K-Means model predicts the cluster label for the template image.

### 5. Visualization
- Scatter plots are generated to visualize:
  - Clustered face features
  - The template image location in feature space
- This helps interpret similarity and classification outcome.

---

## Files in Repository

├── Lab5_filled.ipynb
├── plaksha_Faculty.jpg
├── Dr_Shashi_Tharoor.jpg
├── README.md


---

## Tools & Libraries Used

- Python 3
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Scikit-learn (`KMeans`)
- SciPy (distance metrics)

---

## Key Observations
- Hue and Saturation are effective low-dimensional features for coarse facial clustering.
- K-Means clustering relies heavily on the choice of distance metric (Euclidean by default).
- The template image is classified based on proximity to learned cluster centroids.
- Visual inspection of clusters validates the classification result.

---

## Learning Outcomes
- Gained hands-on experience with **distance-based learning**
- Understood the role of **feature representation** in clustering
- Learned how unsupervised models can be adapted for classification tasks
- Practiced visualization for model interpretation

---

## Conclusion
This lab demonstrates a complete pipeline—from raw image input to feature extraction, clustering, and classification—highlighting the practical relevance of distance metrics in machine learning. The approach reinforces foundational concepts such as similarity measurement, unsupervised learning, and model evaluation through visualization.

---

## Author
**Vincent Zacharias**  
Plaksha University
