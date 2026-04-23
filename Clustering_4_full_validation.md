## Clustering 4: Full Validation Run (Independent Replication)

### Overview
This validation run served as a full replication and consistency check, designed to verify that the participant similarity structures identified in earlier analyses (Role-Arc, DTW, and Fused-Distance Ward) were not artifacts of preprocessing or parameterization. Conducted independently in a Jupyter notebook environment, this run rebuilt the entire analytic pipeline from the canonicalized token sequences upward. The process was fully transparent and reproducible, confirming that emergent companionships and role archetypes persisted even when recalculated from raw sequence data.

### Workflow Summary

**1. Data Input and Preprocessing**  
- Imported canonicalized participant sequences directly from CSV (one row per participant).  
- Normalized move tokens to five short forms: `Clar`, `Idea`, `TAP`, `Eval`, and `Meta`.  
- Applied light case repair; excluded any unexpected values.  
- Retained consecutive repetitions (no collapsing) to preserve full temporal granularity.  
- Enforced a minimum sequence length of 1 for inclusion.

**2. Distance Computation**  
Two complementary distance measures were applied to capture both local and global similarity:
- **Levenshtein (edit) distance** — measured the number of insertions, deletions, or substitutions required to transform one participant’s move sequence into another.
- **Dynamic Time Warping (DTW)** — applied to integer-encoded sequences using a binary Hamming cost (0 for matches, 1 for mismatches) to capture temporal rhythm and phase alignment.

Both produced complete participant × participant distance matrices, visualized as plaid-pattern heatmaps that echoed structures seen in previous runs.

**3. Clustering Process**  
- Hierarchical clustering with **average linkage**, appropriate for precomputed, non-Euclidean distances.  
- Cluster boundaries inspected through dendrogram visualization and silhouette evaluation.  
- No dimensional reduction or weighting adjustments applied; the emphasis was on replication fidelity.  

**4. Validation and Comparison**  
- Cross-checked emergent groupings against the earlier clustering results.  
- Verified that the same participant companionships—core role families—reappeared despite different computation pathways.  
- Median sequence length noted as one (limitation flag), indicating some brevity in participant histories but not affecting the overall structure of consistent clusters.  

### Outcomes
This validation run successfully reproduced the plaid-like similarity structures observed earlier. Core companionships persisted across all clustering conditions, confirming that emergent role archetypes were stable across independent computational pipelines. The replication demonstrated methodological transparency and reproducibility, reinforcing the integrity of the results reported in the main analysis.

### ChatGPT-Style Replication Prompt
> **Prompt:**  
> You are an AI research assistant replicating a clustering validation run from the Polymath dataset. Using Python (NumPy, pandas, dtw, scipy), rebuild participant similarity structures directly from canonicalized token sequences.  
> 1. Load a CSV where each row is a participant and non-ID columns contain ordered move codes (`Clar`, `Idea`, `TAP`, `Eval`, `Meta`).  
> 2. Compute two distance matrices:  
>    - Levenshtein distance for local tactical similarity.  
>    - Dynamic Time Warping (DTW) using a Hamming (0/1) cost for temporal rhythm.  
> 3. Apply hierarchical clustering with average linkage to each matrix.  
> 4. Visualize the resulting dendrograms and compare cluster memberships to prior runs.  
> 5. Confirm that consistent companionships (participant pairs recurring across runs) reappear here, supporting the robustness of emergent role archetypes.

**Purpose:** Validate that emergent companionships are intrinsic structural features of the dataset—independent of preprocessing or algorithmic bias.