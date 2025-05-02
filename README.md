# Laravel-Curso-Recursos

## Comandos Laravel Comunes

### Instalación y Configuración
```bash
# Crear nuevo proyecto Laravel
composer create-project laravel/laravel nombre-proyecto

# Iniciar servidor de desarrollo
php artisan serve

# Generar key de aplicación
php artisan key:generate
```

### Migraciones y Base de Datos
```bash
# Crear nueva migración
php artisan make:migration create_nombre_tabla_table

# Ejecutar migraciones
php artisan migrate

# Revertir última migración
php artisan migrate:rollback

# Refrescar migraciones (rollback + migrate)
php artisan migrate:refresh
```

### Modelos y Controllers
```bash
# Crear modelo
php artisan make:model NombreModelo

# Crear modelo con migración
php artisan make:model NombreModelo -m

# Crear controller
php artisan make:controller NombreController

# Crear controller con recursos
php artisan make:controller NombreController --resource
```

### Cache y Configuración
```bash
# Limpiar cache
php artisan cache:clear

# Limpiar configuración
php artisan config:clear

# Limpiar rutas
php artisan route:clear

# Limpiar vistas
php artisan view:clear
```

### Autenticación y Login
```bash
# Instalar laravel/breeze (UI de autenticación minimalista)
composer require laravel/breeze --dev

# Instalar laravel/ui (Alternativa con Bootstrap)
composer require laravel/ui

# Instalar autenticación con Bootstrap
php artisan ui bootstrap --auth

# O instalar Breeze con sus vistas
php artisan breeze:install
php artisan migrate

# Instalar dependencias frontend y compilar
npm install
npm run dev

# Si prefieres Laravel Jetstream (UI más completa)
composer require laravel/jetstream

# Instalar Jetstream con Livewire
php artisan jetstream:install livewire

# O Jetstream con Inertia
php artisan jetstream:install inertia

# Después de instalar Jetstream, ejecutar
php artisan migrate
npm install
npm run build
```

### Otros Comandos Útiles
```bash
# Listar todas las rutas
php artisan route:list

# Crear seeder
php artisan make:seeder NombreSeeder

# Ejecutar seeders
php artisan db:seed

# Crear middleware
php artisan make:middleware NombreMiddleware
```
