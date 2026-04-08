# Velzon Material Inertia

Starter project Laravel 11 + Inertia.js + React + Vite dengan template Velzon Material.

Repository:
`https://github.com/AbdoelMadjid/velzon-material-inertia.git`

## Requirement

Sebelum install, pastikan environment sudah tersedia:

- PHP 8.2 atau lebih baru
- Composer
- Node.js dan npm
- MySQL / MariaDB
- Git

## Cara Clone

Clone repository ke lokal:

```bash
git clone https://github.com/AbdoelMadjid/velzon-material-inertia.git
cd velzon-material-inertia
```

## Install Project

Install dependency PHP dan JavaScript:

```bash
composer install
npm install
```

## Konfigurasi Environment

Copy file environment:

```bash
cp .env.example .env
```

Jika memakai Windows Command Prompt:

```bat
copy .env.example .env
```

Jika memakai PowerShell:

```powershell
Copy-Item .env.example .env
```

Lalu generate application key:

```bash
php artisan key:generate
```

## Konfigurasi Database

Edit file `.env`, lalu sesuaikan konfigurasi database:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=material
DB_USERNAME=root
DB_PASSWORD=
```

Buat database sesuai nama yang dipakai di `.env`, misalnya `material`.

Setelah itu jalankan migrasi:

```bash
php artisan migrate
```

Jika proyek ini memakai seeder dan Anda ingin mengisi data awal:

```bash
php artisan db:seed
```

## Menjalankan Project

Jalankan backend Laravel:

```bash
php artisan serve
```

Jalankan Vite dev server di terminal lain:

```bash
npm run dev
```

Setelah itu buka aplikasi di browser, biasanya:

`http://127.0.0.1:8000`

## Build Production

Jika ingin menjalankan asset production, build Vite terlebih dahulu:

```bash
npm run build
```

File build akan dibuat di:

`public/build/manifest.json`

Jika file ini belum ada, Laravel bisa menampilkan error:

`Vite manifest not found at: .../public/build/manifest.json`

Solusinya adalah menjalankan:

```bash
npm run build
```

atau saat development gunakan:

```bash
npm run dev
```

## Ringkasan Instalasi Cepat

```bash
git clone https://github.com/AbdoelMadjid/velzon-material-inertia.git
cd velzon-material-inertia
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

Di terminal lain:

```bash
npm run dev
```

## Catatan

- Pastikan database sudah dibuat sebelum `php artisan migrate`
- Jika asset frontend berubah, jalankan kembali `npm run build` atau `npm run dev`
- Jika ada error cache/config, bisa coba:

```bash
php artisan optimize:clear
```
