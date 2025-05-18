# Recursos Laravel

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

# Revertir migraciones hasta un batch específico
php artisan migrate:rollback --batch=3

# Refrescar migraciones (rollback + migrate)
php artisan migrate:refresh

# Eliminar todas las tablas de la base de datos
php artisan migrate:reset

# Eliminar todas las tablas y ejecutar todas las migraciones y seeders
php artisan migrate:fresh --seed
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

# Crear enlace simbólico del storage
php artisan storage:link    # Crea un enlace simbólico de public/storage a storage/app/public para archivos públicos
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

# Ejecutar un seeder específico
php artisan db:seed --class=NombreSeeder
```

### Comandos de Factories
```bash
# Crear una nueva factory
php artisan make:factory NombreFactory

# Crear factory para un modelo existente
php artisan make:factory NombreFactory --model=NombreModelo

# Crear factory con estado personalizado
php artisan make:factory NombreFactory --state
```
