# VOLVIA

Tienda online chilena especializada en **productos NFC** (con y sin código QR) para:

- Google Reviews
- Instagram
- TikTok
- LinkedIn
- WhatsApp
- Soluciones para restaurantes y llamadores inalámbricos (cotización)

Precios en pesos chilenos (CLP). Incluye tienda, packs, tarjetas colgantes, carrito, cotización para empresas, página Restaurantes, preguntas frecuentes y contacto.

## Tecnología

Sitio estático en **HTML + CSS + JavaScript** (sin framework, sin build). La navegación usa rutas con `#` (por ejemplo `#/tienda`, `#/p/pack-nfc`), por eso no necesita configuración de servidor.

## Estructura

```
volvia-web/
├── index.html            Página principal
├── css/styles.css        Estilos
├── js/app.js             Lógica: productos, rutas, carrito, formularios
├── images/               Logo y fotos de productos
├── package.json          Solo para ejecutar en local
├── .env.example          Plantilla de variables de entorno (hoy no se usa ninguna)
├── .gitignore
└── README.md
```

## Instalar y ejecutar en local

Necesitas [Node.js](https://nodejs.org) 18 o superior.

```bash
git clone https://github.com/TU-USUARIO/volvia-web.git
cd volvia-web
npm start
```

Abre http://localhost:3000. (También puedes abrir `index.html` directamente en el navegador.)

## Desplegar en Vercel

1. Sube este proyecto a un repositorio de GitHub llamado `volvia-web`.
2. En [vercel.com](https://vercel.com) entra con GitHub y elige **Add New > Project**.
3. Importa `volvia-web`. Vercel lo detecta como sitio estático:
   - Framework Preset: **Other**
   - Build Command: vacío
   - Output Directory: vacío (raíz del proyecto)
4. Presiona **Deploy**.

Cada vez que hagas `git push` a la rama `main`, Vercel despliega automáticamente y mantiene la misma URL.

## Cómo modificar

- Productos y precios: arreglo `P` en `js/app.js`.
- Fotos: carpeta `images/` (y el objeto `IMG` en `js/app.js`).
- Estilos: `css/styles.css`.
- Datos de contacto: WhatsApp `+56 9 7415 7259` y correo `contacto.volvia@gmail.com` (buscar en `js/app.js`).

## Pendiente (prototipo)

El carrito y los formularios son un prototipo: no cobran ni envían correos todavía. Flow Chile y el envío de formularios se conectarán más adelante.
