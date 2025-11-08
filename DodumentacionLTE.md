<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Dashboard AdminLTE - Documentación y Ejemplo</title>
    
    <!-- ============================== -->
    <!-- HOJAS DE ESTILO EXTERNAS -->
    <!-- ============================== -->
    <!-- AdminLTE - Framework principal de estilos -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/admin-lte@3.2/dist/css/adminlte.min.css">
    <!-- Font Awesome - Biblioteca de iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts - Fuente tipográfica -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:300,400,400i,700&display=fallback">
    
    <style>
        /* Estilos personalizados para resaltar puntos importantes */
        .highlight-box {
            background-color: #f8f9fa;
            border-left: 4px solid #007bff;
            padding: 15px;
            margin: 15px 0;
            border-radius: 0 4px 4px 0;
        }
        
        .feature-list {
            list-style-type: none;
            padding-left: 0;
        }
        
        .feature-list li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
        }
        
        .feature-list li:before {
            content: "✓ ";
            color: #28a745;
            font-weight: bold;
            margin-right: 10px;
        }
        
        .code-block {
            background-color: #f4f4f4;
            padding: 15px;
            border-radius: 5px;
            overflow-x: auto;
            margin: 15px 0;
            font-family: monospace;
        }
        
        .section-divider {
            border-top: 2px solid #dee2e6;
            margin: 30px 0;
        }
    </style>
</head>
<body class="hold-transition sidebar-mini layout-fixed">
    <div class="wrapper">

        <!-- ============================== -->
        <!-- BARRA DE NAVEGACIÓN SUPERIOR -->
        <!-- ============================== -->
        <nav class="main-header navbar navbar-expand navbar-white navbar-light">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" data-widget="pushmenu" href="#" role="button">
                        <i class="fas fa-bars"></i>
                    </a>
                </li>
                <li class="nav-item d-none d-sm-inline-block">
                    <a href="index.html" class="nav-link">Inicio</a>
                </li>
            </ul>

            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a class="nav-link" href="#documentacion">
                        <i class="fas fa-book"></i> Documentación
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#ejemplo">
                        <i class="fas fa-code"></i> Ejemplo
                    </a>
                </li>
            </ul>
        </nav>

        <!-- ============================== -->
        <!-- BARRA LATERAL (SIDEBAR) -->
        <!-- ============================== -->
        <aside class="main-sidebar sidebar-light-primary elevation-4">
            <a href="index.html" class="brand-link">
                <img src="https://adminlte.io/themes/v3/dist/img/AdminLTELogo.png" alt="AdminLTE Logo" class="brand-image img-circle elevation-3">
                <span class="brand-text font-weight-light">AdminLTE Docs</span>
            </a>

            <div class="sidebar">
                <div class="user-panel mt-3 pb-3 mb-3 d-flex">
                    <div class="image">
                        <img src="https://adminlte.io/themes/v3/dist/img/user2-160x160.jpg" class="img-circle elevation-2" alt="User Image">
                    </div>
                    <div class="info">
                        <a href="#" class="d-block">Administrador</a>
                    </div>
                </div>

                <nav class="mt-2">
                    <ul class="nav nav-pills nav-sidebar flex-column" data-widget="treeview" role="menu" data-accordion="false">
                        <li class="nav-item">
                            <a href="#introduccion" class="nav-link">
                                <i class="nav-icon fas fa-info-circle"></i>
                                <p>Introducción</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#estructura" class="nav-link">
                                <i class="nav-icon fas fa-folder"></i>
                                <p>Estructura</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#html-plano" class="nav-link">
                                <i class="nav-icon fas fa-file-code"></i>
                                <p>HTML Plano</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#php" class="nav-link">
                                <i class="nav-icon fas fa-server"></i>
                                <p>Con PHP</p>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="#ejemplo-completo" class="nav-link">
                                <i class="nav-icon fas fa-desktop"></i>
                                <p>Ejemplo Completo</p>
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </aside>

        <!-- ============================== -->
        <!-- CONTENIDO PRINCIPAL -->
        <!-- ============================== -->
        <div class="content-wrapper">
            <div class="content-header">
                <div class="container-fluid">
                    <div class="row mb-2">
                        <div class="col-sm-6">
                            <h1 class="m-0">Documentación AdminLTE</h1>
                        </div>
                        <div class="col-sm-6">
                            <ol class="breadcrumb float-sm-right">
                                <li class="breadcrumb-item"><a href="#">Inicio</a></li>
                                <li class="breadcrumb-item active">Documentación</li>
                            </ol>
                        </div>
                    </div>
                </div>
            </div>

            <section class="content">
                <div class="container-fluid">
                    <!-- ============================== -->
                    <!-- INTRODUCCIÓN -->
                    <!-- ============================== -->
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <h1 id="introduccion">Introducción a AdminLTE</h1>
                                </div>
                                <div class="card-body">
                                    <div class="highlight-box">
                                        <p><strong>AdminLTE</strong> es una plantilla de administración basada en Bootstrap que proporciona una interfaz moderna y profesional para aplicaciones web.</p>
                                    </div>
                                    
                                    <ul class="feature-list">
                                        <li>Esencialmente una colección de archivos HTML, CSS y JavaScript</li>
                                        <li>Puede usarse con HTML plano o integrarse con PHP y otros lenguajes de backend</li>
                                        <li>Proporciona componentes preconstruidos para crear paneles de administración</li>
                                        <li>Totalmente responsive y compatible con múltiples navegadores</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="section-divider"></div>
                    
                    <!-- ============================== -->
                    <!-- ESTRUCTURA DE ARCHIVOS -->
                    <!-- ============================== -->
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <h1 id="estructura">Estructura de Archivos</h1>
                                </div>
                                <div class="card-body">
                                    <div class="highlight-box">
                                        <p>Al descargar AdminLTE, encontrarás una estructura de carpetas organizada que facilita su implementación.</p>
                                    </div>
                                    
                                    <div class="code-block">
                                        AdminLTE/<br>
                                        ├── dist/          # Archivos compilados (listos para usar)<br>
                                        │   ├── css/<br>
                                        │   ├── js/<br>
                                        │   └── img/<br>
                                        ├── plugins/       # Plugins de jQuery y otros que AdminLTE utiliza<br>
                                        ├── examples/      # Ejemplos de cómo usar las páginas<br>
                                        ├── pages/         # Ejemplos de páginas<br>
                                        └── index.html     # Página de inicio de demostración
                                    </div>
                                    
                                    <div class="highlight-box">
                                        <p><strong>Punto importante:</strong> La carpeta <code>dist/</code> contiene los archivos ya compilados y listos para usar en producción.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="section-divider"></div>
                    
                    <!-- ============================== -->
                    <!-- USO CON HTML PLANO -->
                    <!-- ============================== -->
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <h1 id="html-plano">Uso con HTML Plano</h1>
                                </div>
                                <div class="card-body">
                                    <div class="highlight-box">
                                        <p>Para prototipos rápidos o proyectos estáticos, AdminLTE puede usarse directamente con HTML plano.</p>
                                    </div>
                                    
                                    <div class="code-block">
&lt;!DOCTYPE html&gt;<br>
&lt;html lang="es"&gt;<br>
&lt;head&gt;<br>
    &lt;meta charset="utf-8"&gt;<br>
    &lt;meta name="viewport" content="width=device-width, initial-scale=1"&gt;<br>
    &lt;title&gt;AdminLTE 3 | Dashboard&lt;/title&gt;<br><br>
    &lt;!-- Google Font: Source Sans Pro --&gt;<br>
    &lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:300,400,400i,700&display=fallback"&gt;<br>
    &lt;!-- Font Awesome Icons --&gt;<br>
    &lt;link rel="stylesheet" href="plugins/fontawesome-free/css/all.min.css"&gt;<br>
    &lt;!-- Theme style --&gt;<br>
    &lt;link rel="stylesheet" href="dist/css/adminlte.min.css"&gt;<br>
&lt;/head&gt;<br>
&lt;body class="hold-transition sidebar-mini"&gt;<br>
    &lt;div class="wrapper"&gt;<br><br>
        &lt;!-- Aquí va la estructura de la plantilla: Navbar, Sidebar, Content, etc. --&gt;<br><br>
    &lt;/div&gt;<br><br>
    &lt;!-- jQuery --&gt;<br>
    &lt;script src="plugins/jquery/jquery.min.js"&gt;&lt;/script&gt;<br>
    &lt;!-- Bootstrap 4 --&gt;<br>
    &lt;script src="plugins/bootstrap/js/bootstrap.bundle.min.js"&gt;&lt;/script&gt;<br>
    &lt;!-- AdminLTE App --&gt;<br>
    &lt;script src="dist/js/adminlte.min.js"&gt;&lt;/script&gt;<br>
&lt;/body&gt;<br>
&lt;/html&gt;
                                    </div>
                                    
                                    <div class="highlight-box">
                                        <p><strong>Punto importante:</strong> La estructura básica requiere el contenedor <code>wrapper</code> que organiza toda la interfaz.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="section-divider"></div>
                    
                    <!-- ============================== -->
                    <!-- USO CON PHP -->
                    <!-- ============================== -->
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <h1 id="php">Uso con PHP</h1>
                                </div>
                                <div class="card-body">
                                    <div class="highlight-box">
                                        <p>Para proyectos dinámicos con lógica de servidor, AdminLTE se integra perfectamente con PHP.</p>
                                    </div>
                                    
                                    <div class="code-block">
&lt;?php<br>
// index.php<br>
session_start();<br>
// Aquí puedes incluir lógica de autenticación, etc.<br>
?&gt;<br>
&lt;!DOCTYPE html&gt;<br>
&lt;html&gt;<br>
&lt;head&gt;<br>
    &lt;title&gt;Panel Admin - &lt;?php echo $pageTitle; ?&gt;&lt;/title&gt;<br>
    &lt;?php include 'includes/head.php'; ?&gt;<br>
&lt;/head&gt;<br>
&lt;body class="hold-transition sidebar-mini"&gt;<br>
    &lt;div class="wrapper"&gt;<br>
        &lt;?php <br>
        include 'includes/navbar.php';<br>
        include 'includes/sidebar.php';<br>
        ?&gt;<br><br>
        &lt;div class="content-wrapper"&gt;<br>
            &lt;section class="content"&gt;<br>
                &lt;div class="container-fluid"&gt;<br>
                    &lt;?php<br>
                    // Contenido dinámico<br>
                    if(isset($_GET['page'])) {<br>
                        include 'pages/' . $_GET['page'] . '.php';<br>
                    } else {<br>
                        include 'pages/dashboard.php';<br>
                    }<br>
                    ?&gt;<br>
                &lt;/div&gt;<br>
            &lt;/section&gt;<br>
        &lt;/div&gt;<br>
    &lt;/div&gt;<br><br>
    &lt;?php include 'includes/scripts.php'; ?&gt;<br>
&lt;/body&gt;<br>
&lt;/html&gt;
                                    </div>
                                    
                                    <div class="highlight-box">
                                        <p><strong>Punto importante:</strong> La estructura recomendada para PHP separa los componentes en archivos incluibles para mejor organización.</p>
                                    </div>
                                    
                                    <div class="code-block">
proyecto/<br>
├── index.php<br>
├── includes/<br>
│   ├── head.php<br>
│   ├── navbar.php<br>
│   ├── sidebar.php<br>
│   └── scripts.php<br>
├── pages/<br>
│   ├── dashboard.php<br>
│   ├── usuarios.php<br>
│   └── configuracion.php<br>
├── dist/           (archivos de AdminLTE)<br>
├── plugins/        (dependencias)<br>
└── assets/         (tus archivos personalizados)
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="section-divider"></div>
                    
                    <!-- ============================== -->
                    <!-- EJEMPLO COMPLETO -->
                    <!-- ============================== -->
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <h1 id="ejemplo-completo">Ejemplo Completo de Dashboard</h1>
                                </div>
                                <div class="card-body">
                                    <div class="highlight-box">
                                        <p>Este ejemplo muestra un dashboard completo con AdminLTE que incluye estadísticas, gráficos y componentes interactivos.</p>
                                    </div>
                                    
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
                                        
                                        <!-- Tarjeta de usuarios -->
                                        <div class="col-lg-3 col-6">
                                            <div class="small-box bg-warning">
                                                <div class="inner">
                                                    <h3 class="card-counter">44</h3>
                                                    <p>Usuarios Registrados</p>
                                                </div>
                                                <div class="icon">
                                                    <i class="fas fa-user-plus"></i>
                                                </div>
                                                <a href="#" class="small-box-footer">
                                                    Más info <i class="fas fa-arrow-circle-right"></i>
                                                </a>
                                            </div>
                                        </div>
                                        
                                        <!-- Tarjeta de visitas -->
                                        <div class="col-lg-3 col-6">
                                            <div class="small-box bg-danger">
                                                <div class="inner">
                                                    <h3 class="card-counter">65</h3>
                                                    <p>Visitas Únicas</p>
                                                </div>
                                                <div class="icon">
                                                    <i class="fas fa-chart-pie"></i>
                                                </div>
                                                <a href="#" class="small-box-footer">
                                                    Más info <i class="fas fa-arrow-circle-right"></i>
                                                </a>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <div class="highlight-box">
                                        <p><strong>Punto importante:</strong> Los componentes como <code>small-box</code> son ideales para mostrar estadísticas clave de forma visualmente atractiva.</p>
                                    </div>
                                    
                                    <div class="row mt-4">
                                        <div class="col-md-6">
                                            <div class="card">
                                                <div class="card-header">
                                                    <h3 class="card-title">
                                                        <i class="fas fa-chart-bar mr-1"></i>
                                                        Gráfico de Ventas
                                                    </h3>
                                                </div>
                                                <div class="card-body">
                                                    <canvas id="salesChart" height="200"></canvas>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-md-6">
                                            <div class="card">
                                                <div class="card-header">
                                                    <h3 class="card-title">
                                                        <i class="fas fa-users mr-1"></i>
                                                        Usuarios Recientes
                                                    </h3>
                                                </div>
                                                <div class="card-body">
                                                    <ul class="list-group">
                                                        <li class="list-group-item d-flex justify-content-between align-items-center">
                                                            María García
                                                            <span class="badge badge-primary badge-pill">Nuevo</span>
                                                        </li>
                                                        <li class="list-group-item d-flex justify-content-between align-items-center">
                                                            Juan Pérez
                                                            <span class="badge badge-primary badge-pill">Nuevo</span>
                                                        </li>
                                                        <li class="list-group-item">Ana López</li>
                                                        <li class="list-group-item">Carlos Rodríguez</li>
                                                    </ul>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <div class="highlight-box mt-4">
                                        <p><strong>Explicación de lo que se usó y por qué:</strong></p>
                                        <ul>
                                            <li><strong>Estructura HTML de AdminLTE:</strong> Contenedor principal <code>wrapper</code> que organiza toda la estructura</li>
                                            <li><strong>Componentes utilizados:</strong> Cards, Small boxes, Charts, Lists</li>
                                            <li><strong>Librerías y dependencias:</strong> AdminLTE, Bootstrap 4, Font Awesome, jQuery, Chart.js</li>
                                            <li><strong>¿Por qué esta estructura?</strong> Responsive, modular, profesional y funcional</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- ============================== -->
        <!-- PIE DE PÁGINA -->
        <!-- ============================== -->
        <footer class="main-footer">
            <strong>Copyright &copy; 2023 <a href="https://adminlte.io">AdminLTE Docs</a>.</strong>
            Documentación completa para implementación.
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
    
    <script>
        // Script para inicializar componentes y funcionalidades
        $(document).ready(function() {
            // Inicializar componentes de AdminLTE
            $('[data-widget="pushmenu"]').pushmenu();
            $('[data-widget="treeview"]').treeview();
            
            // Animación de contadores
            $('.card-counter').each(function() {
                $(this).prop('Counter', 0).animate({
                    Counter: $(this).text()
                }, {
                    duration: 2000,
                    easing: 'swing',
                    step: function(now) {
                        $(this).text(Math.ceil(now));
                    }
                });
            });
            
            // Gráfico de ejemplo
            var ctx = document.getElementById('salesChart').getContext('2d');
            var salesChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Ene', 'Feb', 'Mar', 'Abr', 'May', 'Jun'],
                    datasets: [{
                        label: 'Ventas 2023',
                        data: [12, 19, 3, 5, 2, 3],
                        backgroundColor: [
                            'rgba(54, 162, 235, 0.2)',
                            'rgba(54, 162, 235, 0.2)',
                            'rgba(54, 162, 235, 0.2)',
                            'rgba(54, 162, 235, 0.2)',
                            'rgba(54, 162, 235, 0.2)',
                            'rgba(54, 162, 235, 0.2)'
                        ],
                        borderColor: [
                            'rgba(54, 162, 235, 1)',
                            'rgba(54, 162, 235, 1)',
                            'rgba(54, 162, 235, 1)',
                            'rgba(54, 162, 235, 1)',
                            'rgba(54, 162, 235, 1)',
                            'rgba(54, 162, 235, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>