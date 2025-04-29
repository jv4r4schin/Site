# AI Product Demo - Laravel Application

A modern web application for demonstrating AI product capabilities, built with Laravel and Supabase.

## Features

- User Authentication with Supabase
- Role-based Access Control
- AI Configuration Management
- File Upload and Processing
- News Management
- Subscription Plans
- Interactive Dashboards
- Modern UI with Tailwind CSS and Alpine.js

## Requirements

- PHP 8.1 or higher
- Composer
- MySQL/PostgreSQL
- Node.js & NPM
- Supabase Account

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd ai-product-demo
```

2. Install PHP dependencies:
```bash
composer install
```

3. Copy the environment file and configure your settings:
```bash
cp .env.example .env
php artisan key:generate
```

4. Configure the following in your `.env` file:
```
APP_NAME="AI Product Demo"
APP_URL=http://localhost:8000

SUPABASE_URL=your-project-url
SUPABASE_KEY=your-anon-key
SUPABASE_SECRET=your-service-role-key
```

5. Set up the database:
```bash
php artisan migrate
```

6. Create an admin user:
```bash
php artisan tinker
User::create(['name' => 'Admin', 'email' => 'admin@example.com', 'password' => Hash::make('password')])->assignRole('admin');
```

7. Start the development server:
```bash
php artisan serve
```

## Security

- All routes are protected with authentication middleware
- Role-based access control using Spatie Permissions
- Supabase authentication integration
- File validation and sanitization
- CSRF protection

## Directory Structure

```
ai-product-demo/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   └── Middleware/
│   ├── Models/
│   └── Services/
├── database/
│   └── migrations/
├── resources/
│   └── views/
└── routes/
    └── web.php
```

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License.
