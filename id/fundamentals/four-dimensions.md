# Empat Dimensi Service Management

Empat dimensi adalah checklist ITIL agar tidak ada yang terlewat: setiap layanan dan setiap practice harus dipertimbangkan lintas organisasi dan orang, informasi dan teknologi, mitra dan pemasok, serta value stream dan proses. Mengabaikan salah satunya adalah mode kegagalan yang klasik — teknologi hebat dengan orang yang tidak terlatih, atau proses sempurna yang bergantung pada satu pemasok yang tidak pernah ditinjau.

## Mengapa Empat Dimensi

Sebuah layanan tidak hidup di satu dimensi saja. Sistem yang sempurna secara teknis tetap bisa gagal karena timnya tidak terlatih, kontrak dengan pemasok tidak punya jalur eskalasi, atau serah-terima antar tim membuat permintaan jatuh terlantar. Empat dimensi memberi Anda lensa yang bisa diulang: sebelum sebuah desain disetujui atau sebuah practice diubah, telusuri keempatnya dan tanyakan apa yang kurang. Keempat dimensi berlaku untuk *semua* 34 practices — terlepas dari pengelompokan versi mana yang Anda pakai (**verifikasi detail terkini di peoplecert.org / dokumentasi resmi**).

| Dimensi | Cakupannya | Titik buta yang umum |
| --- | --- | --- |
| Organizations & People | Peran, keterampilan, budaya, struktur, tanggung jawab | Pelatihan dan komunikasi |
| Information & Technology | Data, pengetahuan, dan teknologi yang dipakai untuk menyediakan layanan | Keamanan dan aksesibilitas |
| Partners & Suppliers | Pemasok, penyedia cloud, MSP, kontrak, hubungan | Ketergantungan dan rencana keluar |
| Value Streams & Processes | Bagaimana alur pekerjaan berjalan ujung-ke-ujung, dari permintaan hingga hasil | Serah-terima dan waktu tunggu |

## Organizations & People

Dimensi ini membahas bagaimana orang diorganisasi dan apa yang mereka butuhkan untuk mengerjakan pekerjaan itu: peran pekerjaan, keterampilan, budaya, komunikasi, dan kewenangan. Teknologi tidak berjalan sendiri — sebuah proses hanya berfungsi bila ada yang menaunginya, tahu cara mengeksekusinya, dan memahami mengapa itu penting.

Contoh konkret: sebuah perusahaan membeli alat ITSM yang sangat baik, mengonfigurasi setiap modul, dan meluncurkannya — tetapi tidak ada yang dilakukan pelatihannya, kepemilikan informal lama masih berlaku, dan staf terus bekerja menyampingi alat tersebut. Dimensi People yang gagal: alatnya baik, organisasinya belum siap. Pemeriksaan khas di sini: Siapa yang menaungi ini? Siapa yang terlatih? Apa yang berubah bagi mereka, dan apakah ada yang sudah memberi tahu mereka?

## Information & Technology

Ini mencakup data dan pengetahuan yang diandalkan layanan, plus teknologi yang dipakai untuk menyampaikan dan mendukungnya: aplikasi, infrastruktur, perangkat lunak penunjang, dan knowledge base. Dimensi ini juga mencakup bagaimana informasi diklasifikasi, dilindungi, dan dibuat bisa dipakai.

Titik butanya adalah keamanan dan aksesibilitas: data yang tidak diklasifikasi siapa pun, dashboard internal tanpa model izin akses, atau dokumentasi yang hanya bisa diakses dua orang. Contoh konkret: alat pencarian intranet yang diluncurkan tanpa kontrol akses, sehingga dokumen review gaji muncul di hasil pencarian — teknologinya bekerja persis sesuai konfigurasinya, tetapi penanganan informasinya tidak pernah dirancang.

## Partners & Suppliers

Layanan modern dirakit: platform cloud, produk SaaS, MSP, operator telekomunikasi, pemasok perangkat keras, dan kontraktor semuanya berada di dalam rantai penyampaian Anda. Dimensi ini mencakup pemilihan, kontrak, integrasi, manajemen performa, serta hubungan itu sendiri.

Titik buta yang klasik adalah ketergantungan tanpa rencana keluar: layanan berjalan sepenuhnya di satu pemasok, kontraknya diperpanjang otomatis, dan tidak ada yang tahu cara bermigrasi keluar atau bahkan apa komitmen level layanannya. Contoh konkret: sebuah gangguan di penyedia cloud menghentikan bisnis selama berjam-jam, dan tim insiden menemukan bahwa tidak ada kontak eskalasi yang ditetapkan dan tidak ada waktu respons kontraktual — teknologinya gagal di hulu, tetapi dimensi Partners-lah yang jadi celah sebenarnya.

## Value Streams & Processes

Dimensi ini adalah bagaimana alur pekerjaan berjalan ujung-ke-ujung: urutan aktivitas, siapa mengerjakan apa, dan di mana pekerjaan menunggu. Sebuah proses yang terdefinisi di dokumen tetapi tidak terlihat dalam praktik — dengan serah-terima yang tidak terdokumentasi dan antrean tersembunyi — tidak dihitung.

Titik buta yang klasik adalah serah-terima dan waktu tunggu. Contoh konkret: permintaan laptop melewati lima tim; masing-masing punya "proses", tetapi permintaan itu menunggu rata-rata berhari-hari di kotak masuk bersama di antara mereka. Memetakan value stream langsung mengungkap jeda-jeda itu. Perbaikan empat dimensi biasanya menyentuh keempatnya: kepemilikan yang jelas (People), aturan auto-routing (Technology), komitmen lead-time pemasok (Partners), dan alur yang didesain ulang (Value Streams).

## Pertanyaan Self-Check Singkat

Gunakan ini sebelum menyetujui sebuah desain atau meninjau sebuah practice:

```text
Organizations & People   -> Who owns this? Who is trained? Who still
                            doesn't know anything changed?
Information & Technology  -> What data is involved? Is it classified and
                            access-controlled? Is it usable for everyone?
Partners & Suppliers      -> Which vendors sit inside this? What are the
                            escalation and exit terms?
Value Streams & Processes -> Draw the flow. Where does work wait? Which
                            handoff has no owner?
```

## PESTLE: Konteks Eksternal

Di luar empat dimensi terdapat faktor eksternal yang tidak Anda kendalikan tetapi harus direspon — dirangkum oleh **PESTLE**:

```text
P - Political      - government policy, procurement rules
E - Economic       - budgets, currency, market conditions
S - Social         - workforce expectations, remote-work norms
T - Technological  - platform shifts, AI tooling, emerging standards
L - Legal          - privacy law, licensing, regulation
E - Environmental  - energy use, sustainability reporting
```

PESTLE membentuk keempat dimensi: undang-undang privasi baru (Legal) mengubah data apa yang Anda simpan (Information & Technology), apa yang harus dilatihkan kepada staf Anda (Organizations & People), apa yang harus disampaikan pemasok secara kontraktual (Partners & Suppliers), dan bagaimana permintaan ditangani (Value Streams & Processes).

## Analisis Kasus: Peluncuran Portal HR yang Gagal

Sebuah perusahaan meluncurkan portal HR karyawan baru; adopsinya runtuh dan help desk dibanjiri keluhan. Dianalisis lintas keempat dimensi:

```text
Organizations & People   -> No training for HR staff; managers were never told
                            the new approval flow. Help desk had no scripts.
Information & Technology  -> Employee data migrated with duplicate records;
                            portal unreadable on phones (accessibility missed).
Partners & Suppliers      -> SaaS vendor's support hours did not cover the
                            company's regions; no escalation contact in the
                            contract's SLA appendix.
Value Streams & Processes -> Approval handoff from manager to HR sat in a
                            shared inbox; "who approves leave now?" had no
                            documented owner.

Diagnosis: the technology worked; three of four dimensions were untreated.
Fixes map 1:1 to the dimensions above.
```

## Hubungan Empat Dimensi dengan Practices

Keseluruhan 34 practices membutuhkan keempat dimensi agar berfungsi. Contoh — **Incident Management**:

- **Organizations & People** — jadwal piket on-call, keterampilan triase, kewenangan menyatakan insiden besar.
- **Information & Technology** — alat tiket, monitoring, dan knowledge base berisi perbaikan yang sudah dikenal.
- **Partners & Suppliers** — perjanjian eskalasi dengan pemasok perangkat keras atau cloud saat penyebabnya eksternal.
- **Value Streams & Processes** — alur terdokumentasi dari deteksi hingga resolusi hingga penutupan, termasuk serah-terima.

**Catatan:** keempat dimensi ini terbawa ke ITIL 5, yang mempertahankannya sebagai bagian dari tampilan service management-nya — **verifikasi detail terkini di peoplecert.org / dokumentasi resmi.**

## Lihat juga

- [Apa Itu ITIL](what-is-itil.md)
- [Service Value System](service-value-system.md)
- [Manajemen Insiden](../practices/incident-management.md)
- [Metrik & KPI](../career/metrics-kpis.md)
