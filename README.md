# 🍽️ Sistema de Ventas para Restaurante - Restobar Illari

Un sistema completo de gestión para restaurantes y bares desarrollado con Vue.js y PHP. Permite administrar ventas, mesas, inventario y generar reportes detallados para optimizar la operación de tu negocio gastronómico.

## 📋 Características Principales

### 🔐 **Gestión de Usuarios**
- Sistema de login seguro con autenticación
- Gestión de perfiles de usuario
- Cambio de contraseñas
- Control de acceso por roles

### 🏠 **Gestión de Mesas**
- Control de mesas en tiempo real
- Estados: libre, ocupada, reservada
- Asignación de meseros por mesa
- Cancelación y edición de órdenes

### 📦 **Inventario y Productos**
- Gestión de categorías (Platillos y Bebidas)
- Catálogo completo de insumos/productos
- Control de precios y descripciones
- Búsqueda avanzada por nombre o código

### 💰 **Sistema de Ventas**
- Procesamiento de órdenes en tiempo real
- Generación automática de tickets
- Cálculo de totales y pagos
- Historial completo de transacciones

### 📊 **Reportes y Analytics**
- Ventas por día, mes y año
- Reportes por mesero/usuario
- Productos más vendidos
- Gráficas interactivas con Chart.js
- Análisis por horarios y días de la semana

### ⚙️ **Configuración**
- Configuración inicial del negocio
- Datos del local (nombre, teléfono, logo)
- Número de mesas personizable
- Parámetros del sistema

## 🛠️ Tecnologías Utilizadas

### Frontend
- **Vue.js 2.5** - Framework JavaScript progresivo
- **Buefy** - Componentes UI basados en Bulma CSS
- **Vue Router** - Navegación SPA
- **Chart.js** - Gráficas y visualización de datos
- **Webpack** - Bundler de módulos
- **Material Design Icons** - Iconografía

### Backend
- **PHP 7.4+** - Lenguaje del servidor
- **MySQL** - Base de datos relacional
- **PDO** - Abstracción de base de datos
- **API REST** - Arquitectura de servicios

### Herramientas de Desarrollo
- **npm** - Gestor de paquetes
- **Babel** - Transpilador ES6+
- **ESLint** - Linter de código
- **Webpack Dev Server** - Servidor de desarrollo

## 📁 Estructura del Proyecto

```
📦 Restaurante-ventas
├── 📁 api/                    # Backend PHP
│   ├── funciones.php          # Funciones de base de datos
│   ├── iniciar_sesion.php     # Autenticación
│   ├── registrar_*.php        # Endpoints de registro
│   ├── obtener_*.php          # Endpoints de consulta
│   └── fotos/                 # Imágenes subidas
├── 📁 src/                    # Frontend Vue.js
│   ├── App.vue                # Componente principal
│   ├── main.js                # Punto de entrada
│   ├── 📁 components/         # Componentes Vue
│   │   ├── 📁 Usuarios/       # Gestión de usuarios
│   │   ├── 📁 Insumos/        # Gestión de productos
│   │   ├── 📁 Categorias/     # Gestión de categorías
│   │   ├── 📁 Ventas/         # Sistema de ventas
│   │   ├── 📁 Ordenar/        # Gestión de órdenes
│   │   └── 📁 Configuracion/  # Configuración del sistema
│   ├── 📁 router/             # Configuración de rutas
│   └── 📁 Servicios/          # Servicios HTTP
├── 📁 build/                  # Configuración de Webpack
├── 📁 config/                 # Configuración de entornos
├── bd_esquema.sql             # Esquema de base de datos
├── package.json               # Dependencias de Node.js
└── index.html                 # Plantilla HTML principal
```

## 🚀 Instalación y Configuración

### Prerrequisitos

- **Node.js 14.x o 16.x** (⚠️ **Importante**: No usar Node.js 18+)
- **PHP 7.4+**
- **MySQL 5.7+** o **MariaDB**
- **Servidor web** (Apache, Nginx, XAMPP, etc.)

### 1. Clonar el Repositorio

```bash
git clone https://github.com/BryanAndresO/Restaurante-ventas.git
cd Restaurante-ventas
```

### 2. Configurar la Base de Datos

```sql
-- Crear base de datos
CREATE DATABASE illari_ventas;

-- Importar esquema
mysql -u root -p illari_ventas < bd_esquema.sql
```

### 3. Configurar el Backend

1. Copiar la carpeta `api` al directorio del servidor web:
```bash
# Para XAMPP
cp -r api/ /xampp/htdocs/illari-ventas/api/
```

2. Verificar configuración de base de datos en `api/funciones.php`:
```php
$host = "localhost";
$db   = "illari_ventas";
$user = "root";           // Tu usuario MySQL
$pass = "";               // Tu contraseña MySQL
```

### 4. Instalar Dependencias Frontend

```bash
# Asegúrate de usar Node.js 14.x o 16.x
npm install
```

### 5. Configurar URL del API

Editar `src/Servicios/HttpService.js`:
```javascript
const RUTA_GLOBAL = "http://localhost/illari-ventas/api/"
```

### 6. Ejecutar en Desarrollo

```bash
npm run dev
```

### 7. Compilar para Producción

```bash
npm run build
```

## 🌐 Acceso al Sistema

- **Frontend**: http://localhost:8080
- **API**: http://localhost/illari-ventas/api/
- **Base de datos**: http://localhost/phpmyadmin

## 🎯 Uso del Sistema

### Configuración Inicial
1. Al acceder por primera vez, configurar datos del negocio
2. Crear usuario administrador
3. Configurar número de mesas
4. Subir logo del establecimiento

### Flujo de Trabajo Típico
1. **Login** → Iniciar sesión con credenciales
2. **Configurar Productos** → Crear categorías e insumos
3. **Gestionar Mesas** → Asignar órdenes a mesas
4. **Procesar Ventas** → Registrar consumos y pagos
5. **Generar Reportes** → Analizar ventas y rendimiento

## 🎨 Capturas de Pantalla

*[Aquí puedes agregar imágenes del sistema en funcionamiento]*

## 🤝 Contribuir

1. Fork del repositorio
2. Crear rama para nueva característica (`git checkout -b feature/AmazingFeature`)
3. Commit de cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**PacoHunterDev** - *Desarrollo inicial*

**BryanAndresO** - *Mantenimiento del repositorio*

## 🐛 Reporte de Problemas

Si encuentras algún bug o tienes sugerencias, por favor:
1. Revisa los [issues existentes](https://github.com/BryanAndresO/Restaurante-ventas/issues)
2. Crea un nuevo issue con descripción detallada
3. Incluye pasos para reproducir el problema

## 📞 Soporte

Para soporte técnico o consultas:
- Crear un issue en el repositorio
- Documentación en la wiki del proyecto

---

⭐ Si este proyecto te resulta útil, ¡no olvides darle una estrella!
