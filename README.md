# Dasbor Data Pasar Saham dan Pendapatan

Proyek Data Science untuk mengekstraksi, membersihkan, dan memvisualisasikan data kinerja saham serta pendapatan historis dua perusahaan: **Tesla (TSLA)** dan **GameStop (GME)**.

## Daftar Isi

- [Gambaran Umum](#gambaran-umum)
- [Fitur Utama](#fitur-utama)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Struktur Proyek](#struktur-proyek)
- [Alur Kerja](#alur-kerja)
- [Instalasi](#instalasi)
- [Cara Menjalankan](#cara-menjalankan)
- [Catatan dan Keterbatasan](#catatan-dan-keterbatasan)
- [Rencana Pengembangan](#rencana-pengembangan)
- [Lisensi](#lisensi)

## Gambaran Umum

Proyek ini menggabungkan dua sumber data: API keuangan untuk harga saham historis, dan web scraping untuk data pendapatan kuartalan. Data mentah dari kedua sumber diproses menjadi dataset yang bersih, lalu ditampilkan dalam dasbor interaktif yang memperlihatkan hubungan antara pergerakan harga saham dan pendapatan kuartalan suatu perusahaan dari waktu ke waktu.

Tujuan utama proyek:

- Menunjukkan alur kerja Data Science end-to-end, mulai dari pengambilan data hingga visualisasi.
- Memudahkan analisis hubungan antara kinerja pendapatan dan pergerakan harga saham.
- Menyediakan dasar yang dapat dikembangkan untuk perusahaan lain.

## Fitur Utama

| Fitur | Deskripsi |
|---|---|
| Ekstraksi data saham | Mengambil data harga saham historis langsung dari Yahoo Finance menggunakan pustaka `yfinance`. |
| Web scraping | Mengekstrak data pendapatan kuartalan dari tabel HTML pada halaman web menggunakan `requests` dan `BeautifulSoup`. |
| Pembersihan data | Menggunakan `pandas` untuk menangani nilai kosong (null), menghapus simbol mata uang dan tanda koma, serta memformat tipe data. |
| Visualisasi interaktif | Membuat grafik garis interaktif dengan `plotly` yang menampilkan tren harga saham dan pendapatan secara berdampingan. |

## Teknologi yang Digunakan

| Kategori | Teknologi |
|---|---|
| Bahasa pemrograman | Python 3 |
| Manipulasi data | pandas |
| API keuangan | yfinance |
| Web scraping | requests, bs4 (BeautifulSoup) |
| Visualisasi data | plotly |
| Lingkungan kerja | Jupyter Notebook / JupyterLab |

## Struktur Proyek

```
.
├── Revenue Data and Building a Dashboard.ipynb   # Notebook utama (ekstraksi, pembersihan, visualisasi)
└── README.md                                      # Dokumentasi proyek
```

> Sesuaikan nama berkas pada diagram di atas dengan nama berkas yang sebenarnya di repositori Anda.

## Alur Kerja

1. **Ekstraksi harga saham**: mengambil data historis TSLA dan GME melalui `yfinance`.
2. **Scraping pendapatan**: mengunduh halaman web dan membaca tabel pendapatan kuartalan dengan `BeautifulSoup`.
3. **Pembersihan data**: menghapus simbol `$` dan tanda koma, membuang baris kosong, serta mengonversi kolom ke tipe numerik dan tanggal.
4. **Visualisasi**: membangun grafik interaktif untuk membandingkan harga saham dan pendapatan dari waktu ke waktu.

## Instalasi

1. Clone repositori ini:

   ```bash
   git clone https://github.com/<username>/<nama-repositori>.git
   cd <nama-repositori>
   ```

2. (Opsional) Buat dan aktifkan virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate        # macOS/Linux
   venv\Scripts\activate           # Windows
   ```

3. Instal dependensi:

   ```bash
   pip install pandas yfinance requests beautifulsoup4 plotly lxml jupyterlab
   ```

## Cara Menjalankan

1. Jalankan JupyterLab:

   ```bash
   jupyter lab
   ```

2. Buka berkas notebook `Revenue Data and Building a Dashboard.ipynb`.
3. Jalankan seluruh sel secara berurutan (**Run > Run All Cells**).
4. Dasbor interaktif akan tampil pada bagian akhir notebook.

## Catatan dan Keterbatasan

- Data harga saham bergantung pada ketersediaan layanan Yahoo Finance melalui `yfinance`.
- Web scraping bergantung pada struktur HTML halaman sumber. Jika struktur halaman berubah, kode scraping perlu disesuaikan.
- Proyek ini dibuat untuk tujuan pembelajaran dan analisis, bukan sebagai rekomendasi investasi.

## Rencana Pengembangan

- Menambahkan perusahaan lain untuk dianalisis.
- Menyimpan data hasil pembersihan ke berkas CSV.
- Menambahkan indikator teknikal seperti moving average.
- Menerbitkan dasbor sebagai aplikasi web (misalnya dengan Dash atau Streamlit).

## Lisensi

Tambahkan informasi lisensi di sini (misalnya MIT License).
