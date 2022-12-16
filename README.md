## Laravel Upsert Error

According to this [Laravel Doc](https://laravel.com/docs/9.x/eloquent#upserts), Laravel can use `upsert` method to insert or update records. But when I use it, I got an error.

## How to reproduce the error

clone this repo and do the following steps:
```bash
git clone git@github.com:askdkc/laravel-upsert-error.git
cd laravel-upsert-error
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

Then access to [http://127.0.0.1:8000](http://127.0.0.1:8000)

It will show "SQLSTATE[HY000]: General error: 1 ON CONFLICT clause does not match any PRIMARY KEY or UNIQUE constraint" Error.

Also access to [http://127.0.0.1:8000//updateorcreate](http://127.0.0.1:8000/updateorcreate) This will work fine.
