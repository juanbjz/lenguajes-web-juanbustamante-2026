# Bitácora de inspección HTTP

---

# Sitio 1 - GOV.CO

- URL: https://www.gov.co
- Fecha y hora: 10 de mayo de 2026 - 8:00 PM
- Código de estado: 200
- TTFB: 180 ms
- Tamaño transferido: 2.4 MB
- Número de peticiones: 95
- Redirecciones 3xx observadas: Ninguna
- Autoridad TLS: DigiCert Inc
- Expiración del certificado: 15 de enero de 2027

## Capturas

![Network](capturas/sitio1-network.png)

![TLS](capturas/sitio1-tls.png)

---

# Sitio 2 - EAFIT

- URL: https://www.eafit.edu.co
- Fecha y hora: 10 de mayo de 2026 - 8:20 PM
- Código de estado: 200
- TTFB: 220 ms
- Tamaño transferido: 3.1 MB
- Número de peticiones: 110
- Redirecciones 3xx observadas: Redirección 301 HTTP → HTTPS
- Autoridad TLS: Let's Encrypt
- Expiración del certificado: 22 de febrero de 2027

## Capturas

![Network](capturas/sitio2-network.png)

![TLS](capturas/sitio2-tls.png)

---

# Sitio 3 - Éxito

- URL: https://www.exito.com
- Fecha y hora: 10 de mayo de 2026 - 8:40 PM
- Código de estado: 200
- TTFB: 300 ms
- Tamaño transferido: 5.8 MB
- Número de peticiones: 210
- Redirecciones 3xx observadas: Redirección 302
- Autoridad TLS: DigiCert TLS RSA SHA256
- Expiración del certificado: 30 de noviembre de 2026

## Capturas

![Network](capturas/sitio3-network.png)

![TLS](capturas/sitio3-tls.png)

---

# Reflexión final

Después de analizar los tres sitios web, observé que el sitio que cargó más rápido fue GOV.CO, ya que tuvo un menor tiempo de respuesta TTFB y una menor cantidad de peticiones realizadas. Considero que esto ocurre porque el sitio tiene una estructura más sencilla y menos elementos multimedia comparado con los otros sitios analizados.

También pude observar diferencias en el manejo de las redirecciones. Algunos sitios utilizan redirecciones automáticas de HTTP a HTTPS para garantizar conexiones seguras. Por ejemplo, el sitio universitario realizó una redirección 301 antes de cargar completamente la página principal.

En cuanto a los certificados TLS, noté que no todos fueron emitidos por la misma autoridad certificadora. Algunos sitios utilizan DigiCert mientras que otros usan Let's Encrypt. Esto demuestra que existen diferentes entidades encargadas de validar la seguridad y autenticidad de los sitios web. Además, todos los certificados observados se encontraban vigentes, lo cual garantiza una conexión segura entre el usuario y el servidor.
