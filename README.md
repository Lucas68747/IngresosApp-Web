# IngresosApp Web

Sitio web de **[IngresosApp](https://github.com/Lucas68747/IngresosApp)**, una aplicación de escritorio desarrollada en Python para registrar los ingresos y salidas en predios privados (barrios cerrados, parques industriales, etc.).

El sitio presenta la aplicación, muestra cómo funciona y ofrece la descarga directa de todas las versiones para Windows y Linux.

🌐 **[www.ingresosapp.com.ar](https://www.ingresosapp.com.ar/)**

---

## Versión actual: sitio estático en GitHub Pages

| | |
|---|---|
| **Frontend** | HTML5 y CSS3, sin frameworks ni JavaScript (tipografías Barlow Condensed y Open Sans) |
| **Hosting** | GitHub Pages |
| **Dominio** | `ingresosapp.com.ar`, registrado en NIC Argentina |
| **DNS** | Cloudflare (solo DNS, sin proxy) |
| **Descargas** | Servidas desde los [Releases de IngresosApp](https://github.com/Lucas68747/IngresosApp/releases); los botones principales apuntan siempre a la última versión |

### Estructura

```
├── index.html      # Página única
├── styles.css      # Estilos (paleta compartida con lucassantoro.com.ar)
├── CNAME           # Dominio personalizado para GitHub Pages
└── img/            # Capturas reales de la app, ícono e imagen para redes
```

### Verlo en local

No necesita compilación ni dependencias. Alcanza con abrir `index.html` en el navegador o levantar un servidor simple:

```bash
python -m http.server 8000
# http://localhost:8000
```

---

## Historia del proyecto

### v1 · Despliegue en AWS (2025)

La primera versión del sitio la construí para **practicar infraestructura cloud en un proyecto real**. En lugar de usar un hosting estático, monté y administré el servidor de punta a punta:

- **Aplicación:** Python con **Flask**, plantillas Jinja y Bootstrap.
- **Cómputo:** instancia **Amazon EC2** con Linux.
- **Servidor de aplicaciones:** **Gunicorn** ejecutando la app Flask.
- **Servidor web:** **Nginx** como proxy inverso delante de Gunicorn.
- **DNS:** zona hospedada en **Amazon Route 53**, con el dominio delegado desde NIC Argentina.
- **Despliegue:** actualización manual en el servidor con `git pull` desde este repositorio.

Esa versión me sirvió para pasar por el ciclo completo: crear y configurar la instancia, instalar y conectar Gunicorn con Nginx, apuntar un dominio propio y mantener el servicio en línea.

### v2 · Migración a GitHub Pages (2026)

Con el tiempo quedó claro que el sitio no necesitaba un servidor: Flask solo renderizaba una página fija, sin formularios ni base de datos. Mantener una instancia EC2 encendida para eso generaba un costo mensual sin ningún beneficio para el usuario final, así que decidí **migrarlo a un sitio estático en GitHub Pages**, sin costo de hosting.

En la migración también aproveché para:

- Reemplazar Flask, Jinja y Bootstrap por una única página HTML con CSS propio.
- Sacar el carrusel de fotos de stock (unos 18 MB de imágenes) y usar capturas reales de la app.
- Cambiar el botón "Descargar", que llevaba al repositorio, por **descargas directas** para Windows y Linux.
- Mejorar la accesibilidad: textos alternativos descriptivos, foco visible y contraste.
- Dar de baja los recursos de AWS asociados.

### Actualización para IngresosApp 2.0 (octubre 2026)

- Capturas nuevas de la versión 2.0 y un recorrido por un día en la guardia: llegada, turno, correcciones y cierre.
- Sección «Qué más trae» con las funciones nuevas (agenda, copias de seguridad, búsqueda, recorrido).
- Tabla con **todas las versiones** y sus descargas para Windows y Linux.
- Ícono nuevo de la app como favicon, e imagen y metadatos para cuando se comparte el enlace.
- DNS movido de Route 53 a Cloudflare.

El código de la versión en AWS sigue disponible en la etiqueta [`aws-flask`](https://github.com/Lucas68747/IngresosApp-Web/tree/aws-flask):

```bash
git checkout aws-flask
```

---

## Autor

**Lucas Emanuel Santoro** · [Portfolio](https://www.lucassantoro.com.ar/) · [GitHub](https://github.com/Lucas68747) · [LinkedIn](https://www.linkedin.com/in/lucassantoro/)
