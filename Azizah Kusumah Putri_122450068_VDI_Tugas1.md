#### Nama  : Azizah Kusumah Putri
#### NIM   : 122450068
#### Kelas : RB

#  

## Judul : Making Data Visualization More Efficient and Effective: a Survey

## Penulis : Xuedi Qin, Yuyu Luo, Nan Tang, Guoliang Li

## Tahun : 2019

#  

### 1. Pendahuluan

        Visualisasi data adalah mengubah data yang awalnya abstrak menjadi bentuk visual seperti panjang, posisi, dan warna, sehingga lebih mudah dipahami oleh manusia. Visualisasi data dapat membantu memberikan gambaran yang lebih jelas tentang data yang berukuran besar, serta mempermudah manusia dalam menginterpretasikan hasil analisis data dan pengambilan keputusan. 
        
        Visualisasi data telah berkembang signifikan pada beberapa bidang, serta didorong dengan kontribusi dari banyak komunitas. Kontribusi dari berbagai komunitas telah mengembangkan alat seperti D3, Vega-lite, VizQL, Tableau, dan Microsoft Power BI serta meningkatkan pengalaman visualisasi data secara real-time seperti Hyper DB dan Falcon. Visualisasi data juga banyak digunakan pada aplikasi seperti Excel, Google Sheets, dan Oracle Data Visualization Dekstop. 

    Langkah-langkah dalam melakukan visualisasi data :
        1. Import data, mengambil data dari sumber data
        2. Data preparation, menyiapkan data dengan menormalisasikan data, memperbaiki kesalahan, dan mengisi data yang kosong
        3. Data manipulation, memilih dan menyaring data
        4. Mapping, konversi data menjadi suatu bentuk dan memberikan warna, posisi, dan ukuran
        5. Rendering, mengubah data menjadi representasi visual

    Berdasarkan langkah-langkah tersebut, visualisasi data memiliki 3 arah utama untuk meningkatkan visualisasi data :
        1. Spesifikasi visualisasi, menyediakan berbagai cara untuk menentukan visualisasi yang dibutuhkan, dengan fokus pada tahan pemetaan namun juga beririsan dengan manipulasi data
        2. Pendekatan efisien, memastikan prosesnya dapat diskalakan dan efisien, terutama pada proses manipulasi data dan pemetaan
        3. Rekomendasi visualisasi data, memberikan rekomendasi untuk membantu dalam menentukan visualisasi

#  

### 2. Spesifikasi Visualisasi

#### 2.1 Spesifikasi visualisasi data

    Secara umum, bahasa visualisasi data terdiri dari 3 komponen :
        1. Data ; meliputi baris data yang akan divisualisasikan dan transformasi data
        2. Marks (petunjuk visual) ; mengacu pada jenis representasi visual seperti garis, titik, batang, ukuran, warna, lebar, dan tinggi
        3. Pemetaan ; menentukan bagaimana data dipetakan ke dalam visual

#### 2.2 Kategorisasi bahasa visualisasi data

        Bahasa visualisasi data biasanya dikategorikan berdasarkan ekspresivitas dan kemudahan penggunaannya. Bahasa tingkat rendah biasanya lebih ekspresif tetapi memerlukan semua detail pemetaan, sementara bahasa tingkat tinggi lebih mudah digunakan dan menawarkan default dan batasan untuk menyederhanakan proses. 
        
        Bahasa tingkat rendah memerlukan input yang lebih detail untuk elemen pemetaan, contohnya; 1. Prefuse dan Flare ; Library visualisasi berbasis Java yang membutuhkan input prosedural, 2. Protivis ; toolkit grafis dengan berbasis JavaScript deklaratif, 3. D3 ; pengembangan dari protivis yang lebih baik dalam fitur interaksi, 4. Vega dan Reactive Vega ; memiliki tata bahasa interaksi deklaratif yang mirip dengan pritivis dan D3.
        
        Bahasa tingkat tinggi mengemas detail visualisasi seperti fungsi mapping, dan properti lainnya seperti ukuran, legend, dan warna. Contoh bahasa visualisasi tingkta tinggi seperti; 1. ggplot2 ; berdasarkan "Grammar of Graphics" dalam R, 2. Vega-lite ; pengembangan lebih tinggi dari Vega dan memiliki tata bahasa yang ringkas, 3. Altair ; membuat Vega-lite dapat diakses dalam Python, 4. Echarts ; dirancang untuk non-programmer dalam membuat visualisasi cepat, 5. VizQL ; digunakan oleh Tableau dan berkembang dari sistem Polaris, 6. ZQL ; digunakan oleh Zenvisage dan memiliki struktur tabular untuk spesifikasi.

#### 2.3 Operasi visual berbasis GUI

        Spesifikasi visualisasi data berbasi GUI(Graphical User Interface) lebih ramah bagi pengguna dibandingkan dengan bahasa visualisasi deklaratif. GUI memungkinkan penggunan untuk melakukan maipulasi langsung pada visualisasi dan sangat membantu dalam interaksi manusia dan komputer. Beberapa tools berbasis GUI untuk operasi visual seperti Tableau, Qlik, Excel, Google Sheets, dan lainnya.
        
        Visualisasi data interaktif sering kali melibatkan proses eksplorasi di mana pengguna menyempurnakan spesifikasi visualisasi. Terdapat dua kategori yaitu penyempurnaan query bertahap dan navigasi beraspek. Tools pada penyempurnan query bertahap yaitu Polaris dan Tableau yang memungkinkan visualisasi multidimensi menggunakan struktur tabel yang memudahkan perbandingan berbagai atribut. Tools pada navigasi beraspek seperti DeepEye dan Voyager dapat mendukung eksplorasi visualisasi dengan rekomendasi berdasarkan berbagai aspek, seperti tipe diagram, sumbu X/Y, kategori, dan lainnya.

#### 2.4 Spesifikasi yang tidak lengkap

        Visualisasi data menjadi tidak ada artinya jika tidak bisa memberikan insight dari suatu data. Dalam beberapa kasus, pengguna mungkin tidak sepenuhnya memahami semua aspek data yang ukurannya sangat besar atau seringnya pembaruan data. Pengguna biasanya memberikan input minimal atau 'petunjuk", dan sistem menginterpretasikan serta menyarankan visualisasi yang relevan. Petunjuk tersebut memiliki berbagai jenis, daintaranya; berbasis referensi, berbasis kata kunci, dan berbasis bahasa alami.

#  

### 3. Pendekatan Efisien untuk Visualisasi Data

#### 3.1 Visualisasi data yang tepat

        Pendekatan efisien dalam visualisasi data meliputi beberapa strategi. Pertama, visualisasi data yang tepat menghitung visualisasi secara akurat dan cepat. Kedua, visualisasi data yang tepat memberikan hasil visualisasi yang lebih cepat meski hanya mendekati akurat ketika data sangat besar atau kompleks. Ketiga, visualisasi data yang rpogresif memperhalus visualisasi secara bertahap seiring waktu. Selain itu, integrasi dengan berbasis data mmenjadi penting. Penerjemahan query dilakukan oleh sistem seperti DeepEye dan Polaris yang mengubah query visualisasi menjadi SQL untuk pengambilan data. Penggabungan pengambilan data dan penyajian dialkukan oleh sistem seperti Ermac yang mengintegrasikan penanganan data dan visualisasi untuk meningkaykan efisiensi dan mengurangi latensi. Penggunaan penyimpanan kolom dan indeks meningkatkan kinerja dengan mengoptimalkan pengambilan dan penyaringan data. Perhitungan paralel memanfaatkan beberapa utas untuk melakukan visualisasi secara secara bersamaan, sementara prediksi dan prefetching mempercepat eksplorasi dengan memprediksi dan memuat data berdasarkan interaksi pengguna atau data historis.

#### 3.2 Pendekatan visualisasi data

        Seiring dengan pertumbuhan volume data yang eksponensial, metode pemrosesan tradisional kesulitan untuk memberikan hasil interaktif dengan cepat. Untuk mengatasi hal ini, teknik pemrosesan query mendekati AQP digunakan untuk menyediakan visualisasi dengan cepat. Terdapat 3 pendekatan utama dalam visualisasi data. Pertama, pendekatan berbasis AQP, menggunakan teknik AQP untuk memberikan visualisasi yang cepat namun dengan bekerja pada subset data yang representatif. Sistem seperti Sample+Seek memanfaatkan AQP untuk menawarkan visalisasi interaktif dengan batas kesalahan, sementara Pangloss menyediakan hasil yang menddekati dan tepat, memungkinkan pengguna memverifikasi wawasan dengan data akurat. Kedua, pendekatan berbasis sampling inkremental, menghasilkan visualisasi mendekati awal dengan sampel kecil dan secara bertahap meningkatkan akurasi dari waktu ke waktu dengan memperbesar ukuran sampel. Alat seperti SampleAction dan IncVisAge menggunakan sampling incremental untuk memperbaiki visualisasi, di mana IncVisAge menawarkan pembaruan yang lebih stabil melalui algoritma ISplit dibandingkan dengan fluktasi hasil SampleAction. Ketiga, pendekatan berbasis persepsi manusia, mempertimbangkan bata kognitif persepsi manusia. Metode seperti IFocus dan PFunk-H menghentikan sampling ketika data tambahan tidak lagi signifikan dalam meningkatkan kualitas visualisasi data yang disarankan, fokus pada akurasi persepsi dan meminimalkan dampak pada kualitas visual.

#### 3.3 Visualisasi data progresif

        Selain metode sampling inkremental, terdapat banyak cara yang menyedaikan visualisasi progresif melalui agregasi hierarkis. Pendekatan ini umumnya membangun struktur hierarkis dengan mengagregasi data pada berbagai tingkat, seperti ukuran yang berbeda, rentang nilai, atau zona nilai spasial. Range-Based Binning seperti pada imMens menyediakan visualisasi dengan resolusi berbeda dengan mengubah ukuran bin. Data multidimensi di imMens dibagi menjadi kubus data yang kemudian dipartisi menjadi ubin pada berbagai tingkat. Namun metode ini memiliki keterbatasan, seperti ketidakmampuan untuk mengubah ukuran bin atau jumlah resolusi yang berbeda. Range and Contect-Based Binning dalam penelitian lain menyediakan dua struktur pohon untuk eksplorasi hierarkis. HETree-R((berbasis rentang) mirip dengan imMens, sedangkan HETree-C(berbasis konten) memiliki jumlah titik data yang sama di semua simpul daunnya. Kedua struktur pohon ini memungkinkan eksplorasi data abstraksi atau lebih detail dengan operasi roll-up atau drill-down.
    

#  

###  4. Rekomendasi Visualisasi

        Proses visualisasi bersifat iteratif dan sering kali memerlukan praktisi untuk melakukan modifikasi yang sering. Untuk mempermudah proses ini, sistem rekomendasi visualisasi bertujuan untuk menyarankan visualisasi yang efektif. Pendekatan rekomendasi berdasarkan spesifikasi melibatkan pemberian rekomendasi berdasarkan spesifikasi elemen visualisasi yang lengkap atau sebagian. Rekomendasi berdasarkan perilaku didasarkan pada perilaku dan interaksi pengguna. Rekomendasi yang dipersonalisasi menyesuaikan dengan preferensi dan kebutuhan individu pengguna. 

        Untuk mengatasi tantangan ini, sistem rekomendasi visualisai perlu mengeksplorsi sejumlah besar kemungkinan visualisasi dengan mempertimbangkan berbagai faktor seperti kolom data, transformasi, dan pengkodean visual. Pemangkasan visualisasi yang tidak berguna sangat penting untuk mengelola ruang pencarian yang luas. Setelah pemangkasan, sistem rekomendasi mengevaluasi dan memberi peringkat pada visualisasi yang bermakna berdasarkan metrik atau aturan yang telah ditentukan, dan akhirnya menyarankan visualisasi terbaik kepada pengguna.

#  

### 5. Kesimpulan

        Visualisasi data adalah bidang yang berkembang pesat dengan banyak kemajuan penelitian terbaru dan sistem baru. Dengan meninjau perkembangan terkini dari perspektif manajemen data, dengan fokus pada spesifikasi visualisasi, metode visualisasi yang efisien, dan rekomendasi visualisasi. Meskipun sistem komersial unggul dalam kemudahan penggunaan, masalah dengan efisiensi dan rekomendasi masih ada. Dan menyoroti masalah terbuka dimana peneliti dapat memberikan kontribusi untuk memajukan bidang visualisasi data.
