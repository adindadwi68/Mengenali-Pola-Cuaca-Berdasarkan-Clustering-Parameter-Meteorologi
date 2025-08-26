
> Proyek ini merupakan proyek pribadi menganalisis data parameter cuaca untuk mengenali ola cuaca berdasarkan kelompok parameter yang terbentuk.

## 📁 Struktur Repository
- `Dataset`— [Dataset mentah yang digunakan](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/blob/main/weather_classification_data.csv)
- `Visualization` — [Hasil visualisasi data](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/tree/main/Visual)
- `Notebook` — [Notebook analisis menggunakan Python (Jupyter/Colab)](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/blob/main/KlusteringCuaca.ipynb)
- `README.md` — Halaman utama repo ini.

## 🛠️ Skillset
### 📊 Data Analysis & Manipulation
- `Pandas` (dataframe processing, cleaning, aggregasi)
- `Numpy` (perhitungan numerik & operasi array)

### 📈 Data Visualization
- `matplotlib.pyplot` (visualisasi dasar & kustomisasi)
- `seaborn` (visualisasi statistik)
- `plotly.express & plotly.graph_objects` (visualisasi interaktif, dashboard)
- `plotly.subplots & plotly.figure_factory` (plot kompleks)
- `plottable` (pembuatan tabel interaktif/visual)
- `highlight_text` (annotasi visualisasi)

### 🤖 Machine Learning & Clustering
- `sklearn.cluster.KMeans` (clustering unsupervised)
- `sklearn.cluster.DBSCAN` (clustering berbasis density)
- `sklearn.preprocessing.StandardScaler` (normalisasi & standardisasi data)
- `sklearn.decomposition.PCA` (reduksi dimensi)
- `sklearn.neighbors.NearestNeighbors` (analisis kedekatan data)
- `sklearn.metrics` (evaluasi clustering: Silhouette, Davies–Bouldin, Calinski–Harabasz)

### 📉 Statistik
- `scipy.stats.spearmanr` (analisis korelasi non-parametrik)
- `scipy.stats.anderson` (uji normalitas distribusi)

### ⚙️ Notebook & Styling
- `%matplotlib inline` (setting visualisasi di notebook)
- `matplotlib.cm` (colormap styling)
- `matplotlib.ticker` (format axis)
- `matplotlib.patches` (custom anotasi visual)
- `matplotlib.font_manager` (manajemen font pada visualisasi)


---
# 🌦️ Mengenali Pola Cuaca Berdasarkan Clustering Parameter Meteorologi

Proyek ini melakukan analisis **K-Means Clustering** pada data parameter meteorologi (suhu, kelembaban, curah hujan, tekanan atmosfer, dll) untuk mengenali **pola cuaca** tanpa label awal (*unsupervised learning*).  

Hasil clustering menunjukkan 4 kelompok utama cuaca yang selaras dengan musim, tipe cuaca, cloud cover, dan lokasi geografis.  

## 🔎 Analisis Per Cluster  

### 🌐 Cluster 0  
**Parameter cuaca:**  
- Suhu relatif tinggi (hingga ~32°C)  
- Kelembaban menengah (44–70%)  
- Presipitasi rendah → lebih sering kering  
- Tekanan atmosfer tinggi (~1020 hPa) → stabil  
- UV Index tinggi, jarak pandang baik  

**Distribusi:**  
- **Musim:** Seimbang antara Autumn, Spring, Summer  
- **Weather type:** Sangat dominan *Sunny*  
- **Cloud cover:** Mayoritas *clear* & *partly cloudy*  
- **Lokasi:** Coastal & mountain, seimbang dengan inland  

👉 **Interpretasi:** Cuaca cerah, kering, hangat → tipikal musim transisi atau musim panas.  

---
### 🌐 Cluster 1  
**Parameter cuaca:**  
- Suhu rendah (bahkan < 0°C)  
- Kelembaban sangat tinggi (>80%)  
- Presipitasi tinggi (hingga 74%)  
- Tekanan atmosfer rendah (~990 hPa)  
- UV Index rendah, jarak pandang pendek  

**Distribusi:**  
- **Musim:** Sangat dominan *Winter*  
- **Weather type:** Didominasi *Snowy*, sebagian *Rainy*  
- **Cloud cover:** Mayoritas *overcast*  
- **Lokasi:** Inland & mountain  

👉 **Interpretasi:** Cuaca dingin, basah, mendung/bersalju → khas musim dingin / musim hujan ekstrem.  

---
### 🌐 Cluster 2  
**Parameter cuaca:**  
- Suhu menengah (20–27°C)  
- Kelembaban tinggi (~80%)  
- Presipitasi tinggi  
- Tekanan atmosfer menengah (~1005 hPa)  
- UV Index rendah  

**Distribusi:**  
- **Musim:** Muncul di semua musim, cukup seimbang  
- **Weather type:** Sangat dominan *Rainy*  
- **Cloud cover:** Banyak *overcast*  
- **Lokasi:** Lebih banyak di coastal  

👉 **Interpretasi:** Pola hujan tropis/monsoon → hujan lebat, lembab, dan berawan.  

---
### 🌐 Cluster 3  
**Parameter cuaca:**  
- Suhu relatif hangat (22–28°C)  
- Kelembaban menengah (~65%)  
- Presipitasi sedang (20–30%)  
- Tekanan atmosfer relatif tinggi (~1010 hPa)  
- UV Index sedang  

**Distribusi:**  
- **Musim:** Banyak di *Spring* & *Autumn*  
- **Weather type:** Campuran (Cloudy, sebagian Sunny)  
- **Cloud cover:** Dominan *overcast* & *partly cloudy*  
- **Lokasi:** Tersebar rata (coastal, inland, mountain)  

👉 **Interpretasi:** Pola peralihan musim (transisi) → cuaca tidak ekstrem, campuran cerah & mendung.  

----

### ✨ Ringkasan Pola Cuaca  

- **Cluster 0** → Cerah & kering → Summer / Transisi → 🌞  
- **Cluster 1** → Dingin & basah → Winter / Ekstrem → ❄️  
- **Cluster 2** → Hujan tropis → Rainy / Monsoon → 🌧️  
- **Cluster 3** → Transisi musim → Campuran cerah & mendung → ⛅  

---
## 📬 Kontak
- 📧 Email: [adindadwiilestari@gmail.com](mailto:adindaddwiilestari@gmail.com)
- 💬 Telegram: [@rynt68](https://t.me/rynt68)
- 💼 LinkedIn: [Adinda Dwi Lestari](https://linkedin.com/in/adindadwi06)
