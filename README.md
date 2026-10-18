# UTS Graf Sains Data — RetailRocket dan Neo4j

Notebook untuk mengolah dataset interaksi RetailRocket, membangun graf interaksi pada Neo4j, menganalisis kemiripan pengguna/item, dan mencoba rekomendasi berbasis K-Nearest Neighbors (KNN).

## Isi repository

- `UTS_Graf_Sains_Data_RetailRocket_Neo4j.ipynb` — notebook utama beserta kode, keluaran, dan penjelasan.
- `data/events.csv` — dataset interaksi utama.
- `data/events_P1_training.csv` — data periode P1 untuk pembentukan model/graf.
- `data/events_P2_testing.csv` — data periode P2 untuk evaluasi.
- `requirements.txt` — dependensi Python.

> Pastikan tiga file CSV berada di folder `data/` pada direktori yang sama dengan notebook. Jika file P1 dan P2 dibuat dari notebook, jalankan sel pemuatan dan pembagian periode terlebih dahulu. Jika file tersebut sudah tersedia, periksa nama dan lokasinya sebelum menjalankan notebook.

## Persiapan

1. Instal Python 3.10 atau lebih baru dan Jupyter Notebook/JupyterLab.
2. Instal dependensi:

   ```bash
   pip install -r requirements.txt
   ```

3. Jalankan Neo4j Desktop atau Neo4j Server dan pastikan database yang digunakan aktif.
4. Buka notebook di Jupyter dan jalankan sel secara berurutan.

## Konfigurasi Neo4j

Notebook menggunakan konfigurasi default `bolt://localhost:7687`, username `neo4j`, dan database `neo4j`. Atur kredensial sesuai instalasi lokal sebelum menjalankan sel koneksi. Lebih aman menyimpan kata sandi melalui environment variable daripada menuliskannya di notebook:

- `NEO4J_URI`
- `NEO4J_USER`
- `NEO4J_PASSWORD`
- `NEO4J_DATABASE`

Jangan mengunggah kata sandi asli atau kredensial pribadi ke repository publik.

## Catatan penting

- Beberapa sel membangun ulang graf dan dapat menghapus node/relasi yang sudah ada pada database terpilih. Periksa query sebelum menjalankan ulang.
- Hasil rekomendasi dan metrik evaluasi pada notebook bergantung pada data dan pengguna target yang dipilih. Evaluasi satu pengguna tidak mewakili kinerja keseluruhan sistem rekomendasi.
- Jika GitHub menolak file CSV karena ukuran, jangan mengganti atau memotong dataset tanpa keterangan. Cantumkan sumber dataset dan gunakan metode penyimpanan yang sesuai dengan batas ukuran GitHub.
