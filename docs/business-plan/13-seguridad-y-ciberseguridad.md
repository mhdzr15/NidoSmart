---
title: "Seguridad funcional y ciberseguridad"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.0"
last_updated: "2026-07-12"
---

# Seguridad funcional y ciberseguridad

## 13.1 Regla de acceso

La política será:

> Lectura amplia y escritura restringida.

El agente podrá consultar casi todas las variables, pero sólo podrá ejecutar acciones dentro de límites predefinidos.

## 13.2 Acciones permitidas

* Crear alertas.
* Generar reportes.
* Abrir órdenes de mantenimiento.
* Consultar inventario.
* Preparar órdenes de compra.
* Activar pruebas de equipos no críticos.
* Cambiar parámetros dentro de bandas autorizadas.
* Solicitar aprobación humana.

## 13.3 Acciones restringidas

No deberá modificar libremente:

* Ventilación mínima.
* Disponibilidad de agua.
* Fotoperiodo.
* Dosificación veterinaria.
* Protecciones eléctricas.
* Parámetros de seguridad.
* Alarmas críticas.
* Límites de temperatura.
* Actuadores durante una emergencia.

## 13.4 Controles requeridos

* Segmentación de red.
* Enlace de internet redundante (primario más respaldo satelital, por ejemplo Starlink).
* VPN.
* Autenticación.
* Roles.
* Listas blancas de comandos.
* Registro de acciones.
* Aprobación humana.
* Copias de seguridad.
* Operación manual.
* PLC como autoridad final.
* Paros de emergencia físicos.
* Pruebas periódicas de recuperación.

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Funciones del agente inteligente](./12-funciones-agente-inteligente.md)
- [Documento siguiente: Modelo operativo](./14-modelo-operativo.md)
