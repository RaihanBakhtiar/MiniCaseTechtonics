# D-09 — Anggaran Pemasaran Bootstrapped (Gated Budget)

**Pertanyaan kritis:** Berapa plafon anggaran yang rasional untuk startup tanpa pendanaan VC selama 6–12 bulan?
**PIC:** Raihan · **Dipakai di:** Slide 9 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** tidak ada benchmark eksternal untuk "plafon rasional". Jawaban disusun dari angka tim sendiri (Implementation Plan kedua, Rp300,1 jt) yang dihitung ulang dengan temuan D-03, D-05, D-06. Semua `[L]` di atas input `[A]`.

---

## 1. Jawaban singkat

1. **Amplop anggaran yang bisa dipertahankan (`[A]`):**
   - **Lean (komit di muka):** Rp135,6 jt = kuartal 1 + 2 dari rencana tim.
   - **Base:** **Rp300,1 jt** (rencana tim, termasuk kontingensi 10%, belum memuat koreksi AI).
   - **Cap (hanya bila gate lolos):** **Rp345–412 jt**, tergantung asumsi model AI di D-05.
   Rentang Rp150–350 jt di Brainstorming masuk akal; bagian 2 memberi dasar hitungnya.
2. **Biaya AI tidak boleh disembunyikan di dalam angka Rp300 jt.** Dengan tarif Haiku 5.5, biaya AI satu tahun pada skenario 30% pengguna dan 5 interaksi adalah Rp41,4–101,6 jt. Dengan model kelas menengah (Sonnet), Rp827,6 jt, dan total melonjak menjadi sekitar Rp1,21 miliar: **tidak layak** untuk bootstrapped. Pilihan model adalah keputusan anggaran.
3. **Masalah paling serius ada di akuisisi, bukan di total.** Rencana tim memuat biaya akuisisi eksplisit sekitar **Rp63 jt**. Bila seluruhnya dipakai untuk iklan berbayar, dengan CPI Rp3.000/5.000/8.000 (`[A]`, lihat D-03) itu hanya membeli sekitar **21.000 / 12.600 / 7.900 install**, yaitu **2,6% / 1,6% / 1,0% dari 800 ribu install** (base di checklist Brainstorming). Sisanya harus datang dari organik, kemitraan, dan referral, dan itu belum ada buktinya (growth engine cards masih kosong, poin 26). Jika bukti tidak muncul, turunkan target base, jangan menaikkan anggaran.

## 2. Perhitungan (`[L]`)

**a. Total anggaran dengan koreksi AI** (subtotal tim Rp272,816 jt + biaya AI + kontingensi 10%):

| Asumsi AI (30% pengguna, 5 interaksi/bln) | Biaya AI/tahun | Total + 10% |
|---|---:|---:|
| Plan lama (Rp72/user-bln) | Rp59,9 jt | Rp365,9 jt |
| Haiku 5.5, 2.300 token (Rp50) | Rp41,4 jt | **Rp345,6 jt** |
| Haiku 5.5, output ×3 (Rp122) | Rp101,6 jt | **Rp411,9 jt** |
| Sonnet 5.5 (Rp996) | Rp827,6 jt | Rp1.210 jt |

Tanpa koreksi AI: Rp272,816 jt × 1,10 = Rp300,098 jt (cocok dengan angka tim). Peringatan: lintasan 2,771 juta MAU-bulan di balik tabel ini masih bermasalah (D-01), jadi perlakukan biaya AI sebagai sensitivitas.

**b. Tranche kuartalan dari rencana tim (menjumlah ke Rp300,098 jt):**

| Kuartal | Tranche | Kumulatif | % dari Rp300,1 jt |
|---|---:|---:|---:|
| Q1 | Rp63,91 jt | Rp63,91 jt | 21% |
| Q2 | Rp71,72 jt | Rp135,63 jt | 45% |
| Q3 | Rp79,09 jt | Rp214,72 jt | 72% |
| Q4 | Rp85,378 jt | Rp300,098 jt | 100% |

## 3. Aturan pelepasan dana per gate (usulan, `[A]`; nilai diturunkan dari model)

| Gate | Dana yang dilepas | Syarat lolos (semua) | Dasar angka |
|---|---|---|---|
| G0 (pra-peluncuran) | Q1 Rp63,9 jt | instrumentasi event lengkap; hasil survei WTP dan fake-door ada; model unit economics lolos cek denominator | D-07, D-04 |
| G1 | Q2 Rp71,7 jt | CAC per pembayar ≤ **Rp56.300** (batas impas) dan target ≤ **Rp18.800** (3:1); konversi install→bayar ≥ **1,0%**; biaya AI per user aktif ≤ **Rp150** (alarm di Rp400) | D-03, D-04, D-05 |
| G2 | Q3 Rp79,1 jt | gate G1 terpenuhi dua bulan berturut-turut; payback < masa berbayar rata-rata; D7 sesuai **ambang dari beta** | D-03 |
| G3 | Q4 Rp85,4 jt | kohort pasca-ujian tidak menghasilkan kontribusi negatif; retensi pasca-ujian terukur | D-01 |

Ambang D7 sengaja tidak diisi angka: tidak ada benchmark yang bisa dipertanggungjawabkan (D-04). Tetapkan setelah closed beta (`[E]`) dan tulis aturannya, bukan placeholder `[X]`. Setiap evaluasi menghasilkan satu dari: continue / optimize / stop / scale.

## 4. Catatan konsistensi

- Rp300,1 jt adalah biaya **tambahan** (incremental): gaji tim existing dan pengembangan inti aplikasi tidak dihitung. Nyatakan itu di slide.
- Input tanpa sumber yang masih memengaruhi total: gaji Rp5,5 jt dan Rp8 jt per bulan, serta biaya cloud. Tandai `[A]`.
- Kurs biaya AI dan pembayaran: Rp18.100/US$ (D-05, D-06).

## 5. Yang masih harus dilakukan

- [ ] Raihan menetapkan satu asumsi AI (model + interaksi + porsi pengguna) dan menulis ulang total.
- [ ] Habibi mengisi growth engine cards (jumlah mitra, volume per mitra, K-factor) supaya porsi organik punya dasar bottom-up.
- [ ] Putuskan: bila bukti organik lemah, turunkan target base atau naikkan LTV (paket pass, D-03/D-07).

## 6. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-31 | Berapa anggaran dasar tim? | Subtotal Rp272,816 jt + 10% = Rp300,098 jt; tranche Rp63,91 / 71,72 / 79,09 / 85,378 jt [L] | 08_DISCUSSION_ANSWER/Hasil-Diskusi-Konsisten-dan-Next-Steps.md §4 | Tim (internal) | 16 Nov 2026 | 16 Nov 2026 | Aritmetika sudah diperiksa; input gaji dan cloud masih `[A]` | Raihan | Slide 9 |
| R-32 | Berapa biaya AI per tahun menurut skenario? | Rp41,4 jt (Haiku, 30%, 5 int.) s.d. Rp827,6 jt (Sonnet) [L] | D-05_Biaya-Inferensi-AI.md §4 | Tim (internal) | 16 Nov 2026 | 16 Nov 2026 | Bergantung pada input `[A]`; lihat D-05 | Raihan | Slide 8, 9 |
