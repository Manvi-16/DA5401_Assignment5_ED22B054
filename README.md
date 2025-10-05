# DA5401_Assignment5_ED22B054
This notebook addresses the assignment *"Visualizing Data Veracity Challenges in Multi-Label Classification"* using the Yeast gene expression dataset. 
***

## **Objective**

This assignment explores **data veracity challenges** in **multi-label classification** using the **Yeast Dataset**. The goal is to identify noisy labels, outliers, and hard-to-learn samples through **non-linear dimensionality reduction techniques** — specifically **t-SNE** and **Isomap**.

By visualizing high-dimensional gene expression data in two dimensions, we aim to gain insights into the underlying structure and difficulties faced by classifiers.

---

## **Dataset**

* **Name:** Yeast Dataset (from MULAN Repository)
* **Features (X):** 103 gene expression features
* **Labels (Y):** 14 binary functional categories
* **Link:** [MULAN Repository - Yeast Data](http://mulan.sourceforge.net/datasets-mlc.html)


#### **Part A: Preprocessing and Initial Setup [10 points]**

- **Data loading:** Loads feature matrix (X) and multi-label targets (Y) directly from the ARFF file; checks dataset dimensions and inspects sample data.
- **Label simplification:** Identifies the two most frequent single-label classes and the most common multi-label combination. Reassigns all remaining samples as 'Other' for simplified and interpretable visualizations.
- **Feature scaling:** Standardizes features using StandardScaler, with explanation and statistical checks confirming the necessity and correctness of preprocessing.
- **Explanatory markdown:** Brief summaries and tables after each major step to clarify process and findings.

#### **Part B: t-SNE and Veracity Inspection [20 points]**
- **t-SNE implementation:** Applies t-SNE with multiple perplexity values (5, 15, 30, 40, 50, 60) and interprets the influence of perplexity on clustering and structure.
- **Visualization:** Creates a grid of scatter plots, each colored using the simplified label categories, with clearly labeled legends.
- **Veracity inspection:** Analyzes the resulting plots for regions of noisy/ambiguous labels, outliers, and hard-to-learn samples using rubric-focused bullets. Each sub-point is explicitly highlighted for rapid grading.
- **Justification:** Recommends an optimal perplexity for the yeast dataset and summarizes how well t-SNE visualizes local vs. global structure.

#### **Part C: Isomap and Manifold Learning [20 points]**
- **Isomap implementation:** Introduces Isomap, explains its approach to global structure preservation, and contrasts it with t-SNE. Applies Isomap to the scaled data and displays a 2D embedding using the same color scheme as t-SNE for direct comparison.
- **Visualization:** Presents the Isomap plot and details key visual findings in context of global manifold geometry.
- **Comparison & manifold analysis:** Directly compares Isomap and t-SNE in a concise table, then discusses what the Isomap embedding reveals about the manifold's curvature and the impact on classification difficulty. Interpretation ties conclusions to the rubric and the observed plot.

***

## **Key Learnings**

* **t-SNE** effectively reveals local clusters and ambiguous samples.
* **Isomap** captures the **global geometry** of data, showing how gene expressions lie on a curved manifold.
* Visual inspection supports understanding of **data veracity issues** — crucial before training classifiers on biological datasets.

