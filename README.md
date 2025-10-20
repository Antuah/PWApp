# Mi PWA - Calendario y Formularios

Aplicación Web Progresiva (PWA) con calendario interactivo y formularios.

## 🚀 Características

- ✅ **PWA completa** - Funciona offline con Service Worker
- 📱 **Responsive** - Se adapta a todos los dispositivos
- 📆 **Calendario** - Integración con FullCalendar
- 📝 **Formularios** - Con Select2 para mejor UX
- 🎨 **Diseño austero** - Interfaz minimalista y profesional

## 📦 Instalación de Iconos

1. Abre el archivo `generate-icons.html` en tu navegador
2. Descarga cada icono generado
3. Guarda los iconos en la carpeta `/icons/`

Los tamaños requeridos son:
- 72x72, 96x96, 128x128, 144x144
- 152x152, 192x192, 384x384, 512x512

## 🌐 Despliegue en GitHub Pages

### Paso 1: Subir el repositorio

```bash
git add .
git commit -m "Add PWA manifest and icons"
git push origin main
```

### Paso 2: Configurar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Click en **Settings** (Configuración)
3. En el menú lateral, click en **Pages**
4. En **Source**, selecciona la rama `main` y carpeta `/ (root)`
5. Click en **Save**

### Paso 3: Actualizar el manifest (IMPORTANTE para GitHub Pages)

Una vez que sepas la URL de GitHub Pages (ej: `https://irvesp-13.github.io/pwaApp/`), actualiza el archivo `manifest.json`:

```json
{
  "start_url": "/pwaApp/index.html",
  "scope": "/pwaApp/"
}
```

**Nota**: Reemplaza `/pwaApp/` con el nombre de tu repositorio.

## 🔧 Configuración del Service Worker para GitHub Pages

Si tu URL es `https://usuario.github.io/nombreRepo/`, el service worker necesita ajustes:

1. Abre `sw.js`
2. Actualiza las rutas en `APP_SHELL_ASSETS`:

```javascript
const APP_SHELL_ASSETS = [
    '/nombreRepo/',
    '/nombreRepo/index.html',
    '/nombreRepo/about.html',
    // etc...
];
```

## 📱 Instalar la PWA

Una vez desplegada en GitHub Pages:

### En Android (Chrome):
1. Abre la app en Chrome
2. Toca el menú (⋮)
3. Selecciona "Instalar app" o "Añadir a pantalla de inicio"

### En iOS (Safari):
1. Abre la app en Safari
2. Toca el botón de compartir (□↑)
3. Selecciona "Añadir a pantalla de inicio"

### En Desktop (Chrome/Edge):
1. Abre la app
2. Mira el icono de instalación (+) en la barra de direcciones
3. Click en "Instalar"

## 📋 Estructura del Proyecto

```
pwaApp/
├── index.html          # Página principal
├── about.html          # Acerca de
├── calendar.html       # Calendario con FullCalendar
├── form.html           # Formulario con Select2
├── style.css           # Estilos austeros
├── register.js         # Registro del Service Worker
├── sw.js               # Service Worker
├── manifest.json       # Manifest de la PWA
├── icons/              # Iconos de la PWA
├── screenshots/        # Screenshots para la PWA
└── generate-icons.html # Generador de iconos
```

## 🎨 Personalización

### Colores (en `style.css` y `manifest.json`):
- Theme color: `#333333`
- Background: `#f5f5f5`
- Text: `#1a1a1a`

### Nombre de la App (en `manifest.json`):
```json
{
  "name": "Tu Nombre Aquí",
  "short_name": "Corto"
}
```

## 📄 Licencia

Proyecto educativo - UTEZ 2025

---

Desarrollado por **Irving Uriel Espinosa Hernandez**  
Universidad Tecnológica Emiliano Zapata (UTEZ)  
10mo Cuatrimestre - Ingeniería en Desarrollo y Gestión de Software
