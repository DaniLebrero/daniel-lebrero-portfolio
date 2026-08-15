# Portfolio de Daniel Lebrero

Portfolio estático y responsive preparado para GitHub Pages.

## Incluye

- Presentación profesional y proyectos propios.
- Laboratorio con 24 contenedores y 19 servicios catalogados.
- Formación en TDD, patrones, CI/CD, arquitectura hexagonal y ciberseguridad.
- Preparación de Azure Fundamentals indicada como no certificada todavía.
- Tema claro/oscuro, navegación móvil, accesibilidad y animaciones respetuosas con `prefers-reduced-motion`.

No utiliza frameworks, dependencias ni proceso de compilación.

## Probar en local

```bash
python3 -m http.server 8080
```

Abre `http://localhost:8080`.

## Publicar con GitHub Pages

1. Crea un repositorio vacío, por ejemplo `portfolio` o `DaniLebrero.github.io`.
2. Conecta este repositorio local y haz push:

```bash
git remote add origin git@github.com:DaniLebrero/NOMBRE-DEL-REPOSITORIO.git
git push -u origin main
```

3. En GitHub, abre **Settings > Pages**.
4. Selecciona **Deploy from a branch**, rama `main` y carpeta `/ (root)`.

Las rutas son relativas y funcionan como página de usuario o de proyecto.

## Personalización

- Contenido y enlaces: `index.html`
- Diseño responsive: `styles.css`
- Tema, menú y animaciones: `script.js`
- Foto: `assets/daniel-lebrero.jpg`

La web no expone dominios privados, IP ni paneles del servidor. Conviene revisar antes de publicar cualquier dato que pueda haber cambiado.
