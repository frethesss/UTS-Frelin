# UTS Sistem Rekomendasi - Graph-Based & Collaborative Filtering

Repository ini berisi penyelesaian Tugas UTS Mata Kuliah Sistem Rekomendasi. Proyek ini mencakup implementasi algoritma Collaborative Filtering berbasis graf menggunakan Neo4j, Python, serta evaluasi metrik rekomendasi.

## Isi Repository
- LKM_UTS_Sistem_Rekomendasi.ipynb : Notebook utama yang berisi seluruh kode Python (Soal 3-8 & Evaluasi).
- graph_before.png : Visualisasi graf kondisi SEBELUM enrichment relasi :SIMILAR.
- graph_after.png : Visualisasi graf kondisi SESUDAH enrichment relasi :SIMILAR.
- Laporan_UTS.pdf : Dokumen laporan hasil analisis dan jawaban UTS.

## Ringkasan Metode & Algoritma
1. Bipartite Graph & Item-based VSM:
   - Mengimpor data interaksi P1 (1 Juni - 10 Agustus 2015) ke Neo4j menggunakan optimasi UNWIND & FOREACH.
   - Menghitung Cosine Similarity antar-item menggunakan Sparse CSR Matrix.
   - Menginjeksi relasi :SIMILAR ke dalam Neo4j untuk memperkaya jaringan graf item.
2. User-based KNN Collaborative Filtering:
   - Mengambil target pengguna acak terkontrol (Seed 42).
   - Menghasilkan daftar Top-5 rekomendasi produk berbasis pengguna mirip.

## Hasil Evaluasi Metrik
- Target User ID : 898471
- Ground Truth Item : 264706
- Top-3 Item Diiklankan : 4, 466867, 466864
- Hit@5 : 0
- NDCG@5 : 0.0000 (Kondisi normal akibat kelangkaan data/cold-start pada user target)

## Teknologi yang Digunakan
- Python (Pandas, NumPy, Scipy, Scikit-Learn, NetworkX)
- Neo4j Database & Cypher Query Language
- Jupyter Notebook
