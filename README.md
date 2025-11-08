# Documentación AdminLTE

## Descripción General

**AdminLTE** es una plantilla de administración basada en Bootstrap que proporciona una interfaz moderna y profesional para aplicaciones web.

### Características Principales

- ✅ Esencialmente una colección de archivos HTML, CSS y JavaScript
- ✅ Puede usarse con HTML plano o integrarse con PHP y otros lenguajes de backend
- ✅ Proporciona componentes preconstruidos para crear paneles de administración
- ✅ Totalmente responsive y compatible con múltiples navegadores

## Estructura de Archivos

Al descargar AdminLTE, encontrarás una estructura de carpetas organizada que facilita su implementación.

AdminLTE/
├── dist/ # Archivos compilados (listos para usar)
│ ├── css/
│ ├── js/
│ └── img/
├── plugins/ # Plugins de jQuery y otros que AdminLTE utiliza
├── examples/ # Ejemplos de cómo usar las páginas
├── pages/ # Ejemplos de páginas
└── index.html # Página de inicio de demostración 

> **Nota importante:** La carpeta `dist/` contiene los archivos ya compilados y listos para usar en producción.

## Uso con HTML Plano

Para prototipos rápidos o proyectos estáticos, AdminLTE puede usarse directamente con HTML plano.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>AdminLTE 3 | Dashboard</title>
    
    <!-- Google Font: Source Sans Pro -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:300,400,400i,700&display=fallback">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="plugins/fontawesome-free/css/all.min.css">
    <!-- Theme style -->
    <link rel="stylesheet" href="dist/css/adminlte.min.css">
</head>
<body class="hold-transition sidebar-mini">
    <div class="wrapper">
        <!-- Aquí va la estructura de la plantilla: Navbar, Sidebar, Content, etc. -->
    </div>
    
    <!-- jQuery -->
    <script src="plugins/jquery/jquery.min.js"></script>
    <!-- Bootstrap 4 -->
    <script src="plugins/bootstrap/js/bootstrap.bundle.min.js"></script>
    <!-- AdminLTE App -->
    <script src="dist/js/adminlte.min.js"></script>
</body>
</html>
```html
> Nota importante: La estructura básica requiere el contenedor `wrapper` que organiza toda la interfaz.

Uso con PHP
Para proyectos dinámicos con lógica de servidor, AdminLTE se integra perfectamente con PHP.

