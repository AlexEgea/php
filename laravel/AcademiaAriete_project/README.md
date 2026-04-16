# 🎓 Academia Ariete

Aplicación web desarrollada con **Laravel** para la gestión de una academia.
Permite administrar usuarios, matrículas, noticias, contacto y candidaturas de forma centralizada.

---

## 🚀 Tecnologías utilizadas

* **Backend:** Laravel (PHP)
* **Frontend:** Blade + Tailwind CSS
* **Base de datos:** MySQL / SQLite
* **Build:** Vite
* **Otros:**

  * JWT (autenticación)
  * Sistema de envío de emails

---

## 📌 Funcionalidades principales

* 👤 Gestión de usuarios (admin / usuarios)
* 📝 Sistema de matrículas
* 📩 Formulario de contacto
* 📰 Gestión de noticias
* 📂 Subida de archivos (candidaturas, perfiles, etc.)
* 🔐 Autenticación con JWT
* 📊 Panel de administración

---

## ⚙️ Requisitos

Antes de instalar el proyecto necesitas tener:

* PHP >= 8.x
* Composer
* Node.js + npm
* Base de datos (MySQL o SQLite)

---

## 🛠️ Instalación paso a paso

### 1. Clonar el repositorio

```bash
git clone https://github.com/TU-USUARIO/academiaariete.git
cd academiaariete
```

---

### 2. Instalar dependencias

```bash
composer install
npm install
```

---

### 3. Configurar variables de entorno

Copia el archivo de ejemplo:

```bash
cp .env.example .env
```

⚠️ **IMPORTANTE:** Aquí debes configurar:

```env
APP_NAME=AcademiaAriete
APP_URL=http://localhost

# Base de datos
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_bd
DB_USERNAME=usuario
DB_PASSWORD=contraseña

# Email (opcional pero recomendado)
MAIL_MAILER=smtp
MAIL_HOST=tu_smtp
MAIL_PORT=587
MAIL_USERNAME=tu_email
MAIL_PASSWORD=tu_password
MAIL_ENCRYPTION=tls

# JWT (si aplica)
JWT_SECRET=
```

---

### 4. Generar clave de aplicación

```bash
php artisan key:generate
```

---

### 5. Generar JWT (si el proyecto lo usa)

```bash
php artisan jwt:secret
```

---

### 6. Configurar base de datos

Ejecuta las migraciones:

```bash
php artisan migrate
```

Opcional (si hay seeders):

```bash
php artisan db:seed
```

---

### 7. Compilar assets

```bash
npm run dev
```

O para producción:

```bash
npm run build
```

---

### 8. Ejecutar el servidor

```bash
php artisan serve
```

Accede en:
👉 http://127.0.0.1:8000

---

## 📁 Estructura del proyecto

```
app/            → Lógica de negocio
config/         → Configuración
database/       → Migraciones y seeders
public/         → Archivos públicos
resources/      → Vistas (Blade, CSS, JS)
routes/         → Rutas web/api
storage/        → Archivos generados
```

---

## 🔐 Seguridad

* ❌ No subir el archivo `.env`
* ❌ No subir credenciales reales
* ❌ No subir archivos dentro de `storage/`
* ✔️ Usar `.env.example` como plantilla

---

## 📸 Notas importantes

* El proyecto requiere configuración manual de:

  * Base de datos
  * Correo (si se usan formularios)
* Algunas funcionalidades dependen de:

  * Permisos de escritura en `/storage`
  * Enlace simbólico:

```bash
php artisan storage:link
```

---

## 📈 Posibles mejoras

* Sistema de roles más avanzado
* API REST completa
* Tests automatizados
* Panel con métricas

---

## 👨‍💻 Autor

**Alejandro Aguilera**

* GitHub: https://github.com/AlexEgea
* Portfolio: https://alejandroaguilera.alwaysdata.net/

---

## 📄 Licencia

Este proyecto está desarrollado con fines educativos y de portfolio.

