# SeaTech – Un océano de soluciones tecnológicas

Sitio web corporativo desarrollado con HTML, CSS, JavaScript, PHP y MySQL. Incluye registro de usuarios y un formulario de inventario de equipos informáticos (hardware, software, red, seguridad y mantenimiento), con almacenamiento en base de datos mediante consultas preparadas.

## Funcionalidades

- **Sitio corporativo** con secciones de inicio, sobre nosotros, misión, visión, servicios, sostenibilidad y contacto, y menú adaptable a móviles.
- **Registro de usuarios** con validación del correo electrónico y control de correos duplicados.
- **Inventario de equipos informáticos** organizado en cinco bloques:
  - Información general
  - Especificaciones de hardware
  - Software instalado
  - Conectividad de red
  - Seguridad y mantenimiento
- **Persistencia en MySQL** usando consultas preparadas.

## Tecnologías

| Área | Tecnología |
|------|------------|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | PHP |
| Base de datos | MySQL |
| Entorno local | XAMPP / WAMP |

## Estructura del repositorio

```
SeaTech/
├── proyecto/                  # Código fuente del sitio web
│   ├── index.html
│   ├── register.php           # Registro de usuarios
│   ├── procesar_inventario.php# Procesamiento del inventario de equipos
│   ├── database.sql           # Creación de la base de datos y tablas
│   ├── import.sql             # Datos de ejemplo (opcional)
│   ├── css/styles.css
│   ├── js/script.js
│   └── images/
├── documentacion/             # Documentación del proyecto
└── README.md
```

## Instalación y ejecución local

**Requisitos:** XAMPP (o WAMP) con Apache, PHP y MySQL.

1. Clona el repositorio:
```bash
   git clone https://github.com/TU-USUARIO/SeaTech.git
```
2. Copia el contenido de la carpeta `proyecto/` dentro de `htdocs/SeaTech/` (XAMPP).
3. Inicia **Apache** y **MySQL** desde el panel de XAMPP.
4. Abre **phpMyAdmin** (`http://localhost/phpmyadmin`) e importa el archivo `database.sql`. Esto crea la base de datos `seatech_db` con sus tablas.
5. *(Opcional)* Con `seatech_db` seleccionada, importa `import.sql` para cargar equipos de ejemplo.
6. Abre el sitio en `http://localhost/SeaTech/`.

### Configuración de la conexión

Por defecto el proyecto usa:

- **Servidor:** `localhost`
- **Usuario:** `root`
- **Contraseña:** *(vacía)*
- **Base de datos:** `seatech_db`

Si tu MySQL usa otras credenciales, edítalas al inicio de `register.php` y `procesar_inventario.php`.

## Base de datos

- `usuarios`: nombre, correo, teléfono y fecha de registro.
- `inventario_equipos`: datos generales, hardware, software, red y seguridad de cada equipo, con índices por código, nombre, usuario asignado y estado.

## Documentación

La carpeta [`documentacion/`](./documentacion) contiene los documentos de soporte del proyecto.

## Autor

**Santiago Batista Delgado**
Técnico en Sistemas Teleinformáticos (SENA).
Estudiante de Ingeniería de Sistemas (UNIMINUTO), Tecnología en Análisis y Desarrollo de Software (SENA).

Colombia 2025.
## Nota

Proyecto con fines académicos. Los datos incluidos en `import.sql` son ficticios.
