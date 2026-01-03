# Manajemen Produksi Film Berbasis Web

## Ringkasan

Aplikasi ini adalah sistem manajemen produksi film berbasis web yang dibangun dengan Laravel dan Livewire. Sistem ini mendigitalisasi proses breakdown naskah, shot listing, dan manajemen kru, memudahkan kolaborasi antar departemen (Sutradara, Produser, Kru) dalam satu platform terintegrasi. Aplikasi dilengkapi dengan kontrol akses berbasis peran (RBAC) untuk keamanan data.

## Tujuan

-   Menyediakan platform terpusat untuk manajemen pra-produksi film.
-   Menggantikan metode manual (kertas/spreadsheet) dengan pencatatan digital yang terstruktur.
-   Memfasilitasi komunikasi real-time antar kru mengenai detail scene dan shot.

## Fitur Utama

-   **Manajemen Naskah & Scenes**: Breakdown scene dengan detail lokasi (INT/EXT) dan waktu.
-   **Shot List Detail**: Pencatatan shot, angle, movement, dan lensa secara spesifik.
-   **Manajemen Sub-Shots**: Detail variasi pengambilan gambar dalam satu shot utama.
-   **Role-Based Access Control**: Hak akses berbeda untuk Admin, Sutradara, dan Kru (menggunakan Laratrust).
-   **Todo Management**: Pelacakan tugas kru per departemen.
-   **Dashboard Produksi**: Ringkasan status scene dan progress shooting.

## Arsitektur & Alur Data

-   **Model-View-Controller**: Menggunakan arsitektur standar Laravel.
-   **Reactive Frontend**: Livewire menangani interaksi pengguna (seperti update status shot) secara real-time tanpa reload halaman penuh.
-   **Authorization Layer**: Middleware Laratrust memvalidasi hak akses setiap request berdasarkan role pengguna.
-   **Database**: Relasional (MySQL/SQLite) menyimpan relasi kompleks antara Scenes -> Shots -> SubShots.

## Integrasi & Teknologi

-   **Laravel 11**: Kerangka kerja utama backend PHP.
-   **Livewire 3**: Full-stack framework untuk antarmuka dinamis.
-   **Laratrust**: Library untuk manajemen Role dan Permission yang robust.
-   **TailwindCSS**: Utility-first CSS framework untuk styling antarmuka.

## Petunjuk Deploy Singkat

-   Pastikan server memenuhi requirement PHP 8.2+ dan Composer.
-   Clone repository dan jalankan `composer install` & `npm install`.
-   Salin `.env.example` ke `.env` dan atur koneksi database.
-   Jalankan migrasi dan seeder: `php artisan migrate --seed`.
-   Build assets: `npm run build`.
-   Konfigurasi web server (Nginx/Apache) ke folder `public`.
