# The Mind Before the Moment: Prototype Rancangan Eksperimen

Prototype web untuk rancangan eksperimen *next-in-line effect*: apakah menunggu giliran tampil (antisipasi performa) menurunkan kemampuan mengingat nama orang yang baru saja memperkenalkan diri?

Semuanya ada di satu file, `index.html`, tanpa instalasi apa pun. Tampilannya menyesuaikan laptop dan HP.

## Desain singkat

- **Satu sesi:** 10 peserta yang belum saling kenal memperkenalkan diri secara tatap muka, bergiliran sekitar 30 detik. Urutan tampil diundi acak.
- **Variabel bebas:** antisipasi performa.
  - Pra-tampil (urutan 5–10): mengingat 4 orang yang tampil tepat sebelum gilirannya (n−4 sampai n−1).
  - Pasca-tampil (urutan 1–4): mengingat 4 orang yang tampil tepat setelah mereka (n+1 sampai n+4).
- **Variabel terikat:** akurasi recall nama, yaitu proporsi nama yang tepat sesuai identitasnya.
- **H₁:** akurasi recall kelompok pra-tampil lebih rendah daripada pasca-tampil.

## Isi prototype

**Penjelasan:** 12 adegan animasi, mulai dari pertanyaan pembuka, teori (next-in-line effect, antisipasi performa, teori atenuasi), hipotesis, desain, partisipan, alat ukur, sampai prosedur.

**Simulasi:** 6 langkah satu sesi.

1. Peserta: penyaringan (usia 18–25, bahasa Inggris, belum saling kenal, pendengaran baik, skor SIAS) dan Letter Memory Task
2. Pembukaan: checklist sesi tatap muka dan pengundian urutan tampil
3. Presentasi: timer ±30 detik per peserta
4. Tes ingatan: 4 nama target per peserta, dengan toleransi salah ketik
5. Wawancara: panduan pertanyaan dan cek kesadaran akan tes
6. Hasil: grafik, uji Mann–Whitney dan Welch t (satu arah), analisis per posisi, cek recency, dan ekspor CSV

## Cara menjalankan

**Paling mudah:** buka `index.html` langsung di browser.

**Lewat localhost:** buka terminal di folder ini, lalu jalankan:

```bash
npm run dev   # atau: python3 -m http.server 8081
```

Setelah itu buka http://localhost:8081.

## Catatan

- **Data simulasi:** tombol simulasi mengisi data dari asumsi untuk demo alur, bukan hasil penelitian. Halaman Hasil selalu memberi label pada data simulasi.
- **Wajah:** wajah peserta di prototype ini berupa ilustrasi.
- **Penyimpanan:** data hanya tersimpan di browser yang dipakai. Gunakan tombol **Salin CSV** di langkah Hasil untuk menyimpan data.
- **Batas SIAS:** nilai bawaan 34 bisa diubah di langkah Peserta.

## Rujukan

- Forrin et al. (2019). https://doi.org/10.1016/j.jml.2019.104050
- Brenner (1973). https://doi.org/10.1016/S0022-5371(73)80076-3
- Bond & Omar (1991). https://doi.org/10.1177/0146167291174012
- Treisman (1964). https://doi.org/10.1093/oxfordjournals.bmb.a070274
- SIAS: Mattick & Clarke (1998).
