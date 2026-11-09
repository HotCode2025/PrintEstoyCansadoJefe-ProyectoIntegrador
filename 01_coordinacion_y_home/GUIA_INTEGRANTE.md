# 🚀 Guía de Trabajo y Entrega en GitHub — Parte 1: Coordinación General, Presentación Yokai & Landing Page Frontend

**Rol Asignado:** Integrante 1 — Coordinador de Proyecto / Arquitecto Frontend Base  
**Rama de Git sugerida:** `feature/01-esqueleto-home`  
**Mensaje de Commit sugerido:** `feat(frontend): inicializar aplicacion React, layout global Kinpaku y HomePage`

---

## 📌 1. ¿Qué contiene esta carpeta?

Esta carpeta contiene **exclusivamente los archivos que te corresponden subir a GitHub** para que tu autoría quede registrada en el repositorio oficial de la tecnicatura.

La estructura interna de carpetas (`src/`, `server/`, `db/`, etc.) coincide exactamente con la raíz del proyecto.

### Archivos asignados en este módulo:
- `src/App.jsx`
- `src/main.jsx`
- `src/index.css`
- `src/pages/HomePage.jsx`
- `src/components/layout/MainLayout.jsx`
- `src/components/layout/Header.jsx`
- `src/components/layout/Footer.jsx`
- `index.html`
- `public`
- `README.md`

---

## 🛠 2. Resumen Técnico del Módulo

Este módulo establece la identidad visual Kinpaku & Sumi y el esqueleto de navegación de la aplicación web:
- Enrutamiento con React Router DOM v6 en App.jsx.
- Layout compartido en MainLayout con Header y Footer temáticos.
- Landing page en HomePage.jsx con catálogo destacado, llamada a la acción y estética yokai.
- Estilos base con Tailwind CSS e index.css.

---

## 💻 3. Paso a Paso para Subir tu Parte a GitHub

Seguí estos pasos en tu terminal (Bash o PowerShell) dentro de la carpeta donde tengas clonado el repositorio de la tecnicatura:

### Paso 1: Asegurarte de tener la última versión de `develop` o `main`
```bash
git checkout develop || git checkout main
git pull origin develop || git pull origin main
```

### Paso 2: Crear tu rama de trabajo
```bash
git checkout -b feature/01-esqueleto-home
```

### Paso 3: Copiar los archivos de esta carpeta a tu repositorio
Copiá el contenido de esta carpeta (las subcarpetas `src`, `server`, etc.) directamente sobre la raíz de tu repositorio clonado.

### Paso 4: Revisar qué archivos agregaste
```bash
git status
```

### Paso 5: Agregar los archivos al stage y commitear
```bash
git add .
git commit -m "feat(frontend): inicializar aplicacion React, layout global Kinpaku y HomePage"
```

### Paso 6: Subir tu rama a GitHub
```bash
git push -u origin feature/01-esqueleto-home
```

### Paso 7: Crear el Pull Request en GitHub
1. Entrá al repositorio en GitHub.
2. Vas a ver el botón **"Compare & pull request"**.
3. Seleccioná como rama base `develop` (o `main`) y dejá una descripción clara de lo que implementaste en tu módulo.

---

## 🎓 4. Preguntas Frecuentes para Defender este Código en el Coloquio

Si el profesor te pregunta por los archivos que subiste, acá tenés los fundamentos arquitectónicos clave:

### Pregunta 1: ¿Por qué se desacopló el Layout principal del contenido de cada página?
**Respuesta:** Para respetar el principio Single Responsibility (SRP): MainLayout maneja la estructura común de la vista (Header, Footer, Toast notifications y Outlet), mientras que cada página (como HomePage) solo se enfoca en sus datos y renderizado específico.

### Pregunta 2: ¿Cómo se maneja la carga de recursos estáticos en producción?
**Respuesta:** Todos los recursos estáticos residen en /public (como logos y máscaras). Vite los copia directamente a la raíz de la carpeta de distribución dist sin procesar URLs relativas frágiles.


---
*Equipo Print("Estoy Cansado Jefe") — UTN San Rafael*
