## vue-starter Backend API (Laravel-based)

This application will serve as the companion app to another project called vue-starter. It is meant to be a small demo of a Laravel API, using Dingo and JWT for authentication.

[vue-starter Frontend App](https://github.com/layer7be/vue-starter)

## Installation

### Step 1: Clone the repo
### Step 2: Prerequisites
```
composer install
touch database/database.sqlite
cp .env.example .env
php artisan key:generate
php artisan jwt:generate
php artisan migrate
```
Next up, create some sample data using Tinker. Note: you enter what is after the >>> marks
```
php artisan tinker
>>> factory('App\Dog',10)->create();
>>> $user = new App\User;
=> App\User {#835}
>>> $user->name = 'Yourname';
=> "Yourname"
>>> $user->email = 'you@example.com';
=> "test@test.com"
>>> $user->password = bcrypt('yourpassword');
=> "$2y$10$8MVVBRjHnNYNUsrc5Ee5cOWpiwcAD09wBWioV6J/8/3MmpN0R8So6"
>>> $user->save()
=> true
>>> exit
Exit:  Goodbye.
```

### Step 3: Serve
```
php artisan serve
```