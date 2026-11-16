# D-03 — Benchmark CPI & CAC EdTech Indonesia

**Pertanyaan kritis:** Berapa biaya akuisisi per install (CPI) dan CAC berbayar di Play Store Indonesia?
**PIC:** Habibi · **Dipakai di:** Slide 5, 8 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** tidak ada angka publik yang andal untuk edtech Indonesia. Pakai rentang `[A]` + satu batas `[L]` dari model terbalik. Pilot (`[E]`) yang menggantikannya.

---

## 1. Jawaban singkat

1. **Angka CPI spesifik edtech Indonesia tidak ditemukan** di sumber publik yang bisa dipertanggungjawabkan. Jangan menulis "benchmark CPI edtech Indonesia = Rp X" di deck.
2. **Yang ada hanya patokan kasar:**
   - Singular (laporan Q2 2026): CPI Android global naik 15,1% menjadi **US$0,76**. Dengan kurs Rp18.100 (lihat D-06/D-09) itu sekitar **Rp13.800**. `[B]`, global, lintas vertikal.
   - Satu laporan CPI (Mapendo) menyebut Indonesia masuk kelompok "Tier 2 East" dengan volume install besar pada CPI relatif murah. Kualitatif saja.
   - Angka "CPI edukasi" dari alat Facebook Ads (puluhan dolar, sangat fluktuatif) **tidak representatif**. Jangan dipakai.
3. **Rp5.000 per install (≈US$0,28) di dokumen tim berstatus `[A]`.** Masuk akal sebagai batas bawah, tetapi tidak ada sumber. Untuk skenario, pakai rentang **Rp3.000 / Rp8.000 / Rp15.000** (low/base/high), semuanya `[A]`.
4. **Temuan terpenting bukan angka CPI-nya, tetapi apa yang bisa ditanggung model** (bagian 2).

## 2. Model terbalik: berapa CPI maksimum yang layak? (`[L]`, input `[A]`)

Input: pendapatan bersih per pembayar ≈ Rp19.144 (D-06), biaya AI Rp367 (D-05, skenario verbose), masa berbayar rata-rata 3 bulan `[A]`.

- LTV per pembayar ≈ (19.144 − 367) × 3 ≈ **Rp56.300**
- CAC maksimum per pembayar = LTV ÷ target LTV:CAC
- CPI maksimum per install = CAC maksimum × konversi install→bayar

| Konversi install→bayar | CPI maks. (LTV:CAC ≥ 1) | CPI maks. (LTV:CAC ≥ 3) |
|---|---:|---:|
| 1,0% | Rp563 | Rp188 |
| 1,5% | Rp845 | Rp282 |
| 2,0% | Rp1.127 | Rp376 |
| 2,5% | Rp1.408 | Rp469 |

**Bacaan:** pada harga Rp25.000/bulan dan masa berbayar sekitar 3 bulan, install berbayar hanya impas bila CPI sekitar Rp1.100 ke bawah. Pada CPI Rp5.000 dan konversi 2%, CAC per pembayar = Rp250.000, sekitar 4,4 kali LTV.

**Porsi berbayar maksimum** (dihitung dari konversi 2% dan LTV Rp56.300):

| CPI paid | Maks. porsi paid (impas, 1:1) | Maks. porsi paid (3:1) |
|---|---:|---:|
| Rp2.000 | 56% | 19% |
| Rp5.000 | 22,5% | 7,5% |
| Rp10.000 | 11% | 4% |

**Implikasi:** usulan **70% organik / 30% berbayar** di Brainstorming Klaster B tidak didukung oleh unit economics pada harga Rp25.000. Porsi organik/kemitraan/referral yang konsisten dengan model adalah **sekitar 90–97%**. Dua jalan keluar yang jujur:
- naikkan LTV (paket pass Rp60–99 ribu untuk 3–4 bulan, kuota pembayar grup), atau
- turunkan target dengan menyajikan 1 juta sebagai upside, bukan base (lihat D-08).

Batas model: masa berbayar 3 bulan, konversi pembayar yang sama untuk user berbayar maupun organik, dan margin dari D-05/D-06. Ubah salah satu, hasilnya bergeser. Tabel ini adalah alat uji, bukan prediksi.

## 3. Rencana pilot pengganti angka (`[E]`, level L4)

- 3–4 kanal, masing-masing Rp2–3 juta, 7 hari, tautan atribusi berbeda (kreator, Meta/TikTok ads, kampus/komunitas, referral).
- Ukur per kanal: CPI, sign-up, aktivasi (diagnostic selesai + hasil dibuka), D7, dan klik fake-door paywall.
- Aturan keputusan (`[A]`): hentikan kanal yang CAC per pembayar yang diproyeksikan melebihi LTV; pertahankan kanal yang CPI-nya di bawah batas tabel bagian 2.

## 4. Yang masih harus dilakukan

- [ ] Habibi meminta penawaran kreator mikro dan kampus untuk 3 kota (harga per konten, bukan per install).
- [ ] Ganti "Rp5.000" di Brainstorming dengan rentang di atas.
- [ ] Update Klaster B: porsi organik sesuai bagian 2 atau definisikan ulang target.

## 5. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-12 | Berapa CPI Android global terbaru? | CPI Android naik 15,1% ke US$0,76 pada Q1 2026 [B] | Singular Quarterly Report 2026 Q2, singular.net/quarterly-report-2026-q2/ | Singular | Q2 2026 | 16 Nov 2026 | Sedang; global, lintas vertikal, bukan edtech Indonesia | Habibi | Slide 5, 8 |
| R-13 | Apakah ada CPI edtech Indonesia? | Tidak ditemukan sumber publik andal; data alat Facebook Ads untuk edukasi sangat tidak stabil [A] | superads.ai/facebook-ads-costs/cost-per-app-install/education | Superads | 2025–2026 | 16 Nov 2026 | Rendah; jangan dikutip di deck | Habibi | catatan internal |
