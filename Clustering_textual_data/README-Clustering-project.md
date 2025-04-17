# 🧠 Clustering and Period Analysis in the Works of Annie Ernaux

This project analyzes a corpus of texts by **Annie Ernaux**, using clustering techniques and natural language processing to explore thematic and stylistic shifts across her literary output.

---

## 💡 Objective

The main goal is to investigate whether **unsupervised learning** methods (K-Means and hierarchical clustering) can identify **distinct literary periods** in Ernaux’s writing, based on lexical and stylistic patterns.

The project also evaluates **cluster purity** to measure how well computational models align with human-defined literary periods.

---

## 📁 Data

- **Corpus**: `corpus_Ernaux_v1.xml`  
  An XML-encoded set of Ernaux’s texts, segmented into `<texte>` blocks.
- Each block is treated as a separate document for analysis.
- Period labels (e.g. “Période 1”, “Période 2”) were added manually for evaluation purposes.

---

## 🧪 Methods

1. **Preprocessing**
   - Parse the XML and extract texts
   - Lowercase and clean tokens
2. **Vectorization**
   - Use `TfidfVectorizer` with unigrams and bigrams
   - Apply optional dimensionality reduction with `PCA` for visualization
3. **Clustering Techniques**
   - **K-Means** with `n_clusters=2`, based on expected binary period division
   - **Agglomerative Clustering** with Ward linkage and dendrogram plotting
4. **Evaluation**
   - Compute **cluster purity**
   - Visualize cluster assignments
   - Compare cluster groupings to annotated periods

---

## 📊 Results and Interpretation

### 🔹 K-Means

- Successfully identified 2 distinct clusters that mostly align with the hypothesized periods.
- **Cluster Purity**: ~78% accuracy in matching annotated periods.
- Some texts were ambiguous or stylistically transitional (e.g. *La Femme gelée*, *Journal du dehors*).

> **Conclusion**: K-Means captures meaningful stylistic features but is limited by its spherical cluster assumption and sensitivity to initialization.

---

### 🔹 Hierarchical Clustering

- The dendrogram revealed more **gradual transitions** between styles than binary segmentation.
- With a 2-cluster cutoff, results were close to K-Means.
- At higher resolutions, more **granular groupings** appeared (e.g. texts thematically close despite time gap).

> **Conclusion**: Hierarchical clustering provides a more nuanced view, ideal for literary corpora where transitions are continuous.

---

## 📦 Technologies Used

- Python
- `scikit-learn`: TF-IDF, KMeans, AgglomerativeClustering, PCA
- `matplotlib` & `scipy.cluster.hierarchy` for dendrograms
- `pandas`, `re`, `xml.etree.ElementTree` for text extraction

---

## 📚 Example Output

```text
K-Means cluster breakdown:
Cluster 0 → Période 1 (3)
Cluster 1 → Période 2 (6)
Purity: 0.78

Hierarchical Clustering:
See dendrogram (ward linkage)
```

---

## 👩‍💻 Author

Project by **Chloé Petridis**, as part of a digital humanities course on literary pattern recognition using unsupervised machine learning.
