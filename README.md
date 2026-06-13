# Proyectos — Vida con propósito

PWA offline para planificar proyectos vitales y hacer seguimiento de hábitos. Sin publicidad, sin servidor, sin conexión.

## Archivos

```
proyectos/
├── index.html      ← Aplicación completa (todo en uno)
├── manifest.json   ← Configuración PWA
├── sw.js           ← Service Worker (cache offline)
├── icon.svg        ← Icono de la app
└── README.md       ← Esta guía
```

---

## Desplegar en GitHub Pages (10 minutos)

### 1. Crear repositorio en GitHub
- Ve a [github.com/new](https://github.com/new)
- Nombre: `proyectos` (o el que quieras)
- Visibilidad: **Public** ✓ (necesario para GitHub Pages gratis)
- Clic en **Create repository**

### 2. Subir los archivos
Opción A — Desde el navegador (más fácil):
1. En la página del repositorio → **Add file → Upload files**
2. Arrastra los 4 archivos: `index.html`, `manifest.json`, `sw.js`, `icon.svg`
3. Clic en **Commit changes**

Opción B — Con Git:
```bash
git init
git add .
git commit -m "Proyectos PWA"
git remote add origin https://github.com/TU_USUARIO/proyectos.git
git push -u origin main
```

### 3. Activar GitHub Pages
1. En el repositorio → **Settings** (arriba a la derecha)
2. Menú lateral → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / **/ (root)**
5. Clic en **Save**
6. Espera 1-2 minutos y aparecerá la URL: `https://TU_USUARIO.github.io/proyectos/`

---

## Instalar en el móvil como app

### En Android (Chrome)
1. Abre la URL en Chrome
2. Menú (⋮) → **Añadir a pantalla de inicio**
3. Confirma → se instala como app nativa

### En iPhone (Safari)
1. Abre la URL en Safari (importante: no Chrome)
2. Botón compartir (□↑) → **Añadir a pantalla de inicio**
3. Confirma el nombre → instalar

---

## Características

- **Proyectos vitales** por categoría: financiero 💰, fitness 💪, formación 📚, salud 🏥, personal 🎯, hogar 🏠
- **Tareas**: hábitos recurrentes (diario/semanal/mensual) y tareas puntuales
- **Seguimiento**: hoy/todos los hábitos/pendientes con rachas y dots de 7 días
- **Estadísticas**: racha global 🔥, heatmap de actividad, progreso por proyecto
- **Export/Import** JSON completo para hacer backup o mover entre dispositivos
- **100% offline** después de la primera carga
- **Sin cuenta, sin servidor, sin publicidad**

---

## Exportar / importar datos

- En la app: pestaña **···** (estadísticas) → ⚙️ Ajustes → **Exportar datos**
- Guarda el archivo `.json`
- Para restaurar: **Importar datos** → selecciona el archivo

---

## Actualizar la app

Si modificas los archivos y los vuelves a subir a GitHub, la app se actualiza sola en el siguiente acceso con conexión.

Si quieres forzar la actualización del cache, cambia `'proyectos-v1'` por `'proyectos-v2'` en `sw.js`.
