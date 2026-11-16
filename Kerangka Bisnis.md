# **Kerangka bisnis, monetisasi, dan kelayakan: Terang AI App**

Semua angka di bawah berupa placeholder **\[X\]** dan harus dianggap **ASSUMPTION** sampai divalidasi. Satu-satunya angka dari brief adalah harga awal Rp25.000/bulan. Kerangka ini sengaja dibuat parametrik terhadap segmen, karena pemilihan segmen oleh Tio dan Habibi belum final.

## **0\. Tiga koreksi desain sebelum membangun model**

**a. Template finansial menyimpan inkonsistensi denominator.** Di template, CAC dihitung per *acquired user*, sedangkan LTV dihitung per *paid user* (ARPPU × margin × lifetime). Rasio LTV:CAC dan payback yang membagi keduanya langsung akan menyesatkan: hasilnya menggelembung kira-kira sebesar 1/konversi. Perbaikannya: bandingkan dalam satu basis. Pakai **CAC per paying user** (= total biaya akuisisi ÷ pembayar baru), atau **LTV per acquired user** (= LTV per pembayar × konversi install→bayar). Rumus lengkap ada di bagian 3\.

**b. Churn konstan tidak cocok untuk produk berbatas ujian.** Masa berlangganan dibatasi tanggal ujian, jadi hazard churn melonjak setelah ujian dan berbeda per kohort. Model sebaiknya berbasis kohort dengan tanggal ujian sebagai batas, bukan satu tingkat churn bulanan.

**c. Model terbalik lebih jujur daripada model maju.** Karena anggaran tidak diberikan di brief dan 1 juta user adalah target yang diberikan, tanyakan dulu: *CAC maksimum berapa yang masih layak, diberi konversi dan LTV yang masuk akal?* Lalu bandingkan dengan CAC yang realistis per kanal. Rumusnya di bagian 3\.

**Arsitektur spreadsheet yang disarankan:** Inputs (setiap sel punya ID, status, sumber), Funnel, Cohort, Unit Economics, Budget, Scenarios (base/upside/downside), Sensitivity (tornado), Checks (cek konsistensi denominator). Beri tiap asumsi tag status: **\[V\]** tervalidasi (sumber \+ tahun), **\[B\]** benchmark berkutip, **\[A\]** ASSUMPTION murni, **\[E\]** akan diuji eksperimen.

---

## **1\. Batas free vs premium dan momen penawaran**

**Prinsip:** *free memberi nilai dan bukti; premium memberi kedalaman dan tindak lanjut.* Brief mendefinisikan premium sebagai full exam practice, interview simulation, dan personal analysis. Jika analisis personal sepenuhnya terkunci, user gratis tidak pernah merasakan nilai diferensiasi utama dan aktivasi melemah. Karena itu analisis perlu "dicicipi" gratis dengan kedalaman terbatas.

| Komponen | Free | Premium | Hipotesis / yang diuji |
| ----- | ----- | ----- | ----- |
| Diagnostic awal | Penuh, satu kali | Re-diagnostic berkala | Ini *first value moment*. Jangan dikunci |
| Hasil diagnostic | Skor ringkas \+ 2-3 area terlemah | Peta kelemahan penuh per topik \+ rekomendasi urutan belajar | Free memberi bukti, premium memberi tindak lanjut |
| Latihan adaptif | Kuota harian \[X\] | Tanpa/lebih besar kuotanya | Kuota menciptakan *limit moment* saat motivasi tinggi |
| Tryout penuh | 1 tryout pembuka | Seluruh tryout \+ kondisi waktu nyata | Pengalaman "ujian sungguhan" cukup dicicipi sekali |
| Pembahasan | Kunci \+ pembahasan dasar | Pembahasan AI personal ("mengapa saya salah") | Biaya inferensi AI hanya dikeluarkan untuk pembayar |
| Study plan | Tidak ada | Rencana adaptif | Nilai premium berkelanjutan |
| Simulasi wawancara | 1 sesi mini dengan umpan balik parsial | Sesi penuh \+ rubrik \+ riwayat | Biaya inferensi dibatasi, nilainya tetap terasa |
| Progres | Streak dasar | Analitik longitudinal | Membangun kebiasaan sekaligus alasan upgrade |
| Jalur 3T | Akses gratis penuh dengan verifikasi, terpisah dari funnel komersial | n/a | Didanai pendapatan komersial; harus dikecualikan dari penyebut konversi |

**Catatan kritis:**

* Biaya variabel fitur AI menentukan seberapa murah hati tier gratis boleh dibuat. Ini harus menjadi input eksplisit (ID A-17 di bawah), bukan diasumsikan nol.  
* Fitur "proyeksi skor vs target" menarik tetapi berisiko pada kepercayaan. Hanya tampilkan jika kalibrasinya bisa dibuktikan.  
* Gating hibrida (kedalaman insight \+ kuota ringan) lebih masuk akal daripada trial berbasis waktu, karena trial 7 hari memakai biaya AI tanpa jaminan momen nilai. Ini hipotesis yang perlu diuji, bukan fakta.

**Momen penawaran, berurutan menurut prioritas pengujian:**

1. **Setelah hasil diagnostic** (insight moment): soft paywall pada *kedalaman* analisis.  
2. **Saat menabrak kuota** pada sesi dengan motivasi tinggi (bukan sesi pertama).  
3. **Setelah tryout penuh pertama**: momen "jarak ke target".  
4. **Momen kalender**: hitung mundur ujian, pembukaan pendaftaran. Hati-hati agar diskon tidak melatih user menunggu promo.  
5. **Milestone kebiasaan** (streak D3-D7).  
6. **Momen sosial**: undangan teman atau gift/referral.

**Anti-pola:** paywall sebelum nilai pertama, nag berulang, dan diskon sebelum harga jangkar terbentuk.

**Struktur penawaran:** pertahankan jumlah paket kecil (hipotesis: ≤3 paket agar paywall jelas).

* Bulanan dengan jangkar **Rp25.000** dari casebook.  
* **Pass sampai tanggal ujian** (menyesuaikan horizon kebutuhan, lihat koreksi 0b).  
* Opsi bayar-bersama/grup (kelas, komunitas).

Harga di luar Rp25.000 adalah **ASSUMPTION \[E\]**, diuji lewat fake-door dan A/B. Ada juga friksi pembayaran di segmen pelajar: pembayar bisa orang tua, jadi pertimbangkan tautan bayar yang bisa dibagikan.

---

## **2\. Kerangka funnel**

| Tahap | Definisi event (usulan) | Rumus | Tuas utama | Validasi |
| ----- | ----- | ----- | ----- | ----- |
| Download | Install dari Play Store (iOS terpisah) | Install \= tayangan × konversi listing | ASO, kreator, kemitraan, web-bridge | Data Console, uji kanal berkode atribusi |
| Sign-up | Akun terbuat | Sign-up ÷ download | Friksi pendaftaran, login sosial | Event analytics |
| Activation | Menyelesaikan diagnostic **dan** membuka hasilnya dalam jendela \[X\] jam (usulan, ASSUMPTION) | Aktivasi ÷ sign-up | Onboarding, panjang diagnostic | A/B onboarding |
| Retention | Aktif kembali D1/D7/D30; *weekly active learner* | Retained ÷ aktivasi | Streak, pengingat, kalender ujian | Kurva kohort |
| Paywall exposure | Aktivasi yang melihat ≥1 paywall | Terpapar ÷ aktif | Kebijakan momen penawaran | Log paywall |
| Konversi bayar | Pembelian pertama | Bayar baru ÷ *eligible* | Harga, momen, penawaran | A/B paywall |
| Retensi bayar | Perpanjangan atau churn | Churn kohort-berbasis-tanggal-ujian | Win-back, paket pass | Data langganan |
| Referral | Undangan → install → aktivasi | K \= undangan/user × konversi undangan→aktivasi | Insentif dua sisi, gift 3T | Kode referral |

**Aturan penyebut:**

* Definisikan *eligible active users* secara eksplisit (usulan: aktivasi yang terpapar paywall dalam jendela \[X\] hari), dan keluarkan pengguna jalur 3T gratis.  
* Referral hanya dihitung dari referrer yang sudah aktif, supaya K tidak ter-inflasi oleh install kosong.  
* Pisahkan "1 juta install kumulatif" dari "MAU". Install tanpa aktivasi tidak menghasilkan revenue.

---

## **3\. Daftar asumsi dan rumus**

Seluruh baris berstatus **ASSUMPTION**. Level validasi: **L1** benchmark berkutip (catat sumber, tahun, metodologi), **L2** data internal Terang AI (analitik 10.000+ user web, jika diberikan), **L3** riset primer cepat (wawancara/survei), **L4** eksperimen (fake-door, pilot, A/B).

| ID | Variabel (definisi tepat) | Cara validasi dan level |
| ----- | ----- | ----- |
| A-01 | Volume download per bulan per kanal (organik vs berbayar) | Rencana kanal \+ pilot kecil berkode atribusi (L4), benchmark (L1) |
| A-02 | Porsi organik dalam pertumbuhan | Cek data web (L2), uji kreator vs ads (L4) |
| A-03 | CAC per kanal; definisi **fully-loaded** (kreator, ads, ASO tool, kemitraan) | Penawaran harga kreator/ads, benchmark (L1), pilot (L4) |
| A-04 | Download→sign-up | Benchmark (L1), data beta (L4) |
| A-05 | Sign-up→aktivasi | Beta tertutup, A/B onboarding (L4) |
| A-06 | D1/D7/D30 retention, per kohort tanggal ujian | Beta (L4), kebiasaan belajar via survei (L3) |
| A-07 | Porsi pengguna yang terpapar paywall | Desain produk, log (L4) |
| A-08 | Konversi *eligible*→bayar | Fake-door dan A/B paywall (L4), benchmark freemium edtech (L1) |
| A-09 | Bauran paket (bulanan vs pass) | Uji harga (L4), Van Westendorp/Gabor-Granger (L3), dengan catatan bias stated-vs-revealed |
| A-10 | Realisasi harga setelah promo/diskon | Rencana promo (L4) |
| A-11 | Tingkat refund/chargeback | Benchmark (L1), data awal (L4) |
| A-12 | Churn bayar: distribusi bulan menuju ujian dan porsi pembelian berulang | Kalender resmi (L1), survei (L3) |
| A-13 | Fee platform dan fee pembayaran | Dokumentasi resmi Google Play (L1) |
| A-14 | Harga inklusif/eksklusif pajak dan dampaknya pada pendapatan bersih | Cek aturan pajak dan billing (L1) |
| A-15 | Gross margin | Turunan A-13, A-14, A-17 |
| A-16 | Biaya konten/operasional per user aktif | Data Terang AI (L2) |
| A-17 | **Biaya inferensi AI per user aktif** (free dan paid) | Data Terang AI (L2); jika tak ada, hitung dari token per sesi × harga API (L1) |
| A-18 | Indeks musiman permintaan per bulan | Kalender resmi (L1), Google Trends (indeks relatif, L1) |
| A-19 | Biaya jalur 3T (subsidi) dan rasio subsidi per pembayar | Keputusan desain, data program (L2) |
| A-20 | Kapasitas tim dan biaya SDM | Konfirmasi panitia atau asumsi eksplisit |
| A-21 | Anggaran total dan alokasi per tahap | Brief tidak menyebut angka; putuskan sebagai input skenario |
| A-22 | Kontribusi 10.000+ user web ke fase awal (porsi yang unduh app) | Data web (L2), kampanye jembatan (L4) |

**Rumus (basis konsisten):**

* Sign-up \= download × A-04; Aktivasi \= sign-up × A-05; Terpapar \= aktivasi aktif × A-07  
* Bayar baru \= *eligible* × A-08  
* Bayar aktif\_t \= bayar aktif\_{t−1} × (1 − churn) \+ bayar baru\_t, dengan churn per kohort dan dibatasi tanggal ujian  
* Pendapatan kotor \= bayar aktif × harga terealisasi; pendapatan bersih \= pendapatan kotor × (1 − fee platform/pembayaran) (A-13, A-14)  
* Kontribusi \= pendapatan bersih − biaya inferensi AI − biaya konten/ops − biaya akuisisi  
* **CAC per user terakuisisi** \= biaya akuisisi ÷ user terakuisisi  
* **CAC per pembayar** \= biaya akuisisi ÷ pembayar baru  
* **LTV per pembayar** \= ARPPU × gross margin × masa berbayar yang diharapkan (batas: min(1/churn, bulan menuju ujian))  
* **LTV:CAC** \= LTV per pembayar ÷ CAC per pembayar *(atau LTV per user terakuisisi ÷ CAC per user terakuisisi)*  
* **Payback** \= CAC per pembayar ÷ (harga × margin bulanan)  
* **Model terbalik:** konversi install→bayar minimum \= CAC per install ÷ LTV per pembayar. Sebaliknya, CAC maksimum yang layak \= LTV per pembayar × konversi install→bayar ÷ target LTV:CAC \[X\].

---

## **4\. Roadmap 6-12 bulan (relatif terhadap peluncuran M0)**

Timing kalender absolut belum diverifikasi. Tempatkan fase Scale pada jendela puncak permintaan segmen terpilih (cek kalender resmi). Budget dinyatakan sebagai alokasi proporsional **\[X%\] ASSUMPTION** sampai model selesai. Penentu utamanya adalah *gate*, bukan tanggal: dana dilepas bertahap hanya jika gate tercapai.

| Fase / waktu | Tujuan | Aktivitas kunci | Deliverable / keputusan | Owner (peran) | Gate keluar |
| ----- | ----- | ----- | ----- | ----- | ----- |
| **Pre-launch** (M-2 s.d. M0) | Validasi segmen, proposisi, dan onboarding | Wawancara/fake-door ke user web; waitlist dan jembatan web→app; fondasi ASO; pipeline kreator/mitra; instrumentasi event; jalur pembayaran; verifikasi jalur 3T; materi kepercayaan (metodologi, kebijakan data) | Segmen final; varian paywall; taksonomi event | Product, Growth | Aktivasi beta ≥ \[X\]; sinyal bayar pada fake-door ≥ \[X\]; instrumentasi lengkap; model unit economics lolos |
| **Launch** (M0-M2) | Membuktikan unit economics pada skala kecil | Rilis bertahap; kanal berkode atribusi; A/B onboarding dan paywall; ulasan dan rating awal | Kanal pemenang; konfigurasi paywall | Growth, Product | CAC per pembayar ≤ \[X\]; D7 ≥ \[X\]; konversi ≥ \[X\] |
| **Scale** (M2-M6) | Meningkatkan volume pada jendela puncak | Perluas kanal pemenang; kampanye musiman; kemitraan sekolah/komunitas; referral skala penuh; iterasi ASO | Rilis anggaran per tahap | Growth, Partnerships | Payback ≤ \[X\] bulan; LTV:CAC ≥ \[X\]; CAC marginal tidak naik tajam |
| **Optimize/retain** (M6-M12) | Menjaga kontribusi positif dan meratakan musiman | Mekanik retensi dan win-back pasca ujian; optimasi harga/paket; gelombang segmen kedua; kemitraan institusional | Keputusan ekspansi segmen | Product, Growth, Biz | Churn bayar ≤ \[X\]; kohort berkontribusi positif |

Tampilkan di deck **jalur kumulatif install sebagai rentang low/base/high**, bukan satu garis menuju 1 juta, dan nyatakan porsi organik vs berbayar.

---

## **5\. KPI dan risiko**

**KPI tree** (target **\[X\] ASSUMPTION**, diturunkan dari model, bukan ditebak).

| Tujuan | Driver | KPI (rumus) | Frekuensi | Tindakan jika di bawah target |
| ----- | ----- | ----- | ----- | ----- |
| 1 juta user | Akuisisi | Install; CAC per kanal dan blended | Mingguan | Realokasi ke kanal dengan CAC terendah; hentikan kanal yang gagal gate |
| 1 juta user | Efisiensi kanal | Install→sign-up | Mingguan | Perbaiki listing, friksi daftar |
| Premium berkelanjutan | Aktivasi | Aktivasi (aktif ÷ sign-up); *time-to-first-insight* | Mingguan | Pendekkan diagnostic, ubah onboarding |
| Premium berkelanjutan | Retensi | D1/D7/D30; weekly active learner | Mingguan/bulanan | Uji mekanik kebiasaan dan pengingat |
| Premium berkelanjutan | Konversi | Paywall exposure; konversi bayar | Mingguan | Uji momen dan struktur harga |
| Premium berkelanjutan | Retensi bayar | Churn bayar per kohort; pembelian berulang | Bulanan | Win-back, paket pass |
| Kelayakan | Ekonomi unit | LTV:CAC; payback; gross margin | Bulanan | Hentikan pelepasan anggaran tahap berikutnya |
| Kelayakan | Biaya AI | Biaya inferensi per user aktif | Mingguan | Turunkan kuota free, optimasi model |
| Pertumbuhan | Referral | K; undangan→aktivasi | Mingguan | Ubah insentif |
| Kepercayaan | Kualitas AI | Penilaian kebermanfaatan umpan balik; laporan kesalahan; rating Play Store | Mingguan | Audit konten dan kalibrasi |

Usulan **North Star:** *weekly active learner yang menyelesaikan ≥1 sesi berpenjelasan personal*. Ini hipotesis yang bisa diganti jika data menunjukkan metrik lain lebih prediktif terhadap pembayaran.

**Risk register** (likelihood dan impact adalah **penilaian kualitatif tim**, bukan data):

| Risiko | L | I | Sinyal dini | Mitigasi | Kontingensi / pemilik |
| ----- | ----- | ----- | ----- | ----- | ----- |
| Permintaan musiman jatuh | T | T | Penurunan install dan aktivasi menjelang/seusai ujian | Paket pass; gelombang segmen kedua | Realokasi anggaran, Growth |
| CAC tidak ekonomis | T | T | CAC per pembayar naik terhadap batas model | Fokus kanal organik/kemitraan; gate anggaran | Hentikan kanal, Growth |
| Kepercayaan rendah pada AI | S | T | Rating dan laporan kesalahan memburuk | Transparansi metodologi, verifikasi konten, tinjauan manusia | Rollback fitur, Product |
| Aktivasi/retensi rendah | S | T | Aktivasi dan D7 di bawah gate | Redesain onboarding | Tunda Scale, Product |
| Respons kompetitor kuat | T | S | Penurunan share ASO; promo kompetitor | Diferensiasi pada analisis personal | Fokus sub-segmen, Biz |
| Biaya inferensi AI menggerus margin | S | T | Biaya per user aktif naik | Kuota free, optimasi inferensi | Ubah batas free/premium, Product |
| Ketergantungan platform dan fee | S | S | Perubahan kebijakan/fee | Diversifikasi (web, iOS) | Revisi harga, Biz |
| Privasi data di bawah umur | S | T | Temuan kepatuhan | Persetujuan orang tua, minimisasi data (cek UU PDP) | Hentikan kampanye ke usia terkait, Legal |
| Penyalahgunaan jalur gratis 3T | S | S | Pola akses tak wajar | Verifikasi kelayakan | Pembatasan akses, Product |
| Kapasitas tim terbatas | T | S | Backlog eksperimen menumpuk | Prioritaskan eksperimen berdampak | Kurangi kanal, Biz |

(T \= tinggi, S \= sedang, bisa Anda ganti dengan skor setelah riset.)

---

## **6\. Pertanyaan kritis sebelum angka masuk deck**

**Definisi dan target**

1. Apakah "1 juta" berarti install kumulatif Play Store saja, atau MAU? Apakah iOS dihitung? Dalam horizon 6 atau 12 bulan?  
2. Apakah jalur ke 1 juta *dalam anggaran terbatas* masuk akal? Berapa persen harus organik, dan apa buktinya?  
3. Apakah deck akan menyajikan base case di bawah 1 juta secara jujur, dengan 1 juta sebagai upside?

**Kekonsistenan model**  
 4\. Apakah CAC dan LTV dihitung pada basis yang sama (per pembayar atau per user)?  
 5\. Apa tepatnya penyebut *eligible active users*, dan apakah pengguna jalur 3T sudah dikeluarkan?  
 6\. Apakah churn dimodelkan per kohort dengan batas tanggal ujian, dan berapa porsi yang berhenti setelah ujian?  
 7\. Apakah pendapatan dilaporkan kotor atau bersih setelah fee platform dan pajak? Apakah Rp25.000 inklusif pajak?

**Data yang belum kita punya**  
 8\. Berapa biaya inferensi AI per sesi dan per user aktif? Jika Terang AI tidak memberikannya, bagaimana kita menghitungnya secara transparan?  
 9\. Data apa yang ada tentang 10.000+ user web: komposisi segmen, aktivitas, apakah sudah ada konversi bayar atau uji harga?  
 10\. Apakah anggaran dan kapasitas tim diberikan, atau harus kita tetapkan sebagai input skenario?

**Strategi dan kepercayaan**  
 11\. Mengapa pengguna membayar Rp25.000 padahal LLM generik dan konten gratis tersedia? Bukti apa yang menunjukkan nilai analisis personal Terang AI?  
 12\. Bagaimana mekanisme pendanaan silang jalur 3T (rasio subsidi per pembayar) memengaruhi margin, dan apakah itu masuk model?  
 13\. Apakah harga dan fitur di web berbeda dengan app, sehingga ada kanibalisasi?  
 14\. Bagaimana kita menunjukkan akurasi umpan balik AI kepada juri dan pengguna?

**Disiplin deck**  
 15\. Setiap angka di deck sudah punya ID, status (V/B/A/E), dan rencana validasi?  
 16\. Apa **kriteria berhenti/berubah arah** (misalnya jika konversi di bawah ambang, kita ganti segmen atau struktur harga)?

**Saran penempatan di deck (maks. 10 halaman konten; Feasibility & Implementation 25%):** satu halaman funnel \+ unit economics dengan rentang skenario dan tag status asumsi, satu halaman roadmap \+ anggaran bergerbang, satu halaman KPI \+ risiko. Format "ID asumsi \+ status \+ rencana validasi" itu sendiri menunjukkan kelayakan dan kejujuran asumsi.

**Ketergantungan dengan rekan tim:** definisi event aktivasi dan momen paywall harus selaras dengan user journey Habibi. Bukti harga dan batas free/paid kompetitor dari Tio akan menjadi input A-09 dan A-10. Segmen final menentukan parameter A-06, A-12, dan A-18.

Jika berguna, langkah berikutnya bisa berupa spesifikasi tab Inputs lengkap dengan kolom status dan sumber, atau draf skenario base/upside/downside dalam bentuk parameter (tanpa angka) yang siap diisi begitu validasi selesai.

