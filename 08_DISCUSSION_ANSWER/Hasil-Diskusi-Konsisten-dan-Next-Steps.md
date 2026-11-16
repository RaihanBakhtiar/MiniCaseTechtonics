# Hasil Diskusi yang Konsisten & Rencana Kerja Berikutnya
**MCC Techtonic 3.0 × Terang AI — Tim Semoga Kaya**
Disusun: 16 Nov 2026 · Deadline deck: 17 Nov 2026 · Top 5: 20 Nov · Final: 21 Nov

---

## 0. Cara membaca dokumen ini

Dokumen ini memuat hanya poin yang sudah **konsisten antar-bagian** pada versi terbaru di `08_DISCUSSION_ANSWER` (rantai dari *Problem Identification* kedua sampai *Conclusion*). Setiap poin diberi label dasar:

| Label | Arti | Seberapa bisa dipegang |
|---|---|---|
| **[L]** | Logika atau aritmetika, sudah diperiksa ulang | Tinggi |
| **[Q]** | Bersumber dari casebook/Q&A (dikutip di dokumen tim) | Tinggi setelah dicek ke PDF dan sheet Q&A resmi |
| **[S]** | Penilaian strategis tim | Sedang (argumen, bukan fakta) |
| **[A]** | Asumsi tanpa sumber | Rendah sampai diverifikasi |

**Batasan:** "konsisten" tidak sama dengan "terbukti benar". Fakta eksternal (fee Google Play, tarif AI, harga kompetitor, pasal UU PDP, angka pendaftar) belum diverifikasi dari sumber resmi oleh siapa pun. Bagian lama di awal file 08 (riset v1, Proposed Solution v1, memo, Kerangka Bisnis, Breakdown Diskusi, Implementation Plan pertama) dianggap **superseded**.

---

## 1. Diagnosis masalah

1. **Tiga masalah inti berakar pada musiman.** Akuisisi, aktivasi/retensi, dan konversi/monetisasi sama-sama dipengaruhi kebutuhan persiapan ujian yang berbatas waktu: pengguna berlangganan hanya selama masa persiapan, dan titik drop-off terbesar dipengaruhi musim ujian. **[Q]**
2. **Terang AI tidak mulai dari nol.** Aset awal: 10.000+ user web, komunitas (terutama 3T), kanal organik, pengalaman booth dan event. Kemitraan institusi (mis. IAI) tidak otomatis menjadi saluran distribusi B2C. **[Q]**
3. **Momen nilai pertama = tryout pertama.** Karena itu aktivasi didefinisikan sebagai *menyelesaikan diagnostic dan membuka hasilnya*, bukan install atau sign-up. **[Q + L]**
4. **Data internal kunci tidak tersedia:** konversi aktual, retensi D1/D7/D30, DAU/MAU, CAC, LTV, renewal, komposisi 10.000+ user web. Semuanya wajib berlabel [A] atau [E] di deck. **[Q]**

---

## 2. Strategi

5. **Urutan segmen: UTBK (beachhead) → LPDP (gelombang kedua) → CPNS (ekspansi).** **[S]**
   - Alasan: hanya UTBK yang punya basis volume untuk skala besar, jadwalnya tetap, dan paling dekat dengan misi 3T.
   - Syarat kritis: jika willingness-to-pay (WTP) UTBK terlalu rendah untuk menopang unit economics, arah bergeser ke LPDP-led.
   - Skor segmen 1–5 adalah hipotesis. Uji sensitivitas bobot menunjukkan peringkat bisa terbalik, sehingga pilihan segmen sebenarnya adalah pilihan "skala vs ekonomi per pengguna".
6. **Diferensiasi tunggal:** diagnostic → analisis performa → learning path personal → evaluasi progres. Bank soal, tryout, dan chatbot AI sudah ditawarkan kompetitor (Roboguru, MIPI.ai/Pegasus, Tanya AI), sehingga bukan pembeda. **[S]** (fitur kompetitor dari materi sekunder; harga belum terverifikasi)
7. **Free vs premium.** Prinsip: *free memberi bukti manfaat, premium memberi kedalaman dan tindak lanjut.* **[S + L]**
   - Diagnostic awal gratis penuh satu kali; premium membuka peta kelemahan detail, study plan adaptif, pembahasan AI personal, tryout lanjutan.
   - Momen paywall berurutan: setelah hasil diagnostic → saat kuota latihan habis → setelah tryout penuh pertama. Tidak ada paywall saat aplikasi pertama dibuka.
   - Paket: Free, Monthly (jangkar Rp25.000 dari casebook), Exam Pass sampai tanggal ujian. Harga selain Rp25.000 berstatus [E] (diuji lewat fake-door dan A/B).
   - Basic practice tetap gratis; reward gamifikasi membuka aktivitas tambahan, bukan membatasi latihan dasar.
8. **Tiga pilar:** Partnership-led Acquisition, AI-powered Personalized Learning, Gamified and Stage-based Engagement. **[S]**
9. **Pengguna 3T dipisah dari funnel komersial** (via kode partner/komunitas). Mereka boleh dihitung di target MAU tetapi dikeluarkan dari penyebut konversi, karena aksesnya memang gratis. **[Q + L]**

---

## 3. Metodologi keuangan

10. **CAC dan LTV harus pada basis yang sama:** CAC per paying user vs LTV per paying user. Membandingkan CAC per install dengan LTV per pembayar menggelembungkan rasio kira-kira sebesar 1/konversi. CAC per install tetap dilaporkan sebagai metrik operasional. **[L]** (poin paling kokoh)
11. **CAC fully-loaded:** ads, kreator, partnership, referral reward, event, tools, dan alokasi personel akuisisi. **[L]**
12. **Churn tidak konstan.** Dimodelkan per kohort dengan batas tanggal ujian. LTV = margin kontribusi bulanan × masa berbayar, dibatasi `min(1/churn, bulan menuju ujian)`. **[L]**
13. **Biaya AI per pengguna aktif adalah input eksplisit,** bukan nol, dan dipisah antara pengguna free dan paid. **[L]**
14. **Model terbalik:** hitung CAC maksimum yang masih layak (dari LTV dan konversi), lalu bandingkan dengan CAC realistis per kanal. **[L]**
15. **Scaling gate.** Anggaran tahap berikutnya dilepas hanya jika CAC, diagnostic completion, D7 retention, konversi, dan margin AI memenuhi syarat. Setiap evaluasi menghasilkan satu keputusan: *continue / optimize / stop / scale*. **[S]** (ambang angka belum ditetapkan, lihat bagian 6)

---

## 4. Angka yang aritmetikanya sudah diperiksa ulang

16. **Anggaran dasar Rp300,1 jt** **[L, input masih [A]]**
    - Subtotal Rp272,816 jt + kontingensi 10% = Rp300,0976 jt.
    - Alokasi kuartalan Rp63,91 / 71,72 / 79,09 / 85,378 jt menjumlah dengan benar.
    - Input tanpa sumber: gaji (Rp5,5 jt dan Rp8 jt per bulan) dan biaya cloud.
    - Anggaran ini adalah biaya **tambahan** (incremental); gaji tim existing dan pengembangan inti aplikasi tidak dihitung.
17. **Simulasi AI API** **[L, input [A]]**
    - 5 interaksi × Rp14,4 = Rp72 per pengguna AI aktif per bulan.
    - Total MAU-bulan pada lintasan 12 bulan = 2,771 juta.
    - Biaya tahunan: 10% → Rp19,95 jt; 30% → Rp59,85 jt; 50% → Rp99,76 jt; 100% → Rp199,51 jt.
    - Simulasi 30%: Rp272,816 jt + Rp59,854 jt = Rp332,67 jt; + kontingensi 10% = Rp365,94 jt.
    - Rp14,4 per interaksi belum bersumber (lihat poin 22).

---

## 5. Pengukuran

18. **MAU sebagai definisi operasional target:** pengguna unik dengan ≥1 aktivitas belajar bermakna dalam 30 hari. Pengguna website yang bermigrasi dihitung setelah aktif di aplikasi; deduplikasi Android/iOS wajib. Ini usulan tim, bukan definisi resmi perusahaan. **[Q + S]**
19. **North Star: Weekly Active Learner (WAL)** yang menyelesaikan ≥1 sesi belajar dengan penjelasan/evaluasi personal. **[S]**
20. **Rumus KPI** (activation, D7/D30 per kohort, konversi, CAC, LTV:CAC, payback, referral conversion, biaya AI per pengguna aktif) konsisten di Plan dan Impact. **[L]**

---

## 6. Belum konsisten: jangan dipakai di deck sebelum diselesaikan

| # | Masalah | Mengapa penting | Sumber |
|---|---|---|---|
| 21 | **Lintasan MAU vs kalender ujian.** Plan menaruh pengumuman SNBP di Month 4–6 dan "UTBK Peak Growth" di Month 7–9, dengan MAU naik monoton ke 1 juta di M12. Pola 2025/2026 di Research Log (R-02, R-03) menunjukkan ujian akhir April dan pengumuman akhir Mei. Jika M0 ≈ akhir 2026 **[A]**, puncak permintaan jatuh di sekitar M4–M5 dan M12 (≈ Des 2027) adalah lembah pasca-ujian | Bertentangan dengan masalah musiman yang tim sendiri tetapkan sebagai akar masalah | Plan §4–5; Research-Log |
| 22 | **Biaya AI:** Plan memakai Rp72/user/bulan (5 interaksi); Brainstorming memakai 15 interaksi dengan rentang Rp112–300. Rentang itu tidak cocok dengan inputnya sendiri: 35.000 token × $0,15–0,30 per 1M × Rp16.000 ≈ Rp84–168 | Mempengaruhi margin dan kuota free | Plan §7.3; Brainstorming Klaster C |
| 23 | **Target 1 juta MAU vs ukuran pasar.** SNBT 2025: 860.976 pendaftar; LPDP ≈ 79 ribu (rentang antar-sumber). Target melebihi seluruh pendaftar SNBT 2025. SAM/SOM belum dihitung. Opsi: definisikan sebagai kumulatif *active users* atau tampilkan 1 juta sebagai upside | Pertanyaan pertama juri | Riset §3.1.1, §3.2.1; Market template kosong |
| 24 | **Porsi organik vs berbayar.** Brainstorming mengusulkan 70/30, tetapi Plan tidak memuatnya. Biaya akuisisi eksplisit di Plan ≈ Rp63 jt (≈ Rp63 per MAU; ≈ Rp225 jika gaji dihitung). Jika 30% dari 1 juta pengguna dibeli, ads Rp30 jt hanya setara Rp100 per install | Feasibility 25% | Plan §7.2; Brainstorming Klaster B |
| 25 | **Proyeksi berangka belum ada.** Plan dan Impact hanya memuat rumus; ambang KPI dan gate ditunda "setelah baseline". Ilustrasi revenue 1/2/3% di Plan lama hanya snapshot satu bulan | Juri perlu melihat angka berlabel [A] dan logika pengaitnya | Plan §8.2; Impact §4 |
| 26 | **Growth engine cards kosong:** jumlah sekolah/mitra, volume per mitra, K-factor, mekanisme insentif | Dasar bottom-up angka install | `Strategy-Blueprint.md` |

---

## 7. Rencana kerja berikutnya

### P0: Hari ini (16 Nov)

**A. Keputusan tim (30 menit, semua)**
- [ ] Konfirmasi Implementation Plan kedua (Rp300,1 jt, SNBP–SNBT) sebagai versi final.
- [ ] Tetapkan satu asumsi biaya AI (poin 22) dan satu set skenario (downside/base/upside).
- [ ] Tetapkan definisi 1 juta: MAU atau kumulatif *active users*; cek PDF casebook soal "Play Store users" dan cakupan iOS.
- [ ] Catat semua keputusan di `Team-Context.md`; tandai bagian lama di file 08 sebagai *superseded* dan snapshot ke `99_ARCHIVE`.

**B. Raihan (monetisasi, keuangan, integrasi)**
- [ ] Bangun spreadsheet model dengan tab: Inputs (ID A-01..A-22, status V/B/A/E, sumber), Funnel bulanan terikat kalender, Cohort berbatas tanggal ujian, Unit Economics (CAC per paying user vs LTV per paying user), Scenarios, Checks, Reverse Model.
- [ ] Hitung revenue **kumulatif 12 bulan**, bukan snapshot satu bulan.
- [ ] Verifikasi dari sumber resmi: fee Google Play untuk langganan; apakah QRIS/e-wallet lewat Play Billing atau gateway; PPN pada Rp25.000; tarif API provider; benchmark gaji (UMK/UMP).
- [ ] **Selesai bila:** semua angka punya ID, status, sumber atau rumus, dan Checks lolos.

**C. Tio (riset)**
- [ ] Jadwal SNBP, UTBK, dan batch LPDP dari situs resmi. Jadwal 2027 belum rilis per 16 Nov (R-01), jadi pakai pola 2025/2026 berlabel [A].
- [ ] Hitung SAM/SOM dari statistik resmi dan catat sumber, tahun, dan caveat di Research Log.
- [ ] Verifikasi 3–4 harga kompetitor yang akan tampil di slide.
- [ ] Cek teks resmi UU PDP soal data anak (Brainstorming menyebut Pasal 25; perlu dicek ulang).
- [ ] Opsional: survei 4 pertanyaan (5–10 responden). Hasilnya hanya arah, bukan bukti.
- [ ] **Selesai bila:** semua statistik eksternal di deck punya baris di `Research-Log.md`.

**D. Habibi (growth dan produk)**
- [ ] Isi growth engine cards: jumlah mitra, volume per mitra, K-factor, biaya dan insentif kreator/ambassador, CTA, KPI, timing, risiko. Semua angka berlabel [A].
- [ ] Beri Raihan input volume per kanal dan porsi organik vs berbayar.
- [ ] Sinkronkan definisi aktivasi dan momen paywall dengan model.
- [ ] Bentuk lintasan MAU yang mengikuti kalender ujian (puncak, lembah, win-back).

### P1: Sebelum deck dikunci (17 Nov)
- [ ] Isi KPI tree dan gate dengan angka [A] yang diturunkan dari model.
- [ ] Isi roadmap dengan gate keluar per fase dan risk register berindikator dini.
- [ ] Susun deck 10 halaman konten (English, 16:9, PDF), dengan nama file `MCC_TECHTONICxTerangAI_TeamName`, mengikuti bobot: Solution & Strategy 40%, Feasibility & Implementation 25%, Research 20%, Deck Quality 10%, Executive Summary 5%.
- [ ] Pangkas ekosistem fitur (±30 fitur) menjadi satu alur diferensiasi dan satu segmen.
- [ ] Tinjauan skeptis ala juri (peran Claude di SOP): audit klaim dan sumber.

### P2: Kerapian repo
- [ ] Perbarui `Task-Tracker.md` dan `Deck-Outline.md`.
- [ ] Rapikan baris R-03 dan R-04 di Research Log (pipe penutup hilang).
- [ ] Gabungkan duplikat Financial-Model-Template dan `Kerangka Bisnis.md`.

---

## 8. Cek terakhir sebelum angka masuk deck

- [ ] Setiap angka punya ID, status [V]/[B]/[A]/[E], dan rencana validasi.
- [ ] Tidak ada placeholder `[X]` yang tersisa.
- [ ] CAC dan LTV pada basis yang sama.
- [ ] Tiga skenario tersaji, beserta porsi organik vs berbayar.
- [ ] Lintasan MAU konsisten dengan kalender ujian.
- [ ] Definisi "1 juta" konsisten di semua slide.
- [ ] Satu narasi, satu segmen prioritas, satu diferensiasi.
