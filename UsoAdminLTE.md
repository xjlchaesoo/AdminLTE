# Documentación AdminLTE

## Descripción General

**AdminLTE** es una plantilla de administración basada en Bootstrap que proporciona una interfaz moderna y profesional para aplicaciones web.

### Características Principales

-  Esencialmente una colección de archivos HTML, CSS y JavaScript
-  Puede usarse con HTML plano o integrarse con PHP y otros lenguajes de backend
-  Proporciona componentes preconstruidos para crear paneles de administración
-  Totalmente responsive y compatible con múltiples navegadores

### Estructura de Archivos

Al descargar AdminLTE, encontrarás una estructura de carpetas organizada que facilita su implementación.
```html
AdminLTE/
├── dist/ # Archivos compilados (listos para usar)
│ ├── css/
│ ├── js/
│ └── img/
├── plugins/ # Plugins de jQuery y otros que AdminLTE utiliza
├── examples/ # Ejemplos de cómo usar las páginas
├── pages/ # Ejemplos de páginas
└── index.html # Página de inicio de demostración 
```
> **Nota importante:** La carpeta `dist/` contiene los archivos ya compilados y listos para usar en producción.

### Uso con HTML Plano

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
```
> Nota importante: La estructura básica requiere el contenedor `wrapper` que organiza toda la interfaz.

### Usar AdminLTE con PHP:

AdminLTE no es más que un frontend, por lo que puedes integrarlo en un proyecto PHP de la misma manera que con HTML. La diferencia es que ahora puedes usar PHP para generar dinámicamente el contenido.

Por ejemplo, podrías tener un archivo index.php que incluya la estructura base y luego según la lógica de tu aplicación, cargar diferentes vistas o datos.

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

        <!-- Incluir el sidebar -->
        <?php include 'sidebar.php'; ?>

        <!-- Contenido dinámico -->
        <div class="content-wrapper">
            <?php
            // Aquí podrías incluir diferentes vistas según la página
            $page = isset($_GET['page']) ? $_GET['page'] : 'dashboard';
            include $page . '.php';
            ?>
        </div>

    </div>

    <!-- jQuery -->
    <script src="plugins/jquery/jquery.min.js"></script>
    <!-- Bootstrap 4 -->
    <script src="plugins/bootstrap/js/bootstrap.bundle.min.js"></script>
    <!-- AdminLTE App -->
    <script src="dist/js/adminlte.min.js"></script>
</body>
</html>

```
> **Nota importante:** En este ejemplo, estamos incluyendo un archivo sidebar.php y luego cargando dinámicamente el contenido basado en un parámetro page en la URL.

### Personalización

Puedes personalizar los colores, estilos, etc., sobrescribiendo las clases de CSS o utilizando las herramientas de personalización que ofrece AdminLTE (como la personalización de Sass si trabajas con el código fuente).

> **Nota sobre los plugins:** Asegúrate de incluir los plugins necesarios para los componentes que uses (por ejemplo, charts, datatables, etc.). Muchos de estos plugins ya vienen incluidos en la carpeta plugins de AdminLTE.

### Recuerda
AdminLTE es una plantilla de frontend, por lo que puedes usarla con HTML plano o con cualquier backend (PHP, Node.js, Python, etc.). La integración con PHP se hace de la misma manera que con HTML, pero aprovechando la capacidad de PHP para generar contenido dinámicamente.

### ¿HTML o PHP?
AdminLTE funciona con ambos, pero su implementación depende de tu necesidad:

- HTML plano: Para prototipos rápidos o proyectos estáticos
- PHP: Para proyectos dinámicos con lógica de servidor

Formas de usar AdminLTE:
#### 1. Con HTML plano

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>AdminLTE 3 | Dashboard</title>
    
    <!-- Bootstrap 4 -->
    <link rel="stylesheet" href="plugins/bootstrap/css/bootstrap.min.css">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="plugins/fontawesome-free/css/all.min.css">
    <!-- AdminLTE -->
    <link rel="stylesheet" href="dist/css/adminlte.min.css">
</head>
<body class="hold-transition sidebar-mini">
    <div class="wrapper">
        <!-- Navbar -->
        <nav class="main-header navbar navbar-expand navbar-white navbar-light">
            <!-- Contenido del navbar -->
        </nav>

        <!-- Sidebar -->
        <aside class="main-sidebar sidebar-dark-primary elevation-4">
            <!-- Contenido del sidebar -->
        </aside>

        <!-- Content -->
        <div class="content-wrapper">
            <section class="content">
                <div class="container-fluid">
                    <h1>Mi Contenido</h1>
                </div>
            </section>
        </div>
    </div>

    <!-- Scripts -->
    <script src="plugins/jquery/jquery.min.js"></script>
    <script src="plugins/bootstrap/js/bootstrap.bundle.min.js"></script>
    <script src="dist/js/adminlte.min.js"></script>
</body>
</html>

```
#### 2. Con PHP (Recomendado para proyectos reales)

```html
<?php
// index.php
session_start();
// Aquí puedes incluir lógica de autenticación, etc.
?>
<!DOCTYPE html>
<html>
<head>
    <title>Panel Admin - <?php echo $pageTitle; ?></title>
    <?php include 'includes/head.php'; ?>
</head>
<body class="hold-transition sidebar-mini">
    <div class="wrapper">
        <?php 
        include 'includes/navbar.php';
        include 'includes/sidebar.php';
        ?>
        
        <div class="content-wrapper">
            <section class="content">
                <div class="container-fluid">
                    <?php
                    // Contenido dinámico
                    if(isset($_GET['page'])) {
                        include 'pages/' . $_GET['page'] . '.php';
                    } else {
                        include 'pages/dashboard.php';
                    }
                    ?>
                </div>
            </section>
        </div>
    </div>
    
    <?php include 'includes/scripts.php'; ?>
</body>
</html>

```
#### Estructura recomendada para PHP
```html
proyecto/
├── index.php
├── includes/
│   ├── head.php
│   ├── navbar.php
│   ├── sidebar.php
│   └── scripts.php
├── pages/
│   ├── dashboard.php
│   ├── usuarios.php
│   └── configuracion.php
├── dist/           (archivos de AdminLTE)
├── plugins/        (dependencias)
└── assets/         (tus archivos personalizados)

```
### Pasos para comenzar:
1. Descarga AdminLTE desde adminlte.io

### Estructura básica
2. Elaborar uan estructura basica de html, no debe ser muy compleja en este momento porque solo queremos entender como implementar la plantilla.
```html
<div class="wrapper">
  <!-- Navbar -->
  <!-- Sidebar --> 
  <!-- Content Wrapper -->
  <!-- Footer (opcional) -->
</div>
```
### Componentes comunes:
3. Recuerda que existen las siguientes etiquetas que podemos aprovechar a usar para sacarle provecho a la plantilla. 
```html
- Cards: <div class="card">

- Boxes: <div class="box">

- Tables: <table class="table">

- Forms: Formularios con clases de Bootstrap.
```
# Proyecto usando AdminLTE

4. Ahora si vamos a crear un ejemplo real de un dashboard con AdminLTE que incluya:

- Una estructura básica con sidebar y navbar
- Una tarjeta (card) con un gráfico (usando Chart.js)
- Una tabla con datos
- Un formulario modal
- Y algunos elementos de interacción con JavaScript.

Iremos explicando cada parte y por qué se usa.

### Estructura de archivos:

- index.html
- css/custom.css (opcional, para estilos personalizados)
- js/custom.js (para lógica personalizada)
- incluir las dependencias necesarias (Bootstrap, jQuery, AdminLTE, Font Awesome, y Chart.js) a través de CDN.
- 
  > **Nota important:** Puedes llamar a tus archivos que desees.
  
#### index.html
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>MiPanel - Dashboard</title>
    
    <!-- ============================== -->
    <!-- HOJAS DE ESTILO EXTERNAS -->
    <!-- ============================== -->
    <!-- AdminLTE - Framework principal de estilos -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/admin-lte@3.2/dist/css/adminlte.min.css">
    <!-- Font Awesome - Biblioteca de iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts - Fuente tipográfica -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:300,400,400i,700&display=fallback">
    <!-- Nuestros estilos personalizados -->
    <link rel="stylesheet" href="styles.css">
</head>
<body class="hold-transition sidebar-mini layout-fixed">
    <div class="wrapper">

        <!-- ============================== -->
        <!-- BARRA DE NAVEGACIÓN SUPERIOR -->
        <!-- ============================== -->
        <nav class="main-header navbar navbar-expand navbar-white navbar-light">
            <!-- Enlaces izquierda -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <!-- Botón para colapsar/expandir sidebar -->
                    <a class="nav-link" data-widget="pushmenu" href="#" role="button">
                        <i class="fas fa-bars"></i>
                    </a>
                </li>
                <li class="nav-item d-none d-sm-inline-block">
                    <a href="index.html" class="nav-link">Inicio</a>
                </li>
            </ul>

            <!-- Enlaces derecha -->
            <ul class="navbar-nav ml-auto">
                <!-- Menú desplegable de notificaciones -->
                <li class="nav-item dropdown">
                    <a class="nav-link" data-toggle="dropdown" href="#">
                        <i class="far fa-bell"></i>
                        <span class="badge badge-warning navbar-badge">15</span>
                    </a>
                    <div class="dropdown-menu dropdown-menu-lg dropdown-menu-right">
                        <span class="dropdown-item dropdown-header">15 Notificaciones</span>
                        <div class="dropdown-divider"></div>
                        <a href="#" class="dropdown-item">
                            <i class="fas fa-envelope mr-2"></i> 4 nuevos mensajes
                        </a>
                        <!-- Más items de notificación... -->
                    </div>
                </li>
                
                <!-- Botón pantalla completa -->
                <li class="nav-item">
                    <a class="nav-link" data-widget="fullscreen" href="#" role="button">
                        <i class="fas fa-expand-arrows-alt"></i>
                    </a>
                </li>
                
                <!-- Menú de usuario -->
                <li class="nav-item dropdown">
                    <a class="nav-link" data-toggle="dropdown" href="#">
                        <i class="fas fa-user-circle"></i> Admin
                    </a>
                    <div class="dropdown-menu dropdown-menu-right">
                        <a href="#" class="dropdown-item">
                            <i class="fas fa-user mr-2"></i> Mi Perfil
                        </a>
                        <a href="#" class="dropdown-item">
                            <i class="fas fa-cog mr-2"></i> Configuración
                        </a>
                        <div class="dropdown-divider"></div>
                        <a href="#" class="dropdown-item">
                            <i class="fas fa-sign-out-alt mr-2"></i> Cerrar Sesión
                        </a>
                    </div>
                </li>
            </ul>
        </nav>

        <!-- ============================== -->
        <!-- BARRA LATERAL (SIDEBAR) -->
        <!-- ============================== -->
        <aside class="main-sidebar sidebar-light-primary elevation-4">
            <!-- Logo de la marca -->
            <a href="index.html" class="brand-link">
                <img src="https://adminlte.io/themes/v3/dist/img/AdminLTELogo.png" alt="AdminLTE Logo" class="brand-image img-circle elevation-3">
                <span class="brand-text font-weight-light">BackOffice</span>
            </a>

            <!-- Contenido del sidebar -->
            <div class="sidebar">
                <!-- Panel de información del usuario -->
                <div class="user-panel mt-3 pb-3 mb-3 d-flex">
                    <div class="image">
                        <img src="https://adminlte.io/themes/v3/dist/img/user2-160x160.jpg" class="img-circle elevation-2" alt="User Image">
                    </div>
                    <div class="info">
                        <a href="#" class="d-block">Administrador</a>
                    </div>
                </div>

                <!-- Menú de navegación -->
                <nav class="mt-2">
                    <ul class="nav nav-pills nav-sidebar flex-column" data-widget="treeview" role="menu" data-accordion="false">
                        <li class="nav-item">
                            <a href="#" class="nav-link active">
                                <i class="nav-icon fas fa-tachometer-alt"></i>
                                <p>Dashboard</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#" class="nav-link">
                                <i class="nav-icon fas fa-users"></i>
                                <p>Usuarios</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#" class="nav-link">
                                <i class="nav-icon fas fa-shopping-cart"></i>
                                <p>Productos</p>
                            </a>
                        </li>
                        <!-- Más items del menú... -->
                    </ul>
                </nav>
            </div>
        </aside>

        <!-- ============================== -->
        <!-- CONTENIDO PRINCIPAL -->
        <!-- ============================== -->
        <div class="content-wrapper">
            <!-- Encabezado de página -->
            <div class="content-header">
                <div class="container-fluid">
                    <div class="row mb-2">
                        <div class="col-sm-6">
                            <h1 class="m-0">Dashboard</h1>
                        </div>
                        <div class="col-sm-6">
                            <!-- Migas de pan (breadcrumb) -->
                            <ol class="breadcrumb float-sm-right">
                                <li class="breadcrumb-item"><a href="#">Inicio</a></li>
                                <li class="breadcrumb-item active">Dashboard</li>
                            </ol>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Contenido principal -->
            <section class="content">
                <div class="container-fluid">
                    <!-- ============================== -->
                    <!-- TARJETAS DE ESTADÍSTICAS -->
                    <!-- ============================== -->
                    <div class="row">
                        <!-- Tarjeta de pedidos -->
                        <div class="col-lg-3 col-6">
                            <div class="small-box bg-info">
                                <div class="inner">
                                    <h3 class="card-counter">150</h3>
                                    <p>Nuevos Pedidos</p>
                                </div>
                                <div class="icon">
                                    <i class="fas fa-shopping-cart"></i>
                                </div>
                                <a href="#" class="small-box-footer">
                                    Más info <i class="fas fa-arrow-circle-right"></i>
                                </a>
                            </div>
                        </div>
                        
                        <!-- Tarjeta de ratio de conversión -->
                        <div class="col-lg-3 col-6">
                            <div class="small-box bg-success">
                                <div class="inner">
                                    <h3 class="card-counter">53<sup style="font-size: 20px">%</sup></h3>
                                    <p>Ratio de Conversión</p>
                                </div>
                                <div class="icon">
                                    <i class="fas fa-chart-line"></i>
                                </div>
                                <a href="#" class="small-box-footer">
                                    Más info <i class="fas fa-arrow-circle-right"></i>
                                </a>
                            </div>
                        </div>
                        <!-- Más tarjetas de estadísticas... -->
                    </div>

                    <!-- ============================== -->
                    <!-- CONTENIDO PRINCIPAL - FILA -->
                    <!-- ============================== -->
                    <div class="row">
                        <!-- Columna izquierda (70%) -->
                        <section class="col-lg-7 connectedSortable">
                            <!-- Gráfico de ventas -->
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">
                                        <i class="fas fa-chart-line mr-1"></i>
                                        Ventas Mensuales
                                    </h3>
                                    <div class="card-tools">
                                        <button type="button" class="btn btn-tool" data-card-widget="collapse">
                                            <i class="fas fa-minus"></i>
                                        </button>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <div class="chart-container">
                                        <!-- Canvas para el gráfico -->
                                        <canvas id="salesChart" height="250"></canvas>
                                    </div>
                                </div>
                            </div>

                            <!-- Lista de usuarios recientes -->
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Usuarios Recientes</h3>
                                    <div class="card-tools">
                                        <span class="badge badge-danger">8 Nuevos Usuarios</span>
                                        <button type="button" class="btn btn-tool" data-card-widget="collapse">
                                            <i class="fas fa-minus"></i>
                                        </button>
                                    </div>
                                </div>
                                <div class="card-body p-0">
                                    <ul class="users-list clearfix" id="usersList">
                                        <!-- Los usuarios se cargan dinámicamente con JavaScript -->
                                    </ul>
                                </div>
                                <div class="card-footer text-center">
                                    <a href="javascript:void(0)">Ver Todos los Usuarios</a>
                                </div>
                            </div>
                        </section>

                        <!-- Columna derecha (30%) -->
                        <section class="col-lg-5 connectedSortable">
                            <!-- Calendario -->
                            <div class="card bg-gradient-success">
                                <div class="card-header border-0">
                                    <h3 class="card-title">
                                        <i class="far fa-calendar-alt"></i>
                                        Calendario
                                    </h3>
                                    <div class="card-tools">
                                        <button type="button" class="btn btn-success btn-sm" data-card-widget="collapse">
                                            <i class="fas fa-minus"></i>
                                        </button>
                                    </div>
                                </div>
                                <div class="card-body pt-0">
                                    <div id="calendar" style="width: 100%"></div>
                                </div>
                            </div>

                            <!-- Lista de tareas -->
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Lista de Tareas</h3>
                                    <div class="card-tools">
                                        <button type="button" class="btn btn-tool" data-card-widget="collapse">
                                            <i class="fas fa-minus"></i>
                                        </button>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <ul class="todo-list" data-widget="todo-list" id="todoList">
                                        <!-- Las tareas se cargan dinámicamente con JavaScript -->
                                    </ul>
                                </div>
                                <div class="card-footer clearfix">
                                    <button type="button" class="btn btn-info float-right" id="addTaskBtn">
                                        <i class="fas fa-plus"></i> Añadir tarea
                                    </button>
                                </div>
                            </div>
                        </section>
                    </div>
                </div>
            </section>
        </div>

        <!-- ============================== -->
        <!-- PIE DE PÁGINA -->
        <!-- ============================== -->
        <footer class="main-footer">
            <strong>Copyright &copy; 2023 <a href="https://adminlte.io">MiPanel</a>.</strong>
            Todos los derechos reservados.
            <div class="float-right d-none d-sm-inline-block">
                <b>Versión</b> 1.0.0
            </div>
        </footer>
    </div>

    <!-- ============================== -->
    <!-- SCRIPTS EXTERNOS -->
    <!-- ============================== -->
    <!-- jQuery - Biblioteca principal para manipulación DOM -->
    <script src="https://cdn.jsdelivr.net/npm/jquery@3.6.0/dist/jquery.min.js"></script>
    <!-- Bootstrap 4 - Framework CSS/JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/js/bootstrap.bundle.min.js"></script>
    <!-- AdminLTE - Funcionalidades del template -->
    <script src="https://cdn.jsdelivr.net/npm/admin-lte@3.2/dist/js/adminlte.min.js"></script>
    <!-- Chart.js - Biblioteca de gráficos -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Nuestro archivo JavaScript personalizado -->
    <script src="script.js"></script>
</body>
</html>

```
## Explicación de lo que se uso y por qué:
**1. Estructura HTML de AdminLTE**
   
- **Wrapper principal:** <div class="wrapper"> - Contenedor principal que organiza toda la estructura
- **Navbar:** Barra de navegación superior con menús y notificaciones
- **Sidebar:** Menú lateral con opciones de navegación
- **Content Wrapper:** Área principal donde va el contenido

**2. Componentes utilizados**
   
- **Cards:** Para organizar el contenido en secciones visualmente atractivas
- **Small boxes:** Para mostrar estadísticas clave con iconos y colores
- **Charts:** Usé Chart.js para crear gráficos de datos
- **Todo list:** Lista de tareas interactiva
- **User list:** Lista de usuarios con imágenes

**3. CSS personalizado**
   
- **.card-counter:** Para estilizar los números en las estadísticas
- **.user-img:** Para hacer las imágenes de usuario circulares
- **.chart-container:** Para controlar la altura del gráfico

**4. JavaScript para interactividad**
   
- **Chart.js:** Para crear el gráfico de ventas mensuales
- **Contadores animados:** Para que los números en las estadísticas se animen al cargar
- **Gestión de tareas:** Para añadir y eliminar tareas dinámicamente

**5. Librerías y dependencias**
   
- **AdminLTE:** Proporciona la estructura base y componentes
- **Bootstrap 5:** Sistema de grid y componentes base
- **Font Awesome:** Iconos
- **jQuery:** Requerido por AdminLTE para funcionalidades
- **Chart.js:** Para gráficos

## ¿Por qué esta estructura?

- **Responsive:** Se adapta a diferentes tamaños de pantalla
- **Modular:** Cada componente es independiente y reutilizable
- **Profesional:** Tiene una apariencia limpia y moderna
- **Funcional:** Incluye elementos interactivos útiles

Este ejemplo muestra cómo AdminLTE permite crear un panel de administración completo y profesional con relativamente poco código, aprovechando todos sus componentes preconstruidos.
  

