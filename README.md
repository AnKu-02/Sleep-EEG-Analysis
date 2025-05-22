# 🧠 Sleep-EEG-Analysis

**Analyzing the Impact of Slow-Wave and Spindle Coupling on Memory Consolidation During Sleep**  
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
  Used [`YASA`](https://github.com/raphaelvallat/yasa) (based on MNE) to detect slow waves and spindles

- **Coupling Metric**:  
  Counted spindles that peaked within ±1s of a slow-wave trough; normalized by N2/N3 sleep duration

- **Analysis**:  
  Applied **Pearson** and **Spearman correlation** to assess associations with memory scores

- **Visualization**:  
  Plotted trends using **Matplotlib** and **Seaborn**

---

## 📊 Visualizations

### 🧠 EEG Feature Detection

**Raw EEG Segment (Preprocessed)**  
![Raw EEG](results/raw_filtered_eeg_example.png)

**Detected Slow Wave**  
![Slow Wave](results/slowwave.png)

**Detected Spindle**  
![Spindle](results/spindle.png)

---

### 📉 Coupling Distributions

**Histogram: % of Spindles Coupled and Coupling Time**  
![Coupling Histograms](results/histograms_coupling_memory.png)

---

### 🔍 Correlation Analysis

**Coupling Metrics vs Memory Recall**  
![Heatmap Recall](results/heatmap_recall.png)

**Coupling Metrics vs Retention Scores**  
![Heatmap Retention](results/heatmapretention.png)

---

### 📈 Correlation Plots

**Coupling vs Memory Score**  
![Spindle vs Memory](results/scatter_spindle_memory.png)

**Coupling Time (N2/N3) vs Memory Score**  
![Coupling Time vs Memory](results/scatter_time_memory.png)

---

## 🧰 Tech Stack

- `Python`
- `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`
- `MNE-Python`, `YASA`, `SciPy`

