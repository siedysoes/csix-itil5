# Manajemen Problem

Manajemen Problem mengidentifikasi akar masalah dari incident dan problem agar insiden tidak terulang. Jika Manajemen Insiden adalah memadamkan api, Manajemen Problem adalah investigasi kebakaran yang mencegah kebakaran berikutnya.

## Problem vs incident

| Aspek | Incident | Problem |
| --- | --- | --- |
| Waktu | Reaktif — dimulai ketika layanan rusak | Bisa dimulai secara proaktif, jauh sebelum ada incident |
| Tujuan | Memulihkan layanan dengan cepat | Menghilangkan penyebab agar incident berhenti |
| Fokus | Satu gangguan | Pola dan kelemahan sistemik |
| Selesai ketika | Layanan dipulihkan | Penyebab diperbaiki, atau known error didokumentasikan |

Sebuah problem bisa ada tanpa incident sama sekali — sebuah single point of failure yang belum disadari siapa pun — dan satu problem bisa berada di balik lusinan tiket yang tampaknya tidak saling berkaitan.

## Manajemen problem proaktif vs reaktif

| Reaktif | Proaktif |
| --- | --- |
| Dipicu oleh major incident atau oleh incident yang sama yang berulang | Dipicu oleh analisis tren dan pemeriksaan kesehatan |
| Contoh: gangguan ketiga bulan ini dari batch job yang sama | Contoh: meninjau tiket prioritas rendah yang berulang, data kapasitas, dan log error |

Pekerjaan proaktif adalah di mana imbalan terbesarnya berada: tiket prioritas rendah yang berulang murah satu per satu, tetapi mahal bila diakumulasi.

### Sinyal yang layak diselidiki

- Kode error yang sama muncul di pengguna atau lokasi berbeda.
- Tiket yang dibuka kembali tak lama setelah ditandai selesai.
- Satu tim yang berulang kali menaikkan (escalate) jenis tiket yang sama.
- Alert yang berbunyi terjadwal dan secara rutin diabaikan.
- Metrik kapasitas atau performa yang merambat stabil ke satu arah.

## Siklus hidup problem

```text
detect / categorize → root cause analysis → record known error → document workaround
                    → fix via change (Change Enablement) → verify → close
```

## Known error

Sebuah problem yang akar masalah **dan** workaround-nya sudah didokumentasikan disebut **known error** (error yang sudah diketahui). Problem ini tetap terbuka sampai perbaikan permanen diterapkan — workaround membuat pengguna tetap bisa bekerja sementara investigasi berlangsung, dan memberi service desk sesuatu yang konkret untuk ditawarkan selama incident. Pindah dari known error ke closed biasanya berarti mengajukan perbaikan melalui [Change Enablement](change-enablement.md).

## Teknik root cause analysis

| Teknik | Cara kerjanya |
| --- | --- |
| 5 Whys | Terus bertanya "mengapa" sampai Anda mencapai penyebab sistemik, bukan gejala |
| Fault tree | Mendekonstruksi kegagalan ke dalam cabang-cabang penyebab pendukung |
| Analisis kronologis | Membangun linimasa peristiwa untuk melihat apa yang sebenarnya memicu kegagalan |

### 5 Whys dalam praktik

```text
Why did the site go down?   → The web server ran out of memory.
Why?                        → A memory leak in the last release.
Why was that released?      → Load testing did not cover that code path.
Why not?                    → Test data did not simulate real traffic.
→ Systemic cause: a gap in release test coverage — not "the server crashed".
```

## Elemen inti record problem

| Field | Yang perlu ditangkap |
| --- | --- |
| Problem statement | Apa yang bermasalah, dengan bahasa sederhana |
| Gejala | Apa yang benar-benar diamati pengguna dan monitoring |
| Known error | Akar masalah yang terkonfirmasi, setelah ditemukan |
| Workaround | Cara sementara agar layanan tetap bisa dipakai |
| Trigger | Incident atau tren yang memunculkan problem ini |
| Orang yang bertanggung jawab | Orang yang akuntabel untuk mendorong problem ini hingga selesai |

## Bagaimana service desk berkontribusi

- Laporkan kejadian berulang secara eksplisit: "ini keempat kalinya minggu ini" adalah pemicu, bukan keluhan.
- Sampaikan detail gejala dan linimasa — data incident yang buruk membuat root cause analysis jadi tebakan semata.
- Gunakan known error dan workaround di meja layanan, dan konfirmasi apakah workaround itu benar-benar berhasil.
- Jangan biarkan record problem tanpa pemilik; tanyakan siapa yang mendorongnya.

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Berhenti pada penyebab pertama ("server-nya crash" — mengapa?) | Gejala diperlakukan sebagai penyebab; incident terulang kembali |
| Tidak ada tinjauan proaktif | Tiket kecil yang sama berulang selamanya, tidak pernah diselidiki |
| Menutup ketika ada workaround tetapi bukan perbaikan | Known error tidak pernah naik tingkat ke resolusi |
| Root cause analysis hanya setelah major incident | Incident kecil yang bisa dicegah terus menumpuk |
| Record problem tanpa pemilik | Pekerjaan menua diam-diam di backlog yang tidak pernah ditinjau |

## Metrik

Indikator yang berguna mencakup persentase known error yang memiliki workaround terdokumentasi, tingkat incident berulang per kategori, dan usia problem yang masih terbuka. Lihat [Metrik & KPI](../career/metrics-kpis.md) untuk cara menyajikannya.

## Dalam service value chain

Manajemen Problem berkontribusi terutama pada **Improve** (menghilangkan penyebab yang berulang) dan **Design & Transition** (menyalurkan pelajaran ke layanan baru atau yang diubah).

## Lihat juga

- [Manajemen Insiden](incident-management.md)
- [Change Enablement](change-enablement.md)
- [Prinsip Panduan](../fundamentals/guiding-principles.md)
- [Metrik & KPI](../career/metrics-kpis.md)
