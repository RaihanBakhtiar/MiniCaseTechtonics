# D-10 — Kepatuhan Regulasi Pengguna <18 Tahun (UU PDP)

**Pertanyaan kritis:** Apa syarat legal menampung data siswa SMA kelas 11–12 menurut UU PDP?
**PIC:** Raihan · **Dipakai di:** Slide 10 · **Diperiksa:** 16 Nov 2026
**Status setelah riset:** teks Pasal 25 = `[V]`; definisi "anak" dan mekanisme persetujuan = `[B]` (sekunder); rincian aturan pelaksana (PP 33/2026) = **belum dibaca**.

Catatan: ini ringkasan informasi, bukan nasihat hukum. Rancang alur persetujuan final bersama penasihat hukum atau klinik hukum kampus.

---

## 1. Jawaban singkat

1. **Pasal 25 benar seperti yang dicatat di Brainstorming.** Isinya: (1) pemrosesan data pribadi anak diselenggarakan secara khusus; (2) pemrosesan data pribadi anak **wajib mendapat persetujuan dari orang tua anak dan/atau wali anak** sesuai ketentuan peraturan perundang-undangan. `[V]` (teks UU No. 27 Tahun 2022 di Wikisource; cocokkan dengan salinan resmi JDIH/Setneg sebelum dikutip di deck)
2. **Siapa yang dihitung "anak"?** UU PDP sendiri tidak memberi definisi yang jelas (dicatat sebuah jurnal 2025). Praktik rujukan adalah UU Perlindungan Anak: anak = belum berusia **18 tahun** (UU 35/2014 Pasal 1 angka 1, dikutip Hukumonline). Konsekuensi untuk Terang AI: siswa kelas 11–12 yang berusia 16–17 tahun **termasuk**, sedangkan mahasiswa dan fresh graduate (18+) tidak. `[B]`
3. **Persetujuan harus sah**, yakni bebas, sadar, spesifik, dan tidak ambigu (ringkasan sumber sekunder atas Pasal 20). `[B]`
4. **Data anak diklasifikasikan sebagai data pribadi spesifik** (Pasal 4 ayat (2), menurut sebuah repositori Universitas Telkom). Klasifikasi ini biasanya membawa kewajiban lebih berat; **perlu diperiksa** langsung di teks UU dan pada PP 33/2026. `[B]`
5. **Ada aturan pelaksana yang baru:** PP No. 33 Tahun 2026 tentang Peraturan Pelaksanaan UU PDP (dirujuk di artikel Meridian Hukum). **Belum saya baca isinya**; mekanisme verifikasi usia dan persetujuan orang tua bisa diatur di sana. Pasal 25 yang dicek Tio ("perlu dicek ulang" di Hasil Diskusi) sudah terjawab, tetapi PP 33/2026 adalah pekerjaan baru.
6. **Lembaga pelindungan data pribadi** dilaporkan masih dalam proses pembentukan per 2026 (pasal.id). Ini bukan alasan menunda kepatuhan; kewajiban UU sudah berlaku.

## 2. Dampak langsung pada produk dan funnel

Persetujuan orang tua menambah langkah antara sign-up dan aktivasi. Itu mengancam "first value moment" (diagnostic). Tiga opsi desain berikut harus dinilai oleh penasihat hukum, dan keputusan harus tercatat di Team-Context:

| Opsi | Cara kerja | Risiko / catatan |
|---|---|---|
| A. Age gate + persetujuan wali sebelum pemrosesan | Tanya tahun lahir; bila <18, kirim tautan persetujuan ke WhatsApp/email wali (satu ketukan) sebelum diagnostic menyimpan data | Paling aman secara hukum; gesekan paling besar |
| B. Mode terbatas dulu | Sebelum persetujuan wali, hanya data minimum yang diproses dan tidak disimpan; profil dan analisis personal baru terbuka setelah persetujuan | Perlu penilaian hukum: apakah pemrosesan sementara tetap butuh persetujuan; jangan diasumsikan boleh |
| C. Persetujuan lewat institusi (sekolah/komunitas mitra) | Mitra memfasilitasi persetujuan kolektif untuk siswa | Belum tentu menggantikan persetujuan orang tua; tanyakan ke penasihat hukum dan sertakan di perjanjian kemitraan |

Prinsip tambahan yang aman dipakai di semua opsi (`[A]`, praktik umum, bukan kutipan pasal):
- kumpulkan data seminimal mungkin; jangan pakai data anak untuk iklan atau pelacakan lintas aplikasi
- jelaskan secara sederhana apa yang disimpan, untuk apa, dan berapa lama
- sediakan cara orang tua melihat dan menghapus data
- pisahkan persetujuan untuk analisis AI personal dari persetujuan pemrosesan umum

## 3. Metrik dan risiko untuk model

- Tambah satu tahap funnel di model: **consent completion rate** (sign-up→persetujuan wali) dan drop-off di langkah itu. Nilainya `[E]`; jangan menuliskan angka sebelum diuji di beta.
- Dampak pada A-05 (sign-up→aktivasi): pada segmen <18, aktivasi turun bila persetujuan wajib sebelum diagnostic. Bedakan angka aktivasi untuk <18 dan ≥18 di model.
- Dampak ke segmen: LPDP (rata-rata dewasa) tidak terkena. Siswa SMA kelas 11–12 terkena; jalur 3T yang banyak memakai siswa sekolah juga terkena. Nyatakan di slide 10: "Minors consent flow designed; counsel review planned".
- Risk register: "Privasi data di bawah umur" sudah ada (S/T). Tambah sinyal dini: "consent completion rate" dan "aduan orang tua".

## 4. Yang masih harus dilakukan

- [ ] Raihan membaca PP 33/2026 (cari bab data pribadi anak, verifikasi persetujuan) dan mencatat pasal yang relevan.
- [ ] Cocokkan Pasal 25 dengan salinan resmi UU 27/2022 (JDIH Setneg/Kominfo) dan simpan tangkapan layar.
- [ ] Jadwalkan tinjauan ringan oleh klinik hukum kampus atau penasihat hukum untuk memilih opsi A/B/C.
- [ ] Sinkronkan dengan Habibi: urutan onboarding dan momen persetujuan harus tertulis di user journey.

## 5. Baris Research-Log siap tempel

| ID | Question answered | Finding / exact metric | Source title + URL/file | Publisher | Publication date | Access date | Reliability / caveat | Owner | Used in |
|---|---|---|---|---|---|---|---|---|---|
| R-33 | Apa bunyi Pasal 25 UU PDP? | Pemrosesan data anak diselenggarakan khusus dan wajib mendapat persetujuan orang tua/wali [V] | UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi, id.wikisource.org (halaman 13 PDF) | Wikisource (salinan teks resmi) | UU diundangkan 17 Okt 2022 | 16 Nov 2026 | Sedang-tinggi; cocokkan dengan salinan resmi JDIH | Raihan | Slide 10 |
| R-34 | Siapa yang disebut anak? | Anak = belum 18 tahun (UU 35/2014 Pasal 1 angka 1); UU PDP tidak memberi definisi jelas [B] | Hukumnya Orang Tua Langgar Privasi Anak, hukumonline.com/klinik/a/hukumnya-orang-tua-langgar-privasi-anak-lt5ce97312bcfae/ | Hukumonline | 2019 (diperbarui) | 16 Nov 2026 | Sedang (sekunder, tetapi menyebut pasal) | Raihan | Slide 10 |
| R-35 | Aturan pelaksana UU PDP | PP No. 33 Tahun 2026 tentang Peraturan Pelaksanaan UU PDP ada; isi belum dibaca [A] | Akibat Hukum Publikasi Data Anak di Media Sosial..., meridianhukum.com/article/akibat-hukum-publikasi-data-anak-media-sosial-tanpa-persetujuan-orang-tua | Meridian Hukum | 2026 | 16 Nov 2026 | Rendah-sedang (sekunder); baca PP aslinya | Raihan | Slide 10 |
| R-36 | Apakah data anak data pribadi spesifik? | Pasal 4 ayat (2) menggolongkan data anak sebagai data spesifik [B] | repositori.telkomuniversity.ac.id (bab 1 karya ilmiah perekaman aktivitas siswa menengah atas) | Telkom University | n/a | 16 Nov 2026 | Rendah-sedang (karya ilmiah); verifikasi di teks UU | Raihan | Slide 10 |
