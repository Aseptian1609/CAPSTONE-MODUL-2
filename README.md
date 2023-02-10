# Capstone-Modul-2

Adhitia Septian - Capstone Modul 2 - JCDS 1904 Purwadhika

# Exploratory Data Analysis (EDA) 
## Latar Belakang
Pada notebook berisikan pembahasan terkait EDA dengan menggunakan Pakistan's Largest E-Commerce Dataset yang dapat di *download* di link berikut: https://www.kaggle.com/datasets/zusmani/pakistans-largest-ecommerce-dataset?resource=download   
Ini adalah dataset data pesanan e-commerce ritel terbesar dari Pakistan. Ini berisi setengah juta catatan transaksi dari Maret 2016 hingga Agustus 2018. Jadi pada notebook ini akan menggali lebih dalam untuk mendapatkan keputusan yang baik untuk perusahaan dalam meningkatkan keuntungan.

## Rumusan Masalah

- Sebagai seorang Business Owner pasti memerlukan strategi gunanya untuk dapat meningkatkan pelayanan dan penjualan mereka agar dapat bertahan dan bersaing di dunia ecommerce dengan kompetitor. Strategi yang baik dapat menguntungkan perusahaan dan memperbaiki pelayanan yang tepat tentunya dapat bertujuan untuk customer churn( melakukan pembelian berulang ), 

- Analisa khususnya perilaku customer dan hal apa saja yang butuh di tingkatkan, hal ini berguna untuk meningkatkan engagement pengguna dengan aplikasi dan proses checkout barang.

### Fitur

Dataset ini berisi informasi terkait seluruh element dari sebuah transaksi. Ada 26 kolom pada Pakistan Largest Ecommerce Dataset yaitu:

1. Item_id : Kode unik dari setiap item
2. Status : Status dari sebuah transaksi
3. Created_at : Tanggal dilakukannya pemesanan barang
4. Sku : Stock Keeping Unit yang diberikan kepada setiap item barang
5. Price : Harga dari setiap item barang
6. Qty_ordered : Jumlah total item barang dalam satu transaksi
7. Grand_total : Jumlah total yang dibayar oleh customer
8. Increment_id : Kode struk
9. Category_name_1 : Pengelompokan setiap item barang dalam satu kategori
10. Sales_commision_code : Kode komisi penjualan
11. Discount_amount : Jumlah diskon yang diberikan
12. Payment_method : Metode pembayaran
13. Working_date : Jam kerja
14. BI_Status : Memberikan informasi terkait kelanjutan proses pemesanan barang
15. MV : Harga satuan produk
16. Year : Tahun customer bergabung
17. Month : Bulan customer bergabung
18. Customer_since : Berisi keterangan waktu saat konsumen bergabung
19. M-Y : Informasi tentang bulan dan tahun terjadinya transaksi
20. FY : Tahun fiskal perusahaan
21. Customer_ID : Kode unik untuk setiap konsumen
22. Unnamed : 21 : Empty Column
23. Unnamed : 22 : Empty Column
24. Unnamed : 23 : Empty Column
25. Unnamed : 24 : Empty Column
26. Unnamed : 25 : Empty Column

## CLEANING AND UNDERSTANDING DATA

Secara umum, kita bisa melihat bahwa:

- Dataset Pakistan Largest Ecommerce Dataset memiliki 26 kolom dan 1048575 baris, dan menghabiskan memory sekitar 208Mb,
- Sejumlah kolom memiliki data kosong, yaitu, status, sku, category_name_1, sales_commission_code, Customer Since, dan Customer ID,
- Kolom BI Status memiliki nilai yang tidak sesuai,
- Kolom Unnamed berisikan nilai kosong seluruhnya, sehingga melakukan penghapusan adalah keputusan terbaik,
- Kolom created_at memiliki data tipe object. Namun setelah melihat nilai pada kolom ini, seharusnya berisikan data datetime,
- Terdapat spasi pada kolom MV, sehingga dapat diperbaiki untuk penamaan kolom.
- dari analisa grafik pie chart terlihat adanya kerugian dikarenakan pemberian 'discount' yang melebihi total dari biaya 'grand_total_new' hanya sebesar 1% dari 99% penjualan.

## BUSINESS QUESTION, ANALISIS DAN REKOMENDASI

Setelah dilakukan cleaning data, kita dapat melakukan analisis untuk mencari tahu bagaimana performa penjualan pada eCommerce terbesar di Pakistan dengan menjawab beberapa pertanyaan dibawah.
### 1. Bagaimana rata-rata dari total penjualan setiap bulannya ( dari bulan Juli 2016 sampai dengan Agustus 2018)?

#### Analisis: 
Berdasarkan grafik diatas secara umum terlihat bahwa penjualan pada ecommerce di Pakistan mengalami pertumbuhan dari tahun 2016 hingga 2018. karena pada faktanya di Pakistan e-commerce ini baru booming beberapa tahun terakhir, sehingga pada tahun tersebut pertumbuhan penjualan di ecommerce belum begitu terlihat signifikan.

'faktanya ada total 344 pedagang e- niaga di negara tersebut yang terdaftar di bank pada akhir tahun 2016. Pada akhir tahun 2017, jumlah tersebut meningkat menjadi 905. Pertumbuhan ini dibarengi dengan lonjakan transaksi e- commerce dari para pedagang tersebut dari Rs3,9 miliar dalam tiga bulan terakhir tahun 2016 menjadi Rs9,1 miliar dalam tiga bulan terakhir tahun sebelumnya.'

source: "Pakistan’s booming e-commerce market is just getting started" https://www.dawn.com/news/1397446 
#### Rekomendasi :

Pertama yang paling penting untuk menarik banyak pengguna aplikasi kita wajib membuat tampilan aplikasi menjadi lebih menarik dan easy to use dalam segi User Interface dan User Experience. dikarenakan mayoritas sebesar 64% penduduk Pakistan di bawah umur 30 tahun dan sudah  lebih terbuka terhadap teknologi informasi dan komunikasi (Pakistan Goverment, 2019).

Source : Government of Pakistan Ministry of Commerce & Textile (Commerce Division). 2019. E-COMMERCE POLICY FRAMEWORK OF PAKISTAN.
### 2. Bagaimana rata rata total penjualan setiap bulannya?

#### Analisa :  
Berdasarkan grafik diatas terlihat bahwa rata-rata penjualan mengalami kenaikan pada bulan ke 2 (Februari) namun terjadi penurunan kembali hingga bulan ke-4 (April), kemudian terjadi tren naik dimana puncak penjualan tertinggi berada pada bulan ke-6 (Juni) yang mana pada saat bulan Juni bertepatan dengan bulan Puasa dimana penduduk Pakistan banyak yang berbelanja persiapan Hari Raya Idul Fitri. Setelah bulan Juni terjadi penurunan penjualan hingga bulan terakhir (bulan Desember).
#### Rekomendasi :  
untuk meningkatkan penjualan setiap bulannya kita harus banyak melakukan promosi, yaitu di:
- seasonal : Idul Fitri, Natal, Waisak, Nyepi, Dll (Agama lain yang ada di Pakistan adalah Kristen, Hindu, Buddha, Jainisme, Zoroastrianisme, dan Baha'i)
- monthly : 1.1( tanggal 1 bulan 1 tiap tahunnya),2.2,3.3 dan seterusnya
- event : Independence day, black friday, libur nasional, dll

source : wikipedia
### Mengurutkan total penjualan 

Analisis: Berdasarkan hasil analisis dan gambar grafik diatas terlihat bahwa penjualan tertinggi terjadi ketika bulan 11 (Bulan November). Hal ini terjadi karena di Pakistan pada akhir Bulan November terdapat event bernama "Black Friday", sehingga menarik banyak warga Pakistan untuk bergabung ke eCommerce dan meningkatkan penjualan perusahaan eCommerce.

Menurut perusahaan ecommerce di Pakistan menyebutkan bahwa sepertiga dari total transaksi saat Black Friday merupakan pelanggan yang aktif, hal ini memiliki arti bahwa trend Black Friday dapat mengingkatkan penjualan eCommerce di Pakistan.
Source:
https://tribune.com.pk/story/1009343/post-black-friday-in-pakistan-e-commerce-entering-a-new-era
### 3. Pada bulan berapa paling banyak pelanggan bergabung ke ecommerce?

Analisa:  
Berdasarkan hasil analisis diatas terlihat bahwa terdapat tren naik setiap bulan 11 (bulan November), artinya Bulan November merupakan bulan dimana paling banyak pelanggan baru bergabung ke eCommerce. Hal ini terjadi karena eCommerce di Pakistan mengadakan 'Black Friday' di akhir Bulan November, dengan adanya event tersebut menarik banyak warga Pakistan untuk bergabung ke eCommerce.

Menurut perusahaan ecommerce di Pakistan menyebutkan bahwa sepertiga dari total transaksi saat Black Friday merupakan pelanggan yang aktif, hal ini memiliki arti bahwa trend Black Friday dapat mengingkatkan penjualan eCommerce di Pakistan.
Source:
https://tribune.com.pk/story/1009343/post-black-friday-in-pakistan-e-commerce-entering-a-new-era
Rekomendasi :  
jangan bergantung pada hari hari besar atau momentum saja tapi ajak pelanggan baru dengan cara memberikan reward pada affiliator eCommerce yang telah berhasil mendatangkan pelanggan untuk berbelanja di eCommerce ini dengan tujuan mendatangkan affiliator-affiliator baru sehingga perusahaan dan affiliator sama-sama diuntungkan. Perusahaan mendapatkan keuntungan promosi/iklan sebagai salah satu strategi pemasaran gratis sehingga meminimalkan cost untuk promosi. Affiliator baru jika berhasil mengiklankan dan memikat konsumen hingga berbelanja di eCommerce ini akan mendapatkan komisi.

### 4. Kategori apa yang menghasilkan penjualan paling banyak?

Analisa:  
Berdasarkan hasil analisis dan visualisasi diatas terlihat bahwa:  

Kategori yang menghasilkan penghasilan tertinggi adalah kategori barang Mobiles & Tablet sekitar 2.1 milyar Ruppee,  
kategori yang menghasilkan penghasilan tertinggi kedua adalah kategori Appliances sekitar 560 juta Ruppee,  
dan kategori yang menghasilkan penghasilan terendah adalah kategori Books, menghasilkan penghasilan hanya sekitar 1 juta rupee.
Alasan mengapa penjualan di ecommerce di Pakistan paling tinggi adalah barang dengan kategori Mobiles & tablets adalah karena pada faktanya penduduk Pakistan membeli barang tersebut secara online karena harga barang tersebut lebih murah dibandingkan dengan membeli langsung ke toko grosir, seperti contohnyadi Saddar (Kota di Pakistan).
source:
Khan, S. Khan., Ahmed, Faisal., Yousuf, Hassan., Hassan, Sohaib ul., & Zia, Syed Abbas. (2014). Online Shoping Behavior in Pakistan. International Conference on Marketing.
Rekomendasi :

bisa dilihat pembelian buku dan School & education merupakan kategori barang dengan jumlah pembelian terendah, sangat jauh lebih rendah dibandingkan dengan yang lainnya. Hal ini sesuai dengan informasi bahwa sepertiga orang Pakistan tidak dapat menulis dan membaca paragraf dalam bahasa apapun. Hal ini juga dapat menjadi potensi bagi pemerintah dan penyedia Ecommerce untuk menjadikan Ecommerce sebagai sumber kampanye untuk meningkatkan minat baca masyarakat Pakistan.jadi menurut saya lakukan cross selling antara produk yang penjualannya besar dengan produk yang penjualannya kecil seperti produk dari category Mobile and Tablets dengan category Books atau Schoool Education. 

### 5. Barang yang paling banyak terjual berasal dari kategori apa?

#### Analisa:  
Berdasarkan gambar grafik di atas terlihat bahwa:  

Kategori yang barangnya paling banyak terjual adalah kategori Mobiles & Tablets, yaitu sebanyak 134.469 barang terjual,  
Kategori yang barangnya paling banyak terjual kedua adalah kategori Men's Fashion, yaitu sebanyak 103.406 barang,  
Kategori yang barangnya paling banyak terjual ketiga berasal dari kategori Others, yaitu sebanyak 86.129 barang, dan  
Kategori yang barangnya paling sedikit terjual berasal dari kategori Books, yaitu sebanyak 2.664 barang.  
Alasan mengapa di ecommerce di Pakistan barang yang paling banyak terjual adalah barang dengan kategori Mobiles & tablets karena pada jurnal yang berjudul "Online Shopping Behavior in Pakistan" menjelaskan bahwa terdapat penduduk Pakistan membeli barang handphone dalam 1 tahun hingga 5 kali, hal ini memberikan arti bahwa penduduk Pakistan memang sering membeli HP, sehingga tidak heran jika kategori Mobiles & Tablets menjadi kategori barang yang paling banyak terjual di eCommerce. selain itu, penduduk Pakistan juga memilih berbelanja di eCommerce karena harga barang di eCommerce lebih murah dibandingkan dengan membeli langsung ke toko grosir, seperti contohnya di Saddar (Kota di Pakistan).
source:
Khan, S. Khan., Ahmed, Faisal., Yousuf, Hassan., Hassan, Sohaib ul., & Zia, Syed Abbas. (2014). Online Shoping Behavior in Pakistan. International Conference on Marketing.
#### Rekomendasi :
untuk memperbanyak penjualan per item di ecommerce juga bisa dengan beberapa cara salah satunya dengan cara upselling, misalnya pembelian 10 Books mendapatkan 1 books. atau pembelian baju di category Mens atau Women Fashion  jumlah yang banyak dapat potongan harga sekian persen. 

### 6. Berapa banyak pelanggan yang menggunakan kode komisi ("Sales commission code")?

#### Analisa:  
Berdasarkan gambar grafik diatas terlihat bahwa yang berbelanja memakai kode komisi hanya 108.348 atau sebesar 18,5%, sedangkan 81.5% atau sebesar 476.165 nya adalah pelanggan yang berbelanja tidak memakai kode komisi yaitu setara dengan 469.743 pelanggan. bisa di analisa bahwa penjualan dengan commission masih sangat sedikit padahal pada saat ini kita lihat banyak perusahaan ecommerce menggunakan commission untuk meningkatkan penjualan mereka.
#### Rekomendasi :

selain menggunakan affiliate yang sudah saya jelaskan sebelumnya diatas, ada juga cara lain untuk memboost penjualan dari segi commission yaitu dengan sistem ' Referral' yaitu user bisa mendapatkan point/rewards yang nantinya akan berguna untuk pembelian barang di ecommerce tersebut. 

Dengan referral, artinya akan ada banyak orang yang ikut membeli produk tersebut. Apalagi konsumen cenderung mempercayai rekomendasi dari orang yang mereka kenal.
menurut riset Annex Cloud, referral marketing dapat menghasilkan 3 hingga 5 kali lipat conversion rate, dan berpeluang meningkatkan customer retention 37% lebih tinggi dibandingkan channel marketing lain. Itulah kenapa marketing ini penting untuk digunakan sebagai upaya meningkatkan penjualan. 


### 7. Metode Pembayaran yang paling banyak dipakai?

#### Analisa:  
Berdasarkan hasil analisis yang dibantu oleh gambar grafik diatas didapatkan hasil bahwa pelanggan ecommerce di Pakistan kebanyakan menyukai metode pembayaran COD, hal ini didukung oleh fakta bahwa metode pembayaran COD menjadi peran penting untuk mengurangi resiko saat berbelanja online karena dengan metode tersebut pelanggan ingin mencobanya sebelum membayar.

Menurut laporan, 95 persen perusahaan elektronik menerima pembayaran untuk pesanan online mereka melalui cash- on- delivery. Hal ini meningkatkan persyaratan likuiditas untuk perusahaan e- niaga dan juga memaksa mereka untuk memiliki tim khusus yang mengelola penerimaan kas untuk perusahaan, sehingga meningkatkan biaya operasional. Pemain yang lebih besar di ruang e- commerce telah mulai memanfaatkan pembayaran digital, dan optimis bahwa industri ini akan bersatu untuk membujuk konsumen agar beralih dari pembayaran tunai di tempat ke pembayaran online. Pembayaran digital juga merupakan rintangan bagi sektor e- commerce Pakistan. Sementara beberapa produk seperti EasyPaisa, JazzCash, dan uPaisa — yang merupakan mobile bank — tersedia saat ini, tidak ada satupun yang memiliki penetrasi pasar yang tinggi. Ini, ditambah dengan fakta bahwa hanya 24 persen penduduk negara itu yang memiliki rekening bank secara signifikan
source:

Khan, S. Khan., Ahmed, Faisal., Yousuf, Hassan., Hassan, Sohaib ul., & Zia, Syed Abbas. (2014). Online Shoping Behavior in Pakistan. International Conference on Marketing.  
Imtiaz, Shoaib., Ali, Syed Hassan., & Kim, Don Jin. E-Commerce Growth in Pakistan: Privacy, Security, and Trust as Potential Issues. Culinary Science & Hospitality Research 26(2):10-18.  
https://www.trade.gov/country-commercial-guides/pakistan-ecommerce
#### Rekomendasi :

Bisa dilihat dari analisa diatas bahwa metode pembayaran banyak menggunakan COD, jadi rentan untuk pelanggan return order atau mengembalikan barang( kalau tidak sesuai dengan pelanggan ) bisa di katakan perusahaan akan memberikan banyak biaya untuk pengiriman dan juga rentan untuk loss dalam penyimpanan uang pemabayran karna pembayaran yang di terima adalah uang kas. jadi kita merekomendasikan untuk merubah metode pembayaran atau meminimalisasi pembayaran yang sebelumnya menggunakan COD menjadi pembayaran via online.    

salah satu metode via online bisa menggunakan payment gateway. Payment gateway merupakan sebuah sistem yang dapat mengotorisasi pembayaran yang dilakukan pelanggan di commerce. Sistem ini memungkinkan untuk dapat menerima pembayaran dari berbagai bank dan metode pembayaran, mulai dari kartu kredit/debit, transfer bank, virtual account, gerai ritel, e-wallet, hingga pay later.  
Bukan hanya itu, ada banyak manfaat lain yang dapat Anda peroleh jika menggunakan payment gateway untuk ecommerce.   
Berikut adalah 4 di antaranya:
- Tidak Perlu Memiliki Banyak Rekening Bank
- Meningkatkan Konversi
- Serba Otomatis
- Lebih Cepat dan Aman

### 8. Kategori mana yang menghasilkan Penghasilan terbesar diantara Transaksi yang memiliki diskon

#### Analisa:   
Berdasarkan gambar grafik diatas terlihat bahwa 
- kategori Entertainment kalau dilihat sub category merupakan produk elektronik seperti TV, audio, Monitor, dll. menghasilkan penjualan terbesar sebesar 513.975 Ruppee, meskipun diskon atau potongan harga yang diberikan kecil sebesar total 2000 ruppee, 
- ternyata Mobile & tablets penjualan di urutan 2 sebesar 471.000 Ruppee, dengan total diskon sebesar 1000 Ruppee. 

- untuk pemberian potongan diskon terbesar pertama adalah kategori Mens Fashion menempati urutan ke-9 penjualan terbesar padahal potongan harga yang diberikan sangat besar, sebesar 45.000 Rupee hampir seluruh category mens fashion menggunakan potongan diskon. 
- dan pemberian diskon terbesar kedua yaitu category womens fashion dengan potongan discount sebesar 12.487 Ruppee.
- kenapa category fashion selalu menjadi pilihan untuk pemberian potongan discount di ecommerce karna Tekstil/Pakaian merupakan 57% dari ekspor Pakistan, dan di kancah lokal, pakaian jadi menghasilkan antara 32-35% dalam penjualan industri. jadi pakaian bisa dijual dengan harga murah atau dengan potongan discount yang besar.


#### Rekomendasi :

untuk discount pada category Mens Fashion dan Female Fashion dapat di minimalisir karena pendapatan penjualan tidak signifikan, bahkan pada category Mens Fashion tidak ada revenue. lebih baik discount di berikan ke category yang penjualannya lebih besar agar bisa lebih meningkatkan penjualan dan pastinya boost revenue juga. dampak pemberian discount pada category lain juga tidak terlalu signifikan, bukti dari analisa diatas adalah pada penjualann entertainment dan mobile & tablets meskipun pemberian discount kecil tetapi penjualan pada kategori tersebut cukup besar. 
untuk strategi pemberian discount yang bisa kita rekomendasikan adalah pemberian diskon pada saat event event besar sperti black friday atau hari besar keagamaan. 
selain itu kita bisa memberikan discount berupa cashback agar pelanggan bisa membeli barang tersebut kembali (churning)
source : https://seller.alibaba.com/businessblogs/px001tae0-10-best-selling-online-products-in-pakistan
### 9. Kategori mana yang menghasilkan melakukan penjualan menggunakan sales commision code
#### Analisa:   
Berdasarkan gambar grafik diatas terlihat bahwa 
- Kategori Entertainment paling banyak penjualan menggunakan sales commission code sebesar 24.484 Ruppee, dikarenakan commission yang besar dalam penjualan di category Entertainment
- disusul Mobile & Tablets di peringkat kedua sebesar 19.705 Ruppee, dan
- Computing di peringkat ketiga terbesar sebesar 16.746 Ruppee
dan Category dengan penjualan dengan komisi terendah adalah
- category Superstore adalah category yang paling sedikit menggunakan komisi yaitu sebesar 466 Ruppee
- disusul category sooghat yaitu 581 Ruppee

#### Rekomendasi :

agar persebaran komisi pada category lainnya juga meningkat kita bisa lakukan affiliate dengan penjualan per category, dengan kata lain setiap category memiliki affiliate masing- masing agar semua penjualan memiliki commission sales yang pada akhirnya menguntungkan kedua belah pihak antara para affiliate dan tentunya perusahaan. kita tau pada negara pakistan category books dan education sangatlah minim, kita juga bisa boost untuk penjualan yang berkaitan dengan education agar level education pakistan juga bisa ditingkatkan dengan cara memberi edukasi lewat influencer dari bidang pendidikan/kerja sama dengan pihak pemerintah pendidikan. 
#### 10. produk apa yang terjual paling banyak ?

#### Analisis : 

Berdasarkan grafik penjualan barang terbanyak nomor 1 dari kategori Mobile & Tablets yaitu MATSAM569DB75ADB2F80 dari analisa saya itu barang elekronik berupa handphone samsung, terjual sebanyak 3775 pcs. diikuti produk dari kategori Sooghat yaitu Al Muhafiz Sohan Halwa Almond, yaitu sejenis kue dengan toping almond terjual sebanyak 2258 pcs.
faktanya memang pada tahun 2016-2018 penjualan mobile  atau smartphone di dunia sedang meningkat drastis.

source : https://www.statista.com/statistics/263437/global-smartphone-sales-to-end-users-since-2007/
#### Rekomendasi :  
strategi khususnya untuk penjualan di kategori mobile and tablet yaitu selalu mengerti apa permintaan pasar, jual produk yang sedang diminati saja, minimalisir produk yang kurang di minati pasar. karena fakta nya rata rata pengguna smartphone selalu mengganti smartphone mereka dalam waktu kurang dari 3 tahun.

source : https://www.gsmarena.com/weekly_poll_how_long_will_you_keep_your_phone-news-44070.php

