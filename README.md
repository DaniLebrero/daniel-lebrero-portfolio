# Portfolio de Daniel Lebrero

Sitio estático en HTML, CSS y JavaScript, publicado en [GitHub Pages](https://danilebrero.github.io/daniel-lebrero-portfolio/).

## Archivos

- `index.html`: presentación, experiencia, proyectos, homelab y formación.
- `styles.css`: diseño adaptable, temas y presentación de los casos prácticos.
- `script.js`: navegación, tema y aparición de secciones.
- `assets/`: imagen de perfil (logotipo), favicon y captura de Top & Performance.

No necesita instalación de dependencias ni un proceso de compilación.

## Previsualización y publicación

Desde este directorio:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Abrir `http://127.0.0.1:8000/`. Revisar escritorio y móvil, temas claro y oscuro, menú, navegación por teclado y enlaces de proyectos. Para publicar, utilizar el flujo de GitHub Pages configurado en el repositorio después de revisar los cambios.

## Inventario del homelab

Instantánea comprobada el **12 de noviembre de 2026** (20:30, Europe/Madrid) mediante:

```sh
docker ps --format '{{.Names}}' --filter status=running
```

| Contenedores en ejecución | Cantidad |
| --- | ---: |
| Entornos locales de Supabase (prefijo `supabase_`) | 18 |
| Otros servicios | 33 |
| Total | 51 |

La cifra cuenta **contenedores**, no aplicaciones. Los 18 de Supabase son **componentes auxiliares** de entornos locales de pruebas (base de datos, API, autenticación, etc.), no 18 aplicaciones. En los otros 33, una misma aplicación suele ocupar varios contenedores junto a su base de datos o su proxy. El total no garantiza la salud funcional de cada servicio y varía al arrancar o detener entornos de pruebas: es una instantánea fechada, no un contador conectado a Docker desde la web.

Al actualizar el inventario, comprobar la ejecución con Docker y cambiar conjuntamente la cifra, el desglose y la fecha en:

1. Las métricas de portada y el bloque `#laboratorio` de `index.html`.
2. Esta tabla.
3. Ambas versiones del README de `DaniLebrero`.

No publicar nombres internos, credenciales ni configuración de acceso para justificar una cifra.

## Evidencias de los casos

- [Top & Performance: desarrollo, despliegue y aprendizajes](https://es.linkedin.com/posts/daniellebrerocarcela_entrenamiento-personal-y-nutrici%C3%B3n-online-activity-7502451813326127104-26ju).
- [TFM BigShop: alcance, resultados y reconocimiento](https://es.linkedin.com/posts/daniellebrerocarcela_ciberseguridad-bigschool-top10-activity-7524202646979772418-u8uV).
- [AZ-900: publicación del logro](https://es.linkedin.com/posts/daniellebrerocarcela_azure-microsoftcertified-az900-activity-7517664563023151104-h9QU).
- Homelab: inventario local de Docker descrito arriba.

La ficha de Top & Performance describe la web publicada y los trabajos documentados por su autor. El 12 de noviembre de 2026 el sitio respondió HTTP 200 (en una comprobación anterior había devuelto 403) y se contrastó su HTML: servido por Cloudflare, con canonical, `robots.txt`, `sitemap.xml`, dos bloques JSON-LD, metadatos Open Graph e imágenes AVIF. `assets/top-performance.jpg` es una captura real de la portada tomada ese día a 1280 × 800 px con Chromium, sin retoques; acompaña al panel de aportaciones. La portada no contiene referencias a Stripe ni a un checkout (el contacto se inicia por WhatsApp), por lo que no se mantiene la antigua descripción de Stripe y webhooks.

## Actualización de noviembre de 2026

- ClassControl se retira del portfolio; Top & Performance ocupa su posición destacada, con una única ficha.
- Se incorpora el TFM como caso de auditoría en laboratorio.
- AZ-900 pasa de preparación a aprobado, enlazando la publicación; no se inventa la URL de una credencial.
- Se añade contexto de soporte N1, Entra ID y SharePoint.
- El homelab usa el inventario actual y distingue pruebas y componentes.
- Los títulos y metadatos usan una presentación común con el perfil de GitHub.
- Se completan canonical, URL e imagen social con la imagen de perfil existente (460 × 460 px, tarjeta `summary`).
- Se corrige el botón de tema: el selector `[data-theme]` coincidía con `<html>` y cualquier clic en la página cambiaba el tema; ahora solo responde el botón.
- Los textos alternativos describen la imagen de perfil como lo que es, un logotipo.

Pendientes de evidencia: el texto actual del perfil de LinkedIn (titular, experiencia, fechas), el estado formal y las fechas de los títulos, y la fecha, el identificador y la URL de la credencial AZ-900. El TFM realizado no se usa como prueba de expedición del título del máster, ni se da por finalizado el grado. La revisión se basa en las tres publicaciones públicas enlazadas arriba: LinkedIn bloquea la lectura automatizada del perfil (HTTP 999), así que su contenido no se ha podido contrastar. Se utiliza provisionalmente la denominación «Máster en Ciberseguridad — BIG school», siguiendo la indicación del usuario y la publicación del TFM, sin afirmar que sea el nombre oficial del título.

El usuario ha autorizado el uso de la captura de Top & Performance y ha confirmado que la redirección de yt-dlp Web es correcta. Ambos puntos quedan resueltos por su confirmación. No existe una imagen social de 1200 × 630 px; si se crea, cambiar `og:image` y `twitter:card` a `summary_large_image`.

## Validación

Comprobar ausencia de ClassControl y de los estados antiguos de AZ-900, una sola ficha de Top & Performance, inventario consistente, anclas internas, referencias a archivos y HTML/SVG bien estructurados. La revisión visual en navegador debe incluir 390 px y 1440 px, temas claro/oscuro, menú móvil y movimiento reducido.

Revisión del 12 de noviembre de 2026 con Chromium sin interfaz a 390, 820 y 1440 px, en ambos temas: sin desplazamiento horizontal, sin errores de consola, anclas e identificadores correctos, menú móvil que abre y cierra con Escape, foco visible en todos los enlaces y botones, y contenido visible con movimiento reducido. No sustituye a una prueba con lector de pantalla ni en dispositivos reales.
