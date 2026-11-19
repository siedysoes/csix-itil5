# Change Enablement

Change Enablement memastikan bahwa change — termasuk change darurat — dinilai, diotorisasi, dijadwalkan, diimplementasikan, dan ditinjau dengan risiko serta gangguan seminimal mungkin. ITIL 4 mengubah nama praktik lama "Change Management" menjadi "Change Enablement"; verifikasi terminologi terkini di peoplecert.org / dokumentasi resmi, karena nama praktik, definisi, dan konten ujian berubah antar rilis.

## Apa yang dihitung sebagai change?

| Contoh change | Catatan |
| --- | --- |
| Perangkat keras baru | Server, switch, penerapan laptop untuk seluruh karyawan |
| Pembaruan perangkat lunak | Patch, upgrade versi, aplikasi baru |
| Perubahan konfigurasi | Aturan firewall, rekaman DNS, penyesuaian izin akses |
| Perubahan proses | Langkah persetujuan baru, jam dukungan yang direvisi |
| Decommissioning | Pensiunkan perangkat keras, aplikasi, atau lingkungan |

Jika itu mengubah layanan, komponennya, atau cara layanan dijalankan, itu adalah change. Inti praktiknya adalah membuat risiko terlihat sebelum implementasi — bukan menambah birokrasi demi birokrasi itu sendiri.

## Tiga tipe change

| Tipe | Otorisasi | Risiko & familiaritas | Penanganan |
| --- | --- | --- | --- |
| Standard | Pra-otorisasi | Risiko rendah, sudah dipahami baik, bisa diulang | Mengikuti pemicu dan prosedur yang terdokumentasi (misalnya reset password, patch rutin dari daftar yang disetujui) |
| Normal | Dinilai dan diotorisasi sebelum implementasi | Bervariasi | Sebagian besar change; membutuhkan penilaian risiko dan persetujuan |
| Urgent / darurat | Diotorisasi dengan cepat karena sifatnya yang mendesak | Sering lebih berisiko | Diimplementasikan dengan cepat, tetap ditinjau sesudahnya |

### Contoh klasifikasi

| Change | Tipe | Alasan |
| --- | --- | --- |
| Menerapkan patch OS rutin dari daftar yang disetujui | Standard | Sudah disetujui di muka, risiko rendah, prosedur terdokumentasi |
| Meng-upgrade database ke versi mayor baru | Normal | Membutuhkan penilaian, pengujian, dan persetujuan |
| Rollback deployment yang rusak pukul 02:00 | Emergency | Keterlambatan akan menimbulkan kerugian lebih besar; tinjauan menyusul |

## Alur change

```text
raise change → classify (standard / normal / emergency) → assess risk & impact
             → authorize (change authority; CAB as advisory) → schedule (change window)
             → implement → verify → review (post-implementation review)
```

## Peran dalam change

| Peran | Tanggung jawab |
| --- | --- |
| Requester | Mengajukan change dengan justifikasi bisnis atau teknis yang jelas |
| Change authority | Menyetujui change; tingkatnya tergantung pada risiko dan lingkup |
| Change manager | Menjalankan proses, memelihara jadwal, memastikan penilaian benar-benar dilakukan |
| CAB (Change Advisory Board) | Memberikan masukan dan saran dari para ahli — di ITIL 4+ peran CAB bergeser ke arah advisori daripada persetujuan akhir; verifikasi formulasi resminya |

## Kalender change

Tampilan bersama atas change yang dijadwalkan, rilis, dan periode freeze. Ini mencegah tabrakan antar tim, menunjukkan kepada stakeholder apa yang sedang berlangsung, dan memperjelas kapan freeze melindungi periode penting — bukan sekadar memblokir semuanya secara default.

## Checklist risiko dan dampak

Sebelum sebuah change normal diotorisasi, konfirmasikan:

```text
[ ] What can go wrong? (likelihood of failure)
[ ] How bad would it be? (impact on users and services)
[ ] Backout plan: how do we revert if it fails?
[ ] Testing: tried in a lower environment first?
[ ] Dependencies: other systems, teams, or changes affected
[ ] Timing: change window, blackout periods, business calendar
[ ] Communication: who needs to know before, during, and after
```

## Change darurat

Change darurat boleh diimplementasikan sebelum otorisasi penuh ketika keterlambatan menimbulkan kerugian yang lebih besar — persetujuan retrospektif diizinkan. Change tetap membutuhkan record, penilaian sejauh waktu mengizinkan, rencana backout bila memungkinkan, dan tinjauan pasca-implementasi; urgensi tidak menghapus akuntabilitas.

### Triase di bawah tekanan

Tidak setiap change selama incident adalah darurat:

- Apakah menunggu memperburuk dampaknya? Jika ya, perlakukan sebagai change darurat.
- Apakah ini bisa menunggu jendela terjadwal berikutnya? Jika ya, ajukan change normal untuk slot tersebut.
- Apakah ini sudah dicakup oleh prosedur standard? Jika ya, ikuti prosedur itu meski di bawah tekanan.

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Menyetujui semua change secara membabi buta | Proses menjadi formalitas belaka; risiko tidak terdeteksi |
| Tanpa rencana backout | Change yang gagal berubah menjadi gangguan tanpa jalan keluar yang mudah |
| Melewati tinjauan pasca-implementasi | Kegagalan berulang; pelajaran tidak pernah tertangkap |
| Membekukan semua change selama incident | Pekerjaan sehat terblokir alih-alih ditriase berdasarkan risiko |
| Change yang bertumpuk dalam jendela yang sama | Ketika ada yang rusak, tidak ada yang tahu change mana yang menyebabkannya |

## Metrik

Tingkat keberhasilan change, change yang gagal, pangsa change darurat, dan change yang diimplementasikan di dalam jendelanya adalah indikator yang umum — lihat [Metrik & KPI](../career/metrics-kpis.md). Bacalah bersama konteksnya: pangsa change darurat yang tinggi adalah sinyal untuk menyelidiki, bukan kegagalan otomatis.

## Dalam service value chain

Change Enablement terutama berada di **Design & Transition** (menilai dan mengotorisasi apa yang masuk ke penggunaan produksi) dan mendukung **Obtain/Build** ketika komponen dibeli atau dibangun.

## Lihat juga

- [Manajemen Problem](problem-management.md)
- [Manajemen Keamanan Informasi](information-security-management.md)
- [Empat Dimensi Service Management](../fundamentals/four-dimensions.md)
- [Metrik & KPI](../career/metrics-kpis.md)
