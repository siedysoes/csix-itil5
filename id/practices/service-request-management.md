# Manajemen Service Request

Manajemen Service Request menangani semua permintaan layanan yang sudah disepakati di awal dan dimulai oleh pengguna — informasi, saran, akses, dan perubahan pada item standar — melalui proses fulfillment yang terdefinisi. Jika dilakukan dengan baik, permintaan terasa dapat diprediksi dan cepat bagi pengguna, dan dapat direncanakan oleh tim yang mengerjakannya.

## Request vs incident vs standard change

| | Service request | Incident | Standard change |
| --- | --- | --- | --- |
| Pemicu | Pengguna menginginkan atau membutuhkan sesuatu | Ada yang rusak | Change berisiko rendah yang sudah disetujui di muka |
| Diharapkan? | Ya, bagian normal bisnis | Tidak, tak terencana | Ya, rutin |
| Hasil akhir | Menyerahkan item layanan | Memulihkan layanan | Mengimplementasikan change |
| Jalur | Alur kerja fulfillment | Siklus hidup incident | Prosedur standard change |

## Contoh permintaan

| Request | Catatan fulfillment |
| --- | --- |
| Penyiapan karyawan baru | Akun, perangkat keras, dan akses sesuai peran |
| Akses ke drive bersama | Persetujuan dari pemilik data |
| Reset password | Sering berupa self-service atau otomatis |
| Permintaan instalasi perangkat lunak | Dari daftar perangkat lunak yang disetujui |
| Permintaan laporan | Ekstraksi data atau pembuatan dashboard |
| Pertanyaan informasi atau saran | Dijawab dari knowledge base |

Permintaan dicatat, dilacak, dan dilaporkan seperti incident — tetapi mindset-nya adalah fulfillment, bukan pemulihan.

## Siklus hidup request

```text
receive / submit → validate (is it in the service catalogue?) → authorize (if needed)
                 → fulfill (assign to fulfillment team) → verify with user → close
```

### Pemeriksaan validasi

```text
[ ] Is the item in the service catalogue?
[ ] Is the requester who they claim to be? (identity check)
[ ] Does the request need approval — if yes, from whom?
[ ] Is anything missing that fulfillment needs (dates, cost centre, manager)?
[ ] Which agreed target applies to this item?
```

### Siapa memenuhi apa

- Service desk menangani item sederhana dan bervolume besar: reset password, keanggotaan grup, perangkat lunak standar.
- Tim spesialis menangani item yang kompleks: perakitan perangkat keras, akses istimewa, laporan kustom.
- Apa pun yang melibatkan biaya atau akses sensitif melewati langkah persetujuan yang eksplisit.

## Service catalogue

Service catalogue (katalog layanan) adalah daftar layanan dan item request yang tersedia dan bisa dipesan pengguna. Inilah yang membuat request dapat diprediksi: item yang sudah dikenal dengan langkah yang sudah dikenal dan linimasa yang diharapkan, alih-alih permintaan email ad-hoc yang tidak bisa direncanakan siapa pun.

## Pra-otorisasi dan standardisasi

- **Item yang sudah disetujui di muka** tidak membutuhkan persetujuan per tiket — langsung berjalan ke fulfillment (misalnya, reset password dari daftar yang disetujui).
- **Item sensitif** membutuhkan otorisasi eksplisit — akses ke data rahasia, sistem istimewa, atau apa pun yang berbiaya.
- **Langkah standar** menjaga waktu fulfillment tetap konsisten dan membuat pelaporan bermakna: request yang sama, jalur yang sama, definisi selesai yang sama.

## Self-service dan otomasi

Portal, artikel knowledge, dan fulfillment otomatis mengalihkan tiket — tetapi hanya jika kontennya akurat dan benar-benar menyelesaikan masalahnya. Pertahankan standar kualitas untuk self-service: artikel yang salah lebih buruk daripada tidak ada artikel, karena pengguna berhenti mempercayai kanal tersebut dan tetap menelepon.

## Ketika sebuah request berubah menjadi incident

Jika pemenuhan sebuah request mengungkap bahwa ada sesuatu yang rusak — akun yang seharusnya ada tetapi tidak ada, layanan yang menghasilkan error saat dibuka — berhenti dan ajukan incident sebagai gantinya. Kedua alur ini memiliki priority, metrik, dan jalur escalation yang berbeda.

## Praktik request yang baik

| Lakukan | Mengapa membantu |
| --- | --- |
| Jaga item katalog tetap singkat dan bernama jelas | Pengguna memilih item yang tepat sejak percobaan pertama |
| Definisikan "selesai" untuk setiap tipe request | Tidak ada penutupan setengah jadi atau tiket berulang |
| Tinjau item bervolume besar untuk diotomasi | Pekerjaan repetitif adalah di mana otomasi memberi hasil |
| Catat persetujuan untuk request terkait akses | Jejak audit saat hak akses ditinjau kemudian |

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Request ditangani sebagai incident | Data priority menjadi bias; metrik incident tercemar |
| Langkah fulfillment tidak terdokumentasi | Penyerapan tidak konsisten; kepemilikan tidak jelas |
| Definisi "selesai" tidak jelas | Tiket ditutup setengah jadi; pengguna mengejar lagi |
| Mengabaikan volume request dalam perencanaan beban kerja | Lonjakan tiba-tiba membebani tim fulfillment |
| Pekerjaan yang sama dicatat sebagai incident sekaligus request | Perhitungan ganda dan upaya ganda |

## Metrik

Lacak waktu fulfillment dan persentase request yang selesai dalam target, dijaga terpisah dari metrik incident — lihat [Metrik & KPI](../career/metrics-kpis.md). Tren volume juga merupakan masukan perencanaan beban kerja, dan target fulfillment yang disepakati biasanya berada di katalog atau SLA.

## Dalam service value chain

Manajemen Service Request terutama berada di **Engage** (interaksi yang menghadap pengguna) dan **Deliver & Support** (pekerjaan fulfillment sehari-hari).

## Lihat juga

- [Manajemen Insiden](incident-management.md)
- [Manajemen Service Level](service-level-management.md)
- [Prinsip Panduan](../fundamentals/guiding-principles.md)
- [Peran & Karier ITSM](../career/itsm-roles.md)
- [Metrik & KPI](../career/metrics-kpis.md)
