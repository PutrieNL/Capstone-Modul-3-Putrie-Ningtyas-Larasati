# Capstone-Modul-3-Putrie-Ningtyas-Larasati
__Latar Belakang:__
Perusahaan dealer mobil bekas dihadapkan pada tantangan yang signifikan ketika menentukan harga jual untuk kendaraan yang mereka tawarkan. Kesulitan muncul karena setiap penyesuaian harga harus dipertimbangkan dengan cermat. Jika harga ditetapkan terlalu tinggi, risiko kendaraan tidak laku terjual akan meningkat, mengancam profitabilitas dan likuiditas perusahaan. Sebaliknya, jika harga ditetapkan terlalu rendah, perusahaan berisiko mengalami kerugian finansial yang serius.

Dengan memahami kompleksitas pasar mobil bekas yang dinamis, penelitian ini bertujuan untuk mengembangkan penentuan harga yang optimal. Tujuannya tidak hanya untuk meminimalkan risiko kerugian finansial bagi perusahaan, tetapi juga untuk mempertahankan posisi daya saing yang kuat di pasar yang sangat kompetitif.  

__Masalah__
Bagaimana menentukan harga yang optimal untuk mobil bekas agar perusahaan tidak mengalami kerugian finansial dan tetap kompetitif di pasar?

__Tujuan:__
Memberikan informasi data harga mobil bekas yang optimal dengan menyelidiki berbagai faktor yang memengaruhi harga mobil bekas serta merumuskan pendekatan yang efektif untuk menetapkan harga yang memperhitungkan berbagai variabel, seperti kondisi pasar, permintaan konsumen, dan atribut kendaraan. Dengan demikian, penelitian ini akan memberikan kontribusi yang berharga dalam menghadapi tantangan kompleks yang dihadapi oleh perusahaan dealar mobil bekas dalam menentukan harga yang tepat untuk produk mereka.


__Pendekatan Analitik__
Langkah pertama adalah melakukan analisis mendalam terhadap data untuk mengidentifikasi pola yang membedakan mobil satu dengan lainnya.
Selanjutnya, kami akan mengembangkan model regresi untuk menyediakan alat prediksi harga yang optimal untuk harga mobil bekas yang akan dijual. 

__Penilaian Metrik__

Untuk mengevaluasi kinerja model, kami akan menggunakan metrik seperti RMSE (Root Mean Square Error), MAE (Mean Absolute Error), dan MAPE (Mean Absolute Percentage Error). RMSE mengukur seberapa jauh rata-rata prediksi model dari nilai yang diamati, sedangkan MAE memberikan gambaran rata-rata dari seberapa besar kesalahan prediksi dalam nilai absolut. MAPE menyajikan rata-rata persentase kesalahan prediksi oleh model. Semakin kecil nilai RMSE, MAE, dan MAPE, semakin baik kualitas prediksi model.

Selain itu, jika model linear dipilih sebagai model terbaik, kami akan mengevaluasi R-squared atau R-squared yang disesuaikan. R-squared memberikan indikasi seberapa baik model memadankan data observasi, dengan nilai mendekati 1 menunjukkan kesesuaian yang lebih baik. Namun, perlu dicatat bahwa metrik ini tidak cocok untuk model non-linear.
__Kesimpulan:__
Berdasarkan evaluasi, fitur 'Year' dan 'Engine_Size' telah teridentifikasi sebagai faktor yang signifikan dalam menentukan harga mobil bekas dalam model ini.

Dengan menggunakan metrik evaluasi seperti RMSE, MAE, dan MAPE, kita menyimpulkan bahwa model memiliki tingkat akurasi yang dapat diterima, dengan MAPE sekitar 24%. Dengan kata lain, rata-rata prediksi harga mobil bekas memiliki kesalahan sekitar 24% dari harga sebenarnya, terutama dalam rentang harga yang telah dilatih oleh model (minimal harga 10.000).

Meskipun demikian, masih ada potensi untuk meningkatkan kinerja model guna memberikan prediksi yang lebih akurat. Langkah-langkah pengembangan selanjutnya dapat mencakup penambahan fitur, eksplorasi model yang lebih kompleks, atau penyetelan lebih lanjut pada hyperparameter.

Untuk mendapatkan wawasan tambahan tentang kinerja model, disarankan untuk melakukan uji A/B terhadap model yang ada. Dengan uji A/B, kita dapat mengevaluasi efektivitas penggunaan model dalam prediksi harga mobil bekas. Hasil dari uji A/B akan memberikan pemahaman yang lebih baik tentang kekurangan model dan area yang memerlukan perbaikan atau peningkatan.

__Rekomendasi__
- Menambahkan data terkini untukmobil bekas di Arab Saudi yang ditawarkan, jika memungkinakan menambahkan fitur baru seperti Riwayat Servis dan Perawatan: Mobil yang memiliki catatan perawatan yang baik dan dilakukan secara teratur biasanya memiliki nilai jual yang lebih tinggi karena pembeli akan merasa lebih percaya diri terhadap kualitas mobil tersebut.

- Menggunakan model prediksi harga mobil bekas kita dapat mnegembangkan model untuk menentukan harga  mobil bekas yang baru masuk ke pasar. Dengan menganalisis faktor-faktor seperti usia mobil, kondisi, dan menambahkan fitur baru seperti Riwayat Servis dan Perawatan kita dapat memberikan estimasi harga yang optimal untuk mobil bekas yang akan dijual.

- Mengecek Prediksi dengan Nilai Error Tinggi: Pertama, kita perlu menghitung error untuk setiap prediksi model terhadap harga mobil bekas. Kita dapat menggunakan metrik evaluasi seperti Mean Absolute Error (MAE) atau Root Mean Squared Error (RMSE) untuk mengukur kesalahan prediksi.Mengelompokkan Error: Setelah menghitung error untuk setiap prediksi, kita dapat mengelompokkan error ke dalam grup overestimation dan underestimation. Kita dapat menggunakan persentil 5% teratas dari error positif sebagai grup overestimation, dan persentil 5% teratas dari error negatif sebagai grup underestimation. Sementara itu, sisanya akan termasuk dalam grup mayoritas.Menganalisis Hubungan dengan Variabel Independen: Kita dapat menggunakan analisis statistik seperti regresi linier atau pengujian hipotesis untuk mengevaluasi hubungan antara error tersebut dengan variabel independen. Ini akan membantu kita menentukan variabel mana yang memiliki pengaruh signifikan terhadap error model.Penerapan Feature Engineering: Berdasarkan hasil analisis, kita dapat menentukan tindakan perbaikan yang diperlukan. Ini bisa termasuk penerapan feature engineering tambahan, seperti menambahkan atau mengubah fitur-fitur yang ada, untuk meningkatkan kinerja model.Training Ulang Model: Setelah melakukan perbaikan pada fitur-fitur atau variabel yang relevan, kita dapat melatih ulang model menggunakan data yang telah diperbarui. Langkah ini memungkinkan model untuk mempelajari pola yang lebih baik dan menghasilkan prediksi yang lebih akurat.Evaluasi Kembali: Akhirnya, kita dapat mengevaluasi kembali kinerja model yang telah diperbarui menggunakan metrik evaluasi yang sama untuk memastikan bahwa perbaikan yang diimplementasikan telah menghasilkan peningkatan yang signifikan dalam akurasi prediksi.Dengan mengikuti langkah-langkah ini, kita dapat mendapatkan wawasan yang lebih baik tentang faktor-faktor apa yang menyebabkan model menghasilkan error yang tinggi, dan kita dapat melakukan tindakan perbaikan yang tepat untuk meningkatkan kinerja model.
