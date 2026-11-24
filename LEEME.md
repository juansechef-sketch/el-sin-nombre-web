# Página de El Sin Nombre

Página independiente: HTML y CSS planos, sin framework, sin compilación, sin
conexión con el app del personal.

```
index.html          el contenido
estilos.css         el diseño (blanco y negro)
img/                logo, íconos y (cuando las haya) fotos
vista-previa.html   copia de un solo archivo, solo para mirarla. NO se sube.
```

Para verla: descomprimir y doble clic en `index.html`.

## Cambios frecuentes en `index.html`

| Qué | Dónde |
|---|---|
| Número de WhatsApp | `var WHATSAPP = "573217703875"` — único lugar; todos los botones lo toman de ahí. Cambiar también el número visible en "Dónde quedamos" y el `telephone` del bloque `ld+json` |
| Horarios | el párrafo `class="cuando"` de cada sección, la tabla `class="horarios"` y `openingHoursSpecification` en el bloque `ld+json` (lo lee Google) |
| Fotos | donde dice `<!-- FOTOS -->`: `<div class="fotos"><img src="img/nombre.jpg" alt="qué se ve" loading="lazy"></div>` |
| Redes sociales | en el pie, donde dice `<!-- Redes sociales -->` |

**Fotos:** JPG horizontal, máximo ~1600 px de ancho y menos de 300 KB cada una.

## Publicar en Cloudflare Pages (gratis)

No necesita Git ni nada instalado:

1. dash.cloudflare.com → **Workers & Pages** → **Create** → pestaña **Pages** →
   **Upload assets**
2. Nombre del proyecto: `elsinnombre` → arrastrar la carpeta (sin
   `vista-previa.html` ni el .zip) → **Deploy**
3. Queda en `https://elsinnombre.pages.dev`
4. **Custom domains** → **Set up a custom domain** → escribir el dominio
   comprado y seguir las instrucciones de DNS que muestra Cloudflare
5. Para actualizar después: mismo proyecto → **Create new deployment** → subir
   la carpeta otra vez
