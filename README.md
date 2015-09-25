## vue-starter Backend API (Laravel-based)

This application will serve as the companion app to another project called vue-starter. It is meant to be a small demo of a Laravel API, using Dingo and JWT for authentication.

[vue-starter Frontend App](https://github.com/layer7be/vue-starter)

## Installation

### Step 1: Clone the repo

### Step 2: Prerequisites
```
composer install
touch database/database.sqlite
php artisan migrate
php artisan db:seed
php artisan key:generate
php artisan vendor:publish --provider="Tymon\JWTAuth\Providers\JWTAuthServiceProvider"
php artisan jwt:generate
```

### Step 3: Serve
```
php artisan serve
```