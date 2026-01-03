# Short Film Production Management System

Aplikasi berbasis web yang dibangun dengan Laravel untuk membantu tim produksi film pendek dalam mengelola manajemen proyek, mulai dari pre-production hingga post-production. Sistem ini memudahkan pengorganisasian scene, shot list, dan tugas kru secara kolaboratif.

## 🚀 Fitur Utama

-   **Manajemen Scene & Shot**: Mengatur breakdown naskah ke dalam scene, shots, dan sub-shots.
-   **Role-Based Access Control**: Hak akses yang berbeda untuk Admin, Sutradara, Kru, dll (menggunakan Laratrust).
-   **Todo & Task Management**: Melacak tugas-tugas yang perlu diselesaikan oleh setiap departemen.
-   **Dashboard Interaktif**: Ringkasan status proyek secara real-time.
-   **Modern UI**: Antarmuka responsif dan bersih menggunakan TailwindCSS.

## 🛠️ Teknologi yang Digunakan

-   **Framework**: [Laravel 11](https://laravel.com)
-   **Frontend**: [Livewire 3](https://livewire.laravel.com) + [TailwindCSS](https://tailwindcss.com)
-   **Authorization**: [Laratrust](https://laratrust.santigarcor.me)
-   **Database**: MySQL / SQLite (Default)

## 📋 Persyaratan Sistem

Pastikan environment development Anda memenuhi persyaratan berikut:

-   PHP >= 8.2
-   Composer
-   Node.js & NPM

## 🔧 Cara Instalasi dan Penggunaan

Ikuti langkah-langkah berikut untuk menjalankan project di komputer lokal Anda:

1. **Clone Repository**

    ```bash
    git clone https://github.com/username/short-film-project.git
    cd short-film-project
    ```

2. **Install Dependencies**
   Install dependensi PHP dan JavaScript:

    ```bash
    composer install
    npm install
    ```

3. **Konfigurasi Environment**
   Salin file contoh konfigurasi dan buat file `.env` baru:

    ```bash
    cp .env.example .env
    ```

    Sesuaikan konfigurasi database di dalam file `.env` jika Anda menggunakan MySQL. Jika menggunakan SQLite, Anda bisa melewati langkah ini (Laravel akan otomatis membuat file sqlite jika belum ada saat migrasi).

4. **Generate App Key**

    ```bash
    php artisan key:generate
    ```

5. **Setup Database**
   Jalankan migrasi dan seeder untuk mengisi database dengan data awal (roles, permissions, contoh user):

    ```bash
    php artisan migrate --seed
    ```

    _Note: Seeder akan membuat data role dan user default yang diperlukan untuk login._

6. **Jalankan Development Server**
   Buka dua terminal terpisah untuk menjalankan Laravel server dan Vite (untuk compile asset):

    Terminal 1 (Laravel):

    ```bash
    php artisan serve
    ```

    Terminal 2 (Vite):

    ```bash
    npm run dev
    ```

7. **Akses Aplikasi**
   Buka browser dan kunjungi `http://localhost:8000`.

## 👤 Akun Demo (Default Seeder)

Jika Anda menjalankan `php artisan migrate --seed`, sistem biasanya akan membuat akun default. Silakan cek `database/seeders/UsersSeeder.php` untuk detail kredensial login (biasanya email: `admin@app.com` atau serupa).
