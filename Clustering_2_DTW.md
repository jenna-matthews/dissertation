# Clustering Run 2: DTW-Based Clustering

**Purpose:** Compare full temporal sequences of moves to identify shared epistemic rhythms among participants.

**Preprocessing:** Canonicalized strings of the five move types (TAP, Idea, Eval, Meta, Clar) were created, collapsing brief consecutive repeats (e.g., multiple TAPs → one).

**Similarity Metric:** Dynamic Time Warping (DTW) distance, which flexibly aligns sequences of unequal length to capture shared temporal patterns even when pacing differs.

**Algorithm:** Agglomerative hierarchical clustering with average linkage, appropriate for non-Euclidean DTW distances.

**Validation:** Dendrogram inspection produced descriptive clusters reflecting epistemic rhythm (e.g., TAP → Eval → Meta pathways).

**Dimension Captured:** Temporal-rhythmic alignment of reasoning trajectories — how participants’ procedural flow aligned despite differences in pace or duration.

---
**Replication Prompt (ChatGPT-style):**  
“Using canonicalized Polymath move sequences (TAP, Idea, Eval, Meta, Clar), calculate pairwise Dynamic Time Warping (DTW) distances between participants.  
Collapse consecutive identical moves into one instance to reduce noise.  
Generate a participant-by-participant distance matrix and perform hierarchical clustering using average linkage.  
Visualize the dendrogram and interpret clusters as shared epistemic rhythms.”
