# 🏢 ARTHA PROPERTI SEJAHTERA
## Kurikulum Lengkap: Menjadi Data Analyst di Perusahaan Property Developer

---

## 📋 Tentang Dataset

**Artha Properti Sejahtera** adalah perusahaan developer property ramah lingkungan yang mengembangkan:
- 🏘️ **Perumahan** (landed house dengan konsep eco-living)
- 🏢 **Apartemen** (high-rise dengan green building certification)
- 🏪 **Area Komersial** (ruko, mal, kawasan industri eco-friendly)

Dataset ini mencakup **10 proyek nyata**, **~1,900+ unit**, **800 customer**, dan **600+ transaksi** selama tahun 2021-2024.

---

## 📁 Struktur File

```
artha_properti/
│
├── README.md                    ← Panduan ini
│
├── data/                        ← Data CSV (10 tabel)
│   ├── employees.csv            (31 karyawan)
│   ├── projects.csv             (10 proyek)
│   ├── units.csv                (1,949 unit)
│   ├── customers.csv            (800 customer)
│   ├── unit_sales.csv           (600 penjualan)
│   ├── payment_transactions.csv (1,921 transaksi)
│   ├── marketing_campaigns.csv  (18 kampanye)
│   ├── marketing_leads.csv      (1,000 leads)
│   ├── green_certifications.csv (21 sertifikasi)
│   └── sustainability_metrics.csv (300 metrics)
│
├── sql/
│   ├── 01_schema.sql            ← Buat struktur tabel
│   ├── 02_seed_data.sql         ← Import data CSV ke SQLite
│   └── 03_latihan_queries.sql   ← 20+ latihan SQL (Dasar→Advanced)
│
├── python/
│   └── analysis.py              ← Script analisis lengkap (8 modul)
│
└── output/                      ← Grafik & laporan hasil analisis
    ├── *.png                    ← 7 visualisasi
    └── Laporan_Artha_Properti.xlsx
```

---

## 🗺️ ROADMAP BELAJAR

### FASE 1: FONDASI (Minggu 1-2)
**Tujuan:** Memahami data & SQL dasar

| Materi | File | Topik |
|--------|------|-------|
| Data Overview | `data/*.csv` | Memahami struktur bisnis property |
| SQL Dasar | `sql/01_schema.sql` | DDL, CREATE TABLE, relationships |
| SELECT & Filter | `sql/03_latihan_queries.sql` (Query 1.1-1.5) | WHERE, LIKE, IN, BETWEEN |

**Latihan:** Jawab pertanyaan bisnis dasar:
- Berapa unit tersedia di proyek Serpong?
- Siapa customer dengan penghasilan > 50 juta/bulan?

---

### FASE 2: AGGREGASI & GROUPING (Minggu 3-4)
**Tujuan:** Membuat laporan summary bisnis

| Materi | File | Topik |
|--------|------|-------|
| GROUP BY & Agregasi | Query 2.1-2.5 | SUM, AVG, COUNT, HAVING |
| Python Pandas Dasar | `python/analysis.py` Modul 1 | pd.read_csv, df.describe(), groupby |
| Visualisasi Dasar | Modul 2 | matplotlib bar chart, pie chart |

**Latihan:** Buat laporan:
- Revenue per proyek bulan ini
- Distribusi metode pembayaran
- Unit terjual vs available per proyek

---

### FASE 3: JOIN & RELASI TABEL (Minggu 5-6)
**Tujuan:** Analisis multi-tabel seperti business analyst

| Materi | File | Topik |
|--------|------|-------|
| JOIN Kompleks | Query 3.1-3.4 | INNER JOIN, LEFT JOIN, multi-table |
| Customer Analysis | Modul 4 | Customer profiling, segmentasi |
| Marketing Analytics | Modul 5 | Campaign ROI, lead funnel |

**Latihan Studi Kasus:**
- *"Marketing minta laporan: campaign mana yang paling efisien dari segi cost per conversion?"*
- *"Siapa customer yang paling sering membeli? Berapa total nilai pembeliannya?"*

---

### FASE 4: WINDOW FUNCTIONS & ADVANCED SQL (Minggu 7-8)
**Tujuan:** Analisis temporal dan perbandingan

| Materi | File | Topik |
|--------|------|-------|
| Window Functions | Query 4.1-4.4 | RANK, LAG/LEAD, RUNNING TOTAL, NTILE |
| Tren Analysis | Modul 2 & 6 | Moving average, YoY comparison |
| Sustainability Metrics | Modul 6 | Environmental KPI analysis |

**Latihan Studi Kasus:**
- *"Direktur minta: bandingkan revenue Q3 2023 vs Q3 2022, naik berapa %?"*
- *"Buat ranking sales person bulan Januari, hanya tampilkan Top 3 tiap bulan"*

---

### FASE 5: DASHBOARD & REPORTING (Minggu 9-10)
**Tujuan:** Menyajikan insights ke stakeholder

| Materi | File | Topik |
|--------|------|-------|
| Dashboard Eksekutif | Query 5.1, Modul 7 | KPI summary, executive view |
| Python Advanced | Modul 7 & 8 | Heatmap, multi-chart dashboard |
| Excel Report | Modul Export | openpyxl, multi-sheet report |

**Deliverable:** Dashboard lengkap berisi:
- Revenue dashboard
- Inventory monitoring
- Marketing performance
- Sustainability scorecard

---

### FASE 6: STUDI KASUS ADVANCED (Minggu 11-12)
**Tujuan:** Simulasi kerja nyata

#### Kasus 1: Revenue Shortfall Investigation
*"Revenue Q2 2024 turun 15% dari target. Temukan penyebabnya!"*
- Analisis tren bulanan
- Breakdown per proyek, tipe unit, sales team
- Rekomendasi tindakan

#### Kasus 2: Inventory Optimization
*"Ada 200+ unit yang sudah 6 bulan tidak terjual. Apa strategi marketing yang tepat?"*
- Identifikasi unit slow-moving
- Analisis price positioning
- Customer segment yang paling cocok

#### Kasus 3: Customer Churn Prevention
*"Customer investor mulai berkurang. Bagaimana mempertahankan mereka?"*
- RFM Analysis
- Customer lifetime value
- Prediksi customer potensial

#### Kasus 4: Green Premium Analysis
*"Apakah properti bersertifikat hijau memang terjual lebih mahal?"*
- Join dengan green_certifications
- Price comparison analysis
- ROI sertifikasi hijau

---

## 🛠️ SETUP & CARA MENJALANKAN

### Prasyarat
```bash
# Install Python libraries
pip install pandas matplotlib seaborn openpyxl sqlite3

# Install SQLite (biasanya sudah tersedia)
sqlite3 --version
```

### Langkah 1: Setup Database SQLite
```bash
cd artha_properti

# Buat database
sqlite3 artha_properti.db < sql/01_schema.sql
sqlite3 artha_properti.db < sql/02_seed_data.sql

# Verifikasi
sqlite3 artha_properti.db "SELECT COUNT(*) FROM unit_sales;"
```

### Langkah 2: Eksplorasi dengan SQL
```bash
# Buka SQLite interactive
sqlite3 artha_properti.db

# Di dalam SQLite:
.mode column
.headers on
SELECT * FROM projects LIMIT 5;
.quit
```

### Langkah 3: Jalankan Analisis Python
```bash
cd artha_properti
mkdir output
python python/analysis.py
```

### Alternatif: Jupyter Notebook
```bash
pip install jupyter
jupyter notebook
# Lalu buka python/analysis.py dan copy ke cells notebook
```

---

## 📊 Tools yang Digunakan

| Tool | Kegunaan | Level |
|------|----------|-------|
| **SQLite** | Database lokal, query latihan | Pemula |
| **Python/Pandas** | Manipulasi & analisis data | Menengah |
| **Matplotlib/Seaborn** | Visualisasi data | Menengah |
| **openpyxl** | Export laporan Excel | Menengah |
| **Jupyter Notebook** | Exploratory analysis | Semua level |

### Tools Bonus (Opsional)
| Tool | Kegunaan |
|------|----------|
| **Tableau Public** | Buat dashboard interaktif (gratis) |
| **Power BI Desktop** | Buat dashboard interaktif (gratis) |
| **DBeaver** | GUI untuk database SQL |
| **VS Code** | IDE untuk Python |

---

## 🎯 Kompetensi yang Dikuasai

Setelah menyelesaikan kurikulum ini, Anda mampu:

✅ Menulis SQL dari dasar hingga window functions  
✅ Menganalisis data penjualan, marketing, dan operasional  
✅ Membuat visualisasi yang informatif dan profesional  
✅ Menyusun laporan Excel multi-sheet otomatis  
✅ Memahami bisnis proses developer property  
✅ Menjawab pertanyaan bisnis dengan data  
✅ Mempresentasikan insights kepada stakeholder  

---

## 📞 Konteks Bisnis

### Departemen yang Berinteraksi dengan Data Analyst
- **Sales & Marketing**: Laporan penjualan, marketing ROI, lead management
- **Finance**: Revenue report, cash flow, payment tracking
- **Project**: Progress proyek, inventory unit, delivery monitoring
- **Management**: Executive dashboard, KPI monitoring, strategic planning
- **Sustainability**: Green metrics, certifications, ESG reporting

### Pertanyaan Bisnis yang Sering Muncul
1. "Berapa total revenue bulan ini vs bulan lalu?"
2. "Campaign digital mana yang paling efisien?"
3. "Unit di proyek mana yang paling cepat habis?"
4. "Sales siapa yang performa terbaik Q3?"
5. "Berapa % customer menggunakan KPR?"
6. "Proyek mana yang paling hijau (sustainability score tertinggi)?"

---

*Dibuat untuk program pembelajaran internal Artha Properti Sejahtera*  
*Versi 1.0 | Data Analyst Training Program 2024*
