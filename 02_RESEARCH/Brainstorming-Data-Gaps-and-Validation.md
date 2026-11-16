# Brainstorming & Backlog: Kekurangan Data dan Rencana Validasi
**MCC Techtonic 3.0 × Terang AI — Tim Semoga Kaya**  
*Dokumen Kerja Tim untuk Mengidentifikasi, Mencari, dan Memvalidasi Gap Data Sebelum Finalisasi Pitch Deck (10 Slide)*

---

## 1. Filosofi & Pedoman Validasi Data
Di kompetisi kasus bisnis, juri menilai integritas metodologi dan kelayakan (*Feasibility 25%*). Mengakui data yang belum ada (*honest assumption*) dengan rencana validasi terstruktur jauh lebih berbobot daripada mengarang angka (*fake accuracy*).

Setiap angka atau metrik yang akan masuk ke slide harus memiliki tag status:
* **[V] Validated:** Data resmi dari otoritas (SNPMB, LPDP, BKN, Q&A resmi Terang AI).
* **[B] Benchmark:** Data industri edtech/mobile app dari laporan riset berkutip (AppsFlyer, SensorTower, Google Play, data akademis).
* **[A] Assumption:** Estimasi terukur berbasis logika matematika tim (cantumkan rumusnya).
* **[E] Experiment:** Metrik yang harus diuji di tahap pilot/A-B testing.

---

## 2. Matriks Prioritas Gap Data (Master Action Board)

| ID | Item Data yang Kurang | Pertanyaan Kritis yang Harus Terjawab | Status Saat Ini | Metode / Rencana Sumber Validasi | PIC | Dipakai di Slide |
|---|---|---|---|---|---|---|
| **D-01** | Kalender Resmi UTBK 2026/2027 | Kapan tanggal pasti registrasi, simulasi, dan hari H ujian UTBK? | `[A]` Pola tahunan umum (Jan-Mei) | Web resmi SNPMB BPPP Kemendikdasmen | Tio | Slide 5, 6, 9 |
| **D-02** | Kalender Batch LPDP 2026/2027 | Tanggal pembukaan Tahap 1 & 2, jadwal TBS, dan wawancara? | `[A]` Dua batch per tahun | Web resmi Beasiswa LPDP Kemenkeu | Tio | Slide 5, 6, 9 |
| **D-03** | Benchmark CPI & CAC EdTech Indonesia | Berapa biaya akuisisi per install (CPI) dan CAC berbayar di Play Store Indonesia? | `[A]` Belum ada angka riil | Benchmark industri (AppsFlyer / Business of Apps / Statista) | Habibi | Slide 5, 8 |
| **D-04** | Benchmark Konversi Funnel Freemium | Berapa % konversi rata-rata: Download → Signup → Active → Paid di edtech lokal? | `[A]` Draf kasar di kerangka | Data agregat riset (Lenny's Newsletter, EdTech mobile app averages) | Habibi | Slide 7, 8 |
| **D-05** | Biaya Inferensi AI per User (COGS) | Berapa rupiah biaya API model (Gemini/Claude/OpenAI) untuk 1 pengguna aktif per bulan? | `[A]` Diasumsikan nol di draft awal | Perhitungan token: kuota chat/sesi × harga per 1M token | Raihan | Slide 7, 8 |
| **D-06** | Platform Fee & Pajak Bersih | Berapa potongan riil dari Google Play Billing, Payment Gateway, dan PPN? | `[A]` Belum dikurangkan dari Rp25.000 | Dokumentasi Google Play Console (15% service fee) + Midtrans/Xendit | Raihan | Slide 7, 8 |
| **D-07** | Willingness to Pay (WTP) & Packaging | Apakah siswa/mahasiswa lebih memilih Rp25rb/bulan atau Rp60rb/pass ujian? Siapa pembayarnya? | `[A]` Hanya mengacu pada casebook Rp25rb | Survei cepat (10-15 responden siswa SMA & pejuang LPDP) | Tio | Slide 3, 7 |
| **D-08** | Profil 10.000+ User Website | Berapa porsi UTBK vs LPDP? Berapa retention rate web-nya? | `[A]` Dianggap blackbox 10k | Catatan Q&A case + asumsi konservatif migrasi (15-25%) | Habibi | Slide 2, 5 |
| **D-09** | Estimasi Anggaran Pemasaran Bootstrapped | Berapa plafon anggaran rasional startup tanpa pendanaan VC untuk 6-12 bulan? | `[A]` Fleksibel sesuai Q&A | Rekayasa finansial bertahap (gated budget Rp150M - Rp350M) | Raihan | Slide 9 |
| **D-10** | Kepatuhan Regulasi Pengguna <18 Tahun | Apa syarat legal menampung data siswa SMA kelas 11-12 menurut UU PDP? | `[A]` Belum dipetakan | Teks UU No. 27/2022 tentang Perlindungan Data Pribadi (Pasal 25) | Raihan | Slide 10 |

---

## 3. Deep-Dive Brainstorming per Klaster

### Klaster A: Kalender & Musiman (Market Seasonality)
* **Gap:** Seasonality adalah alasan drop-off nomor 1 di Terang AI. Jika timeline roadmap meleset 1 bulan saja dari tanggal ujian, akuisisi dan retensi akan anjlok.
* **Pertanyaan Eksplorasi:**
  1. Peluncuran aplikasi akhir 2026: apakah bertepatan dengan masa siswa mulai mencari tryout UTBK?
  2. Kapan waktu jeda (*valley of death*) di mana retensi UTBK turun drastis (Juni-Agustus)? Fitur apa yang bisa menahan mereka (misal: seleksi mandiri PTN atau beralih ke persiapan mahasiswa baru)?
  3. Apakah LPDP Tahap 2 (biasanya Juni–Agustus) bisa menjadi *hedge* (penyeimbang) saat musim UTBK selesai?
* **Sumber yang harus dicek:**
  * Portal SNPMB BPPP: `https://snpmb.bppp.kemdikbud.go.id/`
  * Portal LPDP Kemenkeu: `https://lpdp.kemenkeu.go.id/`

### Klaster B: Akuisisi & Efisiensi Kanal (Acquisition & Unit CAC)
* **Gap:** Target 1 juta install tidak mungkin dicapai dengan iklan berbayar penuh karena Terang AI *bootstrapped* (1 juta install × Rp5.000 CPI = Rp5 Miliar modal yang tidak dimiliki).
* **Pertanyaan Eksplorasi:**
  1. Berapa rasio pertumbuhan Organik vs Berbayar yang kredibel? (Usulan: 70% Organik/Kemitraan/Referral, 30% Paid Ads).
  2. Berapa target *K-factor* (koefisien viralitas) dari sistem referral "belajar bareng / gift kartu tryout"?
  3. Bagaimana struktur insentif untuk *Campus Ambassador* (mahasiswa PTN / awardee LPDP) agar hemat kas? (Misal: sertifikat + akses pro gratis + rev-share per referal).
* **Benchmark yang harus dicari:**
  * Rata-rata organic-to-paid ratio di aplikasi edukasi berkembang.
  * Rasio konversi listing Play Store (*App Store Optimization / ASO conversion rate*).

### Klaster C: Monetisasi, Biaya AI, & Unit Economics
* **Gap:** Perhitungan LTV:CAC di template awal rawan salah karena mencampur aduk pembagi (*denominator inconsistency*). Selain itu, biaya API AI belum pernah dihitung.
* **Pertanyaan Eksplorasi & Rumus:**
  1. **Kalkulasi Biaya AI (COGS per User):**
     * Input: Asumsikan 1 user aktif melakukan 15 interaksi evaluasi/bulan.
     * Token per interaksi = 1.500 token prompt + 800 token completion = 2.300 token.
     * Total token/bulan/user = ~35.000 token.
     * Jika menggunakan model hemat berkecepatan tinggi (Gemini 1.5 Flash / Claude Haiku) dengan tarif ~$0.15 - $0.30 per 1M token:
       $$\text{Biaya AI} \approx 0.035 \times \$0.20 \times \text{Rp16.000} \approx \text{Rp112 - Rp300 per user per bulan}.$$
     * *Kesimpulan awal:* Gross margin software tetap sangat aman (>85%), asalkan kuota di tier gratis dibatasi.
  2. **Net Revenue per User:**
     * Harga langganan: Rp25.000
     * Potongan Google Play (15% di tier pertama <$1M): -Rp3.750
     * Biaya Payment Gateway (QRIS/E-Wallet 0.7% - 1.5%): -Rp350
     * Pendapatan bersih: ~Rp20.900/bulan/user berbayar.
  3. **Struktur Paket "Pass Ujian" vs "Bulanan":**
     * Apakah perlu dibuat "UTBK Sprint Pass" (misal Rp69.000 flat untuk 3-4 bulan sampai hari H)? Ini mengamankan cash upfront dan mengatasi *monthly churn*.

### Klaster D: Kredibilitas AI & Regulasi
* **Gap:** Juri dan calon user akan bertanya: *"Kenapa saya harus bayar Rp25.000 kalau ChatGPT/Claude gratis bisa dipakai nanya soal?"*
* **Pertanyaan Eksplorasi:**
  1. Apa "Moat" (parit pertahanan) Terang AI dibanding LLM generik?
     * *Jawaban:* LLM generik tidak punya sistem tryout adaptif dengan timer riil, tidak punya kalibrasi skor IRT (*Item Response Theory*) standar SNPMB, dan tidak memiliki riwayat kelemahan longitudinal.
  2. **UU PDP (Perlindungan Data Pribadi):**
     * Siswa usia 16-17 tahun memerlukan persetujuan orang tua/wali (*parental consent*) untuk pemrosesan data analitik performa. Bagaimana UX onboarding Terang AI menyiasatinya tanpa menambah friksi?

---

## 4. Panduan Guerilla Research (Survei Cepat 12 Jam)
Jika tim memiliki akses ke adik kelas, saudara, atau teman yang sedang pejuang UTBK / LPDP, ajukan 4 pertanyaan cepat ini untuk memperkuat data kualitatif di slide:

```text
Draft Pertanyaan Validasi Cepat:
1. "Untuk persiapan tes (UTBK/LPDP), sekarang kamu paling sering latihan pakai platform apa? (Sebutkan gratis atau bayar)"
2. "Berapa uang yang menurutmu wajar dikeluarkan per bulan untuk aplikasi latihan soal berbasis AI yang bisa memberi tahu kelemahan spesifikmu? (a. <Rp20rb, b. Rp20-50rb, c. >Rp50rb)"
3. "Kalau langganan, kamu lebih suka bayar per bulan (Rp25rb) atau langsung 1 paket sampai hari H ujian (misal Rp60rb sekali bayar)?"
4. "Sebagai pelajar/fresh grad, kamu bayar sendiri (pakai QRIS/ShopeePay) atau minta orang tua?"
```
*Hasil 5–10 jawaban singkat ini dapat dimasukkan ke slide riset sebagai "Primary Guerilla Survey (n=X) Insights" untuk memvalidasi pilihan fitur dan metode pembayaran.*

---

## 5. Checklist Validasi Sebelum Angka Masuk ke Slide Deck

- [ ] **Tidak ada sel kosong `[X]`:** Semua placeholder di `Deck-Outline.md` dan template finansial sudah terisi angka definitif.
- [ ] **Denominator Konsisten:** CAC dihitung per paying user ($Spend / New Paid Users$) saat dibandingkan dengan LTV per paying user ($ARPPU \times Margin \times Lifetime$).
- [ ] **Skenario 3 Jalur:** Slide finansial menyajikan skenario *Conservative* (misal 500k install, 1.5% konversi), *Base* (800k install, 2.5% konversi), dan *Aggressive/Upside* (1M install, 3.5% konversi).
- [ ] **Traceable Citation:** Sumber data eksternal (SNBT, LPDP, UU PDP, Benchmark) tercatat rapi di `02_RESEARCH/Research-Log.md`.
- [ ] **Gated Budget:** Pengeluaran biaya pemasaran dipatok bertahap per fase (M-2 s.d M0, M0-M2, M2-M6, M6-M12), dengan *exit gate criteria* yang terukur.
