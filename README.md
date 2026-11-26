# The Mind Before the Moment: Prototype Rancangan Eksperimen

Prototype web untuk rancangan eksperimen *next-in-line effect*: apakah menunggu giliran tampil (antisipasi performa) menurunkan kemampuan mengingat nama orang yang baru saja memperkenalkan diri?

Semuanya ada di satu file, `index.html`, tanpa instalasi apa pun.

## Desain singkat

- **Satu sesi:** 10 peserta yang belum saling kenal memperkenalkan diri bergiliran selama 30 detik di Zoom. Urutan tampil diundi acak.
- **Variabel bebas:** antisipasi performa.
  - Pra-tampil (urutan 6–10): mengingat 4 orang yang tampil tepat sebelum gilirannya (n−4 sampai n−1).
  - Pasca-tampil (urutan 1–5): mengingat urutan #6–#9 setelah selesai tampil.
- **Variabel terikat:** akurasi recall nama, yaitu proporsi nama yang tepat sesuai identitasnya.
- **H₁:** akurasi recall kelompok pra-tampil lebih rendah daripada pasca-tampil.

## Isi prototype

Prototype mengikuti 10 langkah sesi:

1. Rancangan dan peta antrean (klik peserta untuk melihat siapa yang harus ia ingat)
2. Penyaringan: usia 18–25, bahasa Inggris, belum saling kenal, tanpa gangguan pendengaran, skor SIAS
3. Pembukaan dan baseline: checklist pembukaan, Letter Memory Task (bisa dijalankan), STAI-6
4. Pembagian urutan secara acak
5. Presentasi dengan timer 30 detik dan pencatatan waktu otomatis
6. Recall bebas (4 slot per peserta, toleransi salah ketik)
7. Istirahat 30 detik
8. Recall berbantuan wajah (diadaptasi dari FNAME)
9. Wawancara, termasuk cek manipulasi dan cek kesadaran akan tes
10. Hasil: grafik, uji Mann–Whitney dan Welch t (satu arah), analisis per posisi (n−4 sampai n−1), perbandingan pada orang yang sama (#6–#9) untuk mengontrol recency, serta ekspor CSV/JSON

## Cara menjalankan

**Paling mudah:** buka `index.html` langsung di browser.

**Lewat localhost:** buka terminal di folder ini, lalu jalankan:

```bash
python3 -m http.server 8000   # Windows: py -m http.server 8000
```

Setelah itu buka http://localhost:8000.

## Catatan

- **Data simulasi:** tombol simulasi mengisi data dari asumsi untuk demo alur, bukan hasil penelitian. Halaman Hasil selalu memberi label pada data simulasi.
- **Wajah:** wajah peserta di prototype ini berupa ilustrasi. Di studi sebenarnya, pakai tangkapan kamera Zoom dengan izin peserta.
- **Penyimpanan:** data hanya tersimpan di browser yang dipakai. Gunakan tombol **Salin CSV** atau **Salin cadangan JSON** di langkah Hasil untuk menyimpan atau memindahkan data.
- **Batas SIAS:** nilai bawaan 34 bisa diubah di langkah Penyaringan.

## Rujukan

- Forrin et al. (2019). https://doi.org/10.1016/j.jml.2019.104044
- Brenner (1973). https://doi.org/10.1016/S0022-5371(73)80076-3
- Bond & Omar (1991). https://doi.org/10.1177/0146167291174012
- Treisman (1964). https://doi.org/10.1093/oxfordjournals.bmb.a070274
- STAI-6: Marteau & Bekker (1992). SIAS: Mattick & Clarke (1998).
