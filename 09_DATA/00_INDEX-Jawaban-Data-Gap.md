# Indeks Jawaban Gap Data — MCC Techtonic 3.0 × Terang AI (Tim Semoga Kaya)

**Dibuat:** 16 Nov 2026 · **Deadline deck:** 17 Nov 2026
**Acuan:** `02_RESEARCH/Brainstorming-Data-Gaps-and-Validation.md` (D-01 sampai D-10) dan butir "belum konsisten" di `08_DISCUSSION_ANSWER/Hasil-Diskusi-Konsisten-dan-Next-Steps.md`.
**Cara pakai:** satu file per gap. Setiap file memuat jawaban singkat, tabel, caveat, tugas lanjutan, dan baris `Research-Log` siap tempel (ID R-05 s.d. R-36; sesuaikan bila ada ID yang bentrok).

---

## 1. Ringkasan status

| ID | Gap | Hasil | Tag | Masih terbuka | PIC |
|---|---|---|---|---|---|
| D-01 | Kalender UTBK/SNBT | 2027 belum rilis (rilis tahun lalu 29–30 Des); pola 2025–2026 jelas; ada situs yang salah melabeli "resmi" | 2026 `[V]`, 2027 `[A]` | tangkapan layar SNPMB bertanggal | Tio |
| D-02 | Kalender LPDP | Tahap 2 2026 terverifikasi dari laman resmi; 2027 belum diumumkan | `[V]` / `[A]` | konfirmasi Tahap 1 dan struktur program | Tio |
| D-03 | CPI & CAC | tidak ada angka publik edtech Indonesia; model terbalik menunjukkan iklan berbayar tidak layak di Rp25.000 | `[A]` + `[L]` | pilot kanal | Habibi |
| D-04 | Konversi funnel | download→bayar freemium ≈2,1%, Education 3,1%; tahap lain tidak ditemukan | `[B]` | buka laporan RevenueCat asli; retensi dari beta | Habibi |
| D-05 | Biaya AI | Rp50–370 per user/bln (Haiku 5.5); ×20 bila model menengah; kurs Rp18.100 | `[V]`/`[L]` | ukur token nyata; pilih model | Raihan |
| D-06 | Fee & pajak | fee langganan 15% sekarang, 10% mungkin setelah 30 Sep 2027; net Rp19.144 (base) | `[V]`/`[A]` | cek Play Console; inklusif atau eksklusif pajak | Raihan |
| D-07 | WTP & packaging | tidak bisa dari riset meja; harga kompetitor 10× lebih tinggi; survei 8 pertanyaan siap sebar | `[B]`/`[E]` | survei dan fake-door | Tio |
| D-08 | Profil web & pasar | web ≤0,25% dari 1 juta; pendaftar SNBT 2026 = 871.496 < 1 juta | `[V]`/`[L]` | data internal Terang AI | Habibi |
| D-09 | Anggaran | Lean Rp135,6 jt / Base Rp300,1 jt / Cap Rp345–412 jt; akuisisi Rp63 jt hanya membeli 1–2,6% dari 800 ribu install | `[L]` | atur ulang bukti organik | Raihan |
| D-10 | UU PDP <18 | Pasal 25 terverifikasi; anak = <18; PP 33/2026 belum dibaca; desain persetujuan perlu tinjauan hukum | `[V]`/`[B]` | baca PP 33/2026, tinjauan hukum | Raihan |

## 2. Lima temuan yang mengubah isi deck

1. **Kurs model sudah usang.** Tim memakai Rp16.000/US$; kurs tengah BI 11 Nov 2026 = Rp18.059. Semua angka berbasis dolar (biaya AI, CPI) naik sekitar 13% (D-05).
2. **Iklan berbayar tidak sanggup menopang harga Rp25.000.** Dengan LTV per pembayar ≈ Rp56.300 dan konversi 2%, CPI impas hanya ≈ Rp1.100. Usulan 70/30 organik/berbayar tidak didukung; porsi organik/kemitraan/referral yang konsisten ≈ 90–97% (D-03). Konsekuensi: **growth engine cards (poin 26) menjadi inti kelayakan**, bukan pelengkap.
3. **Target 1 juta melebihi pasar satu segmen.** Pendaftar SNBT 2026 = 871.496; web 10.000 user hanya menyumbang ≤0,25% (D-08). Sajikan base di bawah 1 juta, 1 juta sebagai upside, atau definisikan ulang sebagai kumulatif lintas segmen dan musim.
4. **Lintasan MAU harus mengikuti musim.** Puncak M3–M4 (Mar–Apr 2027), lembah M6–M8, M12 bukan puncak (D-01). LPDP Tahap 2 (daftar Jun–Jul, substansi Okt–Nov) menjadi penyeimbang (D-02).
5. **Biaya AI kecil, tetapi pilihan model menentukan segalanya.** Model kecil: ≈1–2% dari net; model menengah: 15%+ dari net dan total anggaran melonjak menjadi sekitar Rp1,2 miliar (D-05, D-09).

## 3. Hal yang saya tidak bisa verifikasi (jangan ditulis sebagai fakta)

- Data internal Terang AI (10.000+ user web, retensi, konversi): harus dari Q&A atau tim Terang AI.
- WTP dan preferensi paket: perlu survei primer.
- Benchmark CPI edtech Indonesia dan retensi D1/D7/D30: tidak ditemukan di sumber yang layak kutip.
- Isi PP 33/2026, harga Gemini, jumlah pendaftar LPDP, porsi Android dan akses internet: belum dicek.
- Banyak angka eksternal di atas berasal dari **sumber sekunder** (media, artikel ringkasan). Sebelum masuk deck, ambil dari sumber primernya (situs SNPMB, LPDP, Play Console, laporan RevenueCat asli, teks UU resmi) dan salin ke `Research-Log.md`.

## 4. Urutan kerja yang disarankan sebelum deck dikunci (17 Nov)

1. **Raihan (30 menit):** pilih satu asumsi AI (D-05), kurs Rp18.100, dan net per pembayar Rp19.144 (D-06); perbarui tab Inputs.
2. **Tio:** tangkapan layar SNPMB dan LPDP bertanggal (D-01/D-02); sebar survei 8 pertanyaan (D-07); verifikasi 3–4 harga kompetitor.
3. **Habibi:** kirim permintaan data ke Q&A (D-08); isi growth engine cards dengan angka berlabel `[A]` supaya porsi organik punya dasar (D-03/D-09).
4. **Semua:** putuskan definisi "1 juta" dan tulis di Team-Context.
5. **Raihan:** selesaikan P0 model, lalu minta tinjauan skeptis (peran Claude di SOP) pada versi deck.

## 5. Daftar file

| File | Isi |
|---|---|
| `D-01_Kalender-UTBK-SNBT.md` | kalender resmi 2024–2026, proyeksi 2027, peringatan sumber, implikasi MAU |
| `D-02_Kalender-LPDP.md` | Tahap 2 2026 terverifikasi, proyeksi 2027 |
| `D-03_Benchmark-CPI-CAC.md` | rentang CPI, model terbalik, rencana pilot |
| `D-04_Benchmark-Konversi-Funnel.md` | benchmark download→bayar, saran skenario konversi |
| `D-05_Biaya-Inferensi-AI.md` | tarif, perhitungan per user, sensitivitas tahunan |
| `D-06_Fee-Platform-dan-Pajak.md` | fee Play, perubahan 2026–2027, PPN, tabel net per pembayar |
| `D-07_WTP-dan-Packaging.md` | konteks harga kompetitor, struktur uji, survei 8 pertanyaan |
| `D-08_Profil-User-Web-dan-Ukuran-Pasar.md` | permintaan data, data pasar SNBT 2026, SAM/SOM |
| `D-09_Anggaran-Bergerbang.md` | amplop anggaran, tranche, aturan gate |
| `D-10_UU-PDP-Pengguna-di-Bawah-18.md` | Pasal 25, definisi anak, opsi desain persetujuan |
