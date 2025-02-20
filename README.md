# ** 📝 Research Campaign - by The Golden Gate **

**✅ Members of The Golden gate ✅**

1. M Ridzky Maulady
2. Josua Ricardo Samosir
3. Habib Septrian Priyanto
4. Daniel Andrew Siahaan

## **💻 Languages and Technologies used 💻**

- Python 3.12
- Google Colab or Visual Studio Code
- [Requirements Text]

## **📍 Table of Content 📍**
<!--ts-->
* **Business Understanding**
    * [Problem Statement](#-business-understanding-)
    * [Roles](#-roles)
    * [Goals](#-goals)
    * [Objectives](#-objectives)
    * [Business Metrics](#-business-metrics)
* **Data Preparation**
    * [Data Description](#-data-description-)
* **Data Understanding**
    * [Exploring Datasets](#-data-understanding-)
    * [Data Types Information](#-data-types-information)
    * [Statistical Summary](#-statistical-summary)
    * [EDA (Exploratory Data Analysis)](#-exploratory-data-analysis-eda)
    * [Feature Engineering / Extraction (Business Insight)](#-feature-engineering--extraction)
    * [Business Insight](#-business-insight)
* **Data Cleansing/Preprocessing**
    * [Handling Missing Values](#-handling-missing-value)
    * [Handling Duplicated Rows](#-handling-duplicate-rows)
    * [Handling Invalid Values](#-handling-invalid-values)
    * [Handling Outliers](#-handling-outliers)
    * [Feature Engineering / Extraction](#-feature-engineering--extraction-1)
    * [Feature Transformation (Numeric)](#-feature-transformation-numeric)
    * [Feature Encoding (Categoric)](#-feature-encoding-categoric)
    * [Feature Selection](#-feature-selection)
    * [Data Splitting](#-data-splitting)
    * [Handling Imbalanced Data](#-handling-imbalanced-data)
<!--te-->

## **💼 Business Understanding 💼**

### **📌 Problem Statement**

**AirBnb** adalah sebuah platform yang menyediakan pemilik properti (host) untuk menyewakan property kepada tamu/penyewa. Jenis property pada dataset listing berupa Apartment, House, Cabin, Condominium, Camper/RV, Bungalow, Townhouse, Loft, Boat, Bed & Breakfast, Dorm, Treehouse, Yurt, Chalet, Tent dan Other. Marketing Team ingin melakukan campaign penyesuaian harga kepada pemilik property, di musim apa yang dapat dilakukan campaign untuk mengundang tamu ke Seattle. Berdasarkan dataset AirBnb menghadapi beberapa permasalahan seperti berikut:

- **Superhost** hanya dimiliki 17% dari total listing dan memiliki harga yang fluktuatif. 
- **Booking Instant** hanya dimiliki 16% dari total listing. 

Berdasarkan hal tersebut, Marketing Team meminta Researcher Team untuk menganalisis permasalahan yang terjadi. Selanjutnya AirBnb ingin membuat campaign yang dilakukan Marketing Team tepat sasaran sesuai **pemilik property**. Strategi ini diharapkan mampu meningkatkan kepemilikan label **Superhost** ada penyesuaian dalam penentuan harga terhadap kualitas property dan **Booking Instant** agar mempermudah penyewa dalam melakukan booking.


### **📌 Roles**

Kami adalah **Researcher Team** untuk Airbnb dengan nama **The Golden Gate**. Tim ini mempunyai tugas sebagai konsultan strategis dengan pemahaman mendalam tentang analisis data. Kami bertujuan untuk memberikan wawasan kepada host agar mereka dapat meningkatkan performa properti dan pengalaman pelanggan, berdasarkan data yang akurat dan relevan. Berikut adalah PIC pada tim The Golden Gates:


- **Project Manager**

    Mengelola timeline proyek, dokumentasi, komunikasi tim, serta memastikan kualitas dan konsistensi hasil.

    PIC: `M Ridzky Maulady`

- **Data Analyst**

    Menerjemahkan data menjadi rekomendasi bisnis yang selaras dengan tren dan kebutuhan stakeholders.

    PIC: `Josua Ricardo Samosir`

- **Data Scientist**

    Mengembangkan model machine learning, evaluasi kinerja, dan mengoptimalkan akurasi untuk meningkatkan performa fitur.
    
    PIC: `Habib Septrian Priyanto`
    
- **Data Engineer**

    Melakukan Data Preparation, Cleaning, dan Exploratory Data Analysis (EDA)

    PIC: `Daniel Andrew Siahaan`


### **📌 Goals**

Perusahaan ingin meningkatkan **response rate** dan  meminimalisasi **marketing campaign cost** sehingga dapat memaksimalkan **profit**. 


### **📌 Objectives**

Membuat classification model untuk **memprediksi kelompok customer yang akan merespon campaign** agar dapat **meminimalisasi biaya pemasaran dan memaksimalkan keuntungan** pada campaign marketing berikutnya.


### **📌 Business Metrics**

- **Superhost Adoption Rate**
    
    Persentase efektivitas rekomendasi yang dihasilkan model untuk meningkatkan jumlah Superhost.
    
    _**Indicator :**_ 17% is bad. [Currently Rate] {Source: review_scores_rating, c_data (frekuensi menginap), host_response_time, price dan cancellation_policy}
    
    - **Occupancy Rate**
    
        Mengukur persentase tingkat hunian properti setelah penerapan model harga dinamis untuk menilai dampak dari tindakan yang diambil.

        _**Indicator :**_ 5% is low, 10-19% is average, 20% is good. (Total Nights Available/Nights Booked)*100 ​[Sample]
    
    - **Optimal Pricing**
    
        Menentukan harga ideal yang kompetitif berdasarkan ulasan dan tingkat pemesanan.

        _**Indicator :**_  (Total Revenue/Number of Bookings)

- **Cancellation Rate**
    
    Persentase pembatalan terhadap total pemesanan dalam listing yang menggunakan Booking Instant.

_**Indicator :**_  (Total Bookings/Number of Cancellations)*100
    
        
**📖 References : 📖**

- 


## **📂 Data Description 📂**

**Seattle Airbnb Open Data ([link datasets](https://www.kaggle.com/datasets/airbnb/seattle/data))**

Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA. 

The following Airbnb activity is included in this Seattle dataset:

    Listings, including full descriptions and average review score
    Reviews, including unique id for each reviewer and detailed comments
    Calendar, including listing id and the price and availability for that day

**Dataset Description:**

The training dataset contains `1.482.237 samples`. Contains `102 columns`

**Dataset Listings (1/3)**
Dataset listings berisi 3.818 sampel. Dataset ini mengandung 92 fitur.

### ID dan Informasi Listing
- `id` - Identifikasi unik untuk setiap listing.  
- `listing_url` - URL dari listing di Airbnb.  
- `scrape_id` - Identifikasi untuk proses pengambilan data (scraping).  
- `last_scraped` - Tanggal saat data terakhir kali diambil dari Airbnb.  
- `name` - Nama properti yang ditampilkan di platform.  
- `summary` - Deskripsi singkat mengenai listing.  
- `space` - Deskripsi tentang ruang akomodasi.  
- `description` - Deskripsi mendetail mengenai listing.  

### Informasi Host
- `host_id` - Identifikasi unik untuk host yang memiliki listing.  
- `host_url` - URL profil dari host di Airbnb.  
- `host_name` - Nama host yang memiliki properti.  
- `host_since` - Tanggal ketika host pertama kali mulai menyewakan propertinya di Airbnb.  
- `host_location` - Lokasi host.  
- `host_about` - Deskripsi tentang host.  
- `host_response_time` - Waktu rata-rata host dalam merespons permintaan dari tamu.  
- `host_response_rate` - Persentase dari permintaan yang dijawab oleh host.  
- `host_acceptance_rate` - Persentase permintaan yang diterima oleh host.  
- `host_is_superhost` - `1` jika host adalah superhost, `0` jika tidak.  
- `host_thumbnail_url` - URL untuk gambar thumbnail host.  
- `host_picture_url` - URL untuk gambar profil host.  
- `host_neighbourhood` - Nama lingkungan dari host.  
- `host_listings_count` - Jumlah listing yang dimiliki oleh host.  
- `host_total_listings_count` - Total jumlah listing yang dimiliki oleh host.  

### Lokasi dan Jenis Properti
- `street` - Alamat jalan dari listing.  
- `neighbourhood` - Nama lingkungan dari listing.  
- `neighbourhood_cleansed` - Nama lingkungan yang telah dibersihkan untuk konsistensi.  
- `neighbourhood_group_cleansed` - Nama kelompok lingkungan yang telah dibersihkan.  
- `city` - Kota tempat listing berada.  
- `state` - Negara bagian tempat listing berada.  
- `zipcode` - Kode pos untuk lokasi listing.  
- `market` - Pasar yang terkait dengan listing.  
- `smart_location` - Lokasi yang cerdas, berdasarkan data geo.  
- `country_code` - Kode negara tempat listing berada.  
- `country` - Nama negara tempat listing berada.  
- `latitude` - Koordinat lintang lokasi listing.  
- `longitude` - Koordinat bujur lokasi listing.  
- `is_location_exact` - Indikator apakah lokasi listing tepat (`t`) atau tidak (`f`).  
- `property_type` - Jenis properti (misalnya, `Apartment`, `House`).  
- `room_type` - Tipe kamar (`Entire home/apt`, `Private Room`, `Shared Room`).  

### Kapasitas dan Fasilitas
- `accommodates` - Jumlah tamu maksimum yang dapat ditampung.  
- `bathrooms` - Jumlah kamar mandi yang tersedia.  
- `bedrooms` - Jumlah kamar tidur yang tersedia.  
- `beds` - Jumlah total tempat tidur di listing.  
- `bed_type` - Tipe tempat tidur (misalnya, `Real Bed`, `Futon`).  
- `amenities` - Fasilitas yang disediakan (misalnya, `TV`, `Wi-Fi`).  
- `square_feet` - Luas properti dalam kaki persegi (jika ada).  

### Harga dan Ketersediaan
- `price` - Harga sewa per malam (dalam dolar).  
- `weekly_price` - Harga sewa per minggu (dalam dolar).  
- `monthly_price` - Harga sewa per bulan (dalam dolar).  
- `security_deposit` - Deposit keamanan yang diperlukan (jika ada).  
- `cleaning_fee` - Biaya pembersihan yang dibebankan (jika ada).  
- `guests_included` - Jumlah tamu yang termasuk dalam harga sewa.  
- `extra_people` - Biaya tambahan per tamu tambahan.  
- `minimum_nights` - Jumlah minimum malam untuk pemesanan.  
- `maximum_nights` - Jumlah maksimum malam untuk pemesanan.  
- `calendar_updated` - Tanggal terakhir update kalender.  
- `has_availability` - Indikator apakah listing memiliki ketersediaan (`t`) atau tidak (`f`).  
- `availability_30` - Jumlah hari dalam 30 hari berikutnya ketika listing tersedia.  
- `availability_60` - Jumlah hari dalam 60 hari berikutnya ketika listing tersedia.  
- `availability_90` - Jumlah hari dalam 90 hari berikutnya ketika listing tersedia.  
- `availability_365` - Jumlah hari dalam setahun ketika listing tersedia.  

### Ulasan dan Rating
- `number_of_reviews` - Jumlah total ulasan yang diperoleh listing.  
- `first_review` - Tanggal ulasan pertama yang diterima.  
- `last_review` - Tanggal ulasan terakhir yang diterima.  
- `review_scores_rating` - Skor rating dari ulasan.  
- `review_scores_accuracy` - Skor akurasi dari ulasan.  
- `review_scores_cleanliness` - Skor kebersihan dari ulasan.  
- `review_scores_checkin` - Skor check-in dari ulasan.  
- `review_scores_communication` - Skor komunikasi dari ulasan.  
- `review_scores_location` - Skor lokasi dari ulasan.  
- `review_scores_value` - Skor nilai dari ulasan.  

### Kebijakan dan Verifikasi
- `requires_license` - Indikator apakah listing memerlukan lisensi (`t`) atau tidak (`f`).  
- `license` - Nomor lisensi yang diperlukan (jika ada).  
- `jurisdiction_names` - Nama yurisdiksi di mana listing berada.  
- `instant_bookable` - Indikator apakah listing dapat dipesan secara instan (`t`) atau tidak (`f`).  
- `cancellation_policy` - Kebijakan pembatalan untuk listing.  
- `require_guest_profile_picture` - Indikator apakah memerlukan gambar profil tamu (`t`) atau tidak (`f`).  
- `require_guest_phone_verification` - Indikator apakah memerlukan verifikasi telepon tamu (`t`) atau tidak (`f`).  
- `calculated_host_listings_count` - Jumlah listing yang dimiliki oleh host.  
- `reviews_per_month` - Rata-rata jumlah ulasan per bulan.  

**Dataset reviews (2/3)**
Dataset reviews berisi 84.849 sampel. Ini mencakup 6 fitur "

### Informasi Ulasan  
- **`listing_id`** - Identifikasi untuk listing yang direview.  
- **`id`** - Identifikasi unik untuk ulasan.  
- **`date`** - Tanggal saat ulasan diajukan.  
- **`reviewer_id`** - Identifikasi unik untuk reviewer.  
- **`reviewer_name`** - Nama reviewer.  
- **`comments`** - Teks umpan balik yang diberikan oleh reviewer.  

**Dataset calendar (3/3)**
Dataset calendar berisi 1.393.570 sampel. Ini terdiri dari 4 fitur :

### Informasi Ketersediaan dan Harga
- **`listing_id`** - Identifikasi untuk listing.  
- **`date`** - Tanggal untuk ketersediaan.  
- **`available`** - Status ketersediaan (`t` untuk tersedia, `f` untuk tidak tersedia).  
- **`price`** - Harga untuk tanggal tersebut (dalam dolar, bisa `null` untuk tanggal yang tidak tersedia).  

# **💡 Data Understanding 💡**

## **📌 Explore Datasets**

### **Basic Datasets Information**
- Dataset `listings` memiliki `92 columns` dan `3818 rows`
- Dataset `reviews` memiliki `6 columns` dan `84849 rows`
- Dataset `calendar` memiliki `4 columns` dan `1393570 rows`

#### **Hal yang harus dilakukan**
- Melakukan merge ketiga dataset terlebih dahulu berdasarkan `listing_id`

### **Basic Merged Datasets Information**
- Dataset memiliki `96 columns` dan `3818 rows`
- Dataset memiliki banyak tipe data yang tidak cocok
- Dataset memiliki banyak baris kosong
- Dataset memiliki 4 jenis tipe data yaitu : int64, object, float64, datetime64

### **Checking Duplicate Rows**
- Dataset tidak memiliki nilai duplikat

### **Checking Missing Values**
- Kolom `license` memiliki `3818 nilai null`, persentase sebesar 100% dari jumlah data
- Kolom `square_feet` memiliki `3721 nilai null`, persentase sebesar 97.46% dari jumlah data
- Kolom `monthly_price` memiliki `2301 nilai null`, persentase sebesar 60.27% dari jumlah data
- Kolom `security_deposit` memiliki `1952 nilai null`, persentase sebesar 51.13% dari jumlah data
- Kolom `weekly_price` memiliki `1809 nilai null`, persentase sebesar 47.38% dari jumlah data
- Kolom `notes` memiliki `1606 nilai null`, persentase sebesar 42.06% dari jumlah data
- Kolom `price_calendar` memiliki `1533 nilai null`, persentase sebesar 40.15% dari jumlah data
- Kolom `neighborhood_overview` memiliki `1032 nilai null`, persentase sebesar 27.03% dari jumlah data
- Kolom `cleaning_fee` memiliki `1030 nilai null`, persentase sebesar 26.98% dari jumlah data
- Kolom `transit` memiliki `934 nilai null`, persentase sebesar 24.46% dari jumlah data
- Kolom `host_about` memiliki `859 nilai null`, persentase sebesar 22.50% dari jumlah data
- Kolom `host_acceptance_rate` memiliki `773 nilai null`, persentase sebesar 20.25% dari jumlah data
- Kolom `review_scores_accuracy` memiliki `658 nilai null`, persentase sebesar 17.23% dari jumlah data
- Kolom `review_scores_checkin` memiliki `658 nilai null`, persentase sebesar 17.23% dari jumlah data
- Kolom `review_scores_value` memiliki `656 nilai null`, persentase sebesar 17.18% dari jumlah data
- Kolom `review_scores_location` memiliki `655 nilai null`, persentase sebesar 17.16% dari jumlah data
- Kolom `review_scores_cleanliness` memiliki `653 nilai null`, persentase sebesar 17.10% dari jumlah data
- Kolom `review_scores_communication` memiliki `651 nilai null`, persentase sebesar 17.05% dari jumlah data
- Kolom `review_scores_rating` memiliki `647 nilai null`, persentase sebesar 16.95% dari jumlah data
- Kolom `listing_id` memiliki `627 nilai null`, persentase sebesar 16.42% dari jumlah data
- Kolom `first_review` memiliki `627 nilai null, persentase sebesar 16.42% dari jumlah data
- Kolom `last_review` memiliki `627 nilai null`, persentase sebesar 16.42% dari jumlah data
- Kolom `reviews_per_month` memiliki `627 nilai null`, persentase sebesar 16.42% dari jumlah data
- Kolom `date` memiliki `627 nilai null`, persentase sebesar 16.42% dari jumlah data
- Kolom `space` memiliki `569 nilai null`, persentase sebesar 14.90% dari jumlah data
- Kolom `host_response_time` memiliki `523 nilai null`, persentase sebesar 13.70% dari jumlah data
- Kolom `host_response_rate` memiliki `523 nilai null`, persentase sebesar 13.70% dari jumlah data
- Kolom `neighbourhood` memiliki `416 nilai null`, persentase sebesar 10.90% dari jumlah data
- Kolom `xl_picture_url` memiliki `320 nilai null`, persentase sebesar 8.38% dari jumlah data
- Kolom `thumbnail_url` memiliki `320 nilai null`, persentase sebesar 8.38% dari jumlah data
- Kolom `medium_url` memiliki `320 nilai null`, persentase sebesar 8.38% dari jumlah data
- Kolom `host_neighbourhood` memiliki `300 nilai null`, persentase sebesar 7.86% dari jumlah data
- Kolom `summary` memiliki `177 nilai null`, persentase sebesar 4.64% dari jumlah data
- Kolom `bathrooms` memiliki `16 nilai null`, persentase sebesar 0.42% dari jumlah data
- Kolom `host_location` memiliki `8 nilai null`, persentase sebesar 0.21% dari jumlah data
- Kolom `zipcode` memiliki `7 nilai null`, persentase sebesar 0.18% dari jumlah data
- Kolom `bedrooms` memiliki `6 nilai null`, persentase sebesar 0.16% dari jumlah data
- Kolom `host_thumbnail_url` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_since` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_verifications` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_total_listings_count` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_picture_url` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_listings_count` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `host_name` memiliki `2 nilai null`, persentase sebesar 0.05% dari jumlah data
- Kolom `property_type` memiliki `1 nilai null`, persentase sebesar 0.03% dari jumlah data
- Kolom `beds` memiliki `1 nilai null`, persentase sebesar 0.03% dari jumlah data

## **📌 Data Types Information**
### **List of Column Type:**
- **Object:** listing_url, last_scraped, name, summary, space, description, experiences_offered, neighborhood_overview, notes, transit, thumbnail_url, medium_url, picture_url, xl_picture_url, host_url, host_name, host_since, host_location, host_about, host_response_time, host_response_rate, host_acceptance_rate, host_is_superhost, host_thumbnail_url, host_picture_url, host_neighbourhood, host_verifications, host_has_profile_pic, host_identity_verified, street, neighbourhood, neighbourhood_cleansed, neighbourhood_group_cleansed, city, state, market, smart_location, country_code, country, is_location_exact, property_type, room_type, bed_type, amenities, price_listings, weekly_price, monthly_price, security_deposit, cleaning_fee, extra_people, calendar_updated, has_availability, calendar_last_scraped, first_review, last_review, requires_license, jurisdiction_names, instant_bookable, cancellation_policy, require_guest_profile_picture, require_guest_phone_verification, price_calendar
- **Float64:** host_listings_count, host_total_listings_count, square_feet, bathrooms, bedrooms, beds, review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value, reviews_per_month, listing_id, license
- **Int64:** id, scrape_id, host_id, accommodates, guests_included, minimum_nights, maximum_nights, availability_30, availability_60, availability_90, availability_365, number_of_reviews, calculated_host_listings_count
- **Datetime:** date

## **📌 Statistical Summary**

## **📌 Exploratory Data Analysis (EDA)**

# **💡 Data Cleansing/Preprocessing 💡**

## **📌 Handling Invalid Values**
### **Fitur object ke datetime**
- Fitur yang diubah dari object ke datetime yaitu: `last_scraped, host_since, calendar_last_scraped, first_review, last_review, dan date`. Konversi ini memungkinkan analisis yang lebih efektif terhadap data berbasis waktu. Dengan tipe data datetime, kita dapat melakukan operasi seperti perhitungan durasi, pengelompokan data berdasarkan waktu, dan analisis tren temporal.
### **Fitur object ke float**
- Fitur yang diubah dari object ke float yaitu: `price_listings, weekly_price, monthly_price, security_deposit, cleaning_fee, extra_people, dan price_calendar`. Konversi ini diperlukan untuk memastikan bahwa nilai-nilai yang berhubungan dengan harga dan biaya dapat digunakan dalam analisis numerik.
### **Fitur object ke boolean**
- Fitur yang diubah menjadi tipe data boolean yaitu: `host_is_superhost, host_has_profile_pic, host_identity_verified, is_location_exact, has_availability, instant_bookable, require_guest_profile_picture, dan require_guest_phone_verification`. Konversi ini penting untuk memastikan bahwa kolom-kolom yang berisi informasi biner (ya/tidak) diwakili dengan tipe data yang sesuai.
### **Fitur object ke int**
- Fitur yang diubah menjadi tipe data integer yaitu: `accommodates, bathrooms, bedrooms, beds, minimum_nights, maximum_nights, availability_30, availability_60, availability_90, availability_365, number_of_reviews, review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value, calculated_host_listings_count`. Konversi ini dilakukan untuk memastikan bahwa nilai numerik yang merepresentasikan jumlah atau skor disimpan dalam tipe data yang lebih efisien.
### **Fitur object ke float**
- Fitur yang diubah menjadi tipe data float yaitu: `bathrooms, bedrooms, beds, review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value, reviews_per_month`. Konversi ini dilakukan untuk mempertahankan presisi dalam nilai-nilai yang mungkin memiliki desimal.

## **📌 Handling Missing Values**

### **Drop Column**
- Menghapus kolom `license` dan `square feet` karena terlalu banyak baris yang kosong, membuat kolom tersebut tidak bisa digunakan
- Menghapus kolom `neighbourhood` karena tidak diperlukan, neighbourhood sudah mempunyai versi cleansed nya

### **Drop Row**
- Menghapus baris kosong pada kolom `listing_id` karena kolom id yang kosong tidak valid

### **Imputation Numeric**
- Fitur yang terdapat pada rate_columns = `last_review, first_review, host_response_rate, host_response_time` nilai null Diisi dengan nilai sebelumnya
- Fitur yang terdapat pada `price_columns = price_calendar` nilai null Diisi dengan nilai `median` karena memiliki right skewed dan nilai outlier ekstrem.
- Fitur `monthly_price` nilai null Diisi dengan mengkalikan harga listing perhari dengan jumlah hari per bulan
- Fitur `weekly_price` nilai null Diisi dengan mengkalikan harga listing perhari dengan jumlah hari per minggu
- Fitur yang terdapat pada score_columns = `reviews_per_month, review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value, security_deposit, cleaning_fee` Diisi dengan nilai 0 karena tidak semua listing memiliki review dan fee tambahan

### **Imputation Categoric**
- Fitur yang terdapat pada frequent_text = `space, host_neighbourhood, bathrooms, host_location, bedrooms, host_since, host_total_listings_count, host_listings_count, host_name, property_type, beds, host_acceptance_rate` Diisi dengan kata yang paling banyak muncul atau modus
- Fitur yang terdapat pada not_available = `notes, neighborhood_overview, transit, host_about, summary, zipcode` Diisi dengan kata tidak tersedia
- Fitur yang terdapat pada no_image = `thumbnail_url, medium_url, xl_picture_url, host_picture_url, host_has_profile_pic, host_thumbnail_urle` Diisi dengan kata no image untuk kolom yang memiliki gambar

## **📌 Handling Outliers**
![image](https://github.com/user-attachments/assets/698798f9-e0af-4daa-89dc-365d0c9e6ce7)
![image](https://github.com/user-attachments/assets/6464f3ad-b4dd-4a50-a0ad-a151519d0351)
### **IQR**
- Tidak ada outlier pada dataset ini untuk semua kolom. Semua data dianggap berada dalam batas yang wajar sesuai dengan perhitungan IQR
- Meskipun nilai outlier teratasi semua, Perhitungan IQR tidak cocok untuk mendeteksi outlier dalam dataset dengan distribusi tertentu, terutama jika distribusi tidak normal atau data cenderung homogen.
- Maka pada dataset yang kita miliki tidak terlalu cocok karna banyak memiliki nilai ekstrem.
### **Z-Score**
- Sebelum handling dengan Z-Score, jumlah total baris adalah 3191.
- Setelah Z-Score, terdapat 2841 outliers dan hanya 350 non-outliers yang tersisa.
- Z-Score terlalu ketat untuk dataset dengan distribusi skewed, sehingga menganggap banyak data valid sebagai outlier.
- Hasil Z-Score kurang optimal untuk dataset ini karena terlalu banyak data yang dianggap outlier (89%)
### **Winsorization**
- Outlier All Data: 2755 outlier, dengan 436 data yang tidak terdeteksi sebagai outlier.
- Winsorization menggantikan nilai ekstrim dengan batas atas atau bawah yang telah ditentukan, bukan menghapusnya, sehingga data tetap utuh dan tidak hilang.
- Winsorization dapat diteruskan jika ingin menjaga sebanyak mungkin data sambil mengurangi dampak dari nilai ekstrim.
- Karena Data kita memiliki banyak nilai ekstrem dan tidak terdistribusi normal: Winsorization adalah pilihan yang baik karena menggantikan outlier dengan batas yang lebih realistis tanpa menghapus data, namun tetap dapat mempertahankan informasi penting dalam data.

## **📌 Feature Engineering/Extraction**
### **Membuat kolom day, month, and year**
Memisahkan kolom date menjadi hari, tanggal, dan tahun untuk mendapatkan insight yang lebih rinci
### **Membuat kolom average review score**
Rata-rata dari semua skor ulasan
### **Membuat kolom property attractiveness**
Mengukur seberapa menarik properti berdasarkan ulasan dan skor rata-rata
### **Membuat kolom review positive ratio**
Mengukur kualitas ulasan berdasarkan skor ulasan keseluruhan
### **Membuat kolom booking frequency**
Mengukur apakah properti sering dipesan atau tersedia untuk waktu yang lama
### **Membuat kolom high quality listings**
Mengukur seberapa sering listing mendapatkan skor ulasan tinggi
### **Membuat kolom response speed**
Mengukur seberapa sering listing mendapatkan review tiap bulannya

## **📌 Feature Transformation (Numeric)**
![image](https://github.com/user-attachments/assets/801fbb64-488b-4e3a-9b9b-00c6c23e8c31)
![image](https://github.com/user-attachments/assets/62c93b26-8b65-429b-af7f-05dc2c3de0dc)



## **📌 Feature Encoding (Categoric)**

## **📌 Feature Selection**

## **📌 Data Splitting**

## **📌 Handling Imbalanced Data**
