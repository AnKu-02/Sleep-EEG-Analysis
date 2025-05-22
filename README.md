## **Analyzing the Impact of Slow-Wave and Spindle Coupling on Memory Consolidation During Sleep**  
*A collaborative project between the University of Stuttgart and the University of Freiburg*

This project explores how brain wave activity during sleep may relate to memory performance. We used EEG data from ~1,900 participants (Basel Sleep Dataset) to study the timing of two types of brain rhythms—**slow waves** and **sleep spindles**—and whether their temporal alignment (**coupling**) supports memory consolidation.

---

## 🧾 Project Summary

- During deep (NREM) sleep, the brain shows rhythmic activity such as **slow waves** and **sleep spindles**.
- Some research suggests that when these two rhythms align (i.e., **couple**), it may help store memories more effectively.
- This project uses automated tools to detect coupling and tests whether coupling strength predicts better memory after sleep.

---

## 📚 Dataset Used

- **Source**: [Basel Sleep Dataset](https://www.nature.com/articles/s41597-022-01204-5)  
- **Participants**: ~1,900 healthy adults  
- **EEG Setup**: 4-channel EEG (Fz, Cz, C3, Pz), EOG, EMG  
- **Memory Tasks**: Emotional image recall, 3-back working memory, and motor sequence learning (before and after sleep)

---

## ⚙️ Methods & Tools

- **Sleep Event Detection**:  
  Used [`YASA`](https://github.com/raphaelvallat/yasa) (built on MNE) to detect slow waves and spindles

- **Coupling Metric**:  
  Counted spindles that peaked within ±1s of a slow-wave trough  
  Normalized coupling metrics by **N2/N3 sleep duration**

- **Analysis**:  
  Applied **Pearson** and **Spearman correlation** to assess associations with memory scores

- **Visualization**:  
  Plotted trends using **Matplotlib** and **Seaborn**

---

## 📊 Visualizations

### 🧠 EEG Feature Detection

**Raw EEG Segment (Preprocessed)**  
<img src="results/raw_filtered_eeg_example.png" alt="Raw EEG" width="500"/>

**Detected Slow Wave**  
<img src="results/slowwave.png" alt="Slow Wave" width="500"/>

**Detected Spindle**  
<img src="results/spindle.png" alt="Spindle" width="500"/>

---

### 📉 Coupling Distributions

**Histogram: % of Spindles Coupled and Coupling Time**  
<img src="results/histograms_coupling_memory.png" alt="Coupling Histograms" width="600"/>

---

### 🔍 Correlation Analysis

**Coupling Metrics vs Memory Recall**  
<img src="results/heatmap_recall.png" alt="Heatmap Recall" width="600"/>

**Coupling Metrics vs Retention Scores**  
<img src="results/heatmapretention.png" alt="Heatmap Retention" width="600"/>

---

### 📈 Individual Correlation Plots

**Spindle Coupling vs Memory Score**  
<img src="results/scatter_spindle_memory.png" alt="Spindle vs Memory" width="600"/>

**Coupling Time (N2/N3) vs Memory Score**  
<img src="results/scatter_time_memory.png" alt="Coupling Time vs Memory" width="600"/>

---

## 🧰 Tech Stack

- `Python`
- `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`
- `MNE-Python`, `YASA`, `SciPy`

