# D-05 — Biaya Inferensi AI per User (COGS)

**Pertanyaan kritis:** Berapa rupiah biaya API model untuk 1 pengguna aktif per bulan?
**PIC:** Raihan · **Dipakai di:** Slide 7, 8 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** tarif API = `[V]` (halaman resmi Anthropic + laporan peluncuran); token per interaksi dan jumlah interaksi = `[A]`; hasil rupiah = `[L]`.

---

## 1. Jawaban singkat

1. **Dengan model kecil, biaya AI sangat kecil: sekitar Rp50–370 per pengguna aktif per bulan**, atau **0,8%–1,9%** dari pendapatan bersih per pembayar (Rp19.144, lihat D-06). Margin kotor perangkat lunak memang tetap tinggi, seperti kesimpulan awal tim.
2. **Risiko sebenarnya adalah pilihan model.** Memakai model kelas menengah (Sonnet 5.5) membuat biaya naik sekitar **20 kali lipat** (Rp3.000–7.300 per user per bulan pada 15 interaksi), dan pada skenario itu biaya AI memakan sampai **15,6%** pendapatan bersih. Tetapkan model sebagai input eksplisit.
3. **Kurs di model tim sudah usang.** Perhitungan tim memakai Rp16.000/US$. Kurs tengah BI 11 Nov 2026 adalah **Rp18.059** (pasar sekitar Rp18.090), jadi semua biaya berbasis dolar naik sekitar 13%. Pakai **Rp18.100** sebagai base dan **Rp18.500** sebagai downside (satu media menyebut rupiah terancam menembus Rp18.500).
4. **Poin 22 di Hasil Diskusi sudah bisa ditutup:** rentang Rp112–300 di Brainstorming memang tidak cocok dengan inputnya (35.000 token × US$0,15–0,30 per 1 juta token × Rp16.000 = Rp84–168). Hitung ulang di bawah dengan tarif nyata dan kurs terbaru.

## 2. Tarif yang dipakai (`[V]`)

**Claude Haiku 5.5** (rilis 7 Okt 2026): US$0,10 per 1 juta token input dan US$0,50 per 1 juta token output untuk prompt sampai 100.000 token. Di atas 100.000 token seluruh tarif naik lima kali lipat (US$0,50 / US$2,50). Cache read US$0,01; tarif batch US$0,05 / US$0,25 (laporan pihak ketiga, cek halaman harga).
**Claude Sonnet 5.5:** US$2 / US$10 per 1 juta token.

Dua catatan agar tidak salah baca:
- Tarif Haiku 5.5 dilaporkan sama dengan GPT-6 Luna. Tarif Gemini tidak saya periksa; jangan menulis perbandingan Gemini di deck tanpa verifikasi.
- Artificial Analysis dilaporkan menemukan Haiku 5.5 memakai sekitar **tiga kali** token output per tugas dibanding pembandingnya. Karena itu ada skenario "output ×3".

## 3. Perhitungan (`[L]`; input `[A]`: 1.500 token prompt + 800 token output per interaksi, kurs Rp18.100)

Biaya per interaksi, Haiku 5.5: 1.500 × 0,10 + 800 × 0,50 = US$0,00055 ≈ **Rp10**. Dengan output ×3 (2.400 token): US$0,00135 ≈ **Rp24**.

| Skenario | 5 interaksi/bln | 15 interaksi/bln | % dari Rp19.144 (15 int.) |
|---|---:|---:|---:|
| Haiku 5.5, 2.300 token | Rp50 | Rp149 | 0,8% |
| Haiku 5.5, output ×3 | Rp122 | Rp367 | 1,9% |
| Sonnet 5.5, 2.300 token | Rp995 | Rp2.986 | 15,6% |
| Sonnet 5.5, output ×3 | Rp2.444 | Rp7.330 | 38,3% |

**Cek terhadap angka lama tim:** Rp14,4 per interaksi (Plan) berada di antara Haiku normal (Rp10) dan Haiku verbose (Rp24). Jadi Rp72 untuk 5 interaksi tidak absurd, hanya masih setengah-tertebak.

## 4. Biaya tahunan pada lintasan 2,771 juta MAU-bulan (5 interaksi/bln)

| Porsi MAU pengguna fitur AI | Haiku 2.300 token (Rp50) | Plan lama (Rp72) | Haiku output ×3 (Rp122) | Sonnet (Rp996) |
|---|---:|---:|---:|---:|
| 10% | Rp13,8 jt | Rp20,0 jt | Rp33,9 jt | Rp275,9 jt |
| 30% | Rp41,4 jt | Rp59,9 jt | Rp101,6 jt | Rp827,6 jt |
| 50% | Rp69,0 jt | Rp99,8 jt | Rp169,3 jt | Rp1.379 jt |
| 100% | Rp137,9 jt | Rp199,5 jt | Rp338,5 jt | Rp2.759 jt |

Catatan: lintasan 2,771 juta MAU-bulan sendiri masih bermasalah (lihat D-01 dan D-08). Tabel ini menguji sensitivitas biaya, bukan memperkuat lintasan itu.

**Biaya tier gratis:** jika setiap pengguna gratis aktif mendapat 5 interaksi AI per bulan, biayanya Rp50–122 per orang. Dengan 100.000 pengguna gratis aktif, itu **Rp5–12 juta per bulan**. Kuota gratis tetap perlu batas.

## 5. Yang belum tercakup

- Simulasi wawancara memakai suara (speech-to-text / text-to-speech) atau input panjang: biayanya tidak termasuk di tabel dan bisa jauh lebih tinggi per sesi.
- Prompt dengan riwayat belajar panjang: tarif Haiku 5.5 melonjak lima kali lipat di atas 100.000 token.
- Biaya infrastruktur lain (penyimpanan, moderasi, logging).
- Kualitas pembahasan Haiku untuk soal UTBK/LPDP belum diuji. Uji 30–50 soal sebelum memutuskan model (`[E]`).

## 6. Yang masih harus dilakukan

- [ ] Raihan memasukkan tiga input ke tab Inputs: model, interaksi/user/bulan (free dan paid terpisah), kurs.
- [ ] Ukur token nyata dari 20–30 sesi prototipe, ganti 1.500 + 800 yang masih `[A]`.
- [ ] Putuskan satu model dasar untuk deck (usulan: model kecil dengan jalur eskalasi ke model besar untuk kasus sulit, ditandai `[E]`).

## 7. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-17 | Berapa tarif API Haiku 5.5? | US$0,10 input / US$0,50 output per 1 juta token (prompt ≤100K); US$0,50 / US$2,50 di atasnya [V] | Claude Haiku 5.5 overview, platform.claude.com/docs/en/models/haiku-5-5/overview; ppc.land/anthropic-haiku-5-5-costs-90-less-than-4-5-for-prompts-to-100-000-tokens/ | Anthropic; PPC Land | 7 Okt 2026 | 16 Nov 2026 | Tinggi (primer + laporan peluncuran); cek halaman harga resmi saat finalisasi | Raihan | Slide 7, 8 |
| R-18 | Berapa tarif Sonnet 5.5? | US$2 / US$10 per 1 juta token [V-sekunder] | Cross 100,000 tokens on Claude Haiku 5.5..., mixed-news.com/en/?p=35958 | Mixed | Okt 2026 | 16 Nov 2026 | Sedang; verifikasi di halaman harga Anthropic | Raihan | Slide 8 |
| R-19 | Berapa kurs USD/IDR terbaru? | Kurs tengah BI Rp18.059 per US$ (11 Nov 2026) [V-sekunder] | Kurs Dollar ke Rupiah Hari Ini 11 November 2026, journalarta.com/news/2026/11/11/kurs-dollar-ke-rupiah-hari-ini-11-11-2026/ | JournalArta (mengutip BI) | 11 Nov 2026 | 16 Nov 2026 | Sedang-tinggi; ambil angka langsung dari situs BI saat finalisasi | Raihan | Slide 8, 9 |
