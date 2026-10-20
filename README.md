# UTS Sistem Rekomendasi - Item-based Collaborative Filtering & User-based KNN

Repository ini berisi penyelesaian LKM UTS Mata Kuliah Sistem Rekomendasi. Proyek ini mencakup implementasi algoritma Collaborative Filtering, integrasi dengan Database Graf Neo4j, serta evaluasi metrik rekomendasi.

## Isi Repository
- LKM_UTS_Sistem_Rekomendasi.ipynb : Notebook utama yang berisi seluruh kode Python (Soal 4-8 & 2.2 Analytics).
- graph_before.png : Visualisasi graf kondisi SEBELUM enrichment relasi :SIMILAR.
- graph_after.png : Visualisasi graf kondisi SESUDAH enrichment relasi :SIMILAR.
- Laporan_UTS.pdf : Dokumen laporan hasil analisis dan jawaban UTS.

## Ringkasan Metode & Algoritma
1. Item-based Collaborative Filtering:
   - Menghitung Cosine Similarity antar-item menggunakan Sparse CSR Matrix.
   - Menginjeksi relasi :SIMILAR ke dalam Neo4j untuk menghubungkan produk-produk yang memiliki kemiripan tinggi.
2. User-based KNN (k=5):
   - Mengambil target pengguna acak terkontrol (seed 42).
   - Memilih 5 tetangga terdekat untuk menghasilkan daftar Top-5 rekomendasi produk.

## Hasil Evaluasi (2.2 Analytics)
- Target User ID : 1263291
- Ground Truth Item : 107042
- Top-3 Item Diiklankan : 257040, 107042, 415174
- Hit@5 : 1
- NDCG@5 : 0.6309 (Item tersembunyi berhasil ditemukan pada peringkat ke-2)

## Teknologi yang Digunakan
- Python (Pandas, NumPy, Scipy, Scikit-Learn, NetworkX)
- Neo4j Database & Cypher Query Language
- Jupyter Notebook
