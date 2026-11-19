# Manajemen Keamanan Informasi

Manajemen Keamanan Informasi melindungi kerahasiaan, integritas, dan ketersediaan (CIA — confidentiality, integrity, availability) informasi dan layanan. Ini adalah salah satu praktik dalam kerangka ITIL dan jembatan yang menghubungkan manajemen layanan TI sehari-hari dengan keamanan — setiap incident, change, dan permintaan akses membawa sudut pandang keamanan.

## Triad CIA

| Prinsip | Arti | Contoh sederhana |
| --- | --- | --- |
| Confidentiality | Hanya orang yang berwenang yang bisa melihatnya | Data gaji hanya terlihat oleh HR |
| Integrity | Data akurat dan tidak diubah | Total pesanan yang tidak bisa diam-diam diedit siapa pun |
| Availability | Layanan tersedia ketika dibutuhkan | Intranet aktif selama jam kerja |

### Kebiasaan sehari-hari

- Verifikasi identitas sebelum mengungkapkan, mengubah, atau mereset apa pun.
- Berikan akses sekecil mungkin yang menyelesaikan tugas.
- Catat apa yang Anda lakukan — tindakan yang tidak tercatat tidak bisa ditinjau kemudian.

## Mengapa keamanan menjadi bagian dari ITSM

- Sebuah **incident** bisa menjadi incident keamanan — kebocoran data, malware, pengambilalihan akun.
- Sebuah **change** bisa merusak keamanan — aturan firewall yang dibuka "sementara".
- Sebuah **request** bisa membocorkan akses — hak yang diberikan terlalu luas atau kepada orang yang salah.

Keamanan adalah kebiasaan yang diterapkan di dalam setiap praktik, bukan silo terpisah yang muncul di akhir.

### Sudut pandang keamanan dalam pekerjaan sehari-hari

| Praktik | Pertanyaan yang perlu diajukan |
| --- | --- |
| Manajemen Insiden | Bisakah ini menjadi incident keamanan? Jika dicurigai, eskalasi sejak dini |
| Change Enablement | Apakah change ini melemahkan atau melewati sebuah control? |
| Manajemen Service Request | Apakah akses ini dibenarkan, disetujui, dan berbatas waktu? |
| Manajemen Problem | Apakah kegagalan yang berulang menunjukkan kelemahan sebuah control? |

## Security controls

| Tipe | Tujuan | Contoh |
| --- | --- | --- |
| Preventive | Menghentikan peristiwa yang tidak diinginkan | Firewall, access control, MFA |
| Detective | Menyadari bahwa itu terjadi, atau sedang terjadi | Logging, monitoring, alerting |
| Corrective | Membatasi kerusakan dan memulihkan | Patching, restore dari backup |

Control-control saling menumpuk: control detective tidak menghentikan serangan, tetapi mempersingkat waktu serangan berjalan tanpa terdeteksi. Tujuannya bukan keamanan yang sempurna — melainkan mengurangi risiko ke tingkat yang diterima dan bisa dijelaskan oleh bisnis.

## Dasar-dasar risiko

```text
asset → threat → vulnerability → impact → risk
```

Contoh: sebuah basis data pelanggan (asset) menghadapi akses tanpa izin (threat); server belum dipatch (vulnerability); catatan bisa terbuka ke publik (impact) — risiko yang dihasilkan memberi tahu Anda apakah harus mempatch sekarang, memantau, atau membatasi akses. Bahasa risiko adalah cara Anda menentukan prioritas, karena Anda tidak bisa melindungi segalanya secara merata.

## Penanganan security incident

Incident yang bernuansa keamanan tetap mengalir melalui Manajemen Insiden, dengan langkah-langkah containment dan eskalasi dini ke tim keamanan:

```text
detect → contain → eradicate → recover → learn
```

- **Contain** — hentikan penyebaran: isolasikan host, nonaktifkan akun.
- **Eradicate** — hilangkan penyebabnya: malware, akun berbahaya, konfigurasi yang rentan.
- **Recover** — pulihkan layanan dan verifikasi bahwa layanan sudah bersih.
- **Learn** — salurkan temuan ke Manajemen Problem dan ke control-nya sendiri.

Kecurigaan kebocoran data bisa membawa kewajiban hukum dan pemberitahuan — eskalasi, dan jangan menyelidiki sendirian.

## Permintaan akses: alur praktis

```text
verify identity → confirm the business need → check approval (data / system owner)
                → grant least privilege → set a review or expiry date → log the grant
```

Least privilege berarti hanya memberikan apa yang dibutuhkan tugas. Tanggal tinjauan atau kadaluwarsa adalah yang mencegah akses "sementara" menjadi permanen.

## Kaitan dengan kerangka lain

ISO/IEC 27001 adalah standar manajemen keamanan informasi yang bisa disertifikasi, dan ITIL menyediakan praktik manajemen layanan di sekitarnya — pekerjaan sehari-hari menanamkan keamanan dalam cara layanan dijalankan. Verifikasi detail terhadap dokumentasi resmi; sumber belajar ini tidak mengulangi persyaratan standar.

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Keamanan sebagai kotak centang yang dipikirkan belakangan | Masalah ditemukan terlambat, dengan biaya jauh lebih tinggi |
| Akses diberikan "sekali saja" dan tidak pernah dicabut | Hak istimewa menumpuk; risiko orang dalam membesar |
| Tanpa tinjauan berkala atas hak pengguna | Mantan staf atau akun dorman masih punya akses |
| Mengabaikan risiko pihak ketiga dan pemasok | Tautan terlemah sering kali adalah vendor yang tidak dikelola |
| Memperlakukan tiket keamanan sebagai prioritas lebih rendah | Kebocoran kecil diam-diam menjadi incident besar |

## Bingkai defensif

Praktik ini tentang melindungi layanan dan orang-orang yang bergantung padanya — memahaminya membantu Anda mengenali risiko sejak dini dan menjaga layanan tetap dapat dipercaya. Ini adalah sumber belajar independen dan tidak resmi; ITIL adalah merek dagang PeopleCert.

## Dalam service value chain

Manajemen Keamanan Informasi berkontribusi pada **Deliver & Support** (beroperasi dengan aman setiap hari), **Design & Transition** (membangun keamanan ke dalam layanan baru), dan **Improve** (menaikkan baseline keamanan seiring waktu).

## Lihat juga

- [Change Enablement](change-enablement.md)
- [Manajemen Insiden](incident-management.md)
- [Empat Dimensi Service Management](../fundamentals/four-dimensions.md)
- [Apa Itu ITIL](../fundamentals/what-is-itil.md)
