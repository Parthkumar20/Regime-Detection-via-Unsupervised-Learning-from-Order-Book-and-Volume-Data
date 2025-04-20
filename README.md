# Regime-Detection-via-Unsupervised-Learning-from-Order-Book-and-Volume-Data
This project focuses on identifying distinct **market regimes** using unsupervised machine learning techniques applied to high-frequency order book and trade data. The goal is to segment market behavior and analyze transitions between different regimes to better understand market dynamics.
## 📂 Dataset

- 📁 `depth20_1000ms.zip`: Contains Binance order book snapshots at 1-second intervals.
- 📁 `aggTrade.zip`: Contains aggregated trade data from Binance over the same period.

---

## 📊 Features Extracted

- **Mid Price**
- **Bid-Ask Spread**
- **Order Imbalance**
- **Volume and Trade Intensity**
- **Price Volatility**

---

## 🧪 Clustering Algorithms Used

### 🔹 KMeans Clustering
- Applied to engineered features
- Fixed number of clusters
- Good baseline to interpret regime behavior

### 🔹 HDBSCAN Clustering
- Density-based clustering
- Automatically detects noise and variable-density clusters
- Revealed more natural regime separation in time

---

## 📈 Transition Matrix

We calculated regime transition probabilities to analyze the temporal evolution and stickiness of each regime.

<p align="center">
  <img src="path_to_your_hdbscan_transition_plot.png" width="600"/>
</p>

---

## 🖼️ Regime Visualization

Mid price plotted with color-coded regimes over time.

<p align="center">
  <img src="path_to_your_regime_timeseries_plot.png" width="800"/>
</p>

---

## 🛠️ Libraries & Tools

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`
- `hdbscan`
- Jupyter Notebook / Colab

---

## 🔍 Key Insights

- Certain regimes are **more stable**, others switch frequently.
- HDBSCAN captured nuanced market dynamics with better noise handling.
- Transition matrix revealed periods of high vs. low volatility.

---

## 📁 Structure

```bash
├── data/
│   ├── depth20_1000ms/
│   └── aggTrade/
├── notebooks/
│   └── clustering_analysis.ipynb
├── plots/
│   ├── regime_transition_matrix.png
│   └── regime_timeseries.png
├── README.md
└── requirements.txt
