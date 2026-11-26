# Risiko, Keuangan & Tata Kelola Vendor

Sumber belajar independen dan tidak resmi; kami **tidak berafiliasi dengan EC-Council**. EC-Council, CCISO, CISSP, CISM, dan CISA adalah merek dagang pemiliknya; tidak ada materi kursus resmi, bocoran soal, atau konten berhak cipta di sini. Merek resmi saat ini adalah **CCISO v4 — AI-Enhanced** (diverifikasi 26 Nov 2026). Verifikasi kembali di [eccouncil.org](https://www.eccouncil.org/train-certify/certified-chief-information-security-officer-cciso/) dan [cert.eccouncil.org](https://cert.eccouncil.org/).

## Selera risiko bukan sekadar daftar kontrol

Sebelum memilih kontrol, organisasi perlu menyepakati **apa yang bersedia diterimanya**. *Risk appetite* adalah pernyataan tingkat risiko yang masih dianggap wajar demi mencapai tujuan. *Risk tolerance* adalah batas penyimpangan yang masih bisa ditoleransi sebelum eskalasi diperlukan.

Contoh ilustratif, bukan rekomendasi angka: "Kami menerima gangguan singkat pada sistem internal, tetapi tidak pada layanan yang memproses transaksi pelanggan." Pernyataan seperti ini lebih berguna daripada daftar kontrol: membantu menjawab mana yang mendesak. Lihat [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md) untuk kerangka kerja yang sering dipakai pemimpin.

## Kualitatif dan kuantitatif: pilih yang cocok

Penilaian **kualitatif** memakai kategori seperti rendah, sedang, dan tinggi — tetapi kategori itu harus punya kriteria yang disepakati, bukan sekadar perasaan. Penilaian **kuantitatif** berusaha mengestimasi rentang frekuensi dan dampak, misalnya dalam bentuk rentang kerugian atau hari gangguan operasional.

Ada berbagai model populer, tetapi **tidak ada rumus tunggal yang merupakan standar universal** untuk semua organisasi. Tuliskan asumsi, sumber data, dan batas ketidakpastiannya. Angka yang terlalu presisi tanpa dasar lebih berbahaya daripada mengakui keterbatasan data.

## Artefak tata kelola yang benar-benar dipakai

| Artefak | Isi minimum | Fungsi bagi pemimpin |
| --- | --- | --- |
| Risk register | Risiko, penyebab, dampak, pemilik, kontrol, status | Memberi gambaran dan jelas siapa yang bertanggung jawab |
| Treatment plan | Opsi penanganan, tindakan, tenggat, biaya, sisa risiko | Mengubah temuan menjadi pekerjaan yang bisa diikuti |
| Formulir penerimaan risiko | Penjelasan risiko, alasan, masa berlaku, penandatangan berwenang | Membuat keputusan "diterima" dapat dipertanggungjawabkan |
| Daftar pengecualian | Aturan yang tidak dipatuhi, kompensasi, waktu berakhir | Mencegah pengecualian sementara menjadi permanen |

Tinjau artefak ini secara berkala. Register yang tidak pernah berubah hanya dokumen seremonial.

## Siklus anggaran dan bahasa keuangan

Anggaran umumnya bergerak melalui tahapan: identifikasi kebutuhan, justifikasi, negosiasi dengan keuangan, realisasi, lalu evaluasi. Pahami kalender organisasi Anda — usulan yang masuk setelah jendela perencanaan tertutup sering tertunda, betapapun mendesaknya.

| Jenis biaya | Gambaran umum | Contoh |
| --- | --- | --- |
| CAPEX | Pengeluaran investasi awal untuk aset yang digunakan beberapa periode | Platform keamanan baru, perangkat |
| OPEX | Biaya berulang untuk menjalankan layanan | Langganan, pemeliharaan, tenaga kerja kontrak |

Penggolongan di atas hanya gambaran umum; perlakuan akuntansi berbeda antarorganisasi dan perlu dikonfirmasi dengan tim keuangan. Saat menjelaskan nilai, bandingkan biaya kontrol dengan eksposur yang berkurang dan kemampuan bisnis yang tetap berjalan. Sebutkan asumsinya. Hindari klaim seperti "ROI 300%" tanpa dasar yang dapat diaudit: itu adalah perkiraan, bukan jaminan hasil.

## Tata kelola vendor: dari due diligence hingga rencana keluar

- **Sebelum kontrak:** pahami kepemilikan dan lokasi data, daftar sub-pemroses, laporan audit atau sertifikasi yang tersedia, serta catatan insiden sebelumnya. Ajukan pertanyaan tertulis dan simpan jawabannya.
- **Dalam kontrak:** perhatikan *service level agreement* (SLA) — cakupan layanan, waktu respons, dan remediasi — serta hak audit, pemberitahuan insiden, pengembalian atau penghapusan data, dan aturan subkontrak.
- **Selama kerja sama:** pantau realisasi SLA, tinjau temuan secara berkala, dan eskalasi penyimpangan lebih awal.
- **Risiko konsentrasi:** jika banyak layanan kritis bergantung pada satu penyedia, kegagalan satu pihak dapat berdampak luas. Coba bayangkan skenario "vendor ini mendadak tidak tersedia".
- **Rencana keluar:** pastikan data dapat diekspor dalam format yang bisa dipakai, catat waktu dan biaya migrasi, serta kenali alternatifnya. Rencana keluar yang tidak pernah diuji biasanya hanya harapan.

## Batas tanggung jawab

Artikel ini **edukasi, bukan nasihat keuangan, pajak, hukum, atau regulasi**. Kewajiban, perlakuan pajak, dan aturan kontrak sangat bergantung pada negara, sektor, dan jenis organisasi serta dapat berubah. Konsultasikan profesional yang kompeten dan sumber resmi. Statistik survei vendor tentang biaya atau risiko adalah **klaim pemasaran**, bukan patokan atau jaminan.

Untuk konteks tambahan: [CSIX ISO 27001:2022](https://siedysoes.github.io/csix-iso27001/), [CSIX COBIT 7](https://siedysoes.github.io/csix-cobit/), dan [CSIX ITIL 5](https://siedysoes.github.io/csix-itil/).

## Lihat juga

- [Framework & Tool untuk Eksekutif](../exam/frameworks-tools.md)
- [Komunikasi Dewan & Executive Presence](board-communication.md)
- [Lima Domain: Govern hingga Strategize](../fundamentals/five-domains.md)
- [Biaya, Masa Berlaku & CPD](../exam/cost-validity.md)
- [Tata Kelola AI: Realita Lapangan](ai-governance.md)
