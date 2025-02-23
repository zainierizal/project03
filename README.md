California House Pricing

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

