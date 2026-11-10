# CrowdChek

Aplikasi web pemantau keramaian lokasi publik berbasis laporan warga. Proyek UTS Pemrograman Web B (Gasal 2026) — frontend only (HTML5, CSS3, JavaScript).

## Fitur
Dashboard · Pencarian lokasi · Laporan keramaian · Statistik keramaian (Chart.js) · Login & Register · Admin panel

## Struktur fitur
Setiap fitur halaman memiliki file JavaScript sendiri agar dapat dikerjakan secara terpisah:

- Beranda: `js/home.js`
- Dashboard dan peta: `js/dashboard.js` dan `js/map.js`
- Pencarian lokasi: `js/search.js`
- Laporan warga: `js/report.js`
- Statistik: `js/stats.js`
- Login & register: `js/auth.js`
- Admin — ringkasan, lokasi, moderasi laporan, dan pengguna: masing-masing `js/admin-overview.js`, `js/admin-places.js`, `js/admin-reports.js`, dan `js/admin-users.js`
- Fondasi bersama: `js/store.js` (data dan logika) dan `js/ui.js` (komponen antarmuka)

Saat menambah atau memindahkan modul admin, daftarkan skrip fiturnya di `admin.html` sebelum `js/admin.js`. Hindari mengubah file fondasi bersama saat pekerjaan hanya menyentuh satu fitur.

## Menjalankan
Tidak perlu build. Buka `index.html` langsung, atau jalankan server statis: `python3 -m http.server 8000`.

## Akun demo
- Admin: `admin@crowdchek.id` / `admin123`
- Pengguna: `user@crowdchek.id` / `user123`

## Catatan
Data disimpan di `localStorage` (tanpa backend). Admin panel → Ringkasan → "Atur ulang data demo" untuk mengembalikan data awal.

## Deploy
GitHub Pages: Settings → Pages → Branch `main` / root. Netlify/Vercel: drag-drop folder ini.
