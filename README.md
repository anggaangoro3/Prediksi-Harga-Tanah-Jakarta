# 🏙️ Analisis Harga Tanah Jakarta

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=jupyter&logoColor=white)](https://jupyter.org/try)
[![Selenium](https://img.shields.io/badge/Scraping-Selenium-43B02A?logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![Looker Studio](https://img.shields.io/badge/Visualisation-Looker%20Studio-4285F4?logo=google&logoColor=white)](https://lookerstudio.google.com/reporting/83ea8504-fe1b-4d59-9334-b87393cdd6ad))

> **Project Data Science End-to-End**: Dari *Web Scraping* hingga *Dashboard Monitoring* Interaktif untuk memetakan valuasi harga tanah di seluruh wilayah DKI Jakarta.

---

## 📖 Overview

Proyek ini bertujuan untuk menganalisis distribusi dan tren harga tanah di Jakarta secara data-driven. Mengingat tingginya variasi harga properti di ibu kota, proyek ini memberikan wawasan mendalam mengenai:
- **Kesenjangan Harga (Price Gap)** antara harga rata-rata dan harga maksimal di setiap distrik.
- **Pemetaan Wilayah** berdasarkan harga per meter persegi ($m^2$).
- **Analisis Anomali** untuk mendeteksi *outlier* atau kesalahan input harga pada data listing properti.

Data dikumpulkan secara mandiri (*self-collected*) melalui teknik **Web Scraping** dan diolah melalui pipeline pembersihan data yang ketat sebelum divisualisasikan.

---

## 🚀 Key Features

* **🕷️ Automated Data Collection**: Script Python menggunakan **Selenium** untuk scraping ribuan data listing dari portal properti (Rumah123 & 99.co).
* **🧹 Robust Data Cleaning**: Penanganan *missing values*, *duplicate removal*, dan pembersihan *textual data* (konversi "Miliar/Triliun" ke format numerik).
* **📍 Geospatial Analysis**: Integrasi dengan **Geopy** untuk mengubah nama lokasi menjadi koordinat (Latitude/Longitude) presisi.
* **📈 Outlier Detection**: Menggunakan metode IQR dan *domain knowledge* untuk memfilter harga yang tidak masuk akal (contoh: *input error* harga Triliun).
* **📊 Interactive Dashboard**: Deployment hasil analisis ke **Google Looker Studio** dengan fitur filter wilayah, *heatmap*, dan *scorecard*.

---

## 🛠️ Tech Stack

* **Bahasa Pemrograman**: Python
* **Data Scraping**: Selenium, BeautifulSoup
* **Data Processing**: Pandas, NumPy
* **Feature Engineering**: Geopy (Nominatim), Scikit-learn (Scaling/Encoding)
* **Visualization**: Matplotlib, Seaborn (untuk EDA), Google Looker Studio (untuk Dashboard)

---

## 📂 Project Structure

```text
analisis-harga-tanah-jakarta/
│
├── 📂 Demo Screenshot/                # Screenshot hasil dashboard
│   ├── Demo Screenshot 1.png
│   ├── Demo Screenshot 2.png
│   └── Demo Screenshot 3.png
│
├── 📂 raw dataset/                    # Data mentah hasil scraping
│   ├── GABUNGAN_FINAL_DATASET.csv
│   └── baru99co.csv
│
├── 📓 Jakarta_land_price_analysis_pipeline.ipynb  # Notebook utama (Cleaning & Analysis)
├── 📓 Scrping_Rumah123_Selenium.ipynb             # Script scraping data
├── 📄 Link Dashboard                              # Tautan ke dashboard publik
└── 📄 README.md                                   # Dokumentasi proyek
