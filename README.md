# cache-killer-laravel

How to clear Laravel Cache automatically while your .env file is APP_ENV=local

Copy CacheKiller.php to \app\Http\Middleware\CacheKiller.php

Include CacheKiller into Kernel class to run during every request to your application.

``` php
<?php namespace App\Http;

use Illuminate\Foundation\Http\Kernel as HttpKernel;


class Kernel extends HttpKernel
{

    protected $middleware = [
        
        // ...   
        
        \App\Http\Middleware\CacheKiller::class,
    ];

```
