# D-04 — Benchmark Konversi Funnel Freemium

**Pertanyaan kritis:** Berapa % konversi rata-rata download → sign-up → aktif → bayar?
**PIC:** Habibi · **Dipakai di:** Slide 7, 8 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** download→bayar = `[B]` (dari ringkasan laporan RevenueCat dan Adapty); tahap lain (sign-up, aktivasi, D1/D7/D30) **tidak ditemukan** dan tetap `[A]`.

---

## 1. Jawaban singkat

| Metrik | Nilai | Tag | Catatan |
|---|---|---|---|
| Download→bayar, median semua aplikasi (D35) | ≈2,0% | `[B]` | RevenueCat 2026 |
| Download→bayar, model freemium (D35) | ≈2,1% (2025: 2,2%); P90 sekitar 7,9% | `[B]` | RevenueCat 2025–2026 |
| Download→bayar, hard paywall (D35) | ≈10,7% | `[B]` | tidak relevan untuk model freemium kita |
| Download→bayar, kategori Education | median 3,1%; P90 8,7% | `[B]` | Adapty, State of Paywalls 2026 |
| Trial→bayar, Education | median ≈33,2% | `[B]` | hanya bila ada trial; kita menguji gating kedalaman, bukan trial |
| Aplikasi berharga tinggi vs rendah | 2,7% vs 1,5% | `[B]` | RevenueCat 2025 via Airbridge; harga rendah cenderung konversi lebih rendah |
| Android vs iOS | Android sekitar sepertiga iOS | `[B]` lemah | dari pembacaan ringkasan RevenueCat 2026, cek laporan aslinya |

Definisi "D35" = install yang menghasilkan minimal satu langganan berbayar dalam 35 hari, dibagi seluruh install. Ini **bukan** konversi dari pengguna eligible.

## 2. Implikasi untuk skenario tim

Skenario di checklist Brainstorming: konservatif 1,5%, base 2,5%, agresif 3,5%.

- Base 2,5% sudah **di atas median freemium (≈2,1%)** dan hampir menyentuh median Education yang didominasi iOS (3,1%). Untuk Android Indonesia dengan harga Rp25.000 (≈US$1,38, jauh di bawah median bulanan Education global ≈US$8,38), batas atas yang masuk akal justru lebih rendah.
- Usulan (`[B]` + `[A]`): **konservatif 1,0% / base 2,0% / upside 3,1%.** Angka 3,1% memakai median Education sebagai batas atas, bukan P90.
- Nyatakan denominatornya di slide: "install→bayar D35" atau "eligible→bayar". Konversi dari pengguna eligible akan lebih tinggi daripada konversi dari install, jadi jangan mencampur dua angka itu. Keluarkan pengguna jalur 3T dari penyebut.

## 3. Yang tidak berhasil ditemukan

Untuk **sign-up rate, aktivasi, D1/D7/D30 retention** edtech Indonesia tidak ada angka yang bisa dikutip dari pass ini. Perlakukan sebagai hipotesis `[A]` dan isi dari closed beta (`[E]`). Jangan memasukkan "retensi D30 = X%" ke slide hanya karena ada artikel yang menyebut angka umum.

## 4. Peringatan kualitas sumber

Semua angka di atas berasal dari **artikel ringkasan** (Airbridge, Adapty, PricePush, dan sejenisnya) yang mengutip laporan RevenueCat. Angka bergeser antar tahun (hard paywall 12,1% pada 2025 menjadi 10,7% pada 2026). Sebelum masuk deck, buka laporan asli "State of Subscription Apps 2026" dan catat halaman serta definisinya.

## 5. Yang masih harus dilakukan

- [ ] Habibi membuka laporan RevenueCat 2026 (bagian Education) dan menyalin definisi persis.
- [ ] Ganti skenario 1,5/2,5/3,5% dengan 1,0/2,0/3,1% atau jelaskan mengapa angka tim lebih tinggi.
- [ ] Rancang event analytics yang mengukur aktivasi dan retensi sejak closed beta.

## 6. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-14 | Berapa konversi download→bayar aplikasi freemium? | Median freemium ≈2,1%; hard paywall ≈10,7%; semua aplikasi ≈2,0% (D35, RevenueCat 2026) [B] | Download-to-paid conversion rate benchmarks, thesocialoutline.com/blog/download-to-paid-conversion-rate-benchmarks | The Social Outline (ringkasan RevenueCat) | 2026 | 16 Nov 2026 | Sedang-rendah (sekunder); buka laporan RevenueCat asli | Habibi | Slide 7, 8 |
| R-15 | Berapa konversi kategori Education? | Download→bayar median 3,1%, P90 8,7% [B] | State of Paywalls 2026, adapty.io/blog/freemium-to-premium-conversion-techniques | Adapty | diperbarui 31 Jan 2026 | 16 Nov 2026 | Sedang; metodologi Adapty berbeda dari RevenueCat | Habibi | Slide 8 |
| R-16 | Apakah harga rendah menurunkan konversi? | Aplikasi berharga tinggi 2,7% vs rendah 1,5% (D35) [B] | Subscription App Pricing by Category 2026, airbridge.io/en/blog/subscription-app-pricing-by-category-2026-benchmark | Airbridge (mengutip RevenueCat 2025) | 2026 | 16 Nov 2026 | Sedang-rendah (sekunder); global, bukan Indonesia | Habibi | Slide 8 |
