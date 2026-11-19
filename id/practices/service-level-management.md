# Manajemen Service Level

Manajemen Service Level menetapkan ekspektasi yang jelas kepada pelanggan mengenai level layanan, menyepakatinya, memantau performa terhadapnya, dan mendorong peningkatan. Ini adalah praktik yang membuat layanan terukur dan hubungan pelanggan menjadi jujur, bukan sekadar berdasarkan cerita-cerita anekdot.

## Dokumen kunci

| Istilah | Apa itu |
| --- | --- |
| SLA — Service Level Agreement | Perjanjian dengan **pelanggan** (internal atau eksternal) yang mencakup level layanan |
| OLA — Operational Level Agreement | Perjanjian **antara tim TI internal** yang menopang sebuah SLA |
| Contract / UC — Underpinning Contract | Perjanjian dengan **pemasok eksternal** yang menopang sebuah SLA |
| Service level target | Tujuan yang spesifik dan terukur (misalnya ketersediaan atau waktu respons) |

```text
SLA  (customer ↔ IT)
 └── OLA  (IT team ↔ IT team)
      └── UC  (IT ↔ external supplier)
```

Janji dalam sebuah SLA harus ditopang sampai ke ujung rantai ini; jika tidak, TI berkomitmen pada sesuatu yang tidak bisa dipenuhi satu tim mana pun. Verifikasi definisi dokumen yang tepat terhadap dokumentasi resmi terkini.

## Pelanggan, internal dan eksternal

Pelanggan adalah siapa pun yang mengonsumsi layanan — departemen lain di dalam perusahaan yang sama, atau klien eksternal. "Internal" tidak berarti tidak formal: SLA internal tetap membutuhkan target yang disepakati, metode pengukuran, dan ritme tinjauan.

### Mulai dari yang sederhana

- Pilih sedikit target yang bisa Anda ukur sejak hari pertama.
- Pilih pengukuran yang peduli oleh pelanggan, bukan yang paling mudah diekspor.
- Tinjau ulang target setelah siklus tinjauan pertama; target yang belum diuji hanyalah tebakan.

## Tipe SLA

| Tipe | Struktur | Penggunaan khas |
| --- | --- | --- |
| Berbasis pelanggan | Satu perjanjian per pelanggan | Pelanggan dengan kebutuhan yang berbeda |
| Berbasis layanan | Satu perjanjian per layanan | Layanan yang sama digunakan banyak pelanggan |
| Multi-level | Kombinasi dari keduanya | Lingkungan campuran |

## Siklus SLM

```text
identify service requirements → define targets → draft & agree → monitor & measure
                             → report → review meeting → improve
```

## Apa yang diukur

| Pengukuran | Apa yang memberi tahu Anda | Yang perlu diwaspadai |
| --- | --- | --- |
| Availability | Seberapa sering layanan bisa digunakan | Definisikan titik pengukuran dan jendela pemeliharaan |
| Response time | Kecepatan reaksi pertama | Lingkup harus eksplisit (jam kerja vs 24/7) |
| Resolution time | Waktu untuk memulihkan atau memenuhi | Bisa memberi hadiah pada penutupan cepat alih-alih perbaikan nyata |
| Throughput | Volume yang ditangani (tiket, transaksi) | Volume saja tidak mengatakan apa pun tentang kualitas |
| Satisfaction | Persepsi pelanggan | Desain survei dan ukuran sampel itu penting |

Target harus dapat dicapai, terukur, dan terkait dengan apa yang benar-benar dihargai pelanggan — target yang tidak bisa dipengaruhi siapa pun hanyalah kebisingan.

## Tinjauan service level

Pertemuan rutin dengan pelanggan untuk meninjau laporan versus target, tren, dan perubahan yang akan datang. Tujuannya adalah peningkatan bersama, bukan menyalahkan siapa pun — bawa data, bukan alasan.

Agenda tinjauan yang berguna:

- Performa sejak tinjauan terakhir: aktual versus target.
- Tren dan pencilan — apa yang bergerak, dan ke arah mana.
- Incident dan pelanggaran, serta apa yang dilakukan terhadapnya.
- Perubahan yang akan datang dan efeknya yang diharapkan terhadap level.
- Tindakan yang disepakati, pemiliknya, dan tanggalnya.

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Target yang tidak diukur siapa pun | Kepatuhan di atas kertas; tanpa wawasan nyata |
| Vanity metrik | Angka terlihat bagus sementara pelanggan tidak puas |
| SLA yang memberi hadiah pada perilaku yang salah (misalnya menutup tiket dengan cepat alih-alih memperbaiki) | Tim mengoptimalkan metriknya, bukan layannya |
| Tanpa OLA yang menopang SLA | TI berjanji secara internal pada sesuatu yang tidak bisa ia penuhi |
| Tinjauan dilewati ketika performa baik | Hubungan hanya ada ketika ada masalah |

## Panduan desain

Jaga tetap sederhana: ITIL 4 dan versi selanjutnya menekankan nilai di atas kertas kerja birokratis — segelintir target bermakna yang terukur lebih baik daripada perjanjian tebal yang tidak dibaca siapa pun. Verifikasi panduan terkini di peoplecert.org / dokumentasi resmi.

### Jaga perjanjian tetap terbaca

- Satu bagian pendek per layanan: target, metode pengukuran, dan keala tinjauan.
- Bahasa sederhana — jika pelanggan tidak bisa mengulangi targetnya dengan kata-katanya sendiri, berarti belum disepakati.
- Seorang pemilik di setiap sisi: satu di TI, satu di tim pelanggan.

## Metrik

Persentase pencapaian SLA, jumlah dan sifat pelanggaran, serta tren seiring waktu adalah indikator intinya — lihat [Metrik & KPI](../career/metrics-kpis.md).

## Dalam service value chain

Manajemen Service Level berkontribusi pada **Plan** (memahami kebutuhan layanan), **Engage** (komunikasi pelanggan dan pertemuan tinjauan), dan **Improve** (bertindak atas kesenjangan performa).

## Lihat juga

- [Manajemen Service Request](service-request-management.md)
- [Manajemen Insiden](incident-management.md)
- [Sistem Nilai Layanan](../fundamentals/service-value-system.md)
- [Metrik & KPI](../career/metrics-kpis.md)
