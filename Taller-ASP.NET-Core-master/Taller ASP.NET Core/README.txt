**Taller 2 del 25/11/2025**  

### **Tecnologías utilizadas:**
- ASP.NET Core 8.0 (framework web)
- Entity Framework Core (ORM para base de datos)
- SQLite (base de datos ligera)
- ASP.NET Identity (autenticación y autorización)
- Bootstrap 5 (diseño responsive)
- jQuery (interactividad frontend)
- Sortable.js (drag & drop)

### **Funcionalidades:**

**Gestión de tareas**
- CRUD completo (crear, leer, actualizar, eliminar)
- Cada usuario solo ve sus propias tareas
- Validaciones del lado del servidor y cliente

**Búsqueda y filtros**
- Buscador por título o descripción
- Filtros: todas las tareas, pendientes, completadas
- Contador de tareas mostradas

**Características adicionales**
- Drag & drop para reordenar tareas
- Subida de imágenes adjuntas a las tareas
- Modal para ver detalles de cada tarea
- Bloqueo de edición para tareas completadas
- Checkbox para marcar como completado/pendiente

**Autenticación**
- Sistema de registro de usuarios
- Inicio de sesión
- Protección de rutas (solo usuarios autenticados)
- Cada usuario tiene sus propias tareas aisladas

**Interfaz personalizada**
- Diseño con colores rojos y verdes
- Botones y textos personalizados
- Vista responsive para diferentes dispositivos
- Animaciones y transiciones suaves

### **Arquitectura del proyecto:**

**Patrón MVC**
- Models: TaskItem, ErrorViewModel
- Views: Home, Tasks (Index, Create, Edit), partials
- Controllers: HomeController, TasksController

**Base de datos**
- Tabla TaskItems (id, Title, Description, IsCompleted, Order, Image, ImageContentType, CreatedAt, UserId)
- Relación con AspNetUsers (Identity)
- Migrations para control de versiones del esquema

**Seguridad implementada**
- Solo el dueño puede ver/editar/eliminar sus tareas
- Validación de tokens anti-falsificación (CSRF)
- Logging de intentos no autorizados
- Manejo de errores con try-catch