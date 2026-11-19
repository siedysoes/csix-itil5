# Manajemen Insiden

Manajemen Insiden adalah praktik untuk memulihkan operasi layanan normal secepat mungkin dan meminimalkan dampak bisnis ketika layanan terganggu. Bagi analis help desk dan service desk, ini adalah keterampilan inti sehari-hari: memadamkan masalah dengan baik berarti pemulihan yang cepat, tenang, dan terkomunikasi dengan baik — bukan kekacauan.

## Incident vs problem vs request

| Tipe | Situasi | Tujuan | Waktu |
| --- | --- | --- | --- |
| Incident | Layanan mati atau kualitasnya menurun | Pulihkan layanan sekarang | Segera |
| Problem | Akar masalah belum diketahui — bisa ada bahkan tanpa incident | Temukan dan hilangkan penyebabnya | Investigatif, bisa berjalan lama |
| Request | Pekerjaan normal yang sudah disepakati di awal, tidak ada yang rusak | Fulfill melalui alur kerja yang terdefinisi | Terencana, dalam target |

Klasifikasikan saat intake, bukan saat penutupan. Incident yang berulang bisa menjadi pertanda adanya problem, dan permintaan akses tidak pernah merupakan incident.

## Siklus hidup incident

```text
detect → log & categorize → prioritize (impact × urgency) → assign / escalate
       → diagnose → resolve → verify → close
```

1. **Detect** — alert dari monitoring, kontak pengguna, atau pemberitahuan dari tim lain.
2. **Log & categorize** — satu rekaman dengan kategori dan subkategori yang jelas; ini menjadi bahan untuk pelaporan berikutnya.
3. **Prioritize** — priority berasal dari impact × urgency, bukan dari seberapa keras seseorang meminta.
4. **Assign / escalate** — escalation fungsional ke spesialis, escalation hierarkis ke manajemen bila diperlukan.
5. **Diagnose** — terapkan perbaikan yang sudah dikenal atau sebuah workaround.
6. **Resolve & verify** — konfirmasikan kepada pengguna atau kepada monitoring bahwa layanan benar-benar telah dipulihkan.
7. **Close** — catat resolusi dan workaround apa pun untuk Manajemen Problem.

### Escalation fungsional vs hierarkis

- **Fungsional**: tiket dipindahkan ke tim dengan keahlian yang tepat (jaringan, aplikasi, vendor).
- **Hierarkis**: manajemen dilibatkan ketika incident membutuhkan wewenang, visibilitas, atau sumber daya tambahan — terutama selama major incident.

## Istilah kunci

| Istilah | Arti |
| --- | --- |
| Incident | Gangguan tak terencana atau penurunan kualitas pada sebuah layanan TI |
| Impact | Seberapa besar bisnis atau penggunanya terdampak |
| Urgency | Seberapa cepat penyelesaian dibutuhkan mengingat keadaan |
| Priority | Hasil gabungan dari impact dan urgency (P1–P4), dipakai untuk menentukan urutan |
| Escalation | Memindahkan incident ke tim yang lebih terspesialisasi (fungsional) atau ke manajemen (hierarkis) |
| Major incident | Incident berdampak tinggi yang membutuhkan penanganan terkoordinasi dan mendesak |
| Workaround | Cara sementara untuk memulihkan layanan tanpa memperbaiki penyebabnya |
| Swarming | Mengumpulkan orang-orang yang tepat pada satu tiket, alih-alih mengoperkannya antar antrian |

## Matriks priority (contoh khas)

Setiap organisasi mendefinisikan matriks, target respons, dan target pemulihan mereka sendiri — verifikasi nilai yang digunakan di lingkungan Anda. Angka di bawah ini hanyalah contoh ilustratif.

| Priority | Impact | Urgency | Respons umum | Ekspektasi pemulihan umum |
| --- | --- | --- | --- | --- |
| P1 — Kritis | Tinggi | Tinggi | Menit | Segera, kerja berkelanjutan sampai layanan pulih |
| P2 — Tinggi | Tinggi | Rendah | Hari bisnis yang sama | Beberapa jam hingga beberapa hari |
| P3 — Sedang | Rendah | Tinggi | Hari bisnis yang sama | Beberapa jam hingga beberapa hari |
| P4 — Rendah | Rendah | Rendah | Hari bisnis berikutnya | Rilis berikutnya atau jendela pemeliharaan |

Urgency bisa dinaikkan oleh urgensi waktu bisnis (misalnya tutup buku akhir bulan), tetapi impact adalah sifat layanan — selalu catat mengapa sebuah priority diubah.

## Isi record incident yang baik

- **Pengguna dan layanan yang terdampak** — siapa yang terdampak, bukan hanya sistem mana.
- **Gejala dengan kata-kata pengguna** — ditambah apa yang Anda amati sendiri.
- **Kategori dan subkategori** — dipilih saat pencatatan, bukan saat penutupan.
- **Linimasa tindakan** — agar siapa pun bisa mengambil alih tiket tanpa konteks awal.
- **Resolusi atau workaround** — baris yang akan dipakai ulang oleh Manajemen Problem.

## Penanganan major incident

- Tunjuk seorang **incident manager** untuk mengoordinasi respons dan bertanggung jawab atas linimasa.
- Tunjuk seorang **communications lead** agar pengguna, stakeholder, dan pimpinan tetap terinformasi.
- Jalankan **bridge call** bersama para responder; simpan diskusi teknis di sana alih-alih di utas email yang tersebar.
- Kirim **pembaruan status yang singkat dan teratur** — apa yang sudah diketahui, apa yang sedang dilakukan, dan kapan pembaruan berikutnya datang. Jangan pernah diam.

```text
[14:30] Logins failing for EU users. Suspected database connection exhaustion.
        Team restarting pool nodes. Next update in 15 minutes.
```

Setelah pemulihan, jalankan major incident review dan serahkan temuannya ke Manajemen Problem.

## Praktik incident yang baik

| Lakukan | Mengapa membantu |
| --- | --- |
| Beri pengguna satu titik kontak | Menghindari pekerjaan ganda dan pesan yang saling bertentangan |
| Kategorisasi dengan benar saat pencatatan | Membuat pengelolaan antrian dan pelaporan akurat |
| Jaga pengguna tetap terinformasi | Membangun kepercayaan, dan mengurangi tiket lanjutan "ada update?" |
| Jangan pernah menutup tanpa konfirmasi pemulihan | Mencegah penutupan palsu dan tiket yang dibuka kembali |
| Catat workaround-nya | Menjadi bahan Manajemen Problem dan knowledge base |
| Tentukan priority dari impact × urgency | Urutan yang adil, bukan yang paling keras suaranya |

## Jebakan umum

| Jebakan | Konsekuensi |
| --- | --- |
| Mengkategorisasi hanya saat penutupan | Laporan tidak berguna; tidak ada data tren yang andal |
| Tidak ada proses major incident | Semua orang bicara sekaligus, pembaruan berhenti, gangguan berlarut-larut |
| Menutup tiket yang tidak pernah dikonfirmasi pengguna | Layanan bagi pengguna tetap rusak; kepercayaan tergerus |
| Status "Resolved" padahal layanan masih menurun | Metrik terlihat bagus, kenyataan tidak |
| Escalation terlambat atau tidak sama sekali | Dampak membesar sementara waktu terus berjalan |

## Metrik

Pantau responsivitas dan pemulihan dengan konsep seperti **MTTA** (mean time to acknowledge) dan **MTTR** (mean time to restore), bukan sekadar jumlah tiket mentah, dan baca bersama dengan kategorinya. Lihat [Metrik & KPI](../career/metrics-kpis.md) untuk bagaimana hal ini masuk ke dalam kumpulan KPI yang lebih luas.

## Dalam service value chain

Manajemen Insiden terutama berada di **Deliver & Support**, dengan **Engage** untuk komunikasi pengguna dan **Improve** ketika tren insiden menjadi bahan kerja peningkatan.

## Lihat juga

- [Manajemen Problem](problem-management.md)
- [Manajemen Service Request](service-request-management.md)
- [Sistem Nilai Layanan](../fundamentals/service-value-system.md)
- [Peran & Karier ITSM](../career/itsm-roles.md)
- [Metrik & KPI](../career/metrics-kpis.md)
