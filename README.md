# **✨ Research Campaign - by The Golden Gate ✨**

**✅ Members of The Golden gate ✅**

1. Nur Imam Masri
2. Astuti Rahmawati
3. Prasidya Bagaskara
4. Moh. Harwin Prayoga
5. Riskiyatul Hasanah
6. M Rayhan Azzindani
7. Siti Hajjah Mardiah
8. Christine
9. M. Ifzal Asril

## **Languages and Technologies used**

- Python 3.12
- Google Colab or Visual Studio Code

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

## **⛳ Business Understanding ⛳**

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
    
        
**📝 References :**

- 


## **🕹 Data Description 🕹**

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

- Dataset memiliki `29 columns` dan `2240 rows` data
- Terdapat 3 jenis tipe data yaitu : `int64, object, float64`
- Kolom `Income` memiliki 2216 nilai non-null, dan `24 nilai null / missing values`

## **📌 Data Types Information**

**List of Column Types:**

- **Date**

    `Dt_Customer`

- **Categorical** (10 Columns) : 
    - `ID` - Nominal
    - `Education` - Ordinal (Levels : Basic - Graduation - 2n Cycle - Master - PhD)
    - `Marital_Status` - Nominal
    - `AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Complain, Response` - Nominal (Binary 0 & 1)

- **Continuous** (18 Columns):

    `Year_Birth, Income, Kidhome, Teenhome, 
    Recency, MntWines, MntFruits, MntMeatProducts, 
    MntFishProducts, MntSweetProducts, MntGoldProds, 
    NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, 
    NumStorePurchases, NumWebVisitsMonth, Z_CostContact, Z_Revenue`

**Change the Some column data type**

- Kita mengubah tipe data categorical ke `category`, agar dalam melakukan explorasi dan insight tidak di anggap sebagai data numerical
- Untuk memudahkan dalam proses extraction `Dt_Customer` maupun part of, maka kolom date `object` diubah menjadi `datetime64`

## **📌 Statistical Summary**

## **📌 Exploratory Data Analysis (EDA)**

## **📌 Handling Invalid Values**

## **📌 Handling Outliers**

## **📌 Feature Transformation (Numeric)**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/4962331e-fede-4185-9b24-676068f53654)

Dari hasil temuan, kita dapat menentukan beberapa transformasi yang akan kita lakukan :
- **Scaling and Converting to a Normal Distribution :**
    - log Transformation
    - Box-Cox Transformation
    - Yeo-Johnson Transformation
    
    **Adapun daftar column yang akan kita transform pada proses ini :**
        - Conversion_rate_web
        - MntFishProducts
        - MntFruits
        - MntGoldProds
        - MntMeatProducts
        - MntSweetProducts
        - MntWines
        - NumCatalogPurchases
        - NumDealsPurchases
        - NumStorePurchases
        - NumWebPurchases
        - Primer_purchase
        - Spending
        - Tersier_purchase
        - Total_revenue
    
- **Just Scaling :**
    - Normalization
    - Standardization
    
    **Adapun daftar column yang akan kita transform pada proses ini :**
        - Age
        - Income
        - Lifetime
        - Month_joined
        - NumWebVisitsMonth
        - Recency
        - Total_Purchases
        - Year_Birth

- Sedangkan untuk beberapa kolom yang **tidak perlu melakukan Transformasi** karena rentang nilai yang masih wajar sebagai berikut :
    - Kidhome
    - Teenhome
    - Dependents
    - Total_Cmp

**Choice Determination:**

- Pada proses `Scaling and Converting to a Normal Distribution` ini kita menggunakan `Yeo-Johnson Transformation`, karena dari hasilnya kita bisa melihat hasil bentuk curve yang lebih Normal Distribusi
- Pada proses `Just Scaling` ini kita menggunakan `Normalization` karena lebih robust untuk algoritma yang akan kita gunakan 

**Yeo-Johnson Transformation**

Unlike the Box-Cox transform, it does not require the values for each input variable to be strictly positive.

It supports zero values and negative values. This means we can apply it to our dataset without scaling it first.

```html
pt = PowerTransformer(method='yeo-johnson')
df[log_cols] = pt.fit_transform(df[log_cols])
```

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/2c896c5e-4141-4085-ab20-490fb1d53ac0)

**Normalization**

```html
from sklearn.preprocessing import MinMaxScaler
# create a scaler object
scaler = MinMaxScaler()
# fit and transform the data
df[norm_cols] = pd.DataFrame(scaler.fit_transform(df[norm_cols]), columns=df[norm_cols].columns)
```

**Kesimpulan**

Berdasarkan hasil pengecekan pada beberapa fitur yang telah diproses menggunakan transformation sebelumnya, dapat diketahui bahwa keseluruhan nilai skewnessnya sudah memiliki rentang yang lebih seragam (tidak jauh dan tidak terlalu bervariasi). Sehingga dapat disimpulkan bahwa teknik fitur transformation yang telah kami lakukan sudah valid dan kami.

## **📌 Feature Encoding (Categoric)**

## **📌 Feature Selection**

## **📌 Data Splitting**

## **📌 Handling Imbalanced Data**