# Tata Kelola AI: Realita Lapangan

> **Sumber belajar independen, bukan resmi.** EC-Council, CCISO, CISSP, CISM,
> ISO, NIST, dan nama serupa adalah merek dagang pemiliknya. Kami tidak
> berafiliasi dengan EC-Council, tidak memuat materi kursus resmi maupun bocoran
> ujian. Merek kami: **CSIX CCISO v4**. Label **CCISO v4 / AI-Enhanced** tercatat
> pada materi EC-Council yang diperiksa **26 November 2026**; verifikasi ulang
> halaman penerbit. Statistik vendor adalah **klaim pemasaran**, bukan jaminan.
> Artikel ini edukasi pertahanan dan kepemimpinan — bukan nasihat hukum,
> regulasi, keuangan, pajak, atau investasi, serta tanpa prosedur ofensif.

## Tujuan pembelajaran

Setelah menyelesaikan artikel ini, Anda seharusnya mampu:

1. Mendefinisikan **sistem AI** untuk keperluan tata kelola dan menjelaskan
   mengapa kepemilikan, bukan arsitektur model, menjadi titik awal.
2. Menyusun inventaris sistem AI dan mengklasifikasikannya memakai tingkatan
   dampak yang dinyatakan, termasuk penggunaan *shadow AI* yang belum disetujui.
3. Mengubah skenario risiko menjadi kontrol, persyaratan bukti, dan pemilik
   bernama di dalam register risiko.
4. Menjelaskan arti *lineage* dan retensi data untuk prompt, keluaran, log, dan
   sumber pengambilan (*retrieval*).
5. Membedakan pengawasan manusia yang benar-benar berfungsi dari sekadar
   stempel, serta menentukan kapan keluaran harus dieskalasi.
6. Menyesuaikan prosedur respons insiden yang sudah ada untuk sistem berbasis
   AI tanpa membuat proses paralel yang terputus dari tim lain.
7. Mengajukan pertanyaan pengadaan yang menguji klaim vendor, bukan
   mengulangnya sebagai keyakinan sendiri.
8. Memindai sumber regulasi dan kerangka kerja tanpa mengklaim kepatuhan yang
   tidak bisa Anda pertanggungjawabkan.

Jika poin 2, 3, dan 5 masih abstrak, Anda bisa berdiskusi tentang "etika AI"
dengan lancar tetapi belum siap mengawasi sistem produksi. Kesenjangannya ada
pada artefak, pemilik, dan bukti.

---

## Ini urusan tata kelola, bukan kelas rekayasa

Yang kami sebut **sistem AI** adalah produk, fitur, atau alur kerja yang
memakai model — statistik, generatif, atau bantuan aturan — untuk menghasilkan
keluaran yang ditindaklanjuti orang atau proses. Chatbot, peringkat lamaran,
skor penipuan, ramalan, dan peringkas rapat masuk kategori ini.

Anda tidak perlu melatih model untuk mengawasinya. Keputusan CISO berkisar pada
empat hal: **siapa pemilik keluaran, data apa yang masuk, bagaimana kesalahan
terdeteksi, dan siapa yang boleh menghentikannya**. Insinyur bertanya cara
kerja; pemimpin bertanya kapan penggunaan bisa diterima.

Tiga pola kegagalan paling sering muncul:

- **Tidak bertuan** — alat dipakai, tidak ada yang bertanggung jawab, keamanan
  tahu saat audit lain.
- **Tidak terukur** — demo meyakinkan, tetapi tidak ada uji dengan data sendiri
  atau definisi "cukup baik".
- **Tidak dapat direkonstruksi** — keputusan material diambil tanpa catatan
  input, keluaran, penimpaan, atau wewenang.

Kelima domain CCISO menjadi wadahnya. Peta ini bukan klaim blueprint ujian.

| Domain | Pertanyaan era AI | Artefak yang bisa ditunjukkan pemimpin |
|---|---|---|
| **Govern** | Siapa yang bertanggung jawab atas keputusan? | Pemilik bernama, catatan intake, log pengecualian |
| **Lead** | Bagaimana kita mendengar adopsi alat yang diam-diam terjadi? | Kanal pelaporan, kontak eskalasi, status yang rutin disampaikan |
| **Operate** | Bagaimana kita mendeteksi pergeseran perilaku dan keluaran buruk? | Ambang pemantauan, log keputusan, buku panduan respons |
| **Secure** | Data, izin, dan jalur penyalahgunaan apa yang ada? | Catatan alur data, tinjauan akses, keputusan retensi |
| **Strategize** | Klaim dan biaya vendor mana yang benar-benar nyata? | Hasil evaluasi, syarat kontrak, rencana keluar |

Prinsip tanpa artefak hanya poster; artefak membuatnya bisa diaudit. Untuk
keseluruhan lima domain, lihat [Lima Domain: Govern hingga Strategize](../fundamentals/five-domains.md).

---

## Mulai dari inventaris: Anda tidak bisa mengawasi apa yang tidak Anda sebut

Kontrol pertama adalah **register sistem AI** — tidak seglamir kebijakan, jauh
lebih berguna. Cakupannya: sistem buatan sendiri, produk vendor, fitur tersemat,
dan **shadow AI** (alat dipakai tanpa persetujuan). Shadow AI biasanya berawal
dari tenggat yang ketemu kemudahan, bukan niat buruk. Kanal "datanglah agar kami
bisa membantu" menemukan lebih banyak sistem daripada larangan.

Catatan minimal: tujuan; pemilik dan kontak; vendor serta model; data masuk dan
sensitivitasnya; keluaran dan penerima; integrasi dan izin; tinjauan manusia;
pembalikan; kelompok terdampak; tingkat; tanggal tinjauan; tautan ke evaluasi
dan risiko.

Klasifikasikan berdasarkan **konsekuensi**, bukan berdasarkan kemewahan
teknologinya:

| Tingkat | Contoh | Taruhannya | Tata kelola minimum | Tinjauan |
|---|---|---|---|---|
| **T0 — Dilarang** | Tidak ada dasar yang diterima organisasi, atau penggunaan yang memang ditolak | Tidak dapat diterima menurut kebijakan | Jangan menjalankan; catat penolakannya | Saat ada tantangan |
| **T1 — Rendah** | Peringkas catatan internal, draf komunikasi | Dapat dibatalkan, tidak berdampak ke luar | Pemilik, catatan penggunaan wajar, log dasar | Tahunan |
| **T2 — Sedang** | Bantuan konten pelanggan, analitik internal | Dapat dibalik dengan usaha; dampak komersial | Alur data, uji dengan data sendiri, peninjau bernama, keputusan retensi | Triwulan / saat berubah |
| **T3 — Tinggi** | Perekrutan, kredit, kesehatan, keselamatan, akses, hak | Sulit dibalik; orang terdampak mungkin tidak tahu | Penilaian dampak, uji bias dan galat, tinjauan bermakna, jalur sanggah, tanda tangan eksekutif | Sebelum peluncuran dan berkelanjutan |

Penentuan tingkat adalah keputusan, bukan label vendor. Chatbot yang sama
berada di T1 ketika merangkum dokumentasi publik, dan di T3 ketika memberi
saran kelayakan bantuan. Jika ragu, tentukan tingkat dari keluaran paling
sensitif yang bisa dibayangkan, lalu minta bukti untuk menurunkannya.

### Alur intake dengan cabang STOP dan ESCALATE

Ini adalah **proses persetujuan**, bukan prosedur teknis. Tujuannya
mencegah permintaan yang belum lengkap menjadi sistem produksi karena
momentum rapat.

```
                  +-------------------------------------+
                  | Permintaan atau ide dari bisnis     |
                  +----------------+--------------------+
                                   v
                  +-------------------------------------+
                  | 1. Pemilik bernama + tujuan jelas?  |
                  +------+----------------------+------+
                         | TIDAK                | YA
                         v                      v
                  [ STOP:            +----------------------------------+
                   tidak ada         | 2. Kenali jenis + data masuk    |
                   pemilik ]         +------+-------------------+------+
                                            | BELUM JELAS       | JELAS
                                            v                   v
                                    [ ESCALATE:        +----------------------------------+
                                      privacy /       | 3. Tetapkan tingkat dampak       |
                                      data dulu ]     +------+-------------------+------+
                                                             | TIDAK             | YA
                                                             v                   v
                                                     [ ESCALATE:        +----------------------------------+
                                                       penilai         | 4. Syarat vendor + penggunaan data|
                                                       menetapkan     +------+-------------------+------+
                                                       tingkat               | KABUR             | JELAS
                                                                              v                   v
                                                                     [ STOP:            +----------------------------------+
                                                                       celah           | 5. Evaluasi + tinjauan manusia  |
                                                                       kontrak         + rollback didefinisikan        |
                                                                       dicatat ]       +------+-------------------+------+
                                                                                             | GAGAL             | LULUS
                                                                                             v                   v
                                                                                    [ STOP:            [ SETUJU PILOT ]
                                                                                      desain ulang ]
                                                                                                     |
                                                                                                     v
                                                                                   [ PANTAU -> GERBANG TINJAUAN ]
                                                                                     |DRIFT        |OK
                                                                                     v             v
                                                                              [ HENTIKAN    [ LANJUT + catat
                                                                               + ESCALATE    keputusan ]
                                                                               + NOTIFIKASI ]
```

**STOP** berarti tidak ada peluncuran sampai celahnya diisi. **ESCALATE**
berarti pemilik intake memanggil fungsi bernama — privasi, hukum, pengadaan,
atau komite risiko. Keduanya dicatat supaya celah yang sama tidak muncul lagi
bulan depan. Peran CISO dalam memberi wewenang ini dibahas lebih lanjut di
[Peran CISO: Dari Teknis ke Eksekutif](../fundamentals/ciso-role.md).

---

## Penilaian risiko dan dampak: dari skenario ke kontrol

Likelihood kali impact adalah titik awal, tetapi risiko AI sering tersembunyi
di satu angka. Tambahkan lima pertanyaan:

- **Siapa terdampak?** Pelanggan, karyawan, kandidat, atau masyarakat?
- **Bisakah dibalik?** Draf salah bisa disunting; lamaran ditolak bisa
  menimbulkan kerugian sebelum siapa pun sadar.
- **Seberapa otonom?** Rekomendasi yang bisa diabaikan berbeda dari tindakan
  otomatis.
- **Seberapa luas?** Satu jawaban, satu templat, atau ribuan keputusan?
- **Apakah ada yang tahu?** Kegagalan sunyi tidak punya umpan balik.

Petakan skenario ke kontrol **dan ke bukti bahwa kontrol itu bekerja**. Kontrol
tanpa bukti hanyalah keyakinan.

| Skenario risiko | Sinyal awal | Kontrol | Bukti kontrol bekerja | Pemilik |
|---|---|---|---|---|
| Data sensitif dalam prompt dipakai ulang vendor | Kontrak mengizinkan pelatihan; retensi tidak jelas | Klausul penggunaan data, klasifikasi, redaksi | Syarat ditandatangani plus sampel prompt ditinjau | Pengadaan + pemilik data |
| Keluaran salah mendorong keputusan pelanggan | Eskalasi naik pada satu topik | Batas lingkup, tinjauan wajib, jalur koreksi | Penimpaan tercatat; galat turun pada sampel uji | Pemilik bisnis |
| Bias dalam penyaringan atau penilaian | Tingkat seleksi menyimpang antarkelompok | Uji keadilan sebelum peluncuran, set representatif, uji ulang | Definisi metrik, hasil, dan keputusan perbaikan | Komite risiko |
| Data lintas pelanggan terekspos lewat retrieval | Pengambilan mengembalikan konten tenant lain | Retrieval sadar izin, hak least privilege, uji isolasi | Tinjauan akses dan hasil uji isolasi | Pemilik platform |
| Karyawan menempel data teratur ke alat tak disetujui | Domain asing muncul dalam data penggunaan | Daftar alat resmi, kanal pelaporan, sinyal DLP | Laporan selesai ditangani; penggunaan tak resmi turun | Pemimpin keamanan |
| Perubahan vendor mengubah perilaku | Catatan rilis; keluaran bergeser pada sampel tetap | Klausul notifikasi perubahan, sampel regresi, rollback | Catatan versi dan uji rollback berhasil | Pemilik sistem |
| Jawaban fasih dianggap otoritatif | Penimpaan jarang padahal galat diketahui | Label, sitasi sumber, tinjauan mutu | Log penimpaan menunjukkan pemeriksaan | Pemilik produk |
| Log prompt menjadi insiden kebocoran | Data personal tanpa tanggal kedaluwarsa | Minimalisasi, redaksi, retensi, akses terbatas | Catatan pekerjaan penghapusan dan tinjauan akses | Pemilik data |
Prioritas adalah keputusan bisnis yang dibantu bukti. Skenario berat dengan
kontrol teruji bisa berada di bawah skenario sedang yang tak dipantau. Tulis
alasannya; lihat [Risiko, Keuangan & Tata Kelola Vendor](risk-finance.md).

---

## Lineage data dan ekor panjang prompt

**Provenance data** adalah asal data dan syarat penggunaannya. **Lineage data**
adalah pergerakan dan perubahannya hingga menjadi keluaran. AI menambah
dimensi: prompt menjadi data baru, keluaran menjadi data lagi, dan keduanya
mendarat di log serta sistem vendor yang tidak disetujui pemilik asal.

| Tahap | Pertanyaan yang diajukan | Catatan yang disimpan | Celah yang sering muncul |
|---|---|---|---|
| Sumber | Siapa mengumpulkan, untuk apa, dengan batas apa? | Register sumber dan catatan izin | "Ya kan ada di folder bersama" |
| Persiapan | Bagaimana data dibersihkan, beri label, dan digabung? | Catatan transformasi dan pemiliknya | Pekerjaan terjadi di file lokal seseorang |
| Penggunaan | Pelatihan, fine-tuning, retrieval, atau hanya inference? | Diagram alur data dan entri inventaris | Pelatihan dan retrieval dicampur |
| Keluaran | Apakah jawaban bisa mereproduksi data pihak lain? | Uji sampel dan batas akses | Tidak ada uji lintas konteks yang realistis |
| Retensi | Berapa lama prompt, keluaran, dan embedding bertahan, dan di mana? | Jadwal dan bukti penghapusan | Log disimpan "untuk debug" selamanya |
| Penghapusan | Bisakah permintaan hapus menjangkau semua salinan? | Catatan penghapusan dan konfirmasi vendor | Tidak ada peta salinan hilir |

**Pelatihan** mengubah model; **retrieval** mencari konten saat jawaban
dibuat; **inference** menjalankan model pada sebuah input. Janji "data
pelanggan tidak dipakai untuk melatih model" tidak mengatakan apa pun soal
penyimpanan, tinjauan oleh staf, atau log tiga puluh hari. Tanyakan masing-
masing secara terpisah.

Retensi adalah keputusan tata kelola, bukan default rekayasa. Simpan cukup
untuk merekonstruksi keputusan yang disengketakan dan menyelidiki insiden.
Data personal di log prompt layak mendapat perhatian sama seperti di basis data
— sering lebih, karena teks bebas memuat lebih dari yang disadari. Kewajiban
privasi berbeda menurut negara dan sektor; verifikasi dengan penasihat berwenang.

---

## Bias dan keadilan: satu metrik tidak pernah menyelesaikan masalah

**Bias** adalah kecenderungan sistematis dalam keluaran; **keadilan** menilai
perbedaan mana yang bisa diterima dalam konteks. Metrik berbeda tidak semuanya
bisa dipenuhi bersama. Tugas CISO bukan menyelesaikan perdebatan filosofis,
melainkan membuat pilihan terlihat, mengujinya, dan membuka keterbatasannya.

1. **Set evaluasi yang representatif.** Sertakan populasi, kondisi, dan kasus
   tepi yang benar-benar akan dihadapi sistem. Sampel yang disiapkan vendor
   bukan bukti independen.
2. **Metrik dan pertukaran yang dinyatakan.** Bandingkan galat atau tingkat
   seleksi antarkelompok dan catat apa yang diterima sebagai gantinya.
   Jangan berlindung di balik kalimat "modelnya tidak bias".
3. **Cari proksi.** Menghapus atribut sensitif yang jelas bisa meninggalkan
   korelasi lewat kode pos, riwayat pekerjaan, atau gaya menulis. Tidak
   adanya kolom bukan berarti tidak ada bias.
4. **Pantau setelah peluncuran.** Populasi dan aturan berubah; penilaian sekali
   jadi kedaluwarsa. Jadwalkan uji ulang dan tetapkan ambang yang menghentikan
   pemakaian.

"Kami sudah menghapus kolom sensitif" adalah fakta desain, bukan hasil uji
keadilan. "Audit independen" hanya sekuat ruang lingkup, tanggal, sampel, dan
kesesuaiannya dengan versi yang dipakai. Bukti keadilan adalah foto bersegel
waktu, bukan sertifikat seumur hidup.

---

## Transparansi, penjelasan, dan catatan keputusan

**Transparansi** bertanya apakah orang bisa mengetahui bahwa AI terlibat, apa
fungsinya, dan batas apa yang berlaku. **Explainability** bertanya apakah
sebuah keluaran tertentu bisa dijelaskan secara bermakna. Sistem bisa
transparan di dokumentasi dan tetap menghasilkan keluaran yang tidak bisa
direkonstruksi siapa pun.

Sesuaikan kedalaman penjelasan dengan taruhannya. Alat peringkas T1 cukup
berlabel. Sistem yang memengaruhi pekerjaan, kelayakan, atau akses memerlukan
catatan keputusan: input material, keluaran, aturan yang diterapkan,
peninjau, penimpaan, dan jalur sanggah. Simpan catatan itu di proses bisnis,
jangan hanya di telemetri vendor.

Penjelasan yang dibuat setelah kejadian bisa berupa narasi masuk akal, bukan
alasan yang benar-benar dipakai model. Kelancaran bukan kausalitas. **Model
card** pemasok adalah dokumen awal, bukan bukti kecocokan dengan kasus Anda.

Transparansi punya sisi internal: staf perlu tahu kapan tidak mempercayai alat.
Terbitkan daftar pendek "jangan andalkan ini tanpa tinjauan" dan permudah
eskalasi. Jika orang harus menebak, kontrol gagal saat paling dibutuhkan.

---

## Pengawasan manusia yang benar-benar merupakan kontrol

"Human in the loop" adalah frasa, bukan kontrol. Frasa itu berubah menjadi
kontrol hanya jika tiga syarat terpenuhi:

- **Wewenang** — peninjau boleh berkata tidak, tanpa biaya karier.
- **Informasi** — peninjau melihat sumber, batas, dan konsekuensi yang relevan.
- **Waktu** — ada perhatian yang cukup untuk memeriksa keluaran; antrean
  dua ratus klik cepat adalah stempel karet.

**Bias otomasi** — kecenderungan memercayai saran yang tampak otoritatif —
tumbuh seiring kelancaran teks dan tekanan waktu. Tampilkan ketidakpastian,
minta bukti untuk penerimaan berisiko tinggi, ambil sampel tinjauan, dan catat
penimpaan tanpa menganggap semuanya kesalahan. Penimpaan tinggi bisa berarti
alat buruk atau peninjau teliti; selidiki.

Kedalaman mengikuti tingkat: T1 aturan penggunaan wajar; T2 peninjau bernama;
T3 tinjauan terdokumentasi, jalur sanggah, dan ambang penghentian otomatis.
Manusia tetap bertanggung jawab. Lihat juga [Peran CISO: Dari Teknis ke Eksekutif](../fundamentals/ciso-role.md).

---

## Respons insiden untuk sistem berbasis AI

Jangan membangun proses "insiden AI" paralel. Perpanjang prosedur yang ada;
yang berubah adalah bukti yang dikumpulkan dan permukaan perbaikan.

| Tahap | Pertanyaan khusus AI | Perpanjangan praktik yang ada |
|---|---|---|
| Deteksi | Keluaran buruk, data terekspos, input diracun, atau vendor berubah? | Tambahkan sinyal mutu dan pergeseran ke pemantauan |
| Triage | Keputusan mana yang memakai keluaran terdampak, dan siapa terdampak? | Petakan konsumen keluaran dan catatan keputusan |
| Penahanan | Akses bisa dibatasi atau fitur bisa dihentikan? | Kill switch yang disepakati, rollback, pembatasan retrieval |
| Investigasi | Prompt, sumber, izin, dan versi mana yang terlibat? | Preservasi log dan catatan akses sesuai aturan custody |
| Pemulihan | Apakah keputusan sudah dikoreksi dan dikomunikasikan? | Penarikan keputusan, pemberitahuan koreksi, sampel uji ulang |
| Notifikasi | Kewajiban apa yang muncul, dan siapa yang memutuskan? | Penilaian hukum/privasi atas aturan terverifikasi |
| Pembelajaran | Kontrol apa yang hilang, dan apa kriteria uji ulangnya? | Pembaruan register, perubahan intake, diskusi vendor |

Tiga jebakan berulang: fokus pada model padahal kegagalan ada pada izin atau
alur data; menghapus log yang dibutuhkan penyelidikan; mengumumkan penyebab
sebelum bukti mendukungnya. Pernyataan pertama yang terlalu percaya diri sulit
ditarik kembali.

Ini edukasi operasional pertahanan, tanpa petunjuk memanipulasi model atau
menghindari pengaman.

---

## Pertanyaan pengadaan: uji klaim, jangan mengulangnya

Jaminan pemasok adalah **klaim pemasaran** sampai ruang lingkup, bukti, dan
pengecualiannya diperiksa. Ajukan sebelum tanda tangan:

1. Angka akurasi yang diiklankan mengukur apa, dengan data apa, dan
   dibandingkan dengan baseline apa?
2. Bolehkah kami mengevaluasi alat dengan data representatif kami sendiri di
   bawah syarat kami?
3. Apakah prompt, keluaran, atau embedding disimpan, ditinjau staf, dipakai
   untuk pelatihan atau perbaikan? Berapa lama, dan di wilayah mana?
4. Bagaimana batas antarpelanggan dan izin ditegakkan saat retrieval?
5. Apakah kami diberi tahu sebelum perubahan versi model atau layanan
   mencapai pengguna?
6. Bisakah versi dikunci atau dikembalikan, dan sudahkah prosedur itu diuji?
7. Subkontraktor dan penyedia model mana saja yang ada dalam rantai, dan di
   mana data diproses?
8. Apa komitmen notifikasi insiden, dengan tenggat dan kontak yang jelas?
9. Klaim audit apa yang dibuat, apa ruang lingkupnya, dan kapan diterbitkan?
10. Bagaimana akses administratif, fungsi istimewa, dan pencatatan log
    diatur?
11. Bukti evaluasi apa yang ada untuk **kasus kami**, bukan benchmark umum?
12. Keterbatasan dan penggunaan yang tidak pantas apa yang didokumentasikan
    vendor?
13. Bagaimana produk mendukung koreksi, komplain, dan tinjauan manusia?
14. Apa syarat pengembalian data, penghapusan, dan bantuan keluar?
15. Apa yang terjadi jika pemasok diakuisisi, menaikkan harga secara
    material, atau menghentikan model?

Catat jawaban sebagai bukti. Klaim yang tidak bisa masuk kontrak tidak boleh
menjadi dasar penerimaan risiko. Perhatikan **risiko konsentrasi**: beberapa
alur penting yang bergantung pada satu penyedia atau wilayah menciptakan
kegagalan bersama. Lihat [Risiko, Keuangan & Tata Kelola Vendor](risk-finance.md).

---

## Memindai regulasi tanpa mengklaim kepatuhan

CISO boleh mengatakan "kami sedang memeriksa aturan yang berlaku" tanpa menjadi
lawyer, selama prosesnya disiplin. Siapkan **register sumber**: sumber, versi
atau tanggal, pertanyaan penerapan, pemilik, verifikasi terakhir. Baca dari
penerbitnya, bukan ringkasan blog; penafsiran diserahkan ke penasihat berwenang.

| Sumber | Apa yang diberikan | Apa yang **tidak** dilakukannya | Yang diverifikasi |
|---|---|---|---|
| NIST AI Risk Management Framework | Kosakata dan struktur risiko sukarela | Bukan undang-undang atau skema sertifikasi | Versi terkini dan materi pendamping |
| ISO/IEC 42001 | Struktur sistem manajemen untuk tata kelola AI | Sertifikat tidak membuktikan satu sistem aman | Edisi dan ruang lingkup sertifikat |
| EU AI Act | Kerangka regulasi berbasis risiko dengan kewajiban bertahap | Tidak berlaku global; peran dan kasus menentukan | Teks resmi dan tanggal; memerlukan nasihat hukum |
| GDPR serta undang-undang privasi nasional | Aturan data personal dalam banyak penggunaan AI | Tidak menjawab semua pertanyaan keadilan | Hukum di tiap yurisdiksi terkait |
| Panduan komunitas untuk aplikasi LLM, misalnya OWASP | Istilah dan kategori risiko pertahanan | Bukan regulasi; sering berubah | Rilis terkini; bersifat panduan |

Sebutkan kebijakan internal sebagai otoritas, dan nyatakan apa yang **tidak**
Anda klaimkan: tidak ada pernyataan patuh menyeluruh, penafsiran undang-undang,
atau janji bahwa satu kerangka mencakup semua sistem. Pemindaian regulasi
adalah **kebiasaan verifikasi berulang**, bukan satu slide. Aturan berjalan;
kalimat kuartal lalu bisa kedaluwarsa. Lihat [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md).

---

## Tiga studi kasus fiktif

Ketiga kisah berikut rekaan dan ilustratif. Tidak ada prosedur teknis di
dalamnya — hanya konteks, kendala, keputusan, dan pelajaran.

### Kasus 1 — "Filter cerdas" di tim penjualan

**Konteks.** Sebuah tim penjualan memakai fitur bawaan CRM yang diberi label
"filter cerdas" untuk memberi skor pada prospek dan menentukan siapa yang
mendapat diskon. Tim menganggap itu "bukan AI, cuma aturan pintar". Saat
inventarisasi, ditemukan bahwa skor itu dihasilkan model yang dilatih vendor
dan memakai riwayat email serta data demografi.

**Kendala.** Diskon sudah berjalan dua bulan. Tidak ada pemilik bernama, tidak
ada catatan data masuk, dan kontraknya tidak menyebut retensi. Tim penjualan
takut kehilangan momentum kuartal.

**Keputusan.** CISO mendaftarkan sistem lebih dulu lalu menetapkan T2 karena
keputusan masih bisa dibatalkan manual. Diskon otomatis dihentikan sampai ada
pemilik, alur data, dan sampel uji dari data sendiri. Kanal pelaporan dibuka
tanpa hukuman; vendor diminta menjelaskan penyimpanan dan penggunaan data.
Peninjau bernama ditunjuk dengan ambang: jika galat sampel uji melebihi batas,
skor hanya saran.

**Hasil.** Diskon kembali berjalan dalam mode saran, bukan otomatis. Register
mencatat celah kontrak sebagai item terbuka dengan pemilik dan tanggal, bukan
ditutup karena demo terlihat bagus.

**Pelajaran yang bisa diambil.** Label pemasok tidak menentukan tata kelola;
yang menentukan adalah keputusan yang dipengaruhi. Mengubah wewenang
penggunaan sering lebih cepat dan lebih aman daripada menunggu model yang
sempurna.

### Kasus 2 — Asisten kontrak yang mengutip dokumen pelanggan lain

**Konteks.** Organisasi jasa hukum fiktif menghubungkan asisten internal ke
gudang dokumen untuk mempercepat penyusunan kontrak. Seorang staf melihat
asisten itu mengutip klausul harga yang jelas-jelas milik klien lain.
Transkrip percakapan menyimpan nomor identitas lengkap dan disimpan setahun
atas nama "jaminan mutu".

**Kendala.** Pengacara sudah bergantung pada alat itu. Pemasok bisa mengubah
layanan dari jarak jauh. Tim khawatir mematikan fitur akan mengganggu
tenggat klien, sementara menghapus log akan menghilangkan bukti.

**Keputusan.** Komandan insiden memperlakukan ini sebagai kebocoran data dulu,
mutu AI kemudian. Integrasi dibatasi lewat kill switch; retrieval dipersempit
ke konten publik. Transkrip dan catatan akses dipreservasi. Tim memetakan
percakapan terdampak, lalu meminta privasi dan hukum menilai notifikasi sesuai
aturan terverifikasi. Retensi dipangkas; uji batas izin dengan kriteria uji
ulang bernama dilakukan sebelum fitur dokumen aktif lagi. Kapasitas manual
dipulihkan.

**Hasil.** Alat kembali dalam mode terbatas tanpa akses ke dokumen klien.
Register mencatat paparan, perubahan kontrol, dan kekhawatiran residual.
Tindak lanjut menanyakan mengapa tinjauan desain awal tidak pernah menguji
retrieval lintas pelanggan.

**Pelajaran yang bisa diambil.** Kegagalannya adalah masalah desain dan izin
yang muncul lewat antarmuka AI. Memperpanjang prosedur biasa lebih cepat dan
lebih bisa dipertanggungjawabkan daripada membuat prosedur baru. Membatasi
paparan mendahului memperbagus kualitas jawaban.

### Kasus 3 — Audit "independen" dan dewan yang menginginkan jaminan

**Konteks.** Dewan direksi meminta satu kalimat jaminan bahwa organisasi
"AI-nya aman" sehubungan dengan akuisisi. Pemasok yang diincar menunjukkan
slide "audit independen", angka akurasi tinggi, dan sertifikat sistem
manajemen. CFO ingin menandatangani kontrak minggu ini.

**Kendala.** CISO tidak punya wewenang hukum untuk menyatakan kepatuhan.
Laporan audit tidak mencantumkan ruang lingkup, tanggal, atau versi yang
diuji. Dewan menginginkan kepastian, bukan daftar pertanyaan.

**Keputusan.** CISO menolak jaminan tanpa batas dan menawarkan dua dokumen.
Pertama, **pernyataan terbatas**: sistem yang dinilai, kontrol berbukti, risiko
terbuka beserta pemilik, dan tanggal tinjauan. Kedua, **kartu pengadaan**:
siapa yang mengaudit, ruang lingkupnya, versi, waktu, dan kecocokan dengan
konfigurasi produksi. Klausul notifikasi perubahan dan bantuan keluar diminta
masuk kontrak. Dewan diminta menyetujui **proses** dan jadwal tinjauan, bukan
vonis permanen.

**Hasil.** Dewan menyetujui proses dan jadwal tindak lanjut enam bulan.
Kontrak ditunda satu siklus sampai pertanyaan audit dijawab. Status triwulan
mulai memuat jumlah sistem, penilaian yang jatuh tempo, insiden, dan
pengecualian terbuka.

**Pelajaran yang bisa diambil.** Klaim vendor adalah pemasaran sampai
ruang lingkupnya terlihat. Kepercayaan eksekutif dibangun dengan menunjukkan
apa yang diketahui, apa yang tidak diketahui, dan apa yang akan diukur —
bukan dengan janji bahwa satu dokumen menyelesaikan masalah.

---

## Latihan per bagian

Jawab dengan suara keras sebelum membuka kunci. Ini latihan keputusan, bukan
uji kosakata.

### Set A — Inventaris dan tingkatan

**Q1.** Sebuah tim mengatakan, "Ini bukan AI, cuma filter pintar", untuk
memberi skor kinerja karyawan. Apakah sistem itu masuk register?

**Q2.** Karyawan mengakui menempel data pelanggan ke asisten publik untuk
menyusun balasan. Apa dua langkah pertama Anda?

**Q3.** Vendor mengatakan modelnya "sama di mana saja". Mengapa dua
penggunaan di departemen berbeda tidak otomatis setara?

<details>
<summary><strong>Kunci — Set A</strong></summary>

**A1.** Ya. Tata kelola mengikuti apa yang dilakukan sistem dan keputusan apa
yang dipengaruhinya, bukan labelnya. Keluaran berbantuan model yang memengaruhi
penilaian kerja masuk inventaris.

**A2.** Terima kasih dan catat fakta — data apa, alat apa, kapan — lalu nilai
apakah insiden atau kewajiban pengungkapan muncul menurut aturan terverifikasi.
Budaya hukum-dulu mendorong shadow AI ke bawah tanah.

**A3.** Risiko bergantung pada data, integrasi, wewenang, dan orang terdampak.
Model yang sama berada di T1 untuk peringkas draf dan di T3 untuk keputusan
kelayakan. Yang diklasifikasikan adalah penggunaannya.

</details>

### Set B — Risiko, bukti, dan pengawasan

**Q4.** Alat ber-tingkat tinggi tidak punya pemilik bernama dan intake
terhenti. Apa yang Anda lakukan?

**Q5.** Sistem akan dihentikan dalam enam bulan. Apakah itu menghapus
kebutuhan keputusan retensi?

**Q6.** Vendor menjanjikan "data pelanggan tidak dipakai untuk pelatihan".
Apa pertanyaan lanjutan yang paling penting?

<details>
<summary><strong>Kunci — Set B</strong></summary>

**A4.** STOP peluncuran. Eskalasi ke sponsor dan minta pemilik akuntabel yang
berwenang menerima risiko residual. Sistem T3 tanpa pemilik adalah pengecualian
yang tidak bisa ditutup siapa pun.

**A5.** Tidak. Prompt, keluaran, log, dan embedding yang dibuat sekarang bisa
lebih panjang usianya daripada alatnya. Tentukan retensi dan penghapusan di
vendor maupun salinan lokal sebelum peluncuran, dan sebut siapa yang
mengonfirmasi penghapusan saat keluar.

**A6.** Tanyakan terpisah soal penyimpanan, tinjauan staf, retensi, wilayah,
subkontraktor, dan penggunaan retrieval, lalu tulis janji yang relevan ke
dalam kontrak. Pelatihan hanya satu jalur data.

</details>

### Set C — Keadilan, transparansi, dan catatan

**Q7.** Laporan menyatakan keadilan meningkat. Apa yang membuat Anda
mempercayainya?

**Q8.** Peninjau menyetujui 99 persen rekomendasi dalam waktu kurang dari dua
detik. Apakah pengawasan berjalan?

**Q9.** Jawaban yang fasih ternyata salah dan pelanggan bertindak
berdasarkan itu. Apa yang masuk catatan insiden?

<details>
<summary><strong>Kunci — Set C</strong></summary>

**A7.** Periksa metrik, sampel, tanggal, versi, pelaksana uji, dan pertukaran
yang diterima. Minta uji ulang atas kasus Anda. Angka tanpa ruang lingkup
bukan bukti.

**A8.** Hampir pasti tidak. Periksa wewenang, informasi, dan waktu; ambil
sampel tinjauan untuk melihat ketelitian; tampilkan sumber; selidiki apakah
volume atau desain antarmuka membuat gerbang itu stempel karet.

**A9.** Keputusan dan pelanggan terdampak, input dan keluaran, versi, sumber,
peninjau, penahanan, koreksi, serta bukti untuk tiap klaim. Pisahkan fakta
teramati dari hipotesis awal.

</details>

### Set D — Insiden dan respons

**Q10.** Saat insiden AI, seseorang mengusulkan menghapus semua log prompt
"biar bersih". Apa tanggapan Anda?

**Q11.** Seseorang mengumumkan penyebab insiden di kanal umum sebelum tim
penyelidikan selesai. Apa masalahnya?

**Q12.** Pemasok menolak membahas perubahan model. Apa respons tata kelola
yang bisa dipertanggungjawabkan?

<details>
<summary><strong>Kunci — Set D</strong></summary>

**A10.** Tunda penghapusan catatan yang relevan. Preservasi sesuai aturan
penyelidikan dan custody, terapkan keputusan retensi yang sudah disetujui,
dan catat setiap pemusnahan berikutnya.

**A11.** Insiden AI adalah rantai keputusan desain kecil. Pernyataan percaya
diri di awal sulit ditarik dan bisa merusak kepercayaan serta proses notifikasi.
Sampaikan apa yang teramati, apa yang masih dugaan, dan siapa yang menyelidiki.

**A12.** Catat risiko residual; minta notifikasi perubahan atau penguncian
versi jika memungkinkan; tambahkan uji regresi pada sampel tetap; eskalasi
penerimaan ke pemilik yang berwenang memutuskan.

</details>

### Set E — Pengadaan dan verifikasi

**Q13.** Pemasok mengutip "audit AI independen". Tiga pertanyaan apa yang
harus Anda ajukan?

**Q14.** Direktur bertanya apakah organisasi "sudah patuh terhadap AI Act".
Apa jawaban yang bisa dipertanggungjawabkan?

**Q15.** Dewan menginginkan satu jaminan "AI kami aman". Apa yang Anda
tawarkan sebagai gantinya?

<details>
<summary><strong>Kunci — Set E</strong></summary>

**A13.** Siapa yang melakukan audit dan seberapa independen? Apa ruang
lingkupnya, pada data dan versi apa? Kapan dilaksanakan, dan apakah
konfigurasi produksi cocok? Label saja hampir tidak membuktikan apa pun.

**A14.** Sebutkan apa yang sudah diverifikasi, oleh siapa, dan untuk sistem
mana; nyatakan bahwa penerapan bergantung pada peran, wilayah, dan kasus
penggunaan; katakan konfirmasi sedang dicari. Jangan mengimprovisasi simpulan
hukum.

**A15.** Pernyataan terbatas: ruang lingkup, sistem yang dinilai, kontrol
berbukti, risiko terbuka beserta pemilik, dan tanggal tinjauan berikutnya.
Tolak jaminan tanpa batas.

</details>

---

## Kesalahan umum yang perlu dihafal

- **Kebijakan tanpa inventaris** — prinsip indah, tetapi tidak ada satu pun
  sistem bernama yang diatur.
- **Berpikir model-dulu** — mengawasi algoritme sambil mengabaikan data,
  izin, dan keputusan hilir.
- **Salin-klaim vendor** — persentase pemasaran diulang seolah hasil uji
  sendiri.
- **Stempel karet** — klik cepat disebut pengawasan manusia.
- **Penyembuhan metrik** — satu angka keadilan dijadikan vonis moral.
- **Log tanpa akhir** — semua prompt disimpan selamanya dan menciptakan
  masalah kedua.
- **Prosedur paralel** — respons insiden AI yang melupakan hukum, privasi,
  dan komunikasi.
- **Bukti beku** — penilaian sekali dianggap tetap valid setelah sistem
  berubah.
- **Teater kepatuhan** — mengklaim kerangka atau regulasi yang belum diukur
  dan diverifikasi.
- **Tanpa rencana keluar** — bergantung pada pemasok tanpa pengembalian data
  atau kesinambungan.
- **Tingkat dari brosur** — vendor menentukan "risiko rendah" dan organisasi
  menerimanya tanpa uji.
- **Janji komite** — "nanti saja dibahas" dipakai untuk menunda keputusan
  pemilik bernama.

---

## Templat yang bisa dipakai ulang

Salin ke catatan Anda. Nilainya muncul dari pengisian yang jujur, bukan dari
kerapiannya.

### Templat intake sistem AI

```
Nama sistem:          [nama bisnis, bukan nama pemasaran]
Tujuan:               [keputusan atau tugas yang dibantu]
Pemilik bisnis:       [nama, peran, bertanggung jawab atas hasil]
Kontak teknis:        [nama / tim]
Jenis:                [dibuat / dibeli / fitur tersemat / belum jelas]
Vendor + versi:       [nama, identitas layanan atau model, tanggal dilihat]
Data masuk:           [kategori + sensitivitas + sumber]
Data keluar:          [penerima + keputusan yang digerakkan]
Integrasi:            [sistem, izin, batas retrieval]
Orang terdampak:      [pelanggan / staf / kandidat / publik]
Tinjauan manusia:     [tidak ada / nasihat / wajib sebelum tindakan]
Pembalikan:           [dapat dibalik / mahal / tidak dapat dibalik]
Tingkat:              [T0 / T1 / T2 / T3] + alasan
Syarat penggunaan data:[pelatihan / penyimpanan / retensi / wilayah / prosesor]
Rencana evaluasi:     [sampel, metrik, ambang, pemilik, tanggal]
Sanggah / koreksi:    [jalur bagi orang terdampak, bila relevan]
Rollback / kill switch:[siapa menghentikan, caranya, terakhir diuji]
Celah terbuka:        [tiap celah punya pemilik dan tanggal]
Keputusan:            [setujui pilot / STOP / ESCALATE ke ______]
Tanggal tinjauan:     [tanggal + pemicu tinjauan lebih awal]
```

### Register risiko AI

| ID | Skenario | Tingkat | Alasan likelihood | Alasan impact | Kontrol | Bukti | Risiko residual | Perlakuan | Pemilik | Tinjauan |
|---|---|---|---|---|---|---|---|---|---|---|
| AI-01 | | | | | | | | mitigasi / terima / hindari / alihkan | | |
| AI-02 | | | | | | | | mitigasi / terima / hindari / alihkan | | |

Tulis likelihood dan impact dengan kata-kata. Kolom **Bukti** yang kosong
berarti kontrol belum terverifikasi. Risiko yang diterima memerlukan pemilik
bernama dan tanggal.

### Kartu pertanyaan pengadaan

```
[ ] Metrik akurasi + data + baseline dipahami?
[ ] Evaluasi dengan data sendiri diizinkan sesuai syarat kita?
[ ] Pelatihan / penyimpanan / tinjauan / retensi / wilayah dijawab terpisah?
[ ] Batas tenant dan izin didokumentasikan?
[ ] Perubahan versi diumumkan; versi bisa dikunci atau dikembalikan?
[ ] Subkontraktor dan lokasi pemrosesan tercantum?
[ ] Tenggat dan kontak notifikasi insiden disepakati?
[ ] Klaim audit memiliki ruang lingkup, tanggal, dan cocok dengan versi aktif?
[ ] Keterbatasan dan penggunaan tidak pantas didokumentasikan?
[ ] Koreksi, komplain, dan tinjauan manusia didukung produk?
[ ] Pengembalian data, penghapusan, dan bantuan keluar ada di kontrak?
[ ] Risiko konsentrasi dipertimbangkan di seluruh portofolio?
```

### Lembar pemindaian sumber

```
Sumber / penerbit: __________  Versi atau tanggal: __________
Pertanyaan penerapan: _______________________________________
Pemilik: __________  Verifikasi terakhir: __________
Yang TIDAK kami klaim: _____________________________________
Rute ke penasihat berwenang: ________________________________
```

### Status triwulan untuk dewan

```
Sistem: [n] | Baru: [n] | Penilaian jatuh tempo: [n] | Insiden: [n]
Pengecualian T3 terbuka: [n] | Keputusan yang diminta: [satu baris]
```

---

## Glosarium

| Istilah | Arti dengan bahasa sederhana |
|---|---|
| **Sistem AI** | Produk atau alur kerja yang memakai model untuk menghasilkan keluaran yang ditindaklanjuti orang |
| **Shadow AI** | Alat yang dipakai staf tanpa persetujuan organisasi |
| **Tingkat dampak** | Kategori berdasarkan seberapa serius keluaran yang salah atau berbahaya |
| **Intake** | Peninjauan awal terstruktur atas penggunaan AI yang diusulkan |
| **Provenance data** | Dari mana data berasal dan dengan syarat apa ia boleh dipakai |
| **Lineage data** | Bagaimana data bergerak dan berubah dari sumber hingga keluaran |
| **Inference** | Menjalankan model pada sebuah input untuk menghasilkan keluaran |
| **Pelatihan** | Menyesuaikan model dengan data; berbeda dari retrieval dan inference |
| **Retrieval** | Mencari konten saat jawaban dibuat, biasanya dari sumber pengetahuan |
| **Prompt** | Input ke sistem, yang dengan sendirinya bisa menjadi data yang disimpan |
| **Bias otomasi** | Kecenderungan terlalu percaya saran yang tampak otoritatif |
| **Pengawasan manusia** | Tinjauan yang punya wewenang, informasi, dan waktu yang cukup |
| **Drift** | Perubahan perilaku atau data yang membuat penilaian lama tidak lagi andal |
| **Risiko residual** | Apa yang tersisa setelah kontrol diterapkan |
| **Rencana keluar** | Cara organisasi tetap berjalan jika pemasok atau alat hilang |

---

## Referensi dan verifikasi

Verifikasi versi, tanggal, dan penerapan langsung ke penerbitnya. Artikel ini
adalah titik awal belajar, bukan penetapan kepatuhan.

- **Informasi program EC-Council** — label **CCISO v4 / AI-Enhanced** tercatat
  pada materi yang diperiksa **26 November 2026**. Verifikasi ulang merek,
  blueprint, dan kebijakan terkini di [eccouncil.org](https://www.eccouncil.org/)
  dan [cert.eccouncil.org](https://cert.eccouncil.org/).
- **NIST AI Risk Management Framework** — kosakata dan struktur risiko
  sukarela; periksa versi terkini dan materi pendampingnya.
- **ISO/IEC 42001** — standar sistem manajemen AI; periksa edisi dan ruang
  lingkup sertifikat sebelum mempercayai klaim.
- **Teks resmi EU AI Act dan GDPR** — penerapan bergantung pada wilayah,
  peran, dan kasus penggunaan; baca sumber resmi dan minta nasihat hukum.
- **Panduan komunitas OWASP untuk aplikasi LLM** — istilah dan desain
  pertahanan; periksa rilis terkini.
- **MITRE ATLAS** — basis pengetahuan tentang perilaku adversary terhadap
  sistem AI, berguna untuk pemodelan ancaman pertahanan, bukan kumpulan
  petunjuk praktis.
- **Kebijakan internal, selera risiko, kontrak, dan aturan lokal** lebih
  utama daripada kerangka publik dalam keputusan internal.
- **Catatan CSIX pendamping (situs belajar independen):**
  [CSIX ISO 27001](https://siedysoes.github.io/csix-iso27001/),
  [CSIX COBIT](https://siedysoes.github.io/csix-cobit/),
  [CSIX ITIL](https://siedysoes.github.io/csix-itil/),
  [CSIX ECSA](https://siedysoes.github.io/csix-ecsa/),
  [CSIX CPENT AI](https://siedysoes.github.io/csix-cpent/). Ganti
  `siedysoes` saat deploy.

Persentase dan survei vendor adalah **klaim pemasaran** kecuali direproduksi
dalam kondisi Anda. Artikel ini edukasi, bukan nasihat hukum, regulasi,
keuangan, pajak, atau investasi, serta bukan pengganti materi resmi. Untuk
kerangka eksekutif dan komunikasi dewan, lihat
[Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md) dan
[Komunikasi Dewan & Executive Presence](board-communication.md).

## Lihat juga

- [Apa Itu CCISO v4](../fundamentals/what-is-cciso.md)
- [Lima Domain: Govern hingga Strategize](../fundamentals/five-domains.md)
- [CCISO vs CISSP & Kredensial Leadership Lain](../fundamentals/cciso-vs-cissp.md)
- [Peran CISO: Dari Teknis ke Eksekutif](../fundamentals/ciso-role.md)
- [Format Ujian & Blueprint CCISO](../exam/exam-format.md)
- [Rencana Belajar Praktis](../exam/study-plan.md)
- [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md)
- [Biaya, Masa Berlaku & CPD](../exam/cost-validity.md)
- [Komunikasi Dewan & Executive Presence](board-communication.md)
- [Risiko, Keuangan & Tata Kelola Vendor](risk-finance.md)
- [Karier Setelah CCISO](cciso-careers.md)
