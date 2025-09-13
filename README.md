# IngresosApp Web

Sitio web creado como complemento para **IngresosApp**, una aplicación de escritorio desarrollada en Python.  
El propósito de la web es ofrecer un punto de descarga para la app y mostrar un ejemplo de despliegue en un servidor en la nube.

---

## Tecnologías utilizadas

- **Frontend**: HTML5, CSS3 y Bootstrap.  
- **Backend**: Python con Flask.  
- **Infraestructura**: AWS EC2 con Linux, Nginx y Gunicorn.  
- **Control de versiones**: Git y GitHub.

---

## Funcionalidades principales

- Página de inicio con descripción de la aplicación.  
- Botones de descarga que redirigen al repositorio y a los *releases*.  
- Sección de historial de versiones (*changelog*) con enlaces a descargas específicas.  
- Diseño responsive que se adapta a diferentes dispositivos.

---

## ☁️ Despliegue en AWS

- Se configuró una instancia EC2 (Linux).  
- Se instalaron los paquetes necesarios para ejecutar Flask con Gunicorn.  
- Nginx se configuró como proxy inverso para servir la aplicación.  
- La aplicación se actualiza mediante `git pull` desde este repositorio.  

---

## 📥 Descarga de la aplicación

La aplicación **IngresosApp** puede descargarse desde la sección de [**Releases en GitHub**](https://github.com/Lucas68747/IngresosApp/releases).

---

## Historial de versiones

- **v1.0**: Primera versión con función de exportar reportes en PDF.  

<img width="1899" height="904" alt="captura1" src="https://github.com/user-attachments/assets/9a009f15-ef8f-4cc2-8e65-d301b0285f47" />
<img width="1896" height="904" alt="captura2" src="https://github.com/user-attachments/assets/0dab2728-f16e-485c-a1f1-cc6eb43fb3f7" />

