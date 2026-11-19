# Prinsip Panduan

Tujuh guiding principles (prinsip panduan) adalah nasihat universal ITIL: rekomendasi yang memandu sebuah organisasi dalam segala keadaan, terlepas dari perubahan tujuan, strategi, jenis pekerjaan, atau struktur pengelolaan. Prinsip-prinsip ini ada agar sebuah tim bisa mengambil keputusan secara konsisten tanpa perlu buku peraturan untuk setiap situasi — itulah mengapa prinsip ini menjadi jangkar baik bagi ITIL 4 maupun ITIL 5.

## Apa Itu Guiding Principle

Guiding principle bukan langkah proses yang wajib; ia adalah rekomendasi yang *Anda sesuaikan* dengan konteks Anda. Prinsip berlaku di semua tingkat: seorang analis service desk bisa memakai "Keep it simple and practical" saat merancang template email, dan seorang CIO bisa memakai prinsip yang sama saat menyetujui program transformasi. Ketika prinsip bertentangan (dan pasti akan), Anda menimbangnya terhadap hasil yang menciptakan nilai — tidak ada urutan prioritas tetap.

> Catatan: ITIL 5 mempertahankan tujuh guiding principles yang sama, tidak berubah dari ITIL 4. **Verifikasi rumusan terkini di peoplecert.org / dokumentasi resmi.**

## 7 Prinsip Sekilas

| Prinsip | Arti | Contoh praktis di tim IT |
| --- | --- | --- |
| Focus on value | Semua yang dilakukan organisasi harus terhubung ke nilai bagi seseorang | Prioritaskan antrean reset kata sandi di atas laporan internal karena pengguna terhambat |
| Start where you are | Nilai kemampuan yang ada sebelum membangun dari nol | Pakai ulang kategori tiket yang ada, alih-alih mendesain ulang seluruh taksonomi |
| Progress iteratively with feedback | Kerjakan dalam langkah kecil, tinjau, lalu sesuaikan | Luncurkan portal baru ke satu departemen dulu, baru perluas |
| Collaborate and promote visibility | Libatkan orang yang tepat; buat pekerjaan dan keputusan terlihat | Papan backlog bersama yang bisa dilihat semua orang, bukan spreadsheet pribadi |
| Think and work holistically | Pertimbangkan layanan secara utuh, bukan satu komponen | Periksa monitoring dan dokumentasi dukungan di hilir sebelum go-live |
| Keep it simple and practical | Buang langkah yang tidak berkontribusi pada nilai | Pangkas rantai persetujuan change dari lima persetujuan menjadi dua |
| Optimize and automate | Perbaiki dulu, baru otomatiskan proses yang sudah diperbaiki | Perbaiki alur triase yang rusak sebelum mengotomatiskannya lewat skrip |

## Pembahasan Mendalam

### Focus on value

Tanyakan terus-menerus "nilai untuk siapa?" — pelanggan, pengguna, pemegang saham, atau tim Anda sendiri. Aktivitas yang tidak punya penerima nilai yang jelas adalah kandidat untuk dihapus. Misalnya, laporan status mingguan yang tidak dibaca siapa pun tidak punya nilai; sedangkan monitor yang memberi peringatan sebelum pelanggan menyadari gangguan justru punya. Nilai diciptakan bersama: ia hanya dihitung saat hasil pelanggan membaik, bukan sekadar saat tiket ditutup.

### Start where you are

"Start where you are" berarti menilai kondisi Anda saat ini secara jujur — termasuk apa yang sudah berjalan baik — alih-alih mengasumsikan bahwa pembangunan ulang dari nol diperlukan. Pentingnya, prinsip ini *tidak* berarti "jangan pernah berubah": Anda mengevaluasi yang sudah ada dengan bukti (data, observasi), mempertahankan yang bermanfaat, dan mengubah yang tidak. Tim yang mewarisi sistem tiket lama mungkin mempertahankan formulir permintaannya yang masih berfungsi, sementara hanya lapisan pelaporannya yang diganti.

### Progress iteratively with feedback

Proyek besar-bang menyembunyikan masalah sampai sudah terlambat untuk memperbaikinya dengan murah. Pecah pekerjaan menjadi inkremental kecil yang bisa dikelola, sampaikan, kumpulkan umpan balik, dan sesuaikan inkremental berikutnya. Penerapan self-service reset kata sandi ke 50 pengguna sebelum ke 5.000 menghasilkan pelajaran yang cepat dan murah. Umpan balik — bukan sekadar rencana — yang menggerakkan pekerjaan.

### Collaborate and promote visibility

Keputusan yang dibuat dalam kehampaan oleh satu tim cenderung gagal saat bertemu kenyataan. Berkolaborasilah dengan semua pihak yang pekerjaannya terdampak: operasi, keamanan, bisnis, dan pemasok. Visibility berarti dashboard, backlog yang terbuka, dan kanal insiden yang terbuka — saat semua orang bisa melihat informasi yang sama, kepercayaan naik dan kejutan menurun. Panggilan bridge insiden besar justru bekerja karena menempatkan semua pihak dalam satu kanal yang terlihat.

### Think and work holistically

Sebuah layanan lebih dari sekadar server tempatnya berjalan: ia mencakup dokumentasi, keterampilan dukungan, kontrak, data, dan ekspektasi pengguna. Mengoptimalkan satu komponen dengan mengorbankan seluruh sistem menciptakan kemenangan lokal dan kegagalan global — pembuatan yang lebih cepat tetapi tidak bisa didukung operasi. Pemikiran holistik juga mencakup empat dimensi: periksa organisasi dan orang, informasi dan teknologi, mitra dan pemasok, serta value stream untuk setiap perubahan signifikan.

### Keep it simple and practical

Setiap langkah proses harus bisa mempertahankan keberadaannya. Kompleksitas menumpuk diam-diam — kolom persetujuan tambahan, pelaporan yang redundan, serah-terima "kami selalu begini" — dan setiap item itu memakan waktu di setiap tiket berikutnya. Ujiannya sederhana: jika menghapus langkah ini tidak merugikan hasilnya, hapus. Proses sederhana juga adalah proses yang benar-benar diikuti orang.

### Optimize and automate

Otomatiskan yang bisa diulang, dan biarkan manusia menangani penilaian. Urutannya penting: otomatiskan proses yang rusak dan Anda akan mendapat hasil yang rusak, hanya lebih cepat — jadi perbaiki dulu, baru otomatiskan. Kandidat baik: reset kata sandi, provisioning pengguna, peringatan ruang disk, patching rutin. Kandidat buruk: triase insiden untuk gangguan yang ambigu, penilaian etis atau kontrak. Otomatisasi membebaskan orang terampil untuk pekerjaan yang butuh pemikiran; otomatisasi bukan alat pengurangan jumlah karyawan.

## Bagaimana Prinsip Ini Bekerja Bersama

- **Tidak ada urutan prioritas.** Prinsip adalah lensa yang Anda terapkan bersama, bukan checklist berperingkat.
- **Saat bertentangan, timbang terhadap nilai.** "Optimize and automate" mungkin mendorong penggunaan skrip, sementara "Think and work holistically" menandai bahwa tim dukungan tidak bisa memeliharanya — nilai yang memutuskan.
- **Gunakan sebagai pertanyaan keputusan.** Sebelum menyetujui pekerjaan, alirkan cepat melalui ketujuh prinsip; prinsip yang paling tersandung memberi tahu Anda di mana risikonya.

## Penyalahgunaan yang Umum

| Prinsip | Salah baca yang umum | Perbaikan |
| --- | --- | --- |
| Start where you are | "Jangan pernah ubah apa pun; kondisi kami sekarang sudah baik" | Nilai secara jujur; pertahankan yang berfungsi, ubah yang tidak |
| Optimize and automate | Dipakai untuk membenarkan PHK | Fokus pada proses dan beban kerja; prinsip ini tentang pekerjaan, bukan orang |
| Keep it simple and practical | "Sederhana" = melewati kontrol risiko | Kesederhanaan menghilangkan pemborosan, bukan kontrol yang diperlukan |
| Focus on value | Ditafsirkan sebagai "hanya uang yang penting" | Nilai mencakup kepercayaan pengguna, pengurangan risiko, dan kemampuan staf |
| Collaborate and promote visibility | Rapat tanpa akhir alih-alih keputusan | Berkolaborasi dengan orang yang *tepat*; visibility lebih baik daripada seremoni |
| Progress iteratively | Pilot tanpa akhir, tidak pernah diperluas | Iterasikan menuju satu target; setiap siklus harus menggerakkan keseluruhan |

## Penelusuran Keputusan: Haruskah Kami Membeli Alat Service Desk Baru?

Alirkan keputusan yang diusulkan melalui prinsip-prinsip tersebut sebelum mengikat anggaran:

```text
Proposal: buy a new service desk tool to replace the shared mailbox.

Focus on value            -> Who benefits? Faster responses for users;
                             measurable ticket data for the business.
Start where you are       -> The mailbox works for intake; what exactly
                             fails? Categorization and reporting.
Progress iteratively       -> Pilot with one team (2 weeks), review, expand.
Collaborate & visibility   -> Involve service desk staff, security, finance;
                             publish the evaluation criteria.
Think & work holistically -> Migration, integrations, training, and support
                             docs all needed — not just the license.
Keep it simple             -> Do we need every module, or intake + queue +
                             reporting?
Optimize & automate        -> Clean up duplicate request types BEFORE import;
                             then automate routing rules.

Verdict: phased pilot, not a big-bang purchase.
```

Inilah cara prinsip ini dimaksudkan untuk digunakan: bukan sebagai slogan, melainkan sebagai sekumpulan pertanyaan terstruktur yang mengungkap risiko sejak dini.

## Lihat juga

- [Apa Itu ITIL](what-is-itil.md)
- [Service Value System](service-value-system.md)
- [Empat Dimensi Service Management](four-dimensions.md)
