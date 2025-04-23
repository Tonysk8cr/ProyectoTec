Sistema de Reparaciones Electrónicas
Este es un sistema web que desarrollé para gestionar el ingreso de clientes, diagnóstico de dispositivos, asignación de precios y actualización de estados. Todo el acceso está protegido por login y uso de sesiones, así que solo pueden ingresar los usuarios autenticados.

Funcionalidades
Inicio de sesión con validación de sesión activa

Ingreso de nuevos clientes y dispositivos

Registro de formularios de reparación

Asignar diagnóstico y precio final a una reparación

Control del estado del dispositivo

Borrado lógico de formularios

Alertas con JavaScript y mensajes en pantalla

Interfaz limpia con Bootstrap

Estructura del proyecto
bash
Copiar
Editar
Proyecto/
│
├── Controlador/         # Controladores del sistema (Index, Usuario, Reparaciones)
├── Modelo/
│   ├── Entidades/       # Clases de datos como Usuario.php, Cliente.php, etc.
│   ├── Metodos/         # Métodos para interactuar con la BD (UsuarioM.php, ClienteM.php...)
│   └── Conexion.php     # Conexión a la base de datos
│
├── Vista/               # HTML/PHP del frontend (Login, formularios, ingreso cliente...)
│   └── Estilos/         # Archivos CSS (Bootstrap)
│
├── JS/                  # Scripts para búsquedas y validaciones
└── index.php            # Enrutador principal
Requisitos
PHP 8 o superior

Servidor local tipo XAMPP

MySQL

Navegador web

Cómo usarlo
Clonar el repositorio:

bash
Copiar
Editar
git clone https://github.com/Tonysk8cr/ProyectoTec.git
Para la base de datos usar el archivo SCRIPT SQL 

Copiar la carpeta en htdocs de XAMPP o donde tengás configurado tu servidor local.

Sobre el inicio de sesión
Para ingresar al sistema hay que iniciar sesión con un usuario registrado en la base de datos. La verificación de sesión se hace al inicio de cada vista protegida. Si alguien intenta acceder sin estar logueado, lo redirige al login con una alerta.

Nota: Las contraseñas se comparan como texto plano por ahora, pero se puede mejorar con password_hash() y password_verify() si se quiere más seguridad.

Comentarios finales
Este proyecto lo hice con estructura MVC desde cero, sin frameworks. La idea es que se pueda escalar fácil para incluir más funciones como roles de usuario, reportes o conexión con APIs.
