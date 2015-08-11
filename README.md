# Adldap2 - Laravel

## Installation

First, insert Adldap2-Laravel into your `composer.json` file:

    "adldap2\adldap2-laravel": "1.0.*",

Then run `composer update`.

Once finished, insert the service provider in your `config/app.php` file:

    Adldap\Laravel\AdldapServiceProvider::class,
    
Then insert the facade:

    'Adldap' => Adldap\Laravel\Facades\Adldap::class,
    
Now you're all set!

## Usage

You can perform all methods on Adldap through its facade like so:

    $user = Adldap::users()->find('john doe');
    
    $search = Adldap::search()->where('cn', '=', 'John Doe')->get();