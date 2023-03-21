# Requirement
- PHP 8.x.x
- composer
- Xampp/Laragon

# Instalasi Bootsrap 5 Pada Laravel 9 

## 1. Create Project Laravel 9
```
composer create-project laravel/laravel:^9.0 name_project
```

## 2. Install Laravel UI Untuk Bootstrap 5:
```
composer require laravel/ui
```

## 3. Membuat Autentikasi Dengan Bootstrap 5
```
php artisan ui bootstrap
```
```
php artisan ui bootstrap --auth
```

## 4. Install NPM Dan NPM Run Build Untuk Menjalankan Bootstrap 5
```
npm install
```
```
npm run build
```

## 5. Pasang/Tambahkan Source Dibawah Pada halaman yang akan menggunakan Bootstrap 5
### Pada Laravel Biasa
```
@vite(['resources/sass/app.scss', 'resources/js/app.js'])
```
### Pada Project Statamic
```
{{ vite src="resources/js/app.js|resources/sass/app.scss" }}
```

## 6. Jalankan Project 
```
php artisan serve
```

# Setting package.json (Bila terjadi error pada langkah no. 4)

## Membuat Dependensi Baru
```
npm install --save-dev vite laravel-vite-plugin
```

## Buka file package.json. Hapus semua yang ada pada scripts{} Ubah dengan kode dibawah ini:
```
"scripts": {
    "dev": "vite",
    "build": "vite build"
},
```

## Karena Vite adalah pengganti webpack, kita dapat menghapus laravel-mix dan menghapus file webpack.mix.js dari aplikasi sebelumnya:
```
npm remove laravel-mix && rm webpack.mix.js
```

## Tampilan package.json setelah di setting
```
{
    "private": true,
    "scripts": {
        "dev": "vite",
        "build": "vite build"
    },
    "devDependencies": {
        "@popperjs/core": "^2.11.6",
        "axios": "^0.25",
        "bootstrap": "^5.2.3",
        "laravel-vite-plugin": "^0.7.4",
        "lodash": "^4.17.19",
        "postcss": "^8.1.14",
        "sass": "^1.56.1",
        "vite": "^4.2.1"
    }
}
```
