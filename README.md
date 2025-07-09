# 🌿 Simulasi Biomassa dari Limbah Kelapa Sawit
----
## 🌳 Halo Sobat ETL! Selamat datang di repositori "Analisis  Biomassa dari Limbah Kelapa Sawit" 🌱
--
Proyek ini dibuat dalam menyelesaikan week task, dengan tujuan meningkatkan kepedulian terhadap lingkungan sekaligus membangkitkan ketertarikan pada data. Fokus utama proyek ini adalah mengulas potensi biomassa dari limbah kelapa sawit.

Mengapa hal ini penting? Karena biomassa memiliki potensi besar sebagai sumber energi hijau. Namun, minimnya minat dan kurangnya inisiatif dapat menyebabkan potensi ini terabaikan begitu saja. Melalui analisis data dan visualisasi, kita akan menelusuri sejauh mana dampak biomassa ini, serta bagaimana data dapat menjadi alat bantu dalam mendorong transisi energi hijau yang lebih adil dan berkelanjutan.

Yuk, kita gali bareng-bareng! Semoga proyek ini bisa jadi referensi, inspirasi, atau bahkan langkah awal ide besar berikutnya untuk kita semua🌏✨



📊 *Analisis Energi – Ekonomi – Emisi Berbasis Data Sintetis*

---

## 📌 Pendahuluan

### 🔍 Latar Belakang

Dalam menghadapi krisis iklim global dan meningkatnya kebutuhan energi, dunia tengah bergerak menuju transisi energi hijau — yakni peralihan dari sumber energi fosil (batu bara, minyak bumi, gas alam) menuju energi yang lebih bersih dan berkelanjutan.

Salah satu opsi terbarukan yang potensial adalah **biomassa dari limbah kelapa sawit**. Di Indonesia, limbah padat seperti **tandan kosong (TKKS)**, **cangkang**, dan **serat** sangat melimpah, namun sering dibuang atau dibakar terbuka, memicu polusi udara dan emisi karbon. Padahal, limbah ini dapat dikonversi menjadi listrik ramah lingkungan.

---

### 🎯 Mengapa Ini Penting?

| Keunggulan Biomassa | Penjelasan |
|---------------------|------------|
| ♻️ Ramah Lingkungan | Netral karbon karena emisi yang dilepas diserap kembali oleh tanaman |
| 📦 Ketersediaan Lokal | Tidak perlu impor, tersedia dari limbah perkebunan lokal |
| 💰 Efisiensi Ekonomi | Memberi nilai tambah pada limbah yang sebelumnya tidak dimanfaatkan |
| 🌍 Reduksi Emisi | Mencegah polusi dari pembakaran terbuka |

> _"Utilizing palm oil biomass not only improves rural energy access, but also prevents open burning that contributes to air pollution and GHGs."_  
> — **ASEAN-German Energy Programme, 2020**

> _"Biomass has been identified as a major source of renewable energy with potential to reduce carbon emissions if sustainably managed."_  
> — **IEA Bioenergy, 2022**

---

### 🎯 Tujuan Proyek

- Menyimulasikan potensi energi dari limbah sawit
- Menghitung profit ekonomi dari konversi energi
- Mengukur pengurangan emisi CO₂
- Menganalisis hubungan antara lahan, limbah, energi, dan profit

---

## 🗂️ 2. Pembuatan Dataset Sintetis

### 📌 Tujuan

Karena keterbatasan data lapangan, digunakan **data sintetis** yang direkayasa menggunakan `numpy`, `pandas`, dan asumsi realistis dari literatur.

---

### ⚙️ Variabel dalam Dataset

| Variabel | Penjelasan |
|----------|------------|
| `Luas_ha` | Luas kebun sawit |
| `TBS_per_ha` | Produksi TBS per hektar (18–25 ton) |
| `Limbah_ton` | 20% dari total TBS |
| `Rasio_Biomassa` | 50%–70% dari limbah dapat digunakan |
| `Energi_kWh_Riil` | Energi aktual setelah efisiensi 80% |
| `Profit_Bersih_Rp` | Pendapatan dikurangi biaya operasional |
| `Net_Emisi_kg` | Emisi yang berhasil dihindari |

---

### 🧪 Asumsi Simulasi untuk menghitung potensi

| Komponen | Nilai |
|----------|-------|
| Konversi MJ ke kWh | 1 MJ = 0.278 kWh |
| Efisiensi PLT | 80% |
| Harga listrik | Rp 1.450 / kWh |
| Biaya operasional | Rp 30.000 – Rp 60.000 / ton |
| Emisi CO₂ | Teoritis: 1.7 kg/kg, Dihindari: 1.6 kg/kg |

---

### 🔢 Contoh Potongan Data

| Kebun | Luas_ha | Limbah_ton | Biomassa_ton | Energi_kWh_Riil | Profit_Bersih_Rp | Net_Emisi_kg |
|-------|---------|-------------|---------------|------------------|-------------------|---------------|
| 1     | 729     | 2964.45     | 1704.27       | 35.047.245       | Rp 48.912.346.211 | 1.789.626     |
| 2     | 438     | 1664.89     | 951.66        | 19.618.760       | Rp 27.892.116.124 | 946.036       |

---

## 📊 3. Analisis Korelasi & Regresi

### 📌 Korelasi Energi vs Luas Lahan

```python
Korelasi Energi vs Luas Lahan: 0.93
💡 Korelasi kuat positif. Semakin luas kebun, semakin tinggi energi yang dapat dihasilkan.
```

## 📌 Regresi Linear
```python
Koefisien Regresi: 47520.16
Intercept: -218574.06
R-squared: 0.86
📈 Luas kebun adalah faktor prediktor utama energi biomassa.
```

## 📊 Visualisasi

Plot 1: Luas Lahan vs Energi Listrik

Plot 2: Limbah vs Pendapatan

Plot 3: Emisi Dihindari vs Teoritis

Plot 4: Profit Bersih per Kebun

## 💰🌱 4. Evaluasi Ekonomi & Lingkungan
### 💵 Ekonomi
Pendapatan rata-rata: Rp 25–55 Miliar/kebun

Biaya operasional: Rp 5–20 Miliar/kebun

Profit bersih: Positif untuk semua kebun

## 🌍 Lingkungan
Net Emisi CO₂: Positif di semua kebun
→ Artinya emisi lebih banyak dihindari daripada dihasilkan.

## ✅ 5. Penutup
Simulasi ini menunjukkan bahwa:

### Aspek	Hasil
### ⚡ Energi	
Semakin luas kebun, energi meningkat signifikan
### 💸 Ekonomi	
Profit bersih tinggi, layak dikembangkan
### 🌱 Lingkungan	
Emisi CO₂ dapat dikurangi drastis

“Mengganti energi fosil dengan biomassa berbasis limbah bukan sekadar alternatif, tetapi langkah strategis menuju masa depan yang berkelanjutan.”
— IRENA, 2022
### 🌍Limbah bukan akhir dari siklus produksi — ia bisa menjadi awal energi baru yang ramah lingkungan. Dengan pendekatan berbasis data dan analisis yang tepat, biomassa dari kelapa sawit mampu menjawab tantangan energi, ekonomi, dan ekologi secara bersamaan.
