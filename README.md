# 🧾 Módulo CPE - Facturador Electrónico SUNAT (PHP + XML + CURL)

![PHP](https://img.shields.io/badge/PHP-8.1%2B-777BB4?logo=php&logoColor=white)
![SUNAT](https://img.shields.io/badge/SUNAT-Facturador%20Electrónico-red)
![XML](https://img.shields.io/badge/XML-Firma%20Digital-orange)
![cURL](https://img.shields.io/badge/API-cURL-blue)
![License](https://img.shields.io/badge/Licencia-Open%20Source-green)

---

### 📘 Descripción general

El **Módulo CPE (Comprobante de Pago Electrónico)** es el **núcleo del facturador electrónico** que se integra con la **SUNAT (Perú)**.  
Desarrollado en **PHP**, este módulo permite **emitir, firmar y enviar comprobantes electrónicos** como facturas, boletas, notas de crédito y débito, siguiendo las **especificaciones oficiales UBL 2.1**.

Su estructura modular facilita la integración con cualquier sistema de ventas o ERP en PHP/MySQL, garantizando el cumplimiento con los estándares de facturación electrónica exigidos por la SUNAT.

---

### 🚀 Funcionalidades principales

#### 🧾 Emisión de comprobantes
- Genera **XML** válidos según el estándar **UBL 2.1**.
- Soporte para **facturas, boletas, notas de crédito y notas de débito**.
- Admite **detracciones, percepciones y retenciones**.
- Compatibilidad con **guías de remisión electrónicas**.

#### 🔏 Firma digital
- Firma de documentos con **certificados digitales (.pfx / .pem)**.
- Inclusión automática de **DigestValue y SignatureValue**.
- Validación de la estructura firmada antes del envío.

#### 📡 Envío y comunicación con SUNAT
- Comunicación vía **SOAP (cURL)** con los servidores de SUNAT:
  - **Producción:** `https://e-factura.sunat.gob.pe/ol-ti-itcpfegem/billService`
  - **Beta / Pruebas:** `https://e-beta.sunat.gob.pe/ol-ti-itcpfegem-beta/billService`
- Manejo de respuesta XML: código, mensaje y CDR.
- Almacenamiento local de **XML enviados** y **CDR recibidos**.

#### 📁 Gestión de archivos
- Genera estructura automática:
- Compresión ZIP para envío.
- Registro de estados (Pendiente, Aceptado, Rechazado, Observado).

#### 📊 Reportes de emisión
- Listado de comprobantes enviados a SUNAT.
- Estado de validación (aceptado, con errores o pendiente).
- Detalle de CDR (descripción y observaciones).
- Filtros por fecha, tipo de comprobante y serie.

---

🧠 Ventajas del módulo

✅ Cumple con el estándar UBL 2.1 de SUNAT
✅ Compatible con facturas, boletas, notas y guías
✅ Permite determinación automática de detracción
✅ Integrable con cualquier sistema de ventas en PHP/MySQL
✅ Fácil de mantener y escalar 

