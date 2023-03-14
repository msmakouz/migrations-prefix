# This is a test repository

Needed for testing prefixes in migrations.

## Installation

1) Clone this repo:

```bash
git clone https://github.com/msmakouz/migrations-prefix
```

2) Configure database connection (prefix already configured):

```php
// file app/config/database.php
'drivers' => [
    'mysql' => new Config\MySQLDriverConfig(
        connection: new Config\MySQL\TcpConnectionConfig(
            database: '...',
            host: '...',
            port: 3306,
            user: '...',
            password: '...',
        ),
        queryCache: true
    ),
]
```

3) Install dependencies:

```bash
cd migrations-prefix
composer install
```

4) Create and run migration

```bash
cd migrations-prefix
php app.php cycle:migrate
php app.php migrate
```

5) Check db.
