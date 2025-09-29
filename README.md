# Laboratorio: Implementación del Login en Laravel  

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

---

## 1. Descripción del Proyecto  
Este repositorio contiene la implementación del módulo de **autenticación (login/registro)** en **Laravel**, aplicando la arquitectura **MVC (Modelo – Vista – Controlador)**.  
El proyecto incluye la configuración de entornos locales, migraciones de base de datos y la integración de paquetes de autenticación (Laravel UI o Breeze).  

---

## 2. Requisitos Previos  
![PHP](https://img.shields.io/badge/PHP-8.0-blue?logo=php) ![Composer](https://img.shields.io/badge/Composer-latest-orange?logo=composer) ![Laravel](https://img.shields.io/badge/Laravel-10.x-red?logo=laravel) ![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?logo=mysql) ![Node.js](https://img.shields.io/badge/Node.js-18-green?logo=nodedotjs) ![VS Code](https://img.shields.io/badge/Editor-VS%20Code-blue?logo=visualstudiocode)  

- PHP ≥ 8.0  
- Composer (última versión estable)  
- Node.js y npm  
- Servidor local (XAMPP / WampServer / Laragon) con Apache/Nginx y MySQL/MariaDB  
- Editor de código (Visual Studio Code recomendado)  
- Git  

---

## 3. Instalación y Configuración  

1. Clonar repositorio:  
```bash
git clone https://github.com/TUUSUARIO/TUREPO.git
cd TUREPO
```

2. Instalar dependencias:  
```bash
composer install
npm install
```

3. Configurar el archivo `.env`:  
```bash
cp .env.example .env
php artisan key:generate
```
Configurar la base de datos:  
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lab_login
DB_USERNAME=root
DB_PASSWORD=tu_password
```

4. Ejecutar migraciones:  
```bash
php artisan migrate
```

5. Compilar assets:  
```bash
npm run dev
```

6. Levantar servidor local:  
```bash
php artisan serve
```
Abrir en el navegador: `http://127.0.0.1:8000`

---

## 4. Autenticación en Laravel  
Existen dos opciones principales para implementar el sistema de login:  

- **Laravel Breeze** (recomendado, moderno con Tailwind CSS):  
```bash
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate
```

- **Laravel UI** (clásico con Bootstrap):  
```bash
composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev
php artisan migrate
```

---

## 5. Base de Datos y Respaldos  

- Motor: MySQL  
- Nombre de la BD: `lablaravellogin7`  

Respaldo de la base de datos:  
```bash
mysqldump -u root -p lablaravellogin7 > backup.sql
```

El archivo generado se guarda en `/database/backups/`.  

---

## 6. Estructura del Proyecto  
```bash
/app
/bootstrap
/config
/database
  /backups
/public
/resources
  /views
  /screenshots
/routes
README.md
```

---

## 7. Evidencias  
Capturas ubicadas en la carpeta `/resources/screenshots`:  
- Login  
- Registro  
- Dashboard  

---

## 8. Dificultades y Soluciones  

- **Problema:** Versiones incompatibles de PHP y Laravel.  
  - **Solución:** Actualizar PHP a la versión 8.2 en XAMPP.  

- **Problema:** Tablas duplicadas en migraciones.  
  - **Solución:** Ejecutar `php artisan migrate:fresh`.  

- **Problema:** Servicios de MySQL detenidos.  
  - **Solución:** Iniciar manualmente MySQL en XAMPP.  

- **Problema:** Pantalla de Laravel sin estilos.  
  - **Solución:** Ejecutar `npm run dev` para compilar assets correctamente.  

- **Problema:** Errores al ejecutar comandos en PowerShell.  
  - **Solución:** Usar CMD en lugar de PowerShell.  

---

## 9. Referencias  
- [Documentación oficial de Laravel](https://laravel.com/docs)  
- [Guía Laravel Breeze](https://laravel.com/docs/8.x/breeze)  
- [Laracasts: Laravel Authentication](https://laracasts.com/series/laravel-8-from-scratch/episodes/10)  
- [MySQLdump — NebulaCloud](https://nebulacloud.es/blog/como-hacer-un-dump-en-mysql-mysqldump/)  

---

<p align="center">
Desarrollado por la estudiante de la Universidad Tecnológica de Panamá: <br>
<strong>Nombre:</strong> Daniella De León — 8-1011-1020 <br>
<strong>Correo:</strong> Daniella.deleon@utp.ac.pa <br>
<strong>Curso:</strong> Ingeniería Web - Unidad I: MVC <br>
<strong>Instructor:</strong> Ing. Irina Fong <br>
<strong>Fecha de ejecución:</strong> 26 de Septiembre de 2025  
</p>

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 2000 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**
- **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
- **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
