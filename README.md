#**California House Pricing**

**1.1. Latar Belakang**

Harga rumah di California dipengaruhi oleh berbagai faktor kompleks, seperti lokasi, ukuran properti, kondisi pasar, dan karakteristik lingkungan sekitar. Beberapa faktor utama yang memengaruhi harga rumah antara lain jumlah populasi, jumlah rumah tangga, total ruangan dan kamar, kedekatan dengan pantai, usia bangunan, serta pendapatan rata-rata penduduk setempat. Faktor-faktor ini saling berinteraksi untuk menentukan nilai pasar properti di wilayah tersebut.

**1.2. Permasalahan**

Masalah utama yang dihadapi adalah bagaimana cara **memprediksi harga rumah** secara akurat berdasarkan berbagai faktor yang mempengaruhinya, seperti ukuran rumah, lokasi, pendapatan penduduk, dan kedekatan dengan fasilitas umum atau pantai. Prediksi harga yang akurat sangat penting untuk membantu para pelaku bisnis properti dalam **menetapkan harga jual yang tepat** dan **menghindari kerugian** akibat kesalahan dalam penetapan harga.

**1.3. Tujuan**

Tujuan utama dari model prediksi harga rumah adalah untuk **menurunkan kesalahan prediksi** (mengurangi **MSE** atau **MAPE**) dengan memanfaatkan data seperti **lokasi**, **ukuran rumah**, **pendapatan median**, dan **jumlah rumah tangga**. Dengan meningkatkan akurasi prediksi, model ini dapat membantu pengembang dan agen properti **menetapkan harga jual** yang lebih akurat dan relevan dengan kondisi pasar.

**1.4.Stakeholder yang Terlibat**

Model **prediksi harga rumah** ini akan digunakan oleh berbagai pihak yang terlibat dalam industri properti, antara lain:
1. **Pengembang properti dan investor real estate**: Mereka akan memanfaatkan model ini untuk memprediksi harga rumah di berbagai wilayah berdasarkan faktor-faktor yang ada dalam data, seperti lokasi, ukuran rumah, dan pendapatan rumah tangga.
2. **Agen real estate**: Mereka akan menggunakan model ini untuk menetapkan harga jual rumah yang lebih akurat.
3. **Pemerintah atau pembuat kebijakan**: Mereka juga menggunakan model untuk merencanakan pembangunan infrastruktur yang berdampak pada harga properti.
4. **Calon pembeli rumah**: Calon pembeli akan memanfaatkan model ini untuk mendapatkan gambaran lebih jelas tentang harga yang wajar dan sesuai dengan anggaran mereka di berbagai kawasan.

Model ini juga akan digunakan setiap kali ada permintaan untuk **memperkirakan harga rumah**, terutama ketika ada perubahan **di pasar properti**, misalnya perubahan demografis atau infrastruktur baru.

**1.5. Metric Evaluation**

Model ini akan dievaluasi menggunakan beberapa **metrik evaluasi** untuk memastikan kualitas prediksi harga rumah, dengan **prioritas pada RMSE**. Metrik yang digunakan adalah:

1. **RMSE (Root Mean Squared Error)**: RMSE adalah metrik yang sangat berguna untuk mengukur kesalahan kuadrat rata-rata antara nilai yang diprediksi dan nilai aktual. Metrik ini memiliki prioritas tertinggi karena **memberikan penalti lebih besar pada kesalahan besar**, yang penting dalam konteks prediksi harga rumah, di mana kesalahan besar bisa sangat mempengaruhi keputusan harga dan investasi.
   
2. **MAE (Mean Absolute Error)**: MAE mengukur rata-rata kesalahan absolut antara prediksi dan nilai aktual, tanpa memberi bobot lebih pada kesalahan besar. Ini memberikan gambaran yang lebih sederhana dan konsisten tentang kesalahan model, meskipun kurang sensitif terhadap perbedaan besar.

3. **MAPE (Mean Absolute Percentage Error)**: MAPE mengukur kesalahan dalam bentuk persentase, memberikan gambaran seberapa besar kesalahan prediksi dalam konteks relatif terhadap nilai aktual. Ini membantu untuk melihat kinerja model dalam skala persentase, meskipun bisa lebih sensitif terhadap nilai-nilai kecil.

    **Prioritas Penggunaan Metrik**:
    Model ini lebih memprioritaskan **RMSE** sebagai metrik utama karena pentingnya meminimalkan kesalahan prediksi yang besar pada harga rumah. Pengurangan RMSE akan memastikan bahwa model tidak hanya akurat dalam rata-rata, tetapi juga dapat menghindari kesalahan besar yang dapat mengarah pada keputusan investasi yang merugikan.

## **1.6 KESIMPULAN**

### 1.6.1 **METRIC EVALUATION PADA MODEL XGBOOST**

Dengan menggunakan algoritma **Xgboost** pada **Step Kedua**, didapatkan sebuah model machine learning terbaik untuk memprediksi harga rumah di California dengan metric evaluation sebagai berikut:

1. **RMSE (35,615.92)**
   - **Interpretasi**: RMSE mengukur akar rata-rata dari kuadrat kesalahan prediksi model dalam satuan yang sama dengan harga rumah (USD). Nilai **35,615.92 USD** menunjukkan bahwa, secara rata-rata, model salah memprediksi harga rumah sekitar **35,615.92 USD**.
   - **Real Case**: Jika harga rumah yang sebenarnya adalah 300,000 USD, model mungkin memperkirakan harga sekitar **264,384.08 USD** (300,000 - 35,615.92) atau **335,615.92 USD** (300,000 + 35,615.92). Kesalahan sebesar ini bisa berpengaruh besar pada keputusan pembelian atau penjualan rumah.

2. **MAE (24,269.22)**
   - **Interpretasi**: MAE mengukur rata-rata kesalahan mutlak antara prediksi dan harga aktual tanpa memperhatikan arah kesalahan (lebih tinggi atau lebih rendah). Nilai **24,269.22 USD** menunjukkan bahwa, secara rata-rata, model membuat kesalahan sebesar ini dalam setiap prediksi.
   - **Real Case**: Dengan harga rumah 300,000 USD, kesalahan prediksi model bisa sekitar **275,730.78 USD** (300,000 - 24,269.22) atau **324,269.22 USD** (300,000 + 24,269.22). Kesalahan ini menunjukkan seberapa besar variasi prediksi yang mungkin terjadi, yang bisa berdampak pada keakuratan penetapan harga atau tawar-menawar dalam transaksi properti.

3. **MAPE (14.41%)**
   - **Interpretasi**: MAPE mengukur kesalahan prediksi sebagai persentase dari harga rumah yang sebenarnya. Nilai **14.41%** berarti model memprediksi harga rumah dengan kesalahan sekitar **43,230 USD** (14.41% x 300,000 USD).
   - **Real Case**: Jika harga rumah yang sebenarnya adalah 300,000 USD, prediksi model bisa berada dalam kisaran **256,770 USD** (300,000 - 43,230) atau **343,230 USD** (300,000 + 43,230). Kesalahan sebesar ini memberikan gambaran tentang seberapa besar deviasi relatif terhadap harga rumah yang sesungguhnya, yang relevan dalam pengambilan keputusan oleh pembeli atau penjual.
  
Berdasarkan gambar yang Anda unggah, berikut adalah penyesuaian untuk **Feature Importance pada Model XGBoost** yang lebih sesuai dengan hasil visual yang ditunjukkan dalam grafik:

---

### **1.6.2 FEATURE IMPORTANCE PADA MODEL**

1) **`ocean_proximity_INLAND`**:  
   - **Deskripsi**: Menunjukkan kedekatan rumah dengan daerah pedalaman.  
   - **Pemrosesan**: Fitur ini memiliki bobot terbesar dalam model, yang menunjukkan bahwa kedekatan rumah dengan daerah pedalaman sangat mempengaruhi prediksi harga rumah.  
   - **Tujuan**: Model memanfaatkan kedekatan rumah dengan area pedalaman untuk menilai harga rumah secara signifikan.

2) **`longitude`**:  
   - **Deskripsi**: Koordinat geografis rumah di sepanjang garis bujur.  
   - **Pemrosesan**: Fitur ini juga memiliki pengaruh yang besar dalam model, yang menunjukkan bahwa lokasi geografis rumah secara langsung memengaruhi harga rumah.  
   - **Tujuan**: Memahami hubungan harga rumah dengan lokasi geografis di sepanjang garis bujur.

3) **`ocean_proximity_<1H OCEAN`**:  
   - **Deskripsi**: Menunjukkan kedekatan rumah dengan laut dalam jarak kurang dari satu jam.  
   - **Pemrosesan**: Fitur ini juga cukup penting dalam model, meskipun tidak sebesar `ocean_proximity_INLAND` dan `longitude`.  
   - **Tujuan**: Memahami bagaimana kedekatan dengan laut mempengaruhi harga rumah.

4) **`ocean_proximity_NEAR OCEAN`**:  
   - **Deskripsi**: Menunjukkan kedekatan rumah dengan laut.  
   - **Pemrosesan**: Fitur ini menunjukkan pentingnya kedekatan dengan laut dalam memprediksi harga rumah, meskipun tidak seberpengaruh `INLAND`.  
   - **Tujuan**: Menangkap pola harga rumah berdasarkan kedekatannya dengan laut.

5) **`median_income`**:  
   - **Deskripsi**: Pendapatan median rumah tangga di daerah tersebut.  
   - **Pemrosesan**: Menunjukkan pengaruh besar pada harga rumah karena pendapatan median sering kali berhubungan erat dengan daya beli dan harga rumah.  
   - **Tujuan**: Mengidentifikasi hubungan antara pendapatan rumah tangga dan harga rumah.

6) **`population_room`**:  
   - **Deskripsi**: Rasio jumlah populasi terhadap jumlah ruang.  
   - **Pemrosesan**: Meskipun tidak sepopuler beberapa fitur lainnya, fitur ini masih memiliki pengaruh yang cukup penting dalam model.  
   - **Tujuan**: Memahami hubungan antara kepadatan penduduk dan harga rumah.

7) **`ocean_proximity_NEAR BAY`**:  
   - **Deskripsi**: Menunjukkan kedekatan rumah dengan teluk.  
   - **Pemrosesan**: Meskipun penting, pengaruh fitur ini relatif lebih kecil dibandingkan dengan fitur kedekatan laut atau pedalaman.  
   - **Tujuan**: Menggambarkan bagaimana kedekatan dengan teluk mempengaruhi harga rumah.

8) **`latitude`**:  
   - **Deskripsi**: Koordinat geografis rumah di sepanjang garis lintang.  
   - **Pemrosesan**: Meskipun pengaruhnya lebih kecil dibandingkan dengan `longitude`, fitur ini masih memberikan kontribusi pada model.  
   - **Tujuan**: Menggambarkan hubungan lokasi geografis rumah di lintang dengan harga rumah.

9) **`bedroom_household`**:  
   - **Deskripsi**: Jumlah kamar tidur per rumah tangga.  
   - **Pemrosesan**: Fitur ini memiliki pengaruh yang lebih kecil dalam model dan hanya sedikit mempengaruhi harga rumah.  
   - **Tujuan**: Menangkap hubungan antara jumlah kamar tidur per rumah tangga dan harga rumah.

10) **`housing_median_age`**:  
   - **Deskripsi**: Usia median rumah di area tersebut.  
   - **Pemrosesan**: Meskipun penting, fitur ini memiliki pengaruh yang lebih kecil dibandingkan dengan fitur lainnya.  
   - **Tujuan**: Menangkap hubungan antara usia rumah dan harga rumah, meskipun pengaruhnya terbatas.

---

### 1.6.3 LIMITASI MODEL

Setelah dilakukan penghilangan outlier pada kolom target **`median_house_value`**, model menjadi lebih terfokus pada prediksi harga rumah yang realistis dan sesuai dengan kategori lokasi masing-masing. Namun, penghilangan outlier ini juga mengakibatkan **model memiliki limit dalam memprediksi harga rumah**, yang berarti model hanya dapat memberikan prediksi dalam rentang harga tertentu sesuai dengan kategori **`ocean_proximity`**. Dampak dari limitasi adalah sebagai berikut.

1. **INLAND:**
   - **Limit Prediksi Harga**: Model hanya dapat memprediksi harga rumah dalam rentang **14999 - 255200 USD** untuk kategori **INLAND**.
   - **Konsekuensi**: Jika harga rumah di daerah pedalaman lebih rendah dari 14,999 USD atau lebih tinggi dari 255,200 USD, model tidak akan dapat memberikan prediksi yang akurat atau mungkin tidak dapat memberikan prediksi sama sekali. Ini membatasi aplikasi model hanya untuk harga rumah dalam rentang tersebut.

2. **NEAR BAY:**
   - **Limit Prediksi Harga**: Model hanya dapat memprediksi harga rumah dalam rentang **22500 - 427300 USD** untuk kategori **NEAR BAY**.
   - **Konsekuensi**: Prediksi harga rumah di wilayah dekat teluk yang berada di luar rentang harga ini (baik lebih rendah dari 22,500 USD atau lebih tinggi dari 427,300 USD) tidak akan akurat. Model menjadi terbatas dalam memperkirakan harga rumah di area tersebut, yang mengurangi fleksibilitas model.

3. **NEAR OCEAN:**
   - **Limit Prediksi Harga**: Model hanya dapat memprediksi harga rumah dalam rentang **37500 - 426400 USD** untuk kategori **NEAR OCEAN**.
   - **Konsekuensi**: Untuk rumah yang terletak dekat dengan laut, jika harga rumah berada di luar rentang ini, model tidak akan dapat memberikan prediksi yang tepat. Ini membatasi aplikasinya pada harga rumah yang realistis di wilayah tersebut.

4. **<1H OCEAN:**
   - **Limit Prediksi Harga**: Model hanya dapat memprediksi harga rumah dalam rentang **17500 - 427300 USD** untuk kategori **<1H OCEAN**.
   - **Konsekuensi**: Model menjadi terbatas dalam memprediksi harga rumah yang lebih rendah dari 17,500 USD atau lebih tinggi dari 427,300 USD. Prediksi harga di luar rentang ini mungkin tidak valid atau bahkan tidak tersedia.

5. **ISLAND:**
   - **Tidak Diperuntukkan**: Karena kategori **ISLAND** memiliki hanya dua data yang sangat sedikit dan tidak representatif, model **tidak diperuntukkan** untuk memprediksi harga rumah di kategori ini.
   - **Konsekuensi**: Data yang sangat terbatas membuat kategori ini tidak dapat digunakan untuk memprediksi harga rumah. Oleh karena itu, **ISLAND** dihapus dari model, yang juga berarti model tidak dapat memperkirakan harga rumah di wilayah ini.

