# D-06 — Platform Fee & Pajak (Pendapatan Bersih per Pembayar)

**Pertanyaan kritis:** Berapa potongan riil dari Google Play Billing, payment gateway, dan PPN terhadap Rp25.000?
**PIC:** Raihan · **Dipakai di:** Slide 7, 8 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** fee langganan 15% = `[V]`; perubahan fee 2026–2027 = `[V]` (pengumuman) dengan dampak `[A]`; apakah Rp25.000 inklusif pajak = **belum diketahui**, jadi disajikan dua skenario.

Catatan: saya bukan konsultan pajak. Angka di bawah untuk pemodelan; konfirmasi lewat Play Console dan akuntan sebelum dipakai sebagai klaim pasti.

---

## 1. Jawaban singkat

1. **Fee Google Play untuk langganan = 15%.** Google menyatakan tarif layanan untuk semua langganan diturunkan menjadi 15% sejak Okt 2021. `[V]`
2. **Perubahan yang perlu masuk model:** pada 4 Mar 2026 Google mengumumkan struktur baru. Biaya layanan untuk **langganan berulang menjadi 10%**, dan biaya penagihan dipisah dari biaya layanan. Jadwal peluncuran: EEA/Inggris/AS paling lambat 30 Jun 2026, Australia 30 Sep 2026, Korea/Jepang 31 Des 2026, dan **negara lainnya (termasuk Indonesia, berdasarkan pembacaan "negara lainnya") pada 30 Sep 2027**. Artinya: asumsikan **15% untuk M0 sampai sekitar Sep 2027**, lalu skenario upside 10% + tarif penagihan khusus pasar yang belum diketahui. `[V]` pengumuman, `[A]` untuk Indonesia.
3. **Biaya gateway 0,7–1,5% di Brainstorming kemungkinan menghitung dua kali.** Rp20.900 = 25.000 − 3.750 − 350 menjumlahkan fee Play dan fee gateway. Bila pembayaran lewat Play Billing, fee 15% adalah paketnya; pengumuman 2026 justru menyebut biaya penagihan "dipisah" dari biaya layanan, yang menyiratkan keduanya saat ini menyatu. Gateway (Midtrans/Xendit) relevan hanya untuk pembayaran web atau billing alternatif. **Verifikasi di Play Console.**
4. **PPN:** tarif nominal 12% dengan dasar pengenaan pajak (DPP) 11/12, sehingga beban efektif **11%** untuk barang/jasa non-mewah. Google Play menampilkan 12% ke konsumen sejak Jan 2025 (dilaporkan Bisnis/Jakarta Post), jadi dua angka itu beredar. PPN dipungut platform dan **bukan pendapatan developer**.
5. **Rekomendasi angka untuk model:** pakai **Rp19.100 per pembayar per bulan** sebagai base (harga inklusif PPN 11%, fee 15%), dan **Rp21.250** sebagai upside (harga eksklusif pajak). Ganti Rp20.900 di Brainstorming.

## 2. Perhitungan pendapatan bersih Rp25.000 (`[L]`)

Asumsi: fee dihitung atas harga sebelum PPN (praktik umum; verifikasi di dokumentasi Play).

| Skenario | PPN | Fee Play | DPP | Net ke Terang AI |
|---|---|---|---:|---:|
| A. Rp25.000 inklusif PPN 11% (base) | Rp2.477 | 15% | Rp22.523 | **Rp19.144** |
| A'. Inklusif PPN 12% | Rp2.679 | 15% | Rp22.321 | Rp18.973 |
| B. Rp25.000 eksklusif pajak | di atas harga | 15% | Rp25.000 | **Rp21.250** |
| C. Setelah fee turun ke 10% (inklusif 11%) | Rp2.477 | 10% | Rp22.523 | Rp20.270 |
| D. Setelah fee 10% (eksklusif pajak) | n/a | 10% | Rp25.000 | Rp22.500 |
| Brainstorming (tidak dipakai) | – | 15% + gateway | – | Rp20.900 |

Paket pass (`[A]`, contoh): Rp69.000 untuk 4 bulan, inklusif 11%, fee 15% → net Rp52.838, setara Rp13.209 per bulan. Itu lebih rendah per bulan daripada langganan bulanan, tetapi uangnya masuk di muka dan tidak ada risiko churn di tengah masa.

## 3. Tarif lain yang beredar (jangan tertukar)

- Fee standar 15–30% adalah dasar putusan KPPU terhadap Google (denda sekitar Rp202 miliar; dilaporkan Mahkamah Agung menolak kasasi). Putusan itu juga meminta pengurangan minimal 5% bagi developer yang memakai User Choice Billing selama 1 tahun. Google menyebut program percontohan memberi diskon 4% untuk penagihan alternatif. Detail pelaksanaannya belum terverifikasi, jadi **jangan dijadikan asumsi base.**
- Untuk penjualan di luar Play (web), PPN tetap berlaku sesuai aturan, dan Terang AI harus menangani gateway sendiri.

## 4. Dampak pada model

- Margin kotor setelah fee dan AI: (19.144 − 149 s.d. 367) ÷ 25.000 ≈ **75–76% dari harga bruto**, atau sekitar **98–99% dari net** setelah AI. Gunakan definisi margin yang sama di semua slide dan sebutkan basisnya (bruto atau net).
- Satu baris sensitivitas wajib: net per pembayar Rp19.100 vs Rp21.250. Selisihnya 11% dari LTV, cukup untuk menggeser batas CPI di D-03.

## 5. Yang masih harus dilakukan

- [ ] Raihan membuka Play Console (atau dokumentasi "Service fees") untuk memastikan: fee langganan Indonesia saat ini, apakah QRIS/e-wallet termasuk Play Billing, apakah harga di template Indonesia inklusif pajak.
- [ ] Cocokkan tarif PPN yang tampil di Play untuk Indonesia (11% efektif atau 12% tampil).
- [ ] Kalau Google merilis jadwal Indonesia sebelum 30 Sep 2027, perbarui skenario C/D.

## 6. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-20 | Berapa fee Google Play untuk langganan? | 15% untuk semua langganan (sejak Okt 2021) [V] | Google Play & Android dibuat untuk membantu developer meraih kesuksesan, blog.google/intl/id-id/products/platforms/2022_04_google-play-android-dibuat-untuk/ | Google Indonesia | laman statis (entri Okt 2021) | 16 Nov 2026 | Tinggi (primer); cek Play Console untuk kondisi akun | Raihan | Slide 7, 8 |
| R-21 | Apakah fee akan berubah? | Langganan berulang 10%; biaya penagihan dipisah; negara lainnya sampai 30 Sep 2027 [V] | A new era for choice and openness, developer.android.com/blog/posts/a-new-era-for-choice-and-openness | Android Developers Blog (Google) | 4 Mar 2026 | 16 Nov 2026 | Tinggi (primer); jadwal Indonesia berdasarkan pembacaan "negara lainnya" | Raihan | Slide 8, 9 |
| R-22 | Berapa PPN produk digital? | Tarif 12% × DPP 11/12 = efektif 11%; Google Play menampilkan 12% sejak 1 Jan 2025 [V-sekunder] | Ada DPP 11/12 dalam Skema PPN 12%, ekonomi.bisnis.com/read/20250103/259/1828644/... ; pajak.go.id/pajakdigital | Bisnis.com; DJP | 3 Jan 2025 | 16 Nov 2026 | Sedang-tinggi; konfirmasi dengan akuntan | Raihan | Slide 8 |
| R-23 | Putusan KPPU terhadap fee Google | Fee 15–30% dinilai penyalahgunaan posisi dominan; wajib program UCB dengan pengurangan fee ≥5% setahun [B] | Indonesia imposes $12.4 million fine on Google, ppc.land/indonesia-imposes-12-4-million-fine-on-google-over-play-store-billing-practices | PPC Land | Jan 2025 | 16 Nov 2026 | Sedang (sekunder); tidak dijadikan asumsi base | Raihan | catatan internal |
