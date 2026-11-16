# D-08 — Profil 10.000+ User Web & Ukuran Pasar

**Pertanyaan kritis:** Berapa porsi UTBK vs LPDP, berapa retention web, dan seberapa besar target 1 juta dibanding pasar?
**PIC:** Habibi · **Dipakai di:** Slide 2, 5 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** data internal web **tidak bisa dicari di luar**; dijawab dengan daftar permintaan data + asumsi konservatif `[L]`. Ukuran pasar UTBK/SNBT 2026 = `[V]` (data panitia, dikutip media).

---

## 1. Jawaban singkat

1. **Profil user web tetap blackbox sampai Terang AI memberi data.** Yang bisa dilakukan sekarang: ajukan permintaan data yang spesifik (bagian 4) lewat kanal Q&A, dan nyatakan asumsi konservatif.
2. **Kontribusi web ke target 1 juta sangat kecil.** Dengan migrasi 15–25% (asumsi tim, `[A]`), 10.000 user web menjadi **1.500–2.500 install, yaitu 0,15–0,25% dari 1 juta** `[L]`. Jadikan mereka aset untuk seeding (beta tertutup, testimoni, kode referral awal, bukti diagnostic), bukan sumber volume.
3. **Target 1 juta lebih besar dari seluruh pendaftar SNBT 2026.** Pendaftar UTBK-SNBT 2026 = **871.496**; 1 juta = **115%** dari angka itu `[L]` dari `[V]`. Satu segmen saja tidak cukup, bahkan jika seluruh pendaftar memasang aplikasi. Ini menjawab poin 23 di Hasil Diskusi.
4. **Implikasi:** tentukan definisi 1 juta (install kumulatif lintas segmen dan musim, atau MAU), dan sajikan base di bawah 1 juta dengan 1 juta sebagai upside, sesuai saran tim di Kerangka Bisnis.

## 2. Data pasar yang terverifikasi (`[V]`, dikutip dari paparan resmi SNPMB lewat media)

| Metrik | Nilai |
|---|---:|
| Pendaftar UTBK-SNBT 2026 | **871.496** |
| Peserta yang hadir | 846.518 |
| Daya tampung SNBT 2026 | 286.864 |
| Diterima SNBT 2026 | 256.369 (29,42% dari pendaftar) |
| **Tidak diterima** | **≈615.127** (871.496 − 256.369, `[L]`) |
| Pendaftar yang berstatus KIP Kuliah | 251.991 |
| Pendaftar UTBK-SNBT 2025 | 860.976 |
| Pendaftar SNBP 2026 | 806.242; lulus 178.981 |

Fakta tambahan: peserta yang lulus SNBP 2026 **tidak boleh** ikut UTBK-SNBT 2026, 2027, dan 2028, serta jalur mandiri 2026. Mereka bukan lagi calon pengguna UTBK pada tahun-tahun itu.

**Bacaan untuk strategi:** sekitar 615 ribu peserta tidak diterima pada 2026. Sebagian akan mengulang (gap year) atau pindah ke jalur mandiri. Ini bisa menjadi sub-segmen pasca-pengumuman (kebutuhan UTBK berlanjut) yang meratakan musim, tetapi persentase yang mengulang **belum diketahui**. Jangan menulis angka itu tanpa sumber.

## 3. Kerangka SAM/SOM (isi oleh Tio setelah input lengkap)

| Lapisan | Rumus usulan | Input yang sudah ada | Input yang belum ada |
|---|---|---|---|
| TAM (UTBK) | pendaftar UTBK-SNBT tahunan | 871.496 (2026) `[V]` | proyeksi 2027 |
| SAM | TAM × pemilik smartphone Android × akses internet cukup | – | porsi Android, porsi akses internet |
| SOM (tahun 1) | SAM × pangsa realistis dari kanal yang diuji | – | hasil pilot kanal (D-03) |

Segmen lain (LPDP, CPNS, fresh graduate) belum punya angka terverifikasi di pass ini; jangan diisi sebelum ada baris Research-Log.

## 4. Daftar permintaan data ke Terang AI (kirim lewat Q&A)

1. Jumlah user web per bulan pendaftaran (Okt 2024–sekarang) dan jumlah user **aktif** 30 hari terakhir.
2. Komposisi tujuan ujian (UTBK / LPDP / CPNS / lainnya) dan tingkat (SMA/SMK, kuliah, kerja).
3. Aktivitas: persen yang menyelesaikan minimal satu tryout atau diagnostic; rata-rata sesi per minggu.
4. Retensi web (hari ke-7, ke-30) per kohort, jika ada.
5. Apakah pernah ada pembayaran atau uji harga di web?
6. Porsi pengguna 3T dan yang diverifikasi komunitas.
7. Pengguna di perangkat Android vs lainnya.
8. Apakah email/WhatsApp user boleh dipakai untuk mengajak migrasi ke aplikasi (dasar persetujuan menurut UU PDP, lihat D-10)?

Bila Terang AI tidak menjawab, tulis di deck: "Web cohort composition not disclosed; migration modelled at 15–25% [A], contribution ≤0,25% of target."

## 5. Asumsi konservatif untuk model (`[A]`)

| Parameter | Konservatif | Base | Upside |
|---|---:|---:|---:|
| Migrasi web → aplikasi | 10% | 20% | 25% |
| Install dari web | 1.000 | 2.000 | 2.500 |
| Porsi dari target 1 juta | 0,10% | 0,20% | 0,25% |

(15–25% tim; baris konservatif 10% ditambahkan sebagai stress test.)

## 6. Yang masih harus dilakukan

- [ ] Habibi mengirim daftar permintaan data bagian 4 ke kanal Q&A hari ini.
- [ ] Tio memutuskan definisi 1 juta bersama tim dan menulisnya di Team-Context (keputusan tim, poin P0 Hasil Diskusi).
- [ ] Tio menghitung SAM/SOM dengan rumus bagian 3 setelah porsi Android dan akses internet ditemukan dari sumber resmi (BPS/APJII), dicatat di Research-Log.

## 7. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-27 | Berapa pendaftar dan diterima SNBT 2026? | Pendaftar 871.496; diterima 256.369 (29,42%); daya tampung 286.864 [V] | Hanya 29,42 Persen dari Total Pendaftar..., jawapos.com/pendidikan/2605250285/... | JawaPos (mengutip ketua panitia SNPMB) | 25 Mei 2026 | 16 Nov 2026 | Sedang-tinggi; sumber primer = paparan konferensi pers SNPMB | Tio | Slide 2, 3 |
| R-28 | Rincian hasil SNBT 2026 (hadir, KIP-K) | Hadir 846.518; KIP Kuliah 251.991 [V] | Paparan Konferensi Pers Hasil SNBT 2026 (salinan), utbkcak.com/wp-content/uploads/2026/05/Paparan-Konferensi-Pers-Hasil-SNBT-2026.pdf | SNPMB (salinan situs pihak ketiga) | Mei 2026 | 16 Nov 2026 | Sedang (salinan); ambil dari situs SNPMB | Tio | Slide 2, 3 |
| R-29 | Pendaftar SNBT 2025 | 860.976 [V] | Registrasi UTBK SNBT 2026 Dimulai 25 Maret Besok, rri.co.id/nasional/2279868/... | RRI | Mar 2026 | 16 Nov 2026 | Sedang-tinggi | Tio | Slide 2 |
| R-30 | Siapa yang dilarang ikut UTBK? | Lulus SNBP 2026 tidak boleh ikut UTBK 2026, 2027, 2028 dan mandiri 2026 [V] | Panitia Umumkan Hasil SNBP 2026, antaranews.com/berita/5502574/... | ANTARA | 31 Mar 2026 | 16 Nov 2026 | Sedang-tinggi | Tio | Slide 3 |
