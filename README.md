# KB - TK Mary Anthony — Website

Homepage berdasarkan desain Figma "tk mary anthony", dibuat dengan HTML & CSS murni (CSS ditulis langsung di dalam `index.html` supaya file-nya satu dan mudah dibuka di mana saja — tinggal double-click untuk preview di browser).

## Halaman yang sudah dibuat

| File | Isi |
|---|---|
| `index.html` | Homepage publik (header, navigasi, hero, "Our News", footer) |
| `login.html` | Login dengan pilihan peran **Admin** / **Guru** |
| `admin-dashboard.html` | Dashboard Admin: ringkasan, Data Siswa, Data Guru, Pendaftaran, Berita & Event |
| `teacher-dashboard.html` | Dashboard Guru: ringkasan, Absensi, Data Siswa di kelasnya, Catatan Aktivitas Harian |

Dari `index.html`, tombol **Login** belum terhubung ke `login.html` — tinggal tambahkan `<a href="login.html">` di sekitar tombol tersebut kalau mau dihubungkan.

### Dashboard Admin (`admin-dashboard.html`)
- Kartu ringkasan (total siswa, guru, pendaftaran pending, berita terbit) yang otomatis update saat data berubah
- **Data Siswa**: tambah/edit/hapus, pencarian nama & kelas
- **Data Guru**: tambah/edit/hapus, pencarian nama
- **Pendaftaran**: filter status, tombol Terima/Tolak, bisa tambah pendaftaran manual
- **Berita & Event**: tambah/edit/hapus, status Published/Draft

### Dashboard Guru (`teacher-dashboard.html`)
- Ringkasan kelas (TK B1 sebagai contoh), jumlah hadir hari ini, jumlah catatan bulan ini
- **Absensi**: pilih tanggal, tandai Hadir/Sakit/Izin/Alpa per siswa, simpan — riwayat tersimpan per tanggal selama sesi berjalan
- **Data Siswa**: daftar siswa di kelasnya (read-only) + tombol lihat detail termasuk catatan kesehatan
- **Aktivitas Harian**: form catat kegiatan harian, tampil sebagai kartu terbaru di atas

## Catatan penting
- **Ini front-end saja (mockup).** Login tidak memvalidasi akun sungguhan (isi apa saja akan login), dan semua data (siswa, guru, pendaftaran, berita, absensi, catatan aktivitas) tersimpan sementara di memori browser — akan **kembali ke data contoh setiap halaman di-refresh**. Untuk data yang benar-benar tersimpan dan login yang aman, dashboard ini perlu disambungkan ke backend (server + database) dengan sistem autentikasi sungguhan.
- Foto asli di desain Figma tidak disalin langsung karena alasan hak cipta foto. Hero di homepage diganti dengan ilustrasi gradient "matahari & perbukitan". Untuk pakai foto sekolah asli, ganti bagian `.hero` di CSS `index.html` dengan `background-image: url('foto-kamu.jpg')`.
- Data siswa/guru/berita/pendaftaran masih contoh/placeholder, silakan disesuaikan.
- Halaman publik lain (Our School, Academics, Admissions, dst.) belum dibuat karena belum terlihat di screenshot yang dikirim — kirim screenshot halaman lainnya kalau mau dibuatkan juga.

## Cara upload ke GitHub
1. Buka folder project ini lewat terminal
2. `git init`
3. `git add .`
4. `git commit -m "Initial commit: homepage TK Mary Anthony"`
5. Buat repository baru di github.com (jangan centang "Initialize with README")
6. `git remote add origin <url-repo-kamu>`
7. `git branch -M main`
8. `git push -u origin main`

Setelah langkah di atas, file `index.html` akan langsung terlihat sebagai kode di halaman repository GitHub kamu.
