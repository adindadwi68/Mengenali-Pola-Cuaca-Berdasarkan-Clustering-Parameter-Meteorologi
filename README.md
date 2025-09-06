
> Proyek ini merupakan proyek pribadi menganalisis data parameter cuaca untuk mengenali ola cuaca berdasarkan kelompok parameter yang terbentuk.

## 📁 Struktur Repository
- `Dataset`— [Dataset mentah yang digunakan](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/blob/main/weather_classification_data.csv)
- `Visualization` — [Hasil visualisasi data](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/tree/main/Visual)
- `Notebook` — [Notebook analisis menggunakan Python (Jupyter/Colab)](https://github.com/adindadwi68/Mengenali-Pola-Cuaca-Berdasarkan-Clustering-Parameter-Meteorologi/blob/main/KlasifikasiCuaca.ipynb)
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
# 🌦️ Identifikasi Pola Cuaca Berdasarkan Parameter Meteorologi

Penelitian ini bertujuan untuk mengidentifikasi pola cuaca berdasarkan parameter meteorologi dengan menggunakan metode Decision Tree. Atribut target yang digunakan adalah Weather Type, yaitu variabel kategorikal yang merepresentasikan jenis cuaca. Sebelum proses klasifikasi, dilakukan serangkaian praproses data. Tahap awal adalah pemeriksaan missing value, dan hasilnya menunjukkan bahwa dataset tidak memiliki nilai yang hilang. Selanjutnya, seleksi atribut dilakukan dengan melihat korelasi antar variabel numerik. Berdasarkan uji distribusi, data diketahui tidak terdistribusi normal sehingga dipilih korelasi Spearman yang lebih tahan terhadap noise. Hasil analisis menunjukkan bahwa semua atribut numerik memiliki korelasi signifikan sehingga tidak ada variabel yang dieliminasi.

Proses berikutnya adalah deteksi dan penghapusan outlier dengan memanfaatkan metode DBSCAN yang dipadukan dengan PCA untuk mereduksi dimensi menjadi dua, sehingga titik data yang bukan core point maupun border point dianggap sebagai noise dan dihapus. Setelah itu, validasi pengelompokan data dilakukan menggunakan algoritma K-Means, juga dengan bantuan PCA, untuk memastikan keterkelompokan data sesuai tipe cuaca yang ada. Evaluasi korelasi ulang menunjukkan adanya peningkatan nilai korelasi Spearman, yang menandakan bahwa proses filtering berhasil meningkatkan kualitas data.

<p align="center">
<img width="835" height="235" alt="performance2" src="https://github.com/user-attachments/assets/cabeab7a-b580-4264-9d9a-ff91a39839d4" />
</p>

Tahap akhir adalah klasifikasi menggunakan Decision Tree yang diimplementasikan dengan Python (scikit-learn) dan RapidMiner. Hasil klasifikasi menunjukkan tingkat akurasi yang sangat tinggi, yakni 99,56%. Nilai precision dan recall untuk seluruh kelas cuaca (Rainy, Sunny, Cloudy, dan Snowy) juga konsisten berada di atas 99%, yang mengindikasikan bahwa model mampu memprediksi setiap jenis cuaca secara seimbang tanpa terjadi bias signifikan antar kelas.

![tree_highres](https://github.com/user-attachments/assets/6c67d738-e1b1-4c19-8c40-349620862502)

Interpretasi terhadap struktur Decision Tree menunjukkan adanya perbedaan titik awal pemisahan antara implementasi Python dan RapidMiner. Pada model yang dibangun menggunakan Python, atribut utama yang dipilih adalah Precipitation (%). Jika nilai presipitasi rendah (≤ 49,5%), data selanjutnya dipisahkan berdasarkan UV Index untuk membedakan kondisi Cloudy dan Sunny. Sementara itu, pada kondisi presipitasi tinggi (> 49,5%), pemisahan lebih lanjut ditentukan oleh Temperature untuk membedakan antara Snowy dan Rainy.

<p align="center">
<img width="437" height="431" alt="decision tree rapid" src="https://github.com/user-attachments/assets/1818ec21-281a-4f58-988f-0c8ac408ca15" />
</p>

Sebaliknya, pada model RapidMiner, atribut utama yang dipilih sebagai pemisah pertama adalah Temperature. Suhu rendah (≤ 6°C) langsung mengarah pada kondisi Snowy, sedangkan suhu tinggi (> 6°C) dipisahkan lebih lanjut berdasarkan UV Index untuk membedakan Sunny dan kondisi presipitasi. Pada percabangan berikutnya, variabel Precipitation (%) dan Atmospheric Pressure berperan dalam membedakan antara Cloudy, Rainy, dan Snowy.

Perbedaan struktur pohon ini menunjukkan bahwa algoritma Decision Tree dapat menghasilkan aturan yang berbeda tergantung pada implementasi, parameter yang ditentukan, serta metode perhitungan information gain yang digunakan. Namun demikian, kedua model tetap menegaskan bahwa variabel Temperature, Precipitation (%), dan UV Index merupakan parameter yang paling dominan dalam mengklasifikasikan tipe cuaca.

---
## 📬 Kontak
- 📧 Email: [adindadwiilestari@gmail.com](mailto:adindaddwiilestari@gmail.com)
- 💬 Telegram: [@rynt68](https://t.me/rynt68)
- 💼 LinkedIn: [Adinda Dwi Lestari](https://linkedin.com/in/adindadwi06)
