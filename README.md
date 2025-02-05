# k-NN Classification with Different Distance Measures

## Overview
This project implements a **k-Nearest Neighbors (k-NN) classifier** on the **Iris dataset** using different distance measures. The goal is to compare the classification performance of various distance metrics and determine the most effective one.

## Distance Measures Used
1. **Euclidean Distance (L2 Norm)**  
   - Measures straight-line distance between points.
   - Commonly used for continuous numerical data.

2. **Manhattan Distance (L1 Norm)**  
   - Measures distance along axes at right angles.
   - Useful when movement is restricted to a grid-like path.

3. **Minkowski Distance** (Generalized Form)  
   - A generalization of Euclidean and Manhattan distances.
   - Adjusts the effect of different feature relationships.

4. **Cosine Similarity**  
   - Measures the cosine of the angle between vectors.
   - Often used in text and document similarity.

5. **Hamming Distance**  
   - Measures the number of different positions between binary strings.
   - Used in categorical data and error detection.

6. **Jaccard Similarity**  
   - Measures the intersection over the union of sets.
   - Often applied to categorical and binary data.

## Implementation
- The Iris dataset was loaded and split into **training (80%)** and **testing (20%)** sets.
- Standardization was applied for Euclidean, Manhattan, Minkowski, and Cosine similarity.
- Binarization was applied for Jaccard and Hamming distances.
- A **k-NN classifier (k=5)** was trained for each distance measure.
- Accuracy scores were computed for comparison.

## Results
```
Euclidean Accuracy: 1.0000
Manhattan Accuracy: 1.0000
Minkowski Accuracy: 1.0000
Cosine Accuracy: 0.9333
Hamming Accuracy: 0.3333
Jaccard Accuracy: 0.3333
```

## Best Performing Distance Measure
The **Euclidean, Manhattan, and Minkowski distances** all achieved perfect accuracy (**1.0000**). These metrics are well-suited for continuous numerical datasets like the **Iris dataset**, where feature relationships are best captured by geometric distance.

### Reasoning:
- **Euclidean Distance** is ideal when all features have equal importance and are continuous.
- **Manhattan Distance** is robust to outliers and works well for structured grid-like data, though it performed equally well here.
- **Minkowski Distance** generalizes both Euclidean and Manhattan, achieving the same accuracy at **p=3**.
- **Cosine Similarity** was slightly lower (**0.9333**), as it focuses on direction rather than magnitude.
- **Hamming and Jaccard Distances** performed poorly (**0.3333**) since the Iris dataset is not well-suited for categorical distance measures.

## Conclusion
For numerical datasets like **Iris**, **Euclidean Distance** is the most effective measure due to its ability to directly compare feature magnitudes.

For other datasets:
- Use **Manhattan Distance** when robustness to outliers is needed.
- Use **Cosine Similarity** for high-dimensional sparse data.
- Use **Jaccard and Hamming** for categorical or binary data.

## How to Run the Code
1. Install dependencies: `pip install numpy pandas scikit-learn`
2. Run the Python script: `python DistanceMeasures.py`


