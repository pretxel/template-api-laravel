# Template API Laravel

 ## Requirements
- Composer [![Latest Unstable Version](https://poser.pugx.org/composer/composer/v/unstable)](https://packagist.org/packages/composer/composer)
- Laravel [![Latest Stable Version](https://poser.pugx.org/laravel/framework/v/stable.svg)](https://packagist.org/packages/laravel/framework)
- Vagrant [![Latest Stable Version](https://poser.pugx.org/enkas/vagrant/v/stable)](https://packagist.org/packages/enkas/vagrant)

## Manual Setup
Firstly clone the repository
```base
  git clone {{REPO}}
```

Then run the script below
```bash
  cd template-api-laravel
  composer install
```

Copy the file .env.example to .env, and run
```bash
  php artisan key:generate
```

Once all dependences has been installed, use make command to generate the **Vagrantfile** and **Homestead.yml**

```bash
  php vendor/bin/homestead make
```

Now, create the database with migrations
```bash
  php artisan migrate
```

Next, generate documentation with Swagger
```bash
   php artisan l5-swagger:generate
```
Finally, run the environment vagrant

```bash
  vagrant up
```

Optionally, you can access via ssh to the vagrant with
```bash
  vagrant ssh
```
And shutdown
```bash
  vagrant halt
```
If you want delete all traces and data
```bash
  vagrant destroy --force
```
