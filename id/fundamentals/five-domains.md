# Lima Domain: Govern hingga Strategize

> **Sumber belajar independen dan tidak resmi.** EC-Council, CCISO, CISSP, CISM, CISA, ISO, NIST, ISACA, COBIT, dan MITRE ATT&CK adalah merek milik pemiliknya. Situs ini tidak berafiliasi dengan penerbit, tidak memuat materi kursus resmi atau bocoran soal. Artikel ini **tidak** menyatakan bobot domain, durasi atau jumlah soal, nilai lulus, harga, aturan ujian ulang, maupun angka CPD — verifikasi di kanal resmi bertanggal. Statistik vendor adalah **klaim pemasaran**, bukan jaminan hasil.

> **Batas isi.** Edukasi tata kelola dan kepemimpinan, **bukan nasihat hukum, keuangan, pajak, regulasi, atau investasi**. Tidak ada prosedur ofensif, payload, atau petunjuk penghindaran deteksi. Organisasi, orang, dan angka dalam studi kasus bersifat fiktif. Untuk kewajiban konkret, mintalah pendampingan profesional.

---

## Tujuan belajar

Setelah menyelesaikan artikel ini, pembaca seharusnya mampu:

1. Menjelaskan mengapa kelima domain adalah **lensa keputusan**, bukan departemen atau tahap sekali jalan.
2. Untuk tiap domain: menyebut tujuan, keputusan, artefak, pertanyaan metrik, dan mode kegagalannya.
3. Melacak satu risiko bisnis melalui kelima domain dan menyebut artefak serah terimanya.
4. Mengenali cabang **STOP** dan **HOLD** yang menuntut jeda, pemilik bernama, atau wewenang tertulis.
5. Membedakan wewenang tata kelola dari wewenang operasional saat insiden atau tanggapan audit.
6. Menantang klaim teknis dan klaim pemasok lewat pertanyaan domain yang tepat, bukan menambah alat.
7. Memetakan pengalaman sendiri berdasarkan bukti yang dapat diperiksa, bukan jabatan.
8. Memisahkan ide yang stabil dari kemasan yang berubah: versi, aturan administratif, statistik.

Jika poin 3, 4, dan 6 belum bisa, pembaca baru mengetahui *daftar* domain, belum memakainya untuk memutus.

---

## Dari daftar topik menjadi hak keputusan

Daftar topik membantu orang belajar. **Domain** membantu orang memutus. Pemasok pengolah data yang mati adalah ketergantungan pihak ketiga, insiden layanan, pertanyaan desain, masalah komunikasi, dan keputusan anggaran sekaligus. Domain bertanya: *siapa yang memutus, dengan wewenang apa, atas bukti apa, dan dengan konsekuensi apa?*

Kelima domain — **Govern, Lead, Operate, Secure, Strategize** — adalah **lensa yang tumpang tindih**, bukan bagan organisasi. Satu rapat dapat melintasi semuanya dalam satu jam. Urutan penyajian di artikel ini mengikuti daftar pembaca; urutan *ketergantungan* di diagram berikut menempatkan **Secure** sebelum **Operate**, karena organisasi perlu memahami sistem sebelum mengklaim operasinya terkendali. Keduanya bukan jadwal kerja.

| Domain | Tujuan yang dijamin | Keputusan yang dimiliki | Artefak khas | Pertanyaan metrik | Mode kegagalan khas |
|---|---|---|---|---|---|
| **Govern** | Keputusan memiliki pemilik dan batas yang sah | Penerimaan risiko, persetujuan kebijakan, pengecualian, eskalasi | Piagam hak keputusan, registri risiko, registri pengecualian | "Apakah risiko yang diterima masih mutakhir dan bernama pemiliknya?" | Kebijakan kertas tanpa pemilik yang berani memutus |
| **Lead** | Keputusan sampai ke orang yang harus bertindak | Pesan, audiens, eskalasi, penanganan ketidaksepakatan, penolakan | Peta pemangku kepentingan, ringkasan eksekutif, log keputusan | "Apakah keputusan benar-benar dijalankan, dan siapa yang masih menolak?" | Nasihat yang benar secara teknis tetapi diabaikan |
| **Operate** | Program bekerja pada minggu biasa dan minggu yang buruk | Prioritas temuan, komando insiden, jeda layanan, verifikasi perbaikan | Indeks runbook, catatan insiden, paket ukuran, pelacak perbaikan | "Bisakah kami mendeteksi, merespons, dan memulihkan secara dapat diprediksi?" | Menghitung aktivitas sebagai pengganti hasil |
| **Secure** | Penilaian teknis cukup kuat untuk menantang klaim | Postur desain, pemilihan kontrol, batas keyakinan, kebutuhan tinjauan independen | Katalog kontrol, catatan arsitektur, catatan tinjauan desain | "Bisakah paparan dijelaskan dalam bahasa bisnis tanpa kehilangan akurasi?" | Pengetahuan teknis diserahkan seluruhnya kepada pemasok |
| **Strategize** | Risiko berubah menjadi arah yang benar-benar didanai | Urutan pendanaan, pilihan bangun/beli/mitra, portofolio, hal yang sengaja tidak dilakukan | Peta jalan, studi kasus usaha, ukuran manfaat, daftar tertunda | "Apakah pekerjaan yang dibiayai mengubah profil risiko?" | Daftar keinginan tanpa pemilik, uang, atau tanggal tinjau |

Tabel itu bukan hierarki. Menganggap Govern sebagai administrasi, Lead sebagai slide, Operate sebagai help desk, Secure sebagai rekayasa, dan Strategize sebagai spreadsheet adalah cara tercepat kehilangan nilai model ini. Setiap baris memuat **keputusan yang tidak bisa diserahkan kepada alat**, karena ia mendistribusikan wewenang, biaya, dan akuntabilitas.

**Hak keputusan** (*decision rights*) adalah batas resmi siapa yang boleh memutus apa. **Artefak** adalah catatan hasil sebuah domain yang dapat diperiksa orang lain. Tanpa artefak, keputusan hanya hidup di ingatan rapat — dan ingatan rapat berubah cepat.

---

## Alur dari tata kelola ke strategi — dan kembali lagi

Diagram berikut adalah **alur bernalar**, bukan prosedur teknis. `STOP` berarti pekerjaan belum boleh melangkah karena wewenang atau bukti belum ada; `HOLD` berarti jeda sementara untuk stabilisasi. Umpan balik tidak pernah melompat langsung ke "beli alat" — ia kembali ke tata kelola.

```
        +------------------------------------------------+
        | Niat bisnis / kewajiban untuk bertindak         |
        +------------------------+-----------------------+
                                 v
        +------------------------------------------------+
        | GOVERN: ada pemilik bernama & batas wewenang?  |
        +--------+-----------------------------+---------+
                 |TIDAK                        |YA
                 v                             v
      [ STOP: tanpa mandat,          +--------------------------------+
        tidak ada wewenang           | LEAD: sponsor menyampaikan    |
        untuk memutus atau membeli ] | pesan yang sama?               |
                                     +--------+-------------+--------+
                                              |TIDAK        |YA
                                              v             v
                                   [ STOP:      +--------------------------------+
                                     bangun     | SECURE: cukup paham untuk     |
                                     kesepakatan| menantang klaim & asumsi?     |
                                     dulu ]     +--------+-------------+--------+
                                                         |TIDAK        |YA
                                                         v             v
                                              [ STOP:      +--------------------------------+
                                                minta      | OPERATE: bisa berjalan &       |
                                                keahlian   | pulih dengan terukur?          |
                                                independen]+--------+-------------+--------+
                                                                    |TIDAK        |YA
                                                                    v             v
                                                         [ HOLD:      +--------------------------------+
                                                           stabilkan  | STRATEGIZE: ada uang, pemilik,  |
                                                           dulu;      | ukuran, & tanggal tinjau?     |
                                                           jangan     +--------+-------------+--------+
                                                           menambah            |TIDAK        |YA
                                                           beban ]             v             v
                                                               [ STOP:   [ TERBIT: peta jalan +
                                                                 daftar    ukuran manfaat + irama
                                                                 keinginan tinjau + daftar tertunda ]
                                                                 tanpa                    |
                                                                 pemilik ]                v
        +------------------------------------------------------------------------------------+
        | UMPAN BALIK: insiden, temuan audit, metrik, perubahan pemasok/hukum, aduan staf     |
        |                                  -> kembali ke GOVERN                              |
        +------------------------------------------------------------------------------------+
        | PENGECUALIAN: OPERATE memegang komando sementara; GOVERN tetap memegang          |
        | penerimaan risiko residual setelah pulih — HOLD di atas berlaku di sini           |
        +------------------------------------------------------------------------------------+
```

Komando insiden bersifat sementara; penerimaan risiko residual tetap keputusan tata kelola. Menggabungkan keduanya adalah kebingungan paling umum pasca-insiden.

| Gerbang | Bukti yang harus ada | Yang mengatakan "lanjut" | Jika gerbang gagal |
|---|---|---|---|
| Mandat | Piagam bertuan, batas wewenang, penandatangan sah | Sponsor eksekutif | **STOP**: tak ada dasar mengeluarkan biaya |
| Keselarasan | Sponsor mengulang pesan; keberatan dicatat | Tim pimpinan | **STOP**: bangun kesepakatan dulu |
| Kelancaran | Desain menjelaskan paparan dan asumsi | Pimpinan keamanan + insinyur | **STOP**: minta pendapat kompeten |
| Kesiapan operasi | Pemilik, ukuran, eskalasi, dan pemulihan ada | Pemilik layanan & keamanan | **HOLD**: perbaiki model operasi |
| Pendanaan | Uang, orang, ukuran manfaat, tanggal tinjau | Pemilik anggaran | **STOP**: ambisi tanpa pembelian |

Program yang matang melewati gerbang ini karena artefaknya sudah ada. Program yang lemah baru menyadari di gerbang pendanaan bahwa tidak ada yang memiliki risikonya. Insiden dan audit tidak hanya menuntut perbaikan teknis — mereka menguji apakah wewenang tertulis masih sesuai kenyataan.

---

## Govern — hak untuk memutus

**Tujuan.** Govern mengubah kekhawatiran kabur menjadi keputusan yang sah dan dapat dilacak. "Semua orang khawatir tentang data pelanggan" bukan keputusan. "Direktur operasi menerima risiko residual ini sampai 31 Maret, dengan pemicu tinjauan dua insiden serupa dan alasan tertulis" adalah keputusan. Tata kelola bukan penambah dokumen: orang yang tidak hadir dalam rapat harus dapat membela keputusan enam bulan kemudian hanya dari catatannya.

**Keputusan yang dimiliki.** Selera dan penerimaan risiko; kebijakan dan pengecualiannya; pemilik kontrol; batas antara keamanan, TI, hukum, privasi, dan bisnis; serta kapan eskalasi wajib dilakukan. Sistem manajemen keamanan informasi (*Information Security Management System*, ISMS) adalah satu struktur untuk ini, bukan seluruh tata kelola. Kewajiban hukum dibahas penasihat berwenang; artikel ini hanya kerangka berpikir.

**Artefak.** Piagam hak keputusan; registri kebijakan; registri risiko berpemilik; registri pengecualian bertanggal akhir; catatan penerimaan risiko beserta alasannya.

**Metrik.** Hitung keputusan **mutakhir dan bertuan**: risiko lewat tinjauan, pengecualian tanpa tanggal akhir, kontrol tanpa pemilik, waktu eskalasi hingga keputusan. Jumlah kebijakan mengukur ketikan.

**Mode kegagalan.** Kebijakan tak dibaca; registri hanya untuk auditur; komite yang tak pernah memutus; "bisnis sudah menerima" tanpa nama; tata kelola dianggap urusan hukum, bukan manajer lini.

**Kaitan.** Govern memberi wewenang ke Lead, membatasi Operate dan Secure, menetapkan kriteria Strategize. Insiden dan audit mengungkap wewenang yang kabur.

| Pertanyaan hak keputusan | Jawaban yang rapuh | Jawaban yang dapat dibela |
|---|---|---|
| Siapa menerima risiko residual? | "Keamanan bilang aman" | Pemilik bisnis bernama, tanggal, alasan, dan pemicu tinjauan |
| Siapa boleh menyetujui pengecualian? | "Siapa pun yang paling dekat" | Peran yang ditetapkan, kriteria tertulis, keputusan dicatat |
| Siapa pemilik sebuah kontrol? | "IT" secara umum | Peran bernama yang bertanggung jawab menjalankan dan membuktikan |
| Siapa yang menyatakan insiden? | "Tool yang berbunyi" | Peran berwenang dengan ambang batas dan wakilnya |

Yang membedakan Govern yang hidup dari yang mati adalah **pemicu tinjauan**. Risiko yang diterima tanpa pemicu menjadi kebiasaan permanen. Pemicunya boleh tanggal, perubahan pemasok, atau temuan audit; yang penting ada orang yang menyadari saat keputusan lama tidak lagi sesuai.

---

## Lead — membuat keputusan berjalan

**Tujuan.** Lead mengubah wewenang menjadi perilaku terkoordinasi. CISO yang benar secara teknis tetapi tak terlihat secara organisasi belum memimpin. Ia membingkai masalah agar eksekutif, insinyur, dan tim lini melihat apa yang diminta — dan boleh tidak setuju sebelum keputusan mengeras.

**Keputusan yang dimiliki.** Pesan dan audiens; kapan eskalasi dan kepada siapa; penanganan ketidaksepakatan; kapan mengatakan "tidak" pada permintaan yang bertentangan dengan posisi risiko yang disepakati; serta bagaimana melindungi tim dari vonis individu sambil menuntut akuntabilitas. Etika termasuk di sini: menyampaikan kabar tidak nyaman lebih awal.

**Artefak.** Peta pemangku kepentingan; ringkasan eksekutif berisi permintaan keputusan; log keputusan dan keberatan; poin pembicaraan; kontak eskalasi bernama.

**Metrik.** Keputusan yang benar-benar diambil; keputusan dibuka lagi karena premis kabur; kecepatan kabar buruk ke sponsor; rasa aman staf menyampaikan kekhawatiran (kumpulkan anonim).

**Mode kegagalan.** Briefing hanya ke atas; risiko sebagai ketakutan, bukan pilihan; menang rapat, kalah implementasi; memerintah insinyur; metrik merah disembunyikan; kepercayaan diri diira kredibilitas.

**Kaitan.** Lead memberi Govern mandat, Operate wewenang menjeda, meminjam bukti Secure, dan menjual peta jalan Strategize. Tanpa Lead, dokumen Govern tidak bergerak.

| Audiens | Yang mereka butuhkan dari CISO | Keputusan yang Anda minta |
|---|---|---|
| Dewan atau badan tata kelola | Paparan dalam bahasa bisnis, pilihan, dan rekomendasi yang jelas | Menyetujui posisi risiko atau pendanaan |
| Rekan eksekutif | Dampak pada tujuan mereka dan kewajiban yang melekat | Menerima kepemilikan atau mengubah rencana |
| Tim teknis | Alasan kontrol ada dan arti "selesai" | Mengurutkan kerja dan melaporkan hambatan |
| Hukum, privasi, audit | Fakta bersama dan batas yang terdokumentasi | Menyepakati penafsiran atau eskalasi |
| Pemasok | Persyaratan, ekspektasi bukti, dan irama tinjauan | Menerima kewajiban kontraktual |

Bedakan **mendapat persetujuan** dari **membangun pemahaman**. Persetujuan bisa diraih dengan menghemat informasi; pemahaman tidak. Menyampaikan ketidakpastian dengan jelas — "ini yang kita tahu, ini dugaan, ini yang kami periksa berikutnya" — justru meningkatkan kepercayaan. Lihat [Komunikasi Dewan & Executive Presence](../career/board-communication.md).

---

## Operate — program yang bergerak

**Tujuan.** Operate membuat program nyata pada minggu biasa maupun minggu buruk: layanan, pemantauan, insiden, kesinambungan, kesadaran, dan ukuran yang menunjukkan apakah sesuatu membaik. Program yang hanya ada di peta jalan belum beroperasi.

**Keputusan yang dimiliki.** Temuan mana yang dikerjakan dulu; kapan peristiwa menjadi insiden dan siapa komandannya; kapan layanan dijeda; bagaimana bukti dijaga; kapan hukum atau komunikasi dilibatkan; bagaimana perbaikan diverifikasi. Di sini wewenang operasional dan tata kelola terpisah praktisnya: **komandan insiden mengarahkan respons**, **pemilik risiko menerima risiko residual setelah pulih**. Keduanya tidak disatukan hanya karena orangnya sama.

**Artefak.** Katalog layanan dan indeks runbook; catatan insiden berisi titik keputusan, waktu, dan pembuatnya; kontak eskalasi; paket ukuran; pelacak perbaikan beserta kriteria verifikasi; catatan pembelajaran.

**Metrik.** Waktu deteksi dan pemulihan, insiden berjejak keputusan, perbaikan lulus uji ulang, perbandingan kerja terencana dan reaktif. Jumlah peringatan mengukur aktivitas. Kebiasaan dari [CSIX ITIL](https://siedysoes.github.io/csix-itil/) membantu, tetapi ukuran harus mencerminkan risiko sendiri.

**Mode kegagalan.** Heroik sebagai model operasi; antrean peringatan tanpa pemilik; perbaikan tanpa verifikasi; sesi pasca-insiden jadi perburuan kesalahan; ukuran dipilih karena bagus di slide; tanpa wakil komandan.

**Kaitan.** Operate memberi bukti ke Govern, kisah jujur ke Lead, ujian asumsi Secure, dan info hasil ke Strategize. Di sini umpan balik berubah jadi data.

| Ukuran yang lemah | Pertanyaan pengganti | Mengapa penting |
|---|---|---|
| Peringatan ditangani bulan ini | Paparan mana yang benar-benar berkurang? | Volume bisa naik sementara risiko ikut naik |
| Tiket ditutup | Perbaikan mana yang lulus verifikasi? | Penutupan bukan keefektifan |
| Tingkat penyelesaian pelatihan | Bisakah staf menyebut tindakan yang akan mereka ambil? | Kehadiran bukan perilaku |
| Waktu aktif layanan saja | Seberapa cepat kami memulihkan, dan apa yang kami pelajari? | Ketahanan memerlukan ukuran pemulihan |

Sering diabaikan: mencatat **keputusan yang tidak diambil**. Peringatan yang sengaja dibiarkan karena ada pengaman penyeimbang, atau perbaikan yang ditunda karena jendela pemeliharaan, perlu alasan tertulis. Tanpa itu, audit berikutnya membaca keputusan lama sebagai kelalaian.

---

## Secure — kedalaman yang cukup untuk menantang

**Tujuan.** Secure memberi pertimbangan teknis di balik klaim eksekutif. CISO tidak perlu mengonfigurasi setiap kontrol, tetapi harus mengajukan pertanyaan yang mengungkap apakah desain benar-benar melakukan apa yang dikatakan slide atau pemasok — dan tahu kapan jawaban jujurnya "kami belum tahu". Kelancaran teknis adalah alat kredibilitas, bukan alasan mengambil alih kerja spesialis.

**Keputusan yang dimiliki.** Apakah arsitektur sesuai posisi risiko; asumsi identitas, data, dan rantai pasok perangkat lunak mana yang masih diterima; kapan tinjauan independen diperlukan; bukti apa yang cukup untuk menyebut kontrol efektif; ke mana keahlian luar didatangkan. Pemimpin menginterogasi arsitektur, identitas, cloud, aplikasi, data, dan pengembangan aman pada tingkat pertanyaan — bukan konfigurasi.

**Artefak.** Katalog kontrol beserta tujuannya; catatan arsitektur dan batas kepercayaan; catatan tinjauan desain, asumsi, dan pemiliknya; tanya-jawab pemasok; catatan asumsi yang diterima sementara.

**Metrik.** Bagian perubahan material ditinjau; asumsi berdampak tinggi belum diuji; penjelasan satu halaman per kontrol kritis. Jumlah alat bukan ukuran pemahaman.

**Mode kegagalan.** Penilaian diserahkan; bahasa pemasaran jadi arsitektur; kontrol diminta tanpa tahu yang dilindungi; label "berbasis AI" jadi alasan skip tinjauan; kontrol tak bisa dijelaskan ke pembiayanya.

**Kaitan.** Secure memberi Govern uji kelayakan klaim risiko, Lead bukti, Operate peringatan yang dapat ditafsirkan, Strategize pilihan bangun-atau-beli. Pemimpin memiliki **pertanyaan**, bukan sakelar konfigurasi.

| Pertanyaan pemimpin | Jawaban yang lemah | Pertanyaan lanjutan |
|---|---|---|
| Kontrol ini melindungi apa? | "Semua" | Aset mana, ancaman mana, jalur gagal apa? |
| Di mana batas kepercayaannya? | "Ada di cloud" | Siapa yang boleh menyeberang, dan di mana jejaknya? |
| Apa yang sebenarnya dijanjikan pemasok? | "Mereka bilang patuh" | Klaim apa, dibuktikan dengan apa, ditinjau kapan? |
| Apa yang terjadi saat kontrol ini gagal? | "Tidak akan gagal" | Siapa yang dipanggil, dan apa jalur cadangannya? |

Kedalaman yang baik berarti mengenali batas diri. Meminta tinjauan independen bukan kelemahan; menyetujui desain yang tidak dipahami sambil berpura-pura paham adalah kelemahan. Pemasok boleh menjelaskan produknya, tetapi organisasi tetap memiliki asumsinya. Untuk kerangka batas dan izin, bandingkan [Metodologi Penetration Testing](https://siedysoes.github.io/csix-ecsa/id/fundamentals/pentest-methodology/) — tanpa membawa prosedur teknisnya ke rapat eksekutif.

---

## Strategize — arah yang benar-benar didanai

**Tujuan.** Strategize mengubah empat domain sebelumnya menjadi arah yang tahan uji anggaran: pilihan dibiayai, bertuan, bertergantungan, dan memiliki cara mengetahui keberhasilannya. Strategi yang tak bisa menjawab "berapa orang, sampai kapan, apa yang berubah" belum menjadi strategi.

**Keputusan yang dimiliki.** Risiko mana dibiayai dulu; mana masuk peta jalan dan mana menjadi komitmen operasi; pilihan bangun, beli, atau bermitra; ketergantungan pemasok; ukuran manfaat; dan apa yang secara eksplisit **tidak** dilakukan. Mengatakan "tidak" adalah keputusan strategis yang perlu dicatat.

**Artefak.** Peta jalan bertitik tinjau; studi kasus usaha per inisiatif; ukuran manfaat dan nilai awal (*baseline*); registri pemasok; pengeluaran modal versus berulang; daftar tertunda beralasan.

**Metrik.** Item peta jalan bertuan dan berukuran manfaat; ketepatan urutan; apakah indikator risiko yang mendasari pendanaan benar-benar bergerak. Pengiriman sempurna dengan paparan tetap adalah peringatan.

**Mode kegagalan.** Strategi dari alat; katalog tanpa urutan; studi kasus tanpa *counterfactual*; biaya pemeliharaan diabaikan; klaim vendor jadi bukti manfaat; risiko pemasok dianggap bukan risiko sendiri.

**Kaitan dengan domain lain.** Strategize menerima wewenang dari Govern, narasi dari Lead, desain dari Secure, dan bukti dari Operate, lalu mengembalikan rencana dibiayai. Daftar tertunda dikembalikan ke Govern agar pengorbanan tercatat — penerimaan risiko karena kelalaian sering lebih berbahaya daripada yang disengaja.

| Pertanyaan strategis | Bukti yang dibawa | Keputusan yang dicatat |
|---|---|---|
| Mengapa inisiatif ini sekarang? | Risiko dan bukti insiden terkini | Prioritas dan biaya peluang |
| Apa yang berubah jika didanai? | Ukuran manfaat dengan nilai awal | Hasil yang diharapkan, bukan sekadar keluaran |
| Berapa biaya untuk mempertahankannya? | Upaya operasi, keahlian, biaya pemasok | Komitmen seumur hidup, bukan harga pembelian |
| Apa yang tidak kami lakukan? | Daftar tertunda beralasan | Pertukaran nilai yang terlihat |

Tiga pertanyaan menyelamatkan peta jalan dari menjadi brosur: apa yang terjadi jika inisiatif ini **tidak** dibiayai, siapa yang membuktikan manfaatnya nanti, dan kapan kami berhenti bila bukti menunjukkan arah lain. Pertanyaan terakhir paling sulit secara politik, paling murah secara finansial. Lihat [Risiko, Keuangan & Tata Kelola Vendor](../career/risk-finance.md) dan [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md).

---

## Peta interaksi antardomain

Setiap baris adalah **serah terima**: satu domain menyelesaikan kalimat, domain lain melanjutkannya. Serah terima informal menciptakan celah yang baru terlihat saat insiden atau audit datang.

| Dari → ke | Artefak serah terima | Keputusan yang dimungkinkan | Yang rusak jika serah terima gagal |
|---|---|---|---|
| Govern → Lead | Piagam hak keputusan dan posisi risiko | Pemimpin tahu apa yang boleh ia janjikan | Janji publik melampaui wewenang |
| Lead → Govern | Log keputusan yang memuat keberatan | Kebijakan direvisi sebelum mengeras | Ketidakpatuhan diam-diam |
| Secure → Govern | Tinjauan desain dan asumsi yang dinyatakan | Penerimaan risiko berpijak pada kenyataan | Risiko diterima berdasarkan brosur |
| Govern → Operate | Ambang batas, jalur eskalasi, daftar pemilik | Komandan insiden tahu batasnya | Tidak ada yang tahu siapa boleh menjeda |
| Operate → Govern | Catatan insiden dan hasil verifikasi | Risiko residual diperbarui dengan bukti | Registri risiko menjauh dari kenyataan |
| Lead → Operate | Pesan sponsor dan kontak eskalasi | Tim berani menghentikan kerja | Penahanan terlambat dan budaya menyalahkan |
| Secure → Operate | Tujuan kontrol dan ekspektasi deteksi | Peringatan dapat ditafsirkan | Noise yang tidak bisa ditindaklanjuti |
| Operate → Strategize | Ukuran hasil dan pembelajaran | Uang mengalir ke apa yang mengubah hasil | Pendanaan mengikuti keluhan paling keras |
| Strategize → Secure | Pekerjaan arsitektur yang didanai dan batasnya | Desain sesuai kemampuan yang terjangkau | Rencana indah yang tidak bisa dirawat |
| Strategize → Govern | Peta jalan dan daftar tertunda | Govern meninjau apa yang dikorbankan | Penerimaan risiko tanpa catatan karena kelalaian |

### Satu risiko, lima domain

Sebuah perusahaan fiktif bergantung pada satu penyedia eksternal untuk pengolahan data. Ikuti jejaknya:

- **Govern** menetapkan pemilik dan batas gangguan yang diterima — tanpa ini, tidak ada yang bisa menilai apakah pemadaman tiga jam "biasa".
- **Lead** memastikan eksekutif dan pemilik layanan memahami ketergantungan itu; keberatan dicatat.
- **Operate** menguji deteksi, komando, pemberitahuan pelanggan, dan waktu pemulihan.
- **Secure** menanyakan data yang melintasi batas, identitas dipercaya, dan asumsi yang diuji — tanpa tindakan ofensif.
- **Strategize** membiayai alternatif atau menerima ketergantungan bertanggal tinjau, sambil mencatat yang tertunda.

Itu lima keputusan yang masing-masing punya pemilik dan artefak.

---

## Tiga studi kasus fiktif

Ketiga kasus di bawah rekaan, tanpa prosedur teknis maupun nasihat hukum. Mereka menunjukkan keputusan saat informasi tidak lengkap dan tekanan datang dari arah berbeda.

### Kasus 1 — Pabrik Tiga Tungku: wewenang menjeda lini produksi

**Konteks.** Pabrik makanan dengan 180 karyawan memiliki penjadwalan produksi yang terhubung ke jaringan kantor. Manajer pabrik mengusulkan pemisahan jaringan, tetapi pembaruan perangkat lama memerlukan penghentian lini satu shift. Asuransi memperbarui polis dan meminta bukti pengelolaan risiko, bukan daftar perangkat.

**Batasan.** Produksi tidak boleh berhenti saat pesanan besar diproses. Tim TI hanya dua orang. Manajer pabrik khawatir keamanan akan mematikan mesin tanpa pemberitahuan. Tidak ada anggaran khusus tahun ini.

**Keputusan yang diambil.** Govern menulis piagam satu halaman: manajer pabrik berwenang menjeda produksi, pimpinan keamanan hanya boleh mengusulkan jeda pada ambang batas tertentu, direktur operasi menerima risiko residual dengan tanggal tinjauan. Lead mengulang pesan itu ke mandor dan pembelian, serta mencatat keberatan manajer pabrik. Secure menjelaskan batas jaringan kantor dan produksi dalam bahasa proses beserta tiga asumsi yang belum diuji. Operate memilih dua ukuran — waktu pemulihan jadwal dan jumlah jeda disetujui — serta kontak eskalasi bernama. Strategize membiayai pemisahan kuartal berikutnya dan mencatat tertunda pengadaan pengganti beserta alasannya.

**Apa yang diajarkan.** Keputusan terpenting bukan soal perangkat, melainkan siapa boleh menghentikan mesin dan siapa menerima konsekuensinya. Piagam satu halaman mengubah ketakutan menjadi ambang batas yang dapat diuji.

### Kasus 2 — Laut Biru: temuan audit yang tidak bisa ditambal dalam satu minggu

**Konteks.** Lembaga keuangan kecil memiliki temuan audit internal atas tinjauan hak akses yang terlambat. Platform inti tidak bisa diganti dalam satu siklus perencanaan. Dewan meminta kepastian; tim operasi lelah menjawab pertanyaan yang sama.

**Batasan.** Staf frontliner menolak langkah yang memperlambat layanan. Pandangan hukum dan privasi tumpang tindih. Jawaban audit bertenggat, perbaikan sistem butuh waktu lebih lama.

**Keputusan yang diambil.** Govern memperlakukan temuan sebagai masalah kepemilikan dan bukti, bukan alat: eksekutif bernama menerima risiko residual; registri pengecualian memuat tanggal akhir dan pemicu tinjauan. Lead menyampaikan paparan berisi pilihan, bukan daftar kontrol, dan mencatat keberatan perwakilan layanan pelanggan. Secure menegaskan akun mana yang menyentuh data nasabah, pengaman mana yang bekerja, dan mana yang masih diasumsikan. Operate memperbaiki alur tinjauan dan memverifikasi penyelesaian, bukan menerima tanda tangan. Strategize membiayai proses sementara sekarang, perubahan platform kemudian, dukungan pemasok di antaranya.

**Apa yang diajarkan.** Rantai artefak adalah produk utamanya. Bukti memungkinkan Govern menerima pengecualian dengan jujur, Lead mencegah kepanikan, dan Strategize mengubah temuan menjadi urutan investasi.

### Kasus 3 — Kirim Cepat: setelah insiden, bukan sekadar reorganisasi

**Konteks.** Perusahaan distribusi baru memulihkan layanan setelah gangguan berjam-jam. Tinjauan awal menemukan versi bertentangan tentang siapa boleh menjeda layanan, siapa berbicara kepada pelanggan, dan keputusan apa yang dibuat dari informasi belum lengkap.

**Batasan.** Pelanggan meminta jaminan, tim respons kelelahan, beberapa staf takut disalahkan, pimpinan ingin pengumuman restrukturisasi segera.

**Keputusan yang diambil.** CISO memisahkan dua jalur. Operasi menutup insiden dengan linimasa terverifikasi dan sesi pembelajaran tanpa vonis individu, tetapi dengan pemilik perbaikan jelas. Tata kelola menulis ulang piagam: komando insiden, komunikasi eksternal, dan penerimaan risiko residual menjadi tiga peran terpisah, masing-masing berwakil. Lead menyampaikan apa yang berubah dan apa yang belum tanpa menjanjikan mustahilnya keulangan. Secure menandai asumsi gagal dan mewajibkan tinjauan desain. Operate mengganti jumlah tiket dengan waktu pemulihan, jeda keputusan, dan pemilik tercatat. Strategize membiayai identitas dan pemulihan lebih dulu, dengan alasan tertulis untuk yang ditunda. Latihan triwulan menguji peran baru.

**Apa yang diajarkan.** Insiden adalah uji stres tata kelola. Memindahkan kotak pada bagan organisasi menyisakan ambiguitas yang sama. Perbaikan awet adalah wewenang jelas, ukuran jujur, dan pendanaan nyata.

---

## Latihan: latih keputusan, bukan hafalan kosakata

Jawablah sebelum membuka kunci. Lima belas skenario, tiga per domain, menguji pertimbangan — bukan ingatan istilah.

### Govern

**Q1.** Manajer mengatakan tim "sudah menerima secara lisan" risiko residual tinggi. Apa yang masih Anda butuhkan?

<details><summary>Kunci Q1</summary>
**A1.** Pemilik bernama, tanggal, alasan, pemicu tinjauan, dan entri registri risiko. Percakapan membuktikan diskusi, bukan wewenang.
</details>

**Q2.** Temuan audit menyebut "IT" sebagai pemilik kontrol. Apa langkah pertama Anda?

<details><summary>Kunci Q2</summary>
**A2.** Ubah "IT" menjadi peran bernama yang menjalankan kontrol dan menghasilkan bukti; konfirmasi serta catat penerimaan risikonya.
</details>

**Q3.** Pengecualian kebijakan disetujui tanpa tanggal berakhir. Mengapa itu cacat tata kelola?

<details><summary>Kunci Q3</summary>
**A3.** Tanpa tanggal akhir, pengecualian permanen karena diam. Pimpinan berikutnya tak bisa membedakan pilihan sadar dari kelalaian.
</details>

### Lead

**Q4.** Insinyur bilang kontrol baru memperlambat rilis, dan Anda yakin itu perlu. Apa langkah berikutnya?

<details><summary>Kunci Q4</summary>
**A4.** Tanyakan langkah rilis yang terdampak, nyatakan risiko dalam bahasa bisnis, tawarkan pengurutan atau uji coba. Jangan menang argumen lalu kalah saat implementasi.
</details>

**Q5.** Dewan meminta satu angka, tetapi ukuran Anda beragam dan ada yang merah. Bagaimana Anda menjawab?

<details><summary>Kunci Q5</summary>
**A5.** Sampaikan keputusan dan tren di balik angka, jelaskan item merah sebagai paparan yang dikelola, undang keputusan. Jangan memampatkan gambaran jujur menjadi angka menenangkan.
</details>

**Q6.** Seorang rekan diam-diam tidak setuju dengan posisi risiko dalam rapat. Apa yang Anda catat?

<details><summary>Kunci Q6</summary>
**A6.** Keberatannya, premis yang digugat, dan apa yang ditunda. Catatan mencegah konsensus palsu.
</details>

### Operate

**Q7.** Insiden tertangani dan tim ingin menutupnya. Bukti apa yang Anda minta dulu?

<details><summary>Kunci Q7</summary>
**A7.** Verifikasi terhadap kriteria awal: fakta teramati, verifikator, item terbuka, dan pembaruan registri risiko. Penutupan adalah keputusan, bukan rasa lega.
</details>

**Q8.** Dasbor menunjukkan dua ribu peringatan ditangani bulan ini. Pertanyaan apa yang menggantikannya?

<details><summary>Kunci Q8</summary>
**A8.** Paparan mana yang menurun, seberapa cepat layanan dipulihkan, perbaikan mana yang lulus verifikasi. Volume mengukur kerja, bukan risiko.
</details>

**Q9.** Saat insiden, pimpinan meminta jeda karena peluncuran pelanggan. Siapa memutus dan bagaimana dicatat?

<details><summary>Kunci Q9</summary>
**A9.** Komandan insiden memegang penahanan dalam batas Govern; pertukaran nilai bisnis dieskalasi. Catat waktu, keputusan, orang, dan alasan.
</details>

### Secure

**Q10.** Pemasok menyebut produknya "berbasis AI dan otomatis patuh". Apa pertanyaan pertama Anda?

<details><summary>Kunci Q10</summary>
**A10.** Klaim spesifik apa, bukti apa, dinilai siapa, kapan. Perlakukan frasa itu sebagai pemasaran sampai menjadi klaim yang dapat diuji.
</details>

**Q11.** Desain baru menempatkan data sensitif di layanan baru. Apa yang harus dipastikan sebelum menyetujui?

<details><summary>Kunci Q11</summary>
**A11.** Batas kepercayaan, siapa mengakses data, identitas dan jejak, asumsi belum diuji, jalur saat kontrol gagal. Catat asumsi beserta pemiliknya.
</details>

**Q12.** Anda tidak bisa memverifikasi sendiri konfigurasi cloud yang kompleks. Apa perilaku eksekutif yang tepat?

<details><summary>Kunci Q12</summary>
**A12.** Katakan terus terang, datangkan tinjauan independen, catat penasihat dan dasarnya. Kelancaran mencakup pengetahuan tentang batas diri.
</details>

### Strategize

**Q13.** Item peta jalan selesai dibangun, tetapi indikator risikonya tidak bergerak. Apa kesimpulan Anda?

<details><summary>Kunci Q13</summary>
**A13.** Keluaran keliru dianggap hasil. Periksa nilai awal dan ukuran, lalu sesuaikan, hentikan, atau alihkan pendanaan.
</details>

**Q14.** Pemasok menjanjikan penghematan besar, tetapi akan sangat kritikal. Apa yang masuk studi kasus usaha?

<details><summary>Kunci Q14</summary>
**A14.** Biaya seumur hidup termasuk jalur keluar, konsentrasi risiko, nilai awal manfaat, bukti klaim penghematan, irama tinjauan. Harga bukan studi kasus usaha.
</details>

**Q15.** Ada lebih banyak inisiatif layak daripada kapasitas. Apa yang Anda hasilkan dan kepada siapa?

<details><summary>Kunci Q15</summary>
**A15.** Peta jalan berurutan plus daftar tertunda, alasan, pemilik, titik tinjau — disetujui Govern, disampaikan Lead. "Tidak" yang tak tercatat adalah risiko tak terlihat.
</details>

---

## Kesalahan umum yang perlu dihafal

- **Lensa menjadi kotak:** Govern = administrasi, Lead = slide, Operate = help desk, Secure = rekayasa, Strategize = spreadsheet.
- **Alat lebih dulu:** platform dibeli sebelum pemilik risiko ditunjuk.
- **Wewenang karena posisi:** senioritas diira hak menerima risiko.
- **Menghitung, bukan memutus:** jumlah temuan disajikan sebagai penurunan risiko.
- **Teater metrik:** ukuran dipilih agar laporan terlihat baik.
- **Penerjemah pemasok:** klaim vendor diulang tanpa bukti.
- **Amnesia insiden:** rutinitas kembali tanpa registri dan hak keputusan diperbarui.
- **Vonis sebagai metode:** tinjauan menghukum pelapor, bukan membuka wewenang kabur.
- **Kelancaran diserahkan:** pemasok menjelaskan arsitektur organisasi sendiri.
- **Ambisi tanpa dana:** peta jalan tanpa "tidak" dan tanggal tinjau.
- **Obat salah ruang:** kontrol teknis untuk pertanyaan tata kelola.

---

## Template yang bisa disalin

Salin kerangka ini ke catatan. Template kosong tidak membuktikan apa pun; nilainya muncul saat diisi jujur.

### Lembar pemetaan domain

Tuliskan **keputusan spesifik yang Anda pengaruhi**, bukan jabatan. Tanpa artefak yang bisa diperiksa, Anda kemungkinan besar hanya mengamati.

| Domain | Keputusan yang saya pengaruhi | Artefak yang dapat diperiksa | Siapa yang terbantu | Keyakinan (tinggi / sedang / rendah) |
|---|---|---|---|---|
| Govern | | | | |
| Lead | | | | |
| Operate | | | | |
| Secure | | | | |
| Strategize | | | | |

### Catatan hak keputusan

```
Keputusan:        [satu kalimat, apa yang dipilih]
Pemilik domain:   [Govern / Lead / Operate / Secure / Strategize]
Peran akuntabel:  [nama atau peran, bukan "IT" atau "perusahaan"]
Dikonsultasikan:  [peran, termasuk keberatan bila ada]
Bukti digunakan:  [artefak beserta tanggalnya]
Risiko diterima:  [yang tersisa, oleh siapa, sampai kapan]
Pemicu tinjauan:  [tanggal atau peristiwa yang membuka kembali keputusan]
Disampaikan ke:   [audiens dan tanggal]
```

### Daftar periksa serah terima

| Serah terima | Artefak terlampir | Pemilik bernama | Tanggal | Titik tinjau |
|---|---|---|---|---|
| Govern → Lead | | | | |
| Lead → Operate | | | | |
| Secure → Govern | | | | |
| Operate → Strategize | | | | |
| Strategize → Govern | | | | |

### Irama mingguan

```
Senin:    Keputusan apa yang tersendat, dan oleh domain mana?
Rabu:     Bukti apa yang mengubah posisi risiko minggu ini?
Jumat:    Ukuran apa yang akan membuat kami mengubah peta jalan?
Bulanan:  Risiko diterima atau pengecualian apa yang kedaluwarsa tanpa tinjauan?
Triwulan: Inisiatif dibiayai mana yang mengubah hasil, dan apa yang kami hentikan?
```

### Prompt STOP / HOLD

```
Pemicu:       [apa yang terjadi]
Gerbang domain:[gerbang mana yang gagal]
Wewenang:     [siapa yang harus memutus]
Bukti kurang: [apa yang belum ada]
Pilihan:      [lanjut / persempit / tunda / hentikan]
Keputusan:    [dicatat, bertanggal, disampaikan]
```

### Pelacakan satu risiko lintas domain

| Risiko | Pemilik (Govern) | Pesan & keberatan (Lead) | Bukti operasi (Operate) | Asumsi (Secure) | Pendanaan & tertunda (Strategize) |
|---|---|---|---|---|---|
| Ketergantungan pemasok kritis | | | | | |

---

## Glosarium

| Istilah | Arti dengan bahasa sederhana |
|---|---|
| **Hak keputusan** | Siapa yang boleh memutus apa, beserta batasnya |
| **Penerimaan risiko** | Keputusan tertulis dan bertanggung jawab untuk hidup dengan risiko residual |
| **Risiko residual** | Yang tersisa setelah kontrol dijalankan |
| **Artefak** | Catatan yang dapat diperiksa: piagam, registri, ringkasan, peta jalan |
| **ISMS** | Sistem manajemen keamanan informasi; struktur pengelolaan, bukan seluruh tata kelola |
| **Registri risiko** | Daftar hidup berisi risiko, pemilik, perlakuan, dan tanggal tinjau |
| **Registri pengecualian** | Penyimpangan dari kebijakan yang disetujui, lengkap dengan pemilik dan tanggal akhir |
| **Pemilik kontrol** | Peran bernama yang bertanggung jawab atas jalannya kontrol dan buktinya |
| **Jalur eskalasi** | Rute dan kontak yang disepakati untuk keputusan yang tidak bisa diambil lokal |
| **KRI** | *Key risk indicator*: ukuran yang memberi tanda apakah paparan berubah |
| **Kondisi henti** | Peristiwa yang disepakati yang menuntut jeda dan penegasan kembali wewenang |
| **Umpan balik** | Jalur kembalinya insiden, metrik, dan perubahan ke tata kelola |
| **Peta jalan** | Rangkaian perubahan berurutan yang didanai, memiliki pemilik dan titik tinjau |
| **Ukuran hasil** | Bukti bahwa risiko benar-benar turun, bukan sekadar jumlah pekerjaan |
| **Daftar tertunda** | Pekerjaan layak yang sengaja tidak dibiayai, beserta alasannya |

---

## Referensi dan verifikasi

- **ISO/IEC 27001** — standar sistem manajemen keamanan informasi. Edisi yang banyak dipakai adalah **ISO/IEC 27001:2022**, tetapi edisi, amandemen, dan tanggal berlakunya wajib diverifikasi di [ISO](https://www.iso.org/) sebelum mengutip klausul. **ISO/IEC 27002** memberi panduan kontrol; cek versinya terpisah.
- **NIST Cybersecurity Framework (CSF)** — kerangka berbasis hasil; rilis **CSF 2.0** menjadi rujukan umum, tetapi periksa [NIST](https://www.nist.gov/cyberframework) untuk yang terbaru. Fungsi "Govern" di CSF **bukan** domain Govern di sini; keduanya tak saling menggantikan.
- **COBIT** — kerangka tata kelola TI ISACA; keluarga **COBIT 2019** sering dijumpai, tetapi edisi berubah. Verifikasi di [ISACA](https://www.isaca.org/).
- **MITRE ATT&CK** — basis pengetahuan publik tentang perilaku pihak lawan; di sini hanya rujukan defensif, **bukan** instruksi. Nomor versi dan tanggal rilis berubah; cek [MITRE ATT&CK](https://attack.mitre.org/).
- **Publikasi risiko NIST** — misalnya SP 800-30, berguna untuk kosakata penilaian risiko. Konfirmasi status dan penerusnya di NIST.
- **Kanal resmi penerbit** — [eccouncil.org](https://www.eccouncil.org/) dan [cert.eccouncil.org](https://cert.eccouncil.org/). Bahan ditinjau **26 Nov 2026** memakai merek **CCISO v4 — AI-Enhanced**. Nama domain, syarat, dan kebijakan dapat berubah; verifikasi pada hari bertindak. Tidak ada bobot domain atau angka ujian di sini.
- **Kebijakan organisasi, kewajiban hukum, dan penasihat profesional** mengalahkan kerangka publik. Ikuti yang paling ketat dan minta klarifikasi tertulis.

Verifikasi berkala, bukan sekali. Simpan URL dan tanggal pengecekan. Statistik vendor adalah klaim pemasaran, bukan bukti independen.

## Sumber pendamping

Tautan situs publik berikut memakai placeholder `https://siedysoes.github.io/...`; ganti `siedysoes` dengan nama pemilik repositori saat publikasi:

- [Pendamping CSIX ISO 27001 — struktur ISMS](https://siedysoes.github.io/csix-iso27001/)
- [Pendamping CSIX COBIT — tata kelola TI enterprise](https://siedysoes.github.io/csix-cobit/)
- [Pendamping CSIX ITIL — kebiasaan manajemen layanan](https://siedysoes.github.io/csix-itil/)
- [Beranda CSIX CCISO v4](https://siedysoes.github.io/csix-cciso/)
- [Metodologi Penetration Testing — kerangka batas dan izin](https://siedysoes.github.io/csix-ecsa/id/fundamentals/pentest-methodology/)

## Lihat juga

- [Apa Itu CCISO v4](what-is-cciso.md)
- [CCISO vs CISSP & Kredensial Leadership Lain](cciso-vs-cissp.md)
- [Peran CISO: Dari Teknis ke Eksekutif](ciso-role.md)
- [Syarat: CCISO Penuh & Jalur Associate](../exam/eligibility.md)
- [Format Ujian & Blueprint CCISO](../exam/exam-format.md)
- [Rencana Belajar Praktis](../exam/study-plan.md)
- [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md)
- [Biaya, Masa Berlaku & CPD](../exam/cost-validity.md)
- [Komunikasi Dewan & Executive Presence](../career/board-communication.md)
- [Risiko, Keuangan & Tata Kelola Vendor](../career/risk-finance.md)
- [Tata Kelola AI: Realita Lapangan](../career/ai-governance.md)
- [Karier Setelah CCISO](../career/cciso-careers.md)
