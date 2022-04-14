# Analysis-and-Visualization
Analysis and Visualization Melbourne Housing Dataset

**Context**

Sebuah perusahaan real estate memiliki data penjualan dari tahun 2016-2018, perusahaan ingin memiliki pengetahuan tentang penyebaran rumah-rumah berdasarkan tipe dan lokasinya. Jadi ketika seorang customer datang ingin membeli rumah dengan keinginan tertentu, agent real estate bisa mengetahui rumah mana yang cocok untuk customer tersebut


**Goals**

Perusahaan ingin memiliki kemampuan untuk memberikan rekomendasi rumah yang cocok untuk tiap customer nya, sehingga dapat meningkatkan penjualan melalui perusahaan tersebut

**Analytic Approach**

Jadi kita melakukan uji statistik dengan bantuan visualisasi agar proses dari analysis lebih mudah di interpretasikan

**Data Understanding**

Ini adalah kumpulan data yang dibuat oleh Tony Pino.

Itu diambil dari hasil yang tersedia untuk umum yang diposting setiap minggu dari Domain.com.au. Dia membersihkannya dengan baik, dan sekarang terserah Anda untuk membuat keajaiban analisis data. Dataset tersebut meliputi Alamat, Jenis Properti, Pinggiran Kota, Cara Penjualan, Kamar, Harga, Agen Real Estate, Tanggal Penjualan dan Jarak dari C.B.D.

https://www.kaggle.com/datasets/dansbecker/melbourne-housing-snapshot

# Data Cleaning

kolom-kolom yang di drop:
* Bedroom 2 : isi dari data ini sama dengan di kolom Rooms, jadi kita menggunakan salah satu nya saja
* YearBuilt : di drop karena memiliki missing value yang cukup banyak dan tidak bisa di iisi berdassarkan domain knowledge
* Propertycount : tidak ada penjelasan tentang kolom ini pada kaggle, lebih baik di drop karena tidak digunakan juga untuk analisa
* Address : karena analysis ini bukan tentang customer profile jadi kita drop karena tidak digunakan untuk analysis ini

Handling missing Value :
* Missing value pada kolom diisi menggunakan median dari kolom tersebut
* councilArea diisi dengan 'NC' untuk menandakan bahwa row tersebut missing value
* Building Area diisi menggunakan KNN Imputer

# Summary

Dari keseluruhan analysis dapat di simpulkan bahwa hal yang sangat mempengaruhi harga rumah adalah Region nya. Hal tersebut tentu masuk akal karena region metropolitan berada di dekat CBD (central business district), fasilitas yang tersedia di dekat CBD pasti lebih baik dibanding fasilitas di daerah yang jauh dari CBD. Tipe rumah juga sangat mempengaruhi harga jual sedangkan waktu, luas tanah dan bangunan, dan jumlah ruangan jika berdasarkan hasil korelasi nya memiliki pengaruh yang sedang saja atau tidak terlalu besar.

Dapat di **rekomendasikan** untuk calon pembeli rumah di kota melbourne :

* Jika ingin membeli rumah di dekat CBD bisa membeli di Northern Metropolitan. Di region ini ketersediaan rumah, townhouse dan duplex nya cukup banyak, harganya pun lebih rendah dibanding  Western dan Southern Metropolitan. Mungkin karena rata-rata luas bangunan nya lebih kecil di banding rata-rata luas bangunan di western dan southern metropolitan.

* Jika ingin membeli rumah yang termurah, bisa membeli rumah di western victoria. anda dapat membeli rumah dengan luas tanah yang cukup besar dengan harga yang cukup terjangkau, lebih murah di bandingkan harga unit di seluruh region metropolitan. Tetapi untuk membeli rumah disini berarti anda membeli rumah yang jaraknya cukup jauh dari CBD

* Jika ingin membeli rumah yang Termahal, bisa membeli rumah di daerah Southern Metropolitan. bahkan harga 1 duplex disini setara dengan membeli 3 rumah di western victoria. harus dianalisa lebih lanjut diluar data ini mengapa rumah di southern metropolitan sangat mahal.

* Jika ingin membeli rumah yang jauh dari keramaian atu jauh dari CBD anda dapat membeli rumah di eastern victoria. dengan mengeluarkan uang yang sama besar dengan membeli rumah Townhouse di  Northern Metropolitan(terdekat ke CBD), anda bisa membeli rumah dengan luas tanah mencapai 3000
