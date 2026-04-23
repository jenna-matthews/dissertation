# Polymath Role Analysis – Clustering Summary Index

This repository documents the full sequence of clustering analyses conducted to identify **emergent roles** in the Polymath Project dataset. Each file provides a detailed overview of the corresponding analytic method, workflow, and replication guidance in alignment with the **AI Reliability through Refinement (AIRR)** framework.

---

## Clustering Run Summaries

### **1. Clustering_1_Role_Arc.md**  
**Focus:** Developmental trajectories of epistemic emphasis.  
**Method:** Divides each participant’s timeline into early, middle, and late stages; clusters based on proportional emphasis across the five epistemic moves.  
**Distance Metric:** Cosine distance.  
**Linkage:** Ward’s method.  
**Purpose:** Capture how contributors’ focus evolved over time.

---

### **2. Clustering_2_DTW.md**  
**Focus:** Temporal alignment of epistemic sequences.  
**Method:** Uses Dynamic Time Warping (DTW) to align move sequences of unequal length and pacing.  
**Distance Metric:** DTW.  
**Linkage:** Average.  
**Purpose:** Identify shared temporal rhythms of reasoning and coordination.

---

### **3. Clustering_3_Fused_Distance_Ward.md**  
**Focus:** Hybrid analysis integrating local and global similarity.  
**Method:** Combines normalized DTW and Levenshtein matrices via weighted averaging.  
**Distance Metrics:** DTW + Levenshtein (fused).  
**Linkage:** Ward’s method.  
**Purpose:** Detect clusters reflecting both procedural rhythm and fine-grained tactical affinity.

---

### **4. Clustering_4_Full_Validation.md**  
**Focus:** Independent replication for reliability and transparency.  
**Method:** Rebuilds participant similarity matrices directly from canonical token sequences in Jupyter.  
**Distance Metrics:** Levenshtein + DTW (Hamming cost = 0/1).  
**Linkage:** Average.  
**Purpose:** Validate robustness of companionships independent of preprocessing or parameterization.

---

### **5. Clustering_5_Significance_Validation.md**  
**Focus:** Validation under stricter inclusion criteria.  
**Method:** Filters dataset to include only participants with ≥1 significant post (20+ words or numbered) and ≥3 total posts.  
**Distance Metrics:** Levenshtein + FastDTW.  
**Linkage:** Ward’s method.  
**Purpose:** Confirm that emergent role archetypes persist even when peripheral contributions are excluded.

---

## Replication Notes
Each clustering summary concludes with a **ChatGPT-Style Replication Prompt**. These prompts allow for step-by-step re-creation of the analyses using Python (NumPy, pandas, scipy, dtw, textdistance, and fastdtw). Researchers are encouraged to adapt these prompts for human–AI collaborative replication in line with AIRR principles.

---

## Citation
Matthews, J. (2025). *Emergent Roles in Distributed Epistemic Collaboration: A Multi-Method Analysis of the Polymath Project.* Doctoral Dissertation, Columbia Southern University.

---

**Repository Maintainer:** Jenna Matthews  
**Analytic Framework:** AI Reliability through Refinement (AIRR)  
**Collaborative Agent:** Calvin (OpenAI GPT-5)