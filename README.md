# Laravel Filament Starter Project

A professional starter setup for Laravel with Filament Admin Panel, Role & Permission Management, Docker Support, and modern development tools.

---

# 🚀 Tech Stack

- PHP 8.3+
- Laravel 12/13
- Filament v3
- MySQL 8
- Redis
- Docker
- Apache
- Spatie Laravel Permission
- Filament Shield

---

# 📦 Installation

## 1. Clone Repository

```bash
git clone <your-repository-url>
cd filament-project
```

---

# 2. Create Laravel Project

```bash
composer create-project laravel/laravel filament-project
```

Go to project directory:

```bash
cd filament-project
```

---

# ⚙️ Environment Setup

Copy `.env` file:

```bash
cp .env.example .env
```

Generate application key:

```bash
php artisan key:generate
```

Update database credentials inside `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=filament_project
DB_USERNAME=root
DB_PASSWORD=
```

---

# 🐳 Docker Setup (Optional)

Build containers:

```bash
docker compose build --no-cache
```

Run containers:

```bash
docker compose up -d
```

Enter container:

```bash
docker exec -it laravel-filament-app bash
```

---

# 🎨 Install Filament

Install Filament package:

```bash
composer require filament/filament
```

Install Filament panel:

```bash
php artisan filament:install --panels
```

This command will:

- Install Filament assets
- Create admin panel
- Configure authentication
- Publish required files

---

# 🗄️ Database Migration

Run migrations:

```bash
php artisan migrate
```

---

# 👤 Create Filament Admin User

Create admin user:

```bash
php artisan make:filament-user
```

It will ask:

```text
Name:
Email:
Password:
```

---

# ▶️ Run Application

Start Laravel server:

```bash
php artisan serve
```

Open browser:

```text
http://127.0.0.1:8000/admin
```

Login using admin credentials.

---

# 📚 Create Your First Filament Resource

Example: User Resource

```bash
php artisan make:filament-resource User
```

This generates:

- Resource class
- Table listing
- Create form
- Edit form
- Pages

---

# 🛍️ Example Product Module

Create Product model with migration:

```bash
php artisan make:model Product -m
```

Migration example:

```php
Schema::create('products', function (Blueprint $table) {
    $table->id();
    $table->string('name');
    $table->decimal('price', 10, 2);
    $table->text('description')->nullable();
    $table->timestamps();
});
```

Run migration:

```bash
php artisan migrate
```

Generate Filament resource:

```bash
php artisan make:filament-resource Product
```

---

# 🔐 Roles & Permissions

## Install Spatie Laravel Permission

```bash
composer require spatie/laravel-permission
```

Publish configuration and migrations:

```bash
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
```

Run migrations:

```bash
php artisan migrate
```

---

# 🛡️ Filament Shield (RBAC)

Install Filament Shield:

```bash
composer require bezhansalleh/filament-shield
```

Install Shield:

```bash
php artisan shield:install
```

Generate permissions:

```bash
php artisan shield:generate
```

---

# 📂 Recommended Project Structure

```text
app/
├── Actions/
├── DTOs/
├── Enums/
├── Filament/
│   ├── Resources/
│   ├── Pages/
│   ├── Widgets/
│
├── Helpers/
├── Repositories/
├── Services/
├── Traits/
```

---

# 🧰 Useful Artisan Commands

## Create Resource

```bash
php artisan make:filament-resource Product
```

## Create Widget

```bash
php artisan make:filament-widget StatsOverview
```

## Create Custom Page

```bash
php artisan make:filament-page Reports
```

## Optimize Application

```bash
php artisan optimize
```

---

# ⚡ Production Optimization

Before deployment:

```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan optimize
```

---

# 📌 Recommended Packages

| Purpose | Package |
|----------|----------|
| Roles & Permissions | Spatie Permission |
| RBAC UI | Filament Shield |
| API Authentication | Laravel Sanctum |
| Activity Logs | Spatie Activitylog |
| Media Upload | Spatie Medialibrary |
| Excel Export | Laravel Excel |
| Queue Monitoring | Laravel Horizon |
| Debugging | Laravel Telescope |

---

# 🔥 Features

- Modern Laravel Architecture
- Admin Dashboard using Filament
- Role & Permission Management
- RBAC Support
- Docker Ready
- Redis Support
- Scalable Structure
- Production Ready

---

# 📖 Official Documentation

- Laravel: https://laravel.com/docs
- Filament: https://filamentphp.com/docs
- Spatie Permission: https://spatie.be/docs/laravel-permission
- Filament Shield: https://filamentphp.com/plugins/bezhan-saleh-shield

---

# 👨‍💻 Author

Rajesh Kumar Gupta

- PHP Developer
- Laravel Developer
- Full Stack Developer

---

# 📄 License

This project is open-sourced software licensed under the MIT license.
