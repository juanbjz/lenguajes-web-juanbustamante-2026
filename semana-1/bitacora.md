# Bitácora de inspección HTTP

---

# Sitio 1 - GOV.CO

- **URL:** https://www.gov.co
- **Fecha y hora:** 10 de mayo de 2026 - 8:00 PM
- **Código de estado:** 200
- **TTFB:** 180 ms
- **Tamaño transferido:** 2.4 MB
- **Número de peticiones:** 95
- **Redirecciones 3xx observadas:** Ninguna
- **Autoridad TLS:** DigiCert Inc
- **Expiración del certificado:** 15 de enero de 2027

## Capturas

### Network
![Network GOV.CO](capturas/sitio1-network.png)

### TLS
![TLS GOV.CO](capturas/sitio1-tls.png)

---

# Sitio 2 - EAFIT

- **URL:** https://www.eafit.edu.co
- **Fecha y hora:** 10 de mayo de 2026 - 8:20 PM
- **Código de estado:** 200
- **TTFB:** 220 ms
- **Tamaño transferido:** 3.1 MB
- **Número de peticiones:** 110
- **Redirecciones 3xx observadas:** Redirección 301 HTTP → HTTPS
- **Autoridad TLS:** Let's Encrypt
- **Expiración del certificado:** 22 de febrero de 2027

## Capturas

### Network
![Network EAFIT](capturas/sitio2-network.png)

### TLS
![TLS EAFIT](capturas/sitio2-tls.png)

---

# Sitio 3 - Éxito

- **URL:** https://www.exito.com
- **Fecha y hora:** 10 de mayo de 2026 - 8:40 PM
- **Código de estado:** 200
- **TTFB:** 300 ms
- **Tamaño transferido:** 5.8 MB
- **Número de peticiones:** 210
- **Redirecciones 3xx observadas:** Redirección 302
- **Autoridad TLS:** DigiCert TLS RSA SHA256
- **Expiración del certificado:** 30 de noviembre de 2026

## Capturas

### Network
![Network Éxito](capturas/sitio3-network.png)

### TLS
![TLS Éxito](capturas/sitio3-tls.png)

---

# Reflexión final

Después de analizar los tres sitios web, observé que el sitio que cargó más rápido fue GOV.CO, debido a que presentó el menor tiempo de respuesta TTFB con 180 ms y además realizó una menor cantidad de peticiones en comparación con los demás sitios analizados. Considero que esto ocurre porque el portal gubernamental posee una estructura más sencilla y ligera, con menos contenido multimedia y menos scripts externos cargando al mismo tiempo. En contraste, el sitio comercial Éxito presentó un mayor tiempo de carga y una cantidad mucho más alta de solicitudes HTTP, probablemente por el uso de imágenes, anuncios, catálogos dinámicos y herramientas de seguimiento utilizadas en plataformas de comercio electrónico.

También pude identificar diferencias importantes en el manejo de las redirecciones. Mientras GOV.CO ingresó directamente utilizando HTTPS sin redirecciones visibles, el sitio universitario EAFIT realizó una redirección 301 desde HTTP hacia HTTPS, lo cual es una práctica común para obligar conexiones seguras. Por otro lado, el sitio Éxito presentó una redirección 302, generalmente utilizada para redirecciones temporales o de balanceo interno del sitio.

En cuanto a los certificados TLS, observé que no todos fueron emitidos por la misma autoridad certificadora. Algunos sitios utilizaron certificados emitidos por DigiCert y otros por Let's Encrypt. Esto demuestra que existen diferentes entidades encargadas de validar la autenticidad y seguridad de los sitios web. Además, todos los certificados revisados se encontraban vigentes y activos, garantizando conexiones seguras mediante cifrado HTTPS entre el navegador y los servidores web.
