# Service Value System

Service Value System (SVS) menjelaskan bagaimana seluruh komponen dan aktivitas sebuah organisasi bekerja bersama sebagai sebuah sistem untuk menciptakan nilai. Inilah model gambaran besar dari ITIL: alih-alih lifecycle linier, SVS menunjukkan bahan-bahan yang selalu ada (prinsip, governance, value chain, practices, peningkatan) serta alur (value chain) yang mengubah peluang dan permintaan menjadi nilai.

## Apa Itu SVS

Nilai **diciptakan bersama**: penyedia menciptakan potensi nilai melalui layanan, dan pelanggan merealisasikan nilai dengan benar-benar memakainya. SVS adalah sekumpulan komponen yang membuat penciptaan nilai bersama itu bisa diulang. Gagasan kunci:

- Ini adalah sebuah **sistem**: bagian-bagiannya saling bergantung — practices gagal tanpa governance, value chain mandek tanpa peningkatan.
- Ia menerima **peluang dan permintaan** sebagai masukan dan menghasilkan **nilai** sebagai keluaran.
- Rumusannya distabilkan bersama ITIL 4 dan berlanjut ke ITIL 5, yang menambahkan tampilan ITIL Value System. **Verifikasi terminologi terkini di peoplecert.org / dokumentasi resmi.**

## 5 Komponen SVS

| Komponen | Kontribusinya |
| --- | --- |
| Guiding principles | Arah bersama dan panduan pengambilan keputusan bagi semua orang |
| Governance | Cara menilai, mengarahkan, dan memantau pekerjaan organisasi |
| Service value chain | Aktivitas-aktivitas yang saling terhubung untuk mengubah permintaan menjadi nilai |
| Practices | Sekumpulan sumber daya organisasi yang dirancang untuk menjalankan pekerjaan atau mencapai tujuan (34 secara total) |
| Continual improvement | Kebiasaan menyelaraskan semua pekerjaan dengan kebutuhan yang berubah seiring waktu |

## Service Value Chain: 6 Aktivitas

Value chain adalah model operasional di dalam SVS. Enam aktivitas ini bukan urutan yang kaku — aktivitas-aktivitas saling terhubung dan beriterasi bergantung pada value stream.

| Aktivitas | Fungsinya |
| --- | --- |
| Plan | Memahami visi bersama, menetapkan arah, kebijakan, dan batasan |
| Improve | Peningkatan berkelanjutan produk, layanan, dan practices di semua dimensi |
| Engage | Memahami kebutuhan stakeholder, memelihara hubungan dan transparansi |
| Design & Transition | Memastikan layanan memenuhi ekspektasi kualitas, biaya, dan time-to-market — serta membawanya ke lingkungan produksi |
| Obtain/Build | Memperoleh atau membuat komponen layanan (perangkat keras, perangkat lunak, lisensi, skrip) |
| Deliver & Support | Menyampaikan layanan sesuai perjanjian dan memberikan dukungan kepada pengguna |

```text
                 opportunity & demand
                        |
                        v
   +----------------------------------------------+
   |  Plan <----> Engage <----> Improve           |
   |    |            |              ^             |
   |    v            v              |             |
   |  Design & Transition --> Obtain/Build        |
   |    |                         |               |
   |    +-----> Deliver & Support-+               |
   +----------------------------------------------+
                        |
                        v
                     value

  (activities iterate; the loop never "ends")
```

## Value Stream vs Value Chain

**Value chain** adalah kumpulan aktivitas yang tersedia. **Value stream** adalah satu jalur spesifik melalui aktivitas-aktivitas itu, ditempuh untuk memenuhi permintaan tertentu. Setiap jenis permintaan punya stream-nya sendiri, dan memetakannya akan mengungkap pemborosan.

Contoh terperinci — **"permintaan laptop baru"**:

```text
Engage            -> user submits request via portal; service desk acknowledges
Plan              -> policy check: standard build, approved vendor, budget ok
Design & Transition-> configure standard laptop profile (pre-agreed design)
Obtain/Build      -> procure device from vendor; image and encrypt
Deliver & Support -> hand over at desk; user signs; support docs updated
Improve           -> measure lead time; fix the slowest step next quarter
```

Contoh terperinci — **"perbaikan bug perangkat lunak"**: Engage (bug dilaporkan) → Plan (diprioritaskan di backlog) → Design & Transition (perbaikan dirancang, diuji, dirilis) → Obtain/Build (kode/komponen dibangun) → Deliver & Support (dideploy, pengguna diberi tahu) → Improve (akar masalah dikembalikan). Telusuri permintaan yang paling sering muncul di tim Anda dengan cara ini; jeda terpanjang antar aktivitas biasanya adalah tempat masalahnya berada.

## Continual Improvement: Mesinnya

Peningkatanlah yang membuat sistem tetap beradaptasi terhadap perubahan. ITIL menjelaskan **continual improvement model** — siklus berulang yang sering dirangkum secara konseptual sebagai:

1. Apa visinya? (selaras dengan arah organisasi)
2. Di mana kita sekarang? (baseline, dengan data)
3. Ke mana kita ingin menuju? (target state)
4. Bagaimana mencapainya? (rencananya)
5. Ambil tindakan (implementasikan, secara bertahap)
6. Apakah kita sudah sampai? (ukur terhadap baseline — lalu ulangi)

**Verifikasi rumusan resmi langkah-langkah model ini di peoplecert.org / dokumentasi resmi.** Intinya adalah bahwa peningkatan adalah sebuah lingkaran yang menempel pada *segala sesuatu*, bukan proyek tahunan: masing-masing dari enam aktivitas value chain menyertakan peningkatan dalam cara kerjanya.

## Kebingungan yang Umum

Pemula sering tertukar dengan istilah-istilah berikut. Pembedanya dalam satu baris:

| Istilah | Apa itu |
| --- | --- |
| Service Value System | Seluruh sistem: kelima komponen yang bekerja bersama |
| Service Value Chain | Hanya model operasionalnya: enam aktivitas yang saling terhubung |
| Value stream | Satu jalur spesifik melalui value chain untuk satu jenis permintaan |
| Practice | Kemampuan yang terdefinisi (misalnya Incident Management) yang memakai value chain |
| Lifecycle (ITIL v3) | Model lama berbasis tahap yang digantikan oleh value chain |

## Catatan Terminologi

Terminologi SVS dan value chain diperkenalkan dan distabilkan bersama ITIL 4 (2019) serta diteruskan dalam ITIL 5 (diumumkan Januari 2026), yang menambahkan tampilan ITIL Value System dan menekankan value stream mapping. Jumlah dan pengelompokan practices berbeda antar versi — **verifikasi struktur dan rumusan terkini di peoplecert.org / dokumentasi resmi** sebelum memakai materi ini untuk persiapan ujian.

## Lihat juga

- [Apa Itu ITIL](what-is-itil.md)
- [Prinsip Panduan](guiding-principles.md)
- [Empat Dimensi Service Management](four-dimensions.md)
- [Change Enablement](../practices/change-enablement.md)
