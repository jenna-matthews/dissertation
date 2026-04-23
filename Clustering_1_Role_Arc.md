# Clustering Run 1: Role-Arc Clustering

**Purpose:** Trace how each participant’s emphasis on the five epistemic moves (TAP, Idea, Eval, Meta, Clar) evolved over time.

**Segmentation:** Each participant’s timeline was divided into early, middle, and late terciles based on posting order.

**Data Structure:** 15-dimensional vectors (5 moves × 3 stages) representing proportional move frequencies.

**Preprocessing:** Laplace smoothing applied to avoid zero counts.

**Similarity Metric:** Cosine distance, emphasizing proportional alignment over absolute counts.

**Algorithm:** Hierarchical agglomerative clustering with Ward linkage. Cluster boundaries were selected through dendrogram inspection and silhouette score comparisons across a range of K values.

**Dimension Captured:** Temporal-developmental trajectories of epistemic emphasis — how participants’ roles evolved through phases of problem-solving, idea generation, evaluation, meta-coordination, and clarification.

---
**Replication Prompt (ChatGPT-style):**  
“Using the Polymath dataset with canonicalized move codes (TAP, Idea, Eval, Meta, Clar), replicate the Role-Arc clustering.  
Divide each participant’s timeline into early, middle, and late terciles, calculate proportional frequencies for each move type per stage, apply Laplace smoothing, and compute cosine distances among participants.  
Then, perform hierarchical clustering with Ward linkage and select the optimal number of clusters by comparing silhouette scores across K values.”
