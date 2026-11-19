# Metrik & KPI

Pengukuran adalah cara manajemen layanan belajar: Anda tidak bisa memperbaiki apa yang tidak Anda ukur, dan metrik yang salah bisa lebih buruk daripada tidak ada metrik sama sekali. Halaman ini mendefinisikan istilah dasar, menunjukkan di mana metrik diterapkan pada praktik yang umum, dan mencatat kesalahan yang membuat dashboard menjadi tidak berguna. Terminologi metrik terus berkembang — periksa definisi terkini dalam dokumentasi resmi ITIL dan dokumentasi organisasi Anda.

## Definisi

| Istilah | Definisi | Contoh kecil |
| --- | --- | --- |
| Metric | Satu pengukuran tunggal | 42 insiden dibuka hari ini |
| KPI | Metrik yang terikat pada sebuah tujuan dan memberi tahu Anda apakah masih berada pada jalur yang tepat | 95% insiden diselesaikan dalam target bulan ini |
| CSF | Critical Success Factor (faktor keberhasilan kritis) — kondisi yang harus tercapai agar sebuah tujuan berhasil | "Pengguna mengalami gangguan minimal selama upgrade" |
| Baseline | Posisi Anda sekarang, sehingga perubahan dapat diukur | MTTR saat ini: 4 jam |

## Tingkat metrik

| Tingkat | Ritme | Contoh |
| --- | --- | --- |
| Operasional | Harian / mingguan | Tiket yang selesai, backlog saat ini, insiden terbuka |
| Taktis | Bulanan / kuartalan | Capaian SLA, tingkat perbaikan masalah |
| Strategis | Tahunan | Kepuasan pelanggan, biaya per tiket |

## Ciri metrik yang baik

| Aturan | Catatan |
| --- | --- |
| Terikat pada hasil yang terlihat pelanggan | Jika pelanggan tidak bisa merasakannya, pertanyakan |
| Benar-benar bisa dikumpulkan | Metrik yang tidak bisa dikumpulkan siapa pun tidak akan bertahan menghadapi kenyataan |
| Punya target DAN baseline | Target tanpa baseline hanyalah angan-angan; baseline tanpa target hanyalah trivia |
| Tidak memberi hadiah atas kecurangan | Goodhart's law (hukum Goodhart): ketika sebuah ukuran menjadi target, ukuran itu berhenti menjadi ukuran yang baik |

## Metrik ITSM per praktik

Tentukan target dengan hati-hati sesuai konteks Anda sendiri — **periksa target Anda sendiri** terhadap kebutuhan bisnis; jangan pernah menyalin ambang batas secara membabi buta.

| Praktik | Contoh metrik |
| --- | --- |
| Incident | MTTA, MTTR, tingkat buka ulang (reopen rate), % insiden besar |
| Problem | Tingkat insiden berulang, % known error dengan workaround, perbaikan yang telah diimplementasikan |
| Change | Tingkat sukses/gagal/rollback, % perubahan dengan post-implementation review |
| Request | Rata-rata waktu pemenuhan, % yang dipenuhi dalam target |
| Service Level | Capaian SLA %, jumlah pelanggaran (breach), tren dari waktu ke waktu |

## Kesalahan umum

| Kesalahan | Mengapa merugikan |
| --- | --- |
| Vanity metrics | Angka yang tampak bagus tetapi tidak menggerakkan keputusan apa pun |
| Mengukur volume alih-alih hasil | 100 tiket yang ditutup bisa berarti tidak ada yang benar-benar diperbaiki |
| Target yang menghukum kualitas | "Tutup tiket dengan cepat" justru mendorong penutupan yang prematur |
| Tanpa baseline | Tanpa titik awal, Anda tidak bisa mengklaim adanya perbaikan |
| Laporan yang tidak dibaca siapa pun | Laporan yang tak terbaca adalah biaya tanpa manfaat |

### Cek cepat sebelum mempublikasikan sebuah metrik

- Apakah pelanggan mengenali ini sebagai sesuatu yang penting bagi mereka?
- Dua orang bisa menghitung angka yang sama dari data yang sama?
- Apakah kita punya baseline untuk dibandingkan?
- Keputusan apa yang berubah jika angka ini bergerak?

## Ritme pelaporan

```text
Daily:   ops dashboard for the team — volume, open majors, blockers.
Weekly:  backlog & trends for leads — where work is piling up.
Monthly: service review with customers/stakeholders — SLA attainment, breaches, trend.
Quarterly: improvement candidates — pick 1-2 things to change next quarter.
```

## Memilih KPI pertama Anda

Mulai dari nilai pelanggan dan prinsip panduan "Focus on value" (lihat [Prinsip Panduan](../fundamentals/guiding-principles.md)). Pilih paling banyak 1-2 metrik per praktik — daftar pendek yang benar-benar Anda tinjau lebih berharga daripada dinding angka yang tidak dipercaya siapa pun.

Urutan pemilihan yang praktis:

1. Tulis tujuannya dalam bahasa bisnis ("pengguna mendapat bantuan cepat ketika ada yang rusak").
2. Identifikasi kondisi yang harus terpenuhi (CSF: insiden besar dipulihkan dalam jendela waktu yang disepakati).
3. Pilih kumpulan metrik terkecil yang menunjukkan apakah kondisi itu terpenuhi.
4. Catat baseline sebelum Anda mengubah apa pun.
5. Tetapkan target beserta tanggal, lalu tinjau pada ritme yang disepakati.

## Cara mengumpulkan tanpa tim data

- Mulai dari apa yang sudah dicatat sistem tiket Anda — timestamp, kategori, perubahan status.
- Sepakati definisi dengan tim sebelum mulai menghitung (apa yang dihitung sebagai "incident"? apa yang dianggap "resolved"?).
- Mulai dengan spreadsheet sederhana; otomatiskan hanya setelah definisi bertahan selama sebulan pemakaian.
- Periksa ulang definisi setiap kali tooling atau proses berubah.

## Keterhubungannya

Metrik memberi makan continual improvement (perbaikan berkelanjutan) dalam Service Value System: ukur, bandingkan dengan baseline, bertindak, lalu ukur ulang (lihat [Sistem Nilai Layanan](../fundamentals/service-value-system.md)). Service level reporting memakai angka-angka ini persis untuk menjalankan percakapan dengan pelanggan (lihat [Manajemen Level Layanan](../practices/service-level-management.md)).

## Disclaimer

Ini adalah sumber belajar independen yang tidak resmi. ITIL adalah merek dagang PeopleCert. Terminologi metrik dan ukuran yang direkomendasikan terus berkembang — periksa terminologi metrik terkini dalam dokumentasi resmi ITIL dan standar pelaporan organisasi Anda sendiri.

## Lihat juga

- [Ujian ITIL Foundation](foundation-exam.md)
- [Peran & Karier ITSM](itsm-roles.md)
- [Sistem Nilai Layanan](../fundamentals/service-value-system.md)
- [Manajemen Level Layanan](../practices/service-level-management.md)
- [Manajemen Insiden](../practices/incident-management.md)
