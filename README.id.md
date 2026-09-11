<p align="right"><a href="./README.md">English</a> | <b>Bahasa Indonesia</b></p>

# VV-PUNYE Open Source

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![DPG Nominee](https://img.shields.io/badge/DPG-Nominee-blue.svg)](#keselarasan-barang-publik-digital-dpg-alignment)
[![Privacy: Zero Telemetry](https://img.shields.io/badge/Privacy-Zero%20Telemetry-green.svg)](#keamanan-berlapis-privasi--kepatuhan-hukum-security--privacy-architecture)
[![Compliance: GDPR / UU PDP](https://img.shields.io/badge/Compliance-GDPR%20%2F%20UU%20PDP-brightgreen.svg)](#keamanan-berlapis-privasi--kepatuhan-hukum-security--privacy-architecture)
[![Tech: React + Vite](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61dafb.svg)](https://vitejs.dev/)
[![Backend: Fastify](https://img.shields.io/badge/Backend-Fastify-000000.svg)](https://fastify.dev/)
[![Open Collective](https://img.shields.io/badge/Sponsor-Open%20Collective-41B883.svg)](https://opencollective.com/vv-punye-open-source)

**Platform Transaksi & Manajemen Digital Tanpa Kode untuk Produk dan Jasa**

**VV-PUNYE Open Source** adalah perangkat lunak terbuka (*open source*) yang dirancang sebagai Barang Publik Digital (*Digital Public Goods*) berbasis *no-code*. Sistem ini hadir untuk membantu digitalisasi operasional, pemangkasan biaya perantara finansial, pencatatan transaksi, dan transparansi keuangan bagi pelaku usaha kecil (UMKM), pekerja mandiri (*freelancer*), serta masyarakat luas secara cuma-cuma. 

Aplikasi ini secara langsung mendukung pemenuhan **SDG 8 (Pekerjaan Layak & Pertumbuhan Ekonomi)** dan **SDG 9 (Industri, Inovasi, & Infrastruktur)** melalui pengintegrasian penjualan produk fisik, penawaran jasa, dan pencatatan kas komunitas dalam satu platform mandiri yang berdaulat.

---

## 📋 Daftar Isi

- [Latar Belakang & Masalah](#latar-belakang--masalah)
- [Solusi & Fitur Utama](#solusi--fitur-utama)
- [Keselarasan Barang Publik Digital (*DPG Alignment*)](#keselarasan-barang-publik-digital-dpg-alignment)
- [Arsitektur & Teknologi yang Digunakan (*Tech Stack*)](#arsitektur--teknologi-yang-digunakan-tech-stack)
- [Keamanan Berlapis, Privasi, & Kepatuhan Hukum (*Security & Privacy Architecture*)](#keamanan-berlapis-privasi--kepatuhan-hukum-security--privacy-architecture)
- [Strategi Infrastruktur & Kedaulatan Jaringan (*Platform-Agnostic*)](#strategi-infrastruktur--kedaulatan-jaringan-platform-agnostic)
- [Panduan Instalasi Ringkas (*Quick Start*)](#panduan-instalasi-ringkas-quick-start)
- [Peta Jalan Berkelanjutan (*Roadmap*)](#peta-jalan-berkelanjutan-roadmap)
- [Tata Kelola Hibah & Akuntabilitas (*Grant Governance*)](#tata-kelola-hibah--akuntabilitas-grant-governance)
- [Dukungan & Pendanaan (*Sponsorship*)](#dukungan--pendanaan-sponsorship)
- [Panduan Kontribusi (*Contributing Guide*)](#panduan-kontribusi-contributing-guide)
- [Lisensi Perangkat Lunak (*License*)](#lisensi-perangkat-lunak-license)

---

## Latar Belakang & Masalah

Di era digital saat ini, memiliki platform transaksi dan sistem pencatatan mandiri telah menjadi kebutuhan utama bagi pelaku usaha dan pekerja mandiri. Namun, sebagian besar masyarakat menghadapi hambatan besar:

1. **Hambatan Teknis (Ketiadaan Keahlian Pemrograman)**  
   Sebagian besar pelaku usaha kecil dan individu tidak memiliki latar belakang teknologi maupun kemampuan pemrograman. Hal ini membuat solusi *open-source* konvensional sulit diakses karena membutuhkan proses instalasi dan pengelolaan server yang rumit.

2. **Perangkap Biaya Berlangganan & Komisi (*Subscription Trap*)**  
   Solusi komersial yang beredar di pasaran umumnya menerapkan skema biaya sewa bulanan, tahunan, atau potongan komisi dari setiap transaksi penjualan yang sangat menggerus keuntungan.

3. **Kondisi Modal Terbatas pada Fase Merintis**  
   Bagi pelaku usaha yang baru merintis atau memiliki keterbatasan finansial, membayar biaya rutin digitalisasi adalah beban yang sangat berat. Ketika modal terbatas atau penjualan sepi, operasional digital terancam terhenti karena tidak sanggup membayar sewa perangkat lunak (*software*).

4. **Fragmentasi Alat antara Penjualan Produk dan Jasa**  
   Pelaku usaha atau *freelancer* yang menjual produk fisik sekaligus menawarkan keahlian/jasa sering kali terpaksa menggunakan beberapa platform terpisah. Hal ini menciptakan kerumitan operasional dan pemborosan waktu.

5. **Privasi dan Hilangnya Kedaulatan Data (*Vendor Lock-in*)**  
   Ketergantungan pada platform pihak ketiga membuat pemilik usaha tidak memiliki kendali penuh atas data transaksi, riwayat pelanggan, dan aset digital mereka. Data bisnis sering diproses tanpa transparansi oleh penyedia platform komersial.

6. **Kerumitan Sistem (*Feature Bloat*) yang Membingungkan Pemula**  
   Banyak aplikasi manajemen bisnis yang ada saat ini terlalu rumit dan dipenuhi fitur berlebihan yang tidak dibutuhkan oleh usaha pemula, sehingga justru menyulitkan proses adopsi awal.

7. **Keterbatasan Perangkat dan Konektivitas (*Hardware & Connectivity Constraints*)**  
   Banyak perangkat lunak bisnis modern berukuran besar, menuntut spesifikasi perangkat yang tinggi, serta koneksi internet berkecepatan tinggi, sehingga menyulitkan pelaku usaha di daerah dengan infrastruktur terbatas.

8. **Eksploitasi Data Tren Penjualan oleh Platform Terpusat**  
   Platform komersial kerap mengumpulkan dan menganalisis tren transaksi milik usaha kecil untuk kepentingan bisnis internal mereka, yang sering kali justru merugikan para pelaku usaha sebagai pemilik sah data tersebut.

9. **Hambatan Bahasa dan Orientasi Teknis (*Developer-Centric*)**  
   Sebagian besar perangkat lunak *open-source* yang ada dibuat oleh *developer* untuk *developer*, menggunakan istilah teknis yang rumit dan dominan berbahasa asing, sehingga menciptakan jarak bagi masyarakat awam di tingkat lokal.

---

## Solusi & Fitur Utama

**VV-PUNYE Open Source** hadir sebagai Barang Publik Digital (*Digital Public Goods*) yang dirancang untuk menyelesaikan hambatan teknis, biaya, dan infrastruktur bagi pelaku usaha kecil serta pekerja mandiri melalui fitur-fitur unggulan berikut:

1. **Mode Operasional Fleksibel & Inklusif (Produk, Jasa, Komunitas, atau Hibrida)**  
   Sistem dirancang dengan pendekatan fleksibel (*opt-in*) tanpa pemaksaan struktur. Pengguna dari berbagai latar belakang—mulai dari individu, pekerja kreatif, pelaku usaha, hingga komunitas sosial—bebas memilih dan mengaktifkan fitur yang dibutuhkan tanpa terganggu oleh menu yang tidak terpakai:
   * **Mode Produk & Inventaris**: Khusus penjualan barang fisik, pengelolaan stok harian, dan transaksi kasir harian.
   * **Mode Jasa & Portofolio**: Khusus penawaran keahlian personal, layanan profesional, persewaan, dan penjadwalan janji temu.
   * **Mode Komunitas & Inisiatif Sosial**: Khusus transparansi kas organisasi/komunitas, pencatatan dana kegiatan, dan pengelolaan program publik.
   * **Mode Hibrida Tanpa Batas**: Kebebasan menggabungkan penjualan produk, penawaran jasa, dan kegiatan komunitas secara beriringan dalam satu platform terpadu.

2. **Sistem Pencatatan Keuangan Transparan & Berstandar Global (*Investor-Ready*)**  
   Pencatatan harian dibuat sangat sederhana untuk pengguna pemula, namun secara bertahap (*progressive disclosure*) dapat dikembangkan untuk mendukung akuntabilitas tingkat tinggi:
   * **Pencatatan Lintas Perangkat**: Akses cepat dan responsif dari *smartphone*, tablet, maupun komputer/laptop.
   * **Kesiapan Standar Keuangan Internasional**: Mendukung transaksi multi-mata uang (*multi-currency*) dan pencatatan terstruktur berbasis standar akuntansi global, memudahkan usaha lokal membuka akses ke pendanaan atau investor internasional.
   * **Transparansi & Akuntabilitas**: Menyediakan laporan arus kas, laba rugi, dan neraca yang transparan, terverifikasi, serta siap dibagikan kepada pemangku kepentingan (*stakeholders*).
   * **Dasbor Kesehatan Finansial Intuitif**: Visualisasi tren keuangan yang mudah dipahami oleh pengguna awam tanpa harus mempelajari rumus akuntansi rumit.
   * **Ekspor Data & Aksesibilitas**: Riwayat transaksi dapat diekspor kapan saja ke berbagai format standar (CSV, JSON, PDF) untuk kebutuhan audit, perpajakan, atau integrasi sistem di masa depan.

3. **Arsitektur Ringan, Modular, & Pembaruan Tanpa Beban (*Lightweight & Seamless Upgrades*)**  
   Sistem dirancang dengan arsitektur tangguh yang memisahkan fungsi utama dan fitur tambahan secara terisolasi, memastikan aplikasi tetap cepat, stabil, dan mudah dikembangkan:
   * **Sistem Inti Cepat & Hemat Perangkat**: Dibangun dengan ukuran yang sangat ringkas dan hemat sumber daya, menjamin performa lancar pada perangkat berspesifikasi rendah tanpa tersendat (*lag*).
   * **Aktivasi Fitur Cerdas Sekali Klik (*One-Click Feature Toggles*)**: Fitur lanjutan—seperti pemindai nota otomatis, pengingat stok harian, atau modul analitik—tersedia sebagai pilihan opsional yang dapat diaktifkan lewat satu tombol sakelar tanpa instalasi teknis rumit.
   * **Isolasi Sistem & Keamanan Operasional**: Struktur modular memastikan bahwa pembaruan atau penambahan fitur baru tidak akan merusak fungsi dasar aplikasi maupun mengganggu data transaksi yang sudah tersimpan.
   * **Skalabilitas & Keberlanjutan Jangka Panjang**: Penataan arsitektur yang terstruktur menjamin perangkat lunak ini dapat terus tumbuh secara konsisten, fleksibel terhadap kebutuhan lapangan, serta menjadi fondasi kuat untuk keberlanjutan pengembangan di masa depan.

4. **Fleksibilitas Penempatan Server & Kedaulatan Data (*Multi-Deployment & Data Sovereignty*)**  
   Pengguna memegang kendali 100% atas data transaksi, keuangan, dan riwayat pelanggan tanpa keterikatan pada satu penyedia platform (*no vendor lock-in*). Sistem dapat dijalankan secara fleksibel sesuai ketersediaan perangkat:
   * **Komputer / Laptop Pribadi (*Home Server*)**: Memaksimalkan laptop atau PC yang sudah ada di rumah/toko untuk dijadikan server mandiri tanpa perlu membeli perangkat baru.
   * **Perangkat Berdaya Rendah (*Single-Board Computer*)**: Dapat berjalan mulus pada perangkat mini yang hemat listrik (seperti Raspberry Pi, Orange Pi, atau sejenisnya).
   * **Server Pribadi (*Self-Hosted VPS*)**: Pilihan penyebaran bagi pengguna yang menginginkan akses *online* 24/7 dengan kendali akses penuh.
   * **Layanan Cloud Bebas Pilih**: Kemudahan dalam pemasangan di berbagai infrastruktur *cloud server* sesuai kebutuhan dan kenyamanan pengguna.

5. **Akses Gratis 100% & Kemerdekaan Finansial Tanpa Komisi (*Zero Hidden Fees & Economic Empowerment*)**  
   Perangkat lunak ini dikembangkan murni sebagai Barang Publik Digital (*Digital Public Goods*) berlisensi terbuka, menjamin kebebasan akses penuh dan perlindungan marjin usaha tanpa beban finansial tersembunyi:
   * **Bebas Sewa & Tanpa Penguncian Fitur (*No Subscription & Feature Lock*)**: Bebas biaya langganan bulanan/tahunan selamanya, tanpa batas masa uji coba (*trial lock*), serta meniadakan skema fitur berbayar (*freemium/paywall*). Seluruh modul dapat diakses penuh sejak hari pertama.
   * **Tanpa Potongan Komisi Transaksi (*Zero Intermediary Fees*)**: Seluruh hasil penjualan produk fisik maupun nilai pendapatan jasa 100% menjadi hak penuh pemilik usaha/freelancer tanpa ada pemotongan persentase oleh sistem maupun perantara pihak ketiga.
   * **Efisiensi Biaya Operasional & Ketahanan Usaha (*Operational Cost Efficiency*)**: Memangkas biaya *overhead* teknologi hingga 100%, menjaga ketahanan operasional UMKM dan komunitas lokal pada fase awal merintis maupun saat kondisi penjualan sedang sepi.
   * **Independensi Kedaulatan Finansial (*Financial Sovereignty*)**: Menjamin kelangsungan operasional bisnis tidak dapat dihentikan secara sepihak oleh penyedia platform komersial akibat ketidakmampuan membayar biaya sewa sistem.

6. **Performa Ringan, Antarmuka Intuitif, & Kesiapan Lokalisasi Global (*i18n Ready*)**  
   Dirancang agar inklusif dan dapat digunakan secara langsung oleh siapa saja tanpa hambatan teknis maupun keterbatasan perangkat:
   * **Antarmuka Tanpa Kurva Pembelajaran (*Zero-Learning Curve*)**: Tampilan dirancang ramah, komunikatif dalam Bahasa Indonesia sehari-hari, serta mudah dipahami oleh pengguna awam tanpa memerlukan pelatihan teknis khusus.
   * **Desain Lintas Perangkat & Hemat Sumber Daya**: Bekerja dengan mulus di layar ponsel (*smartphone*), tablet, maupun laptop, serta dioptimalkan agar tetap lancar pada perangkat berspesifikasi rendah dan koneksi internet terbatas.
   * **Arsitektur Multibahasa Standar Global (*i18n*)**: Pemisahan yang rapi antara kode program dan teks antarmuka memudahkan komunitas internasional untuk menerjemahkan serta mengadaptasi sistem ini ke dalam berbagai bahasa dunia.

7. **Keamanan, Privasi Utama, & Tanpa Penjejakan (*Privacy-First & Zero Telemetry*)**  
   Sistem dibangun dengan standar privasi tinggi untuk melindungi seluruh aktivitas operasional dan data bisnis pengguna:
   * **Bebas Penjejakan & Iklan**: Aplikasi tidak mengumpulkan data pribadi, riwayat transaksi, maupun analitik perilaku pengguna secara diam-diam (*zero telemetry*).
   * **Perlindungan Data Lokal**: Seluruh basis data disimpan dan dienkripsi langsung pada perangkat pengguna, menghilangkan risiko kebocoran data dari peretasan server terpusat.

8. **Interoperabilitas & Standar Data Terbuka (*Open Standards & Interoperability*)**  
   Mencegah keterisolasian sistem (silo data) dengan memastikan data dapat terhubung secara bebas tanpa batasan vendor:
   * **Format Terbuka Standar**: Seluruh data transaksi, inventaris, dan keuangan tersimpan dalam format terbuka (JSON, CSV, REST API) yang dapat dipindahkan atau diekspor kapan saja untuk kebutuhan audit atau integrasi.
   * **Integrasi Ekosistem Fleksibel**: Memudahkan keterhubungan dengan aplikasi *open-source* lain, perangkat kasir fisik, maupun alat analitik tambahan di masa depan.

9. **Aksesibilitas Inklusif & Operasional Luring (*Offline-First & Inclusive Design*)**  
   Memastikan sistem dapat digunakan secara optimal oleh seluruh lapisan masyarakat tanpa bergantung pada stabilitas jaringan:
   * **Pendekatan *Offline-First***: Transaksi dan pencatatan tetap berfungsi penuh saat koneksi internet terputus, serta akan melakukan sinkronisasi otomatis ketika jaringan kembali tersedia.
   * **Desain Adaptif di Berbagai Kondisi**: Antarmuka memiliki kontras visual yang jelas, navigasi sederhana yang tetap nyaman dibaca di bawah terik matahari, serta mudah dipahami oleh pengguna dari berbagai tingkat literasi digital.

---

## Keselarasan Barang Publik Digital (*DPG Alignment*)

Proyek ini dirancang secara ketat untuk memenuhi Kriteria Standar **Digital Public Goods Alliance (DPGA)**:

* **1. Relevansi SDG**: Memajukan **SDG 8** dan **SDG 9** dengan menyediakan akses infrastruktur transaksi tanpa biaya perantara bagi UMKM.
* **2. Lisensi Terbuka**: Diterbitkan di bawah **MIT License** yang diakui oleh Open Source Initiative (OSI).
* **3. Kepemilikan Jelas**: Aset dan hak cipta didokumentasikan secara terbuka di bawah entitas **VV-PUNYE Open Source & Vytra Vyctoria**.
* **4. Kemerdekaan Platform**: Arsitektur modular yang berjalan independen tanpa ketergantungan pada pustaka komersial tertutup (*no proprietary vendor lock-in*).
* **5. Dokumentasi**: Menyediakan dokumentasi lengkap untuk kode sumber, panduan instalasi, dan arsitektur data.
* **6. Ekstraksi Data (Non-PII)**: Pengguna bebas mengimpor atau mengekspor data transaksi dalam format terbuka (JSON, CSV, REST API, Protocol Buffers).
* **7. Kepatuhan Privasi**: Kepatuhan penuh terhadap regulasi pelindungan data pribadi global dan lokal.
* **8. Kepatuhan Standar**: Memenuhi standar terbuka WebCrypto API, PWA, REST API, dan Protocol Buffers (Protobuf).
* **9. Tidak Menyebabkan Kerugian (*Do No Harm*)**: Dilengkapi enkripsi lokal AES-256-GCM dan arsitektur *Zero Telemetry* untuk mencegah kebocoran data.
* **10. Ketersediaan Berkas Penginstal Mandiri (*Self-Contained Artifacts*)**: Seluruh dependensi aplikasi dipaketkan secara mandiri (*vendorized*) sehingga sistem tetap dapat dibangun (*build*) dan dijalankan di lingkungan terisolasi (*air-gapped environment*) tanpa bergantung pada ketersediaan server eksternal di masa depan.

---

## Arsitektur & Teknologi yang Digunakan (*Tech Stack*)

* **Antarmuka, SPA, & Aplikasi Web (*Frontend, SPA, & PWA*)**:
  * **React + Vite (Single Page Application / SPA)**: Memanfaatkan arsitektur *Single Page Application* agar setiap perpindahan halaman berjalan instan tanpa proses memuat ulang (*reload*). Dikombinasikan dengan Vite untuk kompilasi kode yang sangat ringan, hemat konsumsi memori, serta mempermudah partisipasi kontributor *open-source* global.
  * **Progressive Web App (PWA)**: Aplikasi dapat dipasang langsung di ponsel (Android/iOS) maupun komputer/laptop layaknya aplikasi *native*. Berfungsi penuh secara luring (*offline-first*) dan bebas dari ketergantungan toko aplikasi komersial (*Play Store / App Store*).

* **Serialisasi Data & Penyimpanan Luring (*Protobuf & Storage*)**:
  * **Protocol Buffers (Protobuf / .proto)**: Menggunakan format data biner berskema terbuka untuk mengompresi paket transaksi hingga ukuran sekecil mungkin. Hasilnya, pertukaran data berjalan super cepat, hemat kuota internet, dan sangat tangguh di daerah dengan sinyal lemah (*low-bandwidth ready*).
  * **IndexedDB & SQLite**: Kombinasi basis data mandiri tanpa biaya lisensi. IndexedDB menangani penyimpanan transaksi lokal di dalam peramban (*browser*) perangkat pengguna, sedangkan SQLite digunakan untuk pengelolaan data pada server lokal maupun VPS.

* **Layanan Inti & Mesin Server (*Fastify Backend*)**:
  * **Fastify (Node.js Framework)**: Kerangka kerja server berkinerja tinggi yang dipilih sebagai *backend* tunggal. Fastify memiliki validasi skema otomatis yang menolak data berbahaya sebelum masuk ke sistem, konsumsi RAM yang sangat hemat, serta stabilitas tinggi pada perangkat berspesifikasi rendah (*Single-Board Computer* seperti Raspberry Pi/Orange Pi maupun laptop lawas).
  * **Arsitektur API Terbuka**: Menyediakan skema komunikasi REST dan Protobuf yang terstruktur rapi untuk mempermudah integrasi dengan aplikasi *open-source* lain tanpa keterikatan pada satu penyedia (*no vendor lock-in*).

* **Keamanan Berlapis & Privasi Mutlak (*Multi-Layer Encryption & Zero Telemetry*)**:
  * **Enkripsi Berlapis (AES-256-GCM / WebCrypto API)**: Menerapkan standar kriptografi terbuka untuk melindungi data saat tersimpan di media penyimpanan lokal (*Data at Rest*) maupun saat ditransmisikan melalui jaringan (*Data in Transit*). Kunci enkripsi dipegang penuh oleh pemilik usaha.
  * **Bebas Pelacak & Bebas Iklan**: 100% bersih dari kode penjejak (*zero telemetry*), *cookies* pemasaran pihak ketiga, dan iklan komersial untuk menjaga integritas proyek sebagai Barang Publik Digital (*Digital Public Goods*).

---

## Keamanan Berlapis, Privasi, & Kepatuhan Hukum (*Security & Privacy Architecture*)

Sistem dibangun dengan standar keamanan dan perlindungan data tingkat tinggi:

* **Arsitektur Bebas Penjejakan (*Zero Telemetry*)**: Aplikasi 100% bebas dari kode analitik pihak ketiga, *cookies* pemasaran, atau pengumpulan data perilaku secara diam-diam.
* **Enkripsi Lokal AES-256-GCM (WebCrypto API)**: Seluruh basis data disimpan dan dienkripsi langsung pada perangkat pengguna (*Data at Rest & Data in Transit*). Kunci enkripsi dipegang penuh oleh pemilik akun tanpa ada akses *backdoor*.
* **Kepatuhan Regulasi Privasi (UU PDP & GDPR)**: 
  * Memenuhi prinsip *Data Minimization* UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi (**UU PDP Indonesia**).
  * Memenuhi regulasi perlindungan data Uni Eropa (**GDPR EU Regulation 2016/679**).
  * Menjamin hak kedaulatan data pengguna untuk menghapus (*Right to be Forgotten*) atau memindahkan data (*Data Portability*) kapan saja.
* **Validasi Skema Ketat pada Lapisan Masukan (*Input Gate/Layer*)**: Fastify dan Protobuf secara otomatis memvalidasi struktur data untuk mencegah serangan *SQL Injection*, *Cross-Site Scripting* (XSS), dan *Prototype Pollution*.

---

## Strategi Infrastruktur & Kedaulatan Jaringan (*Platform-Agnostic*)

Sistem dirancang secara fleksibel agar dapat dijalankan pada berbagai tingkatan infrastruktur tanpa keterikatan penyedia layanan (*cloud-agnostic*):

* **Prioritas 1 — Solusi 100% Open-Source & Mandiri (*Self-Hosted*)**: Panduan standar menggunakan *reverse-proxy* terbuka (Caddy, Nginx, atau Traefik) serta alat *tunneling* terbuka (Rathole, BoringProxy, atau FRP) untuk menghubungkan server lokal ke internet secara independen.
* **Prioritas 2 — Layanan Pelindungan Tambahan Opsional (*Opt-In Cloudflare Tunnel/Proxy*)**: Dokumentasi menyediakan opsi panduan konfigurasi Cloudflare secara manual bagi pengguna yang membutuhkan proteksi DDoS otomatis dan SSL gratis tanpa mengikat kode aplikasi pada layanan *proprietary*.
* **Prioritas 3 — Fleksibilitas Perangkat Keras & Cloud**: Bebas dijalankan pada komputer rumah (*home server*), laptop lawas, *Single-Board Computer* (Raspberry Pi / Orange Pi), VPS independen, hingga penyedia layanan *cloud* skala besar.

---

## Panduan Instalasi Ringkas (*Quick Start*)

Panduan cepat untuk menyiapkan dan menjalankan aplikasi di lingkungan lokal atau server pengujian:

### Prasyarat Sistem
Pastikan perangkat Anda telah terpasang perangkat lunak pendukung berikut:
* **Node.js**: Versi `20.x LTS` ke atas (Teruji optimal pada Node.js `v22.x` dan `v24.x`)
* **NPM**: Versi `10.x` atau `11.x` ke atas
* **Git**: Terpasang di sistem operasi Anda

---

### Langkah Pemasangan

1. **Mengunduh Repositori & Masuk ke Direktori Proyek**

   Jalankan perintah berikut di terminal komputer Anda:
   ```bash
   git clone https://github.com/vytravyctoria/VV-PUNYE-Open-Source.git
   cd VV-PUNYE-Open-Source
   ```

2. **Memasang Dependensi Proyek**

   Pasang seluruh pustaka yang dibutuhkan aplikasi:
   ```bash
   npm install
   ```

3. **Menyiapkan Berkas Konfigurasi Lingkungan (*Environment Variables*)**

   Duplikasi berkas pengaturan contoh menjadi berkas konfigurasi aktif:
   * **Linux / macOS / Git Bash**:
     ```bash
     cp .env.example .env
     ```
   * **Windows PowerShell**:
     ```powershell
     Copy-Item .env.example .env
     ```

4. **Menjalankan Mode Pengembangan (*Development Mode*)**

   Jalankan server aplikasi secara lokal:
   ```bash
   npm run dev
   ```
   Aplikasi antarmuka (React + Vite) dan server inti (Fastify) akan berjalan secara bersamaan dan dapat diakses langsung melalui peramban web (*browser*) Anda.

5. **Menjalankan Pengujian Otomatis (*Test Suite - Opsional*)**

   Untuk memverifikasi integritas fungsi kode dan validasi skema:
   ```bash
   npm test
   ```

---

## Peta Jalan Berkelanjutan (*Roadmap*)

Pengembangan **VV-PUNYE Open Source** dilaksanakan secara bertahap dan terukur untuk mendukung transparansi capaian teknis, tata kelola hibah (*grant governance*), serta keterbukaan bagi komunitas global.

Rincian lengkap mengenai tahapan pengembangan, indikator capaian (*milestones*), target *deliverables*, dan laporan kemajuan proyek dapat diakses secara langsung pada dokumen terpisah:

👉 **[Lihat Peta Jalan Pengembangan Lengkap (ROADMAP.id.md)](./ROADMAP.id.md)**

---

## Tata Kelola Hibah & Akuntabilitas (*Grant Governance*)

Proyek ini berkomitmen menjaga transparansi penuh atas seluruh dukungan finansial dan hibah (*grants*) internasional:

* **Pencatatan Kas Publik**: Seluruh penerimaan dana hibah, donasi, dan alokasi pengeluaran dicatat secara terbuka melalui wadah [Open Source Collective](https://opencollective.com/vv-punye-open-source).
* **Independensi Riset & Dampak**: Alokasi dana diprioritaskan untuk pemeliharaan infrastruktur server pengujian mandiri (*self-hosted*), pengujian lintas perangkat keras, serta keberlanjutan edukasi teknologi terbuka melalui **LKP VYCTORIA**.

---

## Dukungan & Pendanaan (*Sponsorship*)

**VV-PUNYE Open Source** dikembangkan murni sebagai Barang Publik Digital yang bebas komisi dan bebas biaya sewa selamanya. Untuk menjaga akuntabilitas, independensi riset, serta keberlanjutan edukasi teknologi melalui **LKP VYCTORIA**, Anda dapat memberikan dukungan sukarela melalui dua jalur resmi berikut:

### 1. Kas Resmi Proyek (*Official Project Collective*)
Dukungan yang dialokasikan khusus untuk operasional pengembangan perangkat lunak, infrastruktur server pengujian mandiri (*self-hosted*), dan pengelolaan hibah (*grants*) internasional berbasis pembukuan kas terbuka:

* **Open Collective (Kolektif Proyek)**: [opencollective.com/vv-punye-open-source](https://opencollective.com/vv-punye-open-source)

### 2. Dukungan Personal & Pengembang Utama (*Individual & Research Host*)
Apresiasi dan dukungan langsung kepada pengembang utama untuk keberlanjutan riset mandiri serta penyediaan materi edukasi digital gratis:

* **Open Collective (Personal)**: [opencollective.com/vytravyctoria](https://opencollective.com/vytravyctoria)
* **Ko-fi**: [ko-fi.com/vytravyctoria](https://ko-fi.com/vytravyctoria)
* **Polar**: [polar.sh/vytravyctoria](https://polar.sh/vytravyctoria)
* **Liberapay**: [liberapay.com/vytravyctoria](https://liberapay.com/vytravyctoria)
* **PayPal**: [paypal.me/vytravyctoria](https://paypal.me/vytravyctoria)
* **Solana Wallet (SPL/SOL)**: `36f9QZafJWEtTVHywuKqBQDjNmWCJoHaTCep3Mmwegbc`

---

## Panduan Kontribusi (*Contributing Guide*)

Kontribusi dari komunitas global—baik berupa perbaikan kode, laporan kendala, penyempurnaan fitur, maupun penerjemahan bahasa—sangat diapresiasi demi menjaga keberlanjutan proyek ini. 

Untuk menjaga ketertiban repositori dan keselamatan pengguna, mohon perhatikan etika serta alur kontribusi berikut:

### 1. Etika Pelaporan Isu (*Issue Etiquette*)

Sebelum membuat tiket baru pada menu **Issues**, pastikan Anda memeriksa daftar isu yang sudah ada agar tidak terjadi duplikasi:

* **Laporan Bug (*Bug Report*)**:  
  Jika menemukan kesalahan teknis atau galat pada sistem, gunakan template **Bug report**. Harap sertakan:
  * Deskripsi masalah yang jelas dan langkah-langkah untuk mereproduksinya (*steps to reproduce*).
  * Lingkungan perangkat (Versi Node.js, peramban/OS, tipe instalasi).
  * Cuplikan layar (*screenshot*) atau catatan galat (*error log*) jika ada.

* **Usulan Peningkatan Fitur (*Feature Request*)**:  
  Jika memiliki ide modul baru atau penyempurnaan antarmuka, gunakan template **Feature request**. Jelaskan:
  * Latar belakang masalah riil yang dihadapi UMKM/pekerja mandiri di lapangan.
  * Solusi fitur yang diusulkan dan mengapa fitur tersebut penting.
  * *Catatan:* Usulan fitur harus selaras dengan prinsip kesederhanaan, *Zero Telemetry*, dan menghindari ketergantungan pada vendor berbayar (*no-vendor lock-in*).

* **Pelaporan Celah Keamanan (*Security & Responsible Disclosure*) — SANGAT PENTING**:  
  Jika Anda menemukan indikasi celah keamanan, potensi kebocoran data, atau kerentanan kriptografi:
  * ❌ **JANGAN** membuat laporan publik di menu *Issues*.
  * 🔒 **GUNAKAN JALUR PRIVAT**: Laporkan secara tertutup melalui menu [GitHub Security Advisories](https://github.com/vytravyctoria/VV-PUNYE-Open-Source/security/advisories) di repositori ini, atau hubungi pengembang langsung melalui kontak resmi. Tim akan segera menelaah dan menyiapkan perbaikan (*patch*) sebelum isu dipublikasikan ke publik.

---

### 2. Standar Kode (*Code Standards*)

Setiap kontributor kode teknis diharapkan mematuhi standar berikut:
* **Validasi Skema**: Seluruh *endpoint* API baru wajib divalidasi skemanya menggunakan Fastify dan skema Protobuf yang ketat.
* **Nir-Telemetri (*Zero Telemetry*)**: Dilarang keras menambahkan kode pelacak analitik pihak ketiga, iklan, maupun kuki tersembunyi.
* **Kemandirian Dependensi**: Tidak diperkenankan menambahkan pustaka dependensi komersial (*proprietary*) atau pustaka yang memicu biaya berlangganan.
* **Modularitas**: Pastikan fitur baru tidak merusak arsitektur dasar (*offline-first*) yang sudah berjalan.

---

### 3. Pengajuan Perubahan (*Pull Request / PR*)

1. Buat cabang fitur baru dari cabang utama (`git checkout -b fitur/nama-fitur`).
2. Tulis pesan komit (*commit message*) yang jelas dan deskriptif.
3. Jalankan pengujian lokal terlebih dahulu (`npm test`) untuk memastikan tidak ada fungsi yang rusak.
4. Ajukan *Pull Request* (PR) ke cabang `main` dengan mencantumkan deskripsi perubahan serta nomor tiket *Issue* terkait.

---

## Lisensi Perangkat Lunak (*License*)

Proyek ini dilisensikan di bawah **MIT License** — sebuah lisensi perangkat lunak terbuka (*open-source*) resmi yang disetujui oleh **Open Source Initiative (OSI)**. 

Hak cipta dan dokumentasi dikelola secara terbuka di bawah entitas **VV-PUNYE Open Source & Vytra Vyctoria**. Lisensi ini memberikan kebebasan mutlak bagi siapa pun untuk menggunakan, mempelajari, mengubah, menggandakan, dan mendistribusikan ulang perangkat lunak ini secara gratis selamanya, menjadikannya memenuhi syarat fundamental sebagai Barang Publik Digital (*Digital Public Goods*).