# Sistema de Gestión de Actividades - Tecnologías de la Información

## 📋 Descripción del Proyecto

Sistema web desarrollado en Django para la gestión eficiente de actividades académicas y profesionales. Esta aplicación permite a los usuarios crear, organizar, completar y eliminar actividades, con un enfoque en la experiencia de usuario y el diseño académico elegante.

El sistema está diseñado específicamente para el área de **Tecnologías de la Información (TI)**, proporcionando una plataforma moderna y profesional para la gestión de tareas y actividades relacionadas con proyectos tecnológicos.

## ✨ Características Principales

- **Autenticación de Usuarios**: Sistema completo de registro e inicio de sesión
- **Gestión de Actividades**: Crear, editar, completar y eliminar actividades
- **Clasificación de Importancia**: Marcar actividades como importantes
- **Seguimiento de Estado**: Distinción entre actividades pendientes y completadas
- **Interfaz Moderna**: Diseño académico elegante con colores suaves y layouts limpios
- **Responsive Design**: Adaptable a diferentes tamaños de pantalla
- **Seguridad**: Autenticación requerida para acceder a las funcionalidades principales

## 🛠️ Tecnologías Utilizadas

- **Backend**: Django 5.1.1
- **Frontend**: HTML5, CSS3, Bootstrap 5.3.3
- **Base de Datos**: SQLite3
- **Fuentes**: Google Fonts (Inter, Playfair Display)
- **Python**: 3.x

## 📦 Requisitos Previos

Antes de instalar el proyecto, asegúrese de tener instalado:

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Git (opcional, para clonar el repositorio)

## 🚀 Instalación y Configuración

### 1. Clonar o descargar el proyecto

```bash
# Si tiene el proyecto en un repositorio Git
git clone <url-del-repositorio>

# O simplemente navegue a la carpeta del proyecto
cd Nuevo
```

### 2. Crear un entorno virtual (recomendado)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Realizar migraciones

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Crear un superusuario (opcional, para acceder al panel de administración)

```bash
python manage.py createsuperuser
```

### 6. Ejecutar el servidor de desarrollo

```bash
python manage.py runserver
```

El proyecto estará disponible en: `http://127.0.0.1:8000/`

## 📁 Estructura del Proyecto

```
Nuevo/
│
├── mi_grupo_personal/          # Configuración principal del proyecto Django
│   ├── __init__.py
│   ├── settings.py             # Configuración del proyecto
│   ├── urls.py                 # URLs principales
│   ├── wsgi.py
│   └── asgi.py
│
├── ti/                         # Aplicación principal (Tecnologías de la Información)
│   ├── __init__.py
│   ├── admin.py                # Configuración del panel de administración
│   ├── apps.py                 # Configuración de la aplicación
│   ├── forms.py                # Formularios de la aplicación
│   ├── models.py               # Modelos de datos
│   ├── views.py                # Vistas de la aplicación
│   ├── tests.py                # Pruebas unitarias
│   │
│   └── templates/              # Plantillas HTML
│       ├── base.html           # Plantilla base
│       ├── inicio.html         # Página de inicio
│       ├── iniciar_sesion.html # Formulario de login
│       ├── registro.html       # Formulario de registro
│       ├── actividades.html   # Lista de actividades
│       ├── crear_actividad.html # Crear nueva actividad
│       └── detalle_actividad.html # Detalle y edición de actividad
│
├── db.sqlite3                  # Base de datos SQLite
├── manage.py                   # Script de administración de Django
├── requirements.txt            # Dependencias del proyecto
└── README.md                   # Este archivo
```

## 🎯 Funcionalidades Detalladas

### Autenticación
- **Registro de Usuarios**: Los usuarios pueden crear una cuenta con nombre de usuario y contraseña
- **Inicio de Sesión**: Acceso seguro al sistema con autenticación
- **Cerrar Sesión**: Función para cerrar la sesión actual

### Gestión de Actividades
- **Crear Actividad**: Formulario para crear nuevas actividades con título, descripción y marca de importancia
- **Listar Actividades**: Visualización de actividades pendientes y completadas
- **Detalle de Actividad**: Vista detallada con opciones de edición
- **Editar Actividad**: Modificar título, descripción y estado de importancia
- **Completar Actividad**: Marcar actividades como completadas con fecha y hora
- **Eliminar Actividad**: Eliminación permanente de actividades

### Características Adicionales
- **Actividades Importantes**: Sistema de marcado para priorizar actividades
- **Filtrado**: Separación entre actividades pendientes y completadas
- **Información de Usuario**: Cada actividad está asociada a su creador
- **Fechas y Horas**: Registro automático de creación y finalización

## 🎨 Diseño y Estilo

El proyecto utiliza un diseño académico y elegante con las siguientes características:

- **Paleta de Colores**: Tonos azules y grises suaves (primario: #2c5f7c, secundario: #4a90a4)
- **Tipografía**: Fuentes modernas (Inter para texto general, Playfair Display para títulos)
- **Layout Limpio**: Diseño minimalista con espaciado adecuado
- **Responsive**: Adaptable a dispositivos móviles, tablets y escritorio
- **Efectos Visuales**: Transiciones suaves y sombras sutiles

## 🔐 Seguridad

- Autenticación requerida para operaciones sensibles
- Protección CSRF en todos los formularios
- Validación de datos en el servidor
- Asociación de actividades con usuarios (cada usuario solo ve sus propias actividades)

## 📝 Modelo de Datos

### Task (Actividad)
- `title`: Título de la actividad (CharField, max_length=100)
- `description`: Descripción detallada (TextField, opcional)
- `created`: Fecha y hora de creación (DateTimeField, automático)
- `datecompleted`: Fecha y hora de finalización (DateTimeField, opcional)
- `important`: Marca de importancia (BooleanField, default=False)
- `user`: Usuario propietario (ForeignKey a User)

## 🧪 Pruebas

Para ejecutar las pruebas del proyecto:

```bash
python manage.py test
```

## 👨‍💼 Panel de Administración

Acceda al panel de administración de Django en:
```
http://127.0.0.1:8000/admin/
```

Utilice las credenciales del superusuario creado anteriormente.

## 📄 Licencia

Este proyecto es de uso académico y educativo.

## 👤 Autor

Desarrollado para el área de Tecnologías de la Información.

## 📞 Soporte

Para consultas o problemas, por favor contacte al administrador del sistema.

---

**Versión**: 1.0.0  
**Última actualización**: 2024





