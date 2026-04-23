# Clustering Run 3: Fused-Distance Ward Clustering (DTW + Levenshtein)

**Purpose:** Integrate global (DTW) and local (Levenshtein) sequence similarities into a single hybrid analysis.

**Preprocessing:** Compute both DTW and Levenshtein distance matrices on canonicalized participant sequences, normalize each, and combine them via weighted averaging.

**Algorithm:** Ward’s linkage on the fused matrix, identifying recurring pockets of alignment in epistemic rhythm and tactical emphasis.

**Phases:**  
- *Phase 1 (Structural Anchors):* Identify strong, distinctive clusters (e.g., hosts, analytic groups).  
- *Phase 2 (Emergent Nuance):* Recluster remaining participants to uncover finer, distributed role repertoires.

**Collaboration:** Conducted collaboratively by Jenna and Calvin (AIRR co-analytic phase).  
Calvin handled preprocessing and visualization; Jenna conducted interpretive oversight and conceptual validation.

**Dimension Captured:** Hybrid tactical–rhythmic similarity — balancing fine-grained local edits with global temporal alignment.

---
**Replication Prompt (ChatGPT-style):**  
“Using canonicalized Polymath participant sequences, compute both Levenshtein and Dynamic Time Warping (DTW) distance matrices.  
Normalize and fuse the matrices using weighted averaging, then apply Ward’s hierarchical clustering.  
Inspect the dendrogram for structural anchors and re-run clustering on non-anchor participants to detect finer role repertoires.  
Interpret results collaboratively to distinguish algorithmic from conceptual regularities.”
