# Catálogo

Tienda estática de productos naturistas y artesanales, hecha con HTML, CSS y JavaScript puro. No necesita servidor, base de datos ni servicios pagos.

## Archivos

- `index.html`: estructura y secciones de la página.
- `style.css`: estilos responsive y paleta visual.
- `script.js`: carga del catálogo, buscador, filtros, carrito y WhatsApp.
- `productos.json`: catálogo editable.

## Editar productos

Abre `productos.json` con un editor de texto y agrega otro objeto dentro de los corchetes `[ ]`. Cada producto debe tener estos campos:

```json
{
  "id": "id-unico-sin-espacios",
  "nombre": "Nombre del producto",
  "precio": 6500,
  "categoria": "Tés e infusiones",
  "foto": "https://direccion-de-la-imagen.jpg",
  "descripcion": "Descripción breve para la tarjeta.",
  "beneficios": "Beneficios que deseas comunicar.",
  "modo_uso": "Cómo se usa o consume.",
  "presentacion": "Frasco de 100 g",
  "disponibilidad": "en stock",
  "destacado": true
}
```

- `precio` debe ser un número, sin símbolo de moneda.
- Usa `"en stock"` o `"agotado"` en `disponibilidad`.
- Usa `true` o `false` en `destacado`.
- Separa cada objeto con una coma, excepto el último.
- Las fotos pueden ser enlaces públicos. Conviene usar JPG o WebP comprimidos y de aproximadamente 700 px.
- Para quitar un producto, elimina su objeto completo del archivo.

El número de WhatsApp se cambia en la primera línea de `script.js`, en `WHATSAPP_NUMBER`, usando código de país y número, sin `+`, espacios ni guiones.

## Publicar gratis

### GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html`, `style.css`, `script.js`, `productos.json` y este README.
3. En el repositorio, entra a **Settings > Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**, selecciona `main` y la carpeta `/ (root)`.
5. Guarda y espera a que GitHub muestre la URL pública.

### Netlify

1. Entra a [netlify.com](https://www.netlify.com/) y crea una cuenta gratuita.
2. Elige **Add new site > Deploy manually**.
3. Arrastra la carpeta completa del proyecto al área de carga.
4. Netlify publicará la página y te dará una URL. También puedes conectar un repositorio para que se actualice cada vez que hagas cambios.

## Nota para probar localmente

Por seguridad, algunos navegadores bloquean `fetch("productos.json")` cuando se abre `index.html` con doble clic. Para probarlo localmente usa una extensión de servidor local de VS Code o publícalo en GitHub Pages/Netlify.
