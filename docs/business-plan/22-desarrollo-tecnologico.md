---
title: "Estrategia de desarrollo tecnológico"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.0"
last_updated: "2026-07-12"
---

# Estrategia de desarrollo tecnológico

## 21.1 Enfoque: technology-first, business-validated

La ejecución del proyecto debe comenzar con el desarrollo de la tecnología, pero no con la construcción de una plataforma completa antes de tener aves y clientes. La estrategia correcta es desarrollar primero un **núcleo tecnológico mínimo**, validarlo en banco de pruebas y después mejorarlo con datos reales de la granja.

El principal riesgo de comenzar exclusivamente por la tecnología es terminar con un sistema sofisticado que automatiza supuestos incorrectos. En avicultura, muchas decisiones dependen de la genética, el alojamiento, el clima, el comportamiento de las aves, el alimento y la rutina sanitaria. Todo eso sólo puede validarse en operación real.

## 21.2 La tecnología es una dependencia crítica, pero no es todo el negocio

NidoSmart depende de la tecnología para:

* Reducir la mano de obra.
* Mantener condiciones ambientales.
* Registrar consumos y producción.
* Detectar fallas.
* Hacer posible el crecimiento modular.
* Convertir la granja en una unidad repetible.

Sin embargo, el negocio también depende de tres elementos que la tecnología no puede sustituir:

1. **Biología:** salud, bienestar, genética y manejo.
2. **Mercado:** clientes dispuestos a comprar recurrentemente al precio necesario.
3. **Operación física:** agua, energía, ventilación, limpieza y bioseguridad.

Por eso, el orden de ejecución **no** debe ser:

> Desarrollar toda la tecnología → construir la granja → buscar clientes.

Debe ser:

> Definir requisitos productivos y comerciales → desarrollar el núcleo tecnológico → probarlo sin aves → instalar el módulo piloto → perfeccionarlo con datos reales.

## 21.3 Tecnología que debe desarrollarse antes de recibir las aves

Antes de introducir la primera parvada, deberán estar funcionando y probados:

### Control crítico

* Lectura de temperatura y humedad.
* Control de ventiladores.
* Control de iluminación.
* Supervisión de nivel y flujo de agua.
* Alarmas por falta de agua.
* Alimentación programada.
* Detección de fallas eléctricas.
* Operación manual de emergencia.
* Respaldo eléctrico para control y comunicaciones.

### Plataforma de datos

* Registro histórico de sensores.
* Base de datos.
* Identificación de cada módulo.
* Panel de monitoreo.
* Sistema de alertas.
* Registro de eventos y acciones.
* Copias de seguridad.

### Integración básica

* PLC o controlador.
* MQTT.
* Node-RED.
* Grafana.
* Acceso remoto mediante VPN.
* Comunicación entre el tablero central y el módulo.

Todo esto deberá probarse con:

* Sensores reales.
* Motores pequeños.
* Focos.
* Válvulas.
* Resistencias o calentadores.
* Simulación de fallas.
* Datos sintéticos.
* Una maqueta parcial del módulo.

## 21.4 Tecnología que debe aplazarse hasta contar con datos reales

Deberán aplazarse estas funciones hasta tener datos reales de operación:

* Inteligencia artificial para predecir enfermedades.
* Visión artificial avanzada.
* Conteo automático perfecto de huevos.
* Optimización automática de alimento.
* Clasificación de huevo por cámara.
* Agentes autónomos de compras.
* Paperclip y coordinación multiagente.
* ERP complejo.
* Automatización total de empaque.
* Gemelo digital sofisticado.
* Algoritmos de control adaptativo.

Estas funciones necesitan históricos confiables. Sin datos reales, se convertirían en demostraciones tecnológicas, no en herramientas productivas.

## 21.5 Producto mínimo tecnológico: NidoSmart Core

La primera versión de **NidoSmart Core** deberá resolver cinco problemas:

1. Mantener vivas y confortables a las aves.
2. Garantizar agua y alimento.
3. Detectar rápidamente una falla.
4. Registrar lo ocurrido.
5. Permitir conectar un segundo módulo sin rediseñar el sistema.

Ése es el verdadero MVP tecnológico. No necesita ser visualmente perfecto ni tener inteligencia artificial avanzada. Debe ser estable, mantenible y seguro.

## 21.6 Secuencia de desarrollo tecnológico

Esta secuencia detalla, dentro de la Fase 1 de la [hoja de ruta](./23-hoja-de-ruta.md), cómo desarrollar y validar la tecnología antes y durante el ingreso de la parvada piloto.

### Etapa 1. Especificación funcional

Antes de programar, deberá definirse:

* Variables que se medirán.
* Rangos permitidos.
* Actuadores.
* Alarmas.
* Modos de falla.
* Operación manual.
* Frecuencia de muestreo.
* Datos que necesita el negocio.
* Interfaces para nuevos módulos.

El resultado deberá ser una matriz similar a ésta:

| Variable           | Sensor            | Frecuencia  | Alarma          | Acción automática              |
| -------------------- | ------------------- | -----------: | ----------------- | -------------------------------- |
| Temperatura         | Sensor ambiental    |        10 s | Alta/baja        | Ventilación o calefacción       |
| Humedad             | Sensor ambiental    |        30 s | Alta              | Aumentar ventilación             |
| Flujo de agua       | Caudalímetro        |       1 min | Cero o anormal    | Alerta y revisión                |
| Nivel de alimento   | Sensor de nivel     |       5 min | Bajo              | Alerta de reposición             |
| Energía             | Medidor/relé        |    Continuo | Pérdida           | Activar contingencia             |
| CO₂                 | Sensor de gas       |       1 min | Alto              | Aumentar ventilación             |
| Amoníaco            | Sensor adecuado     |     1–5 min | Alto              | Ventilar y revisar gallinaza    |

### Etapa 2. Banco de pruebas

Deberá construirse un tablero técnico con:

* PLC.
* Fuente de alimentación.
* Relevadores o contactores.
* Sensores.
* Gateway.
* Broker MQTT.
* Node-RED.
* Base de datos.
* Panel.
* Alarmas.

Posteriormente deberán simularse:

* Sensor desconectado.
* Falta de internet.
* Pérdida de electricidad.
* Ventilador atascado.
* Tanque vacío.
* Fuga de agua.
* Temperatura elevada.
* Reinicio del servidor.
* Caída de comunicaciones.

El sistema deberá fallar de manera segura ante cada uno de estos escenarios.

### Etapa 3. Instalación sin aves

Deberá instalarse la tecnología en el módulo real y operarse durante una o dos semanas sin animales, observando:

* Temperatura real.
* Ciclos día-noche.
* Respuesta de los ventiladores.
* Consumo eléctrico.
* Cobertura de comunicaciones.
* Estabilidad del software.
* Calidad del agua.
* Alarmas falsas.
* Comportamiento del respaldo.

### Etapa 4. Ingreso de la parvada piloto

Cuando entren las aves, la tecnología básica ya deberá ser estable. A partir de ahí se recopilarán datos de:

* Agua.
* Alimento.
* Temperatura.
* Humedad.
* Postura.
* Huevos descartados.
* Mortalidad.
* Energía.
* Horas de trabajo.
* Ventas.

### Etapa 5. Inteligencia progresiva

Después de acumular suficientes datos, Hermes Agent podrá comenzar con tareas de bajo riesgo:

* Resumir la producción.
* Comparar contra la curva esperada.
* Explicar desviaciones.
* Generar reportes.
* Consultar manuales.
* Crear recordatorios de mantenimiento.
* Calcular inventario.
* Preparar compras.

Más adelante podrá recomendar ajustes, pero no controlar libremente los sistemas críticos, conforme al principio establecido en [Arquitectura tecnológica — Principio fundamental](./10-arquitectura-tecnologica.md#101-principio-fundamental).

## 21.7 Desarrollo comercial en paralelo

Aunque el desarrollo tecnológico comience primero, la validación comercial no debe esperar. Mientras se construye el sistema deberá avanzarse también en:

* Entrevistar clientes.
* Validar presentaciones.
* Probar precios.
* Diseñar suscripciones.
* Identificar rutas.
* Cotizar alimento.
* Seleccionar pollitas.
* Revisar permisos.
* Consultar al veterinario.
* Definir procedimientos sanitarios.

De esta forma, la tecnología y el negocio llegan juntos al momento de recibir la parvada.

## 21.8 Regla de desarrollo y meta del MVP

Ninguna función deberá desarrollarse si no reduce un riesgo, una tarea, un costo o una incertidumbre del negocio.

La primera meta no es "crear una granja autónoma". Es:

> Construir una plataforma confiable que opere un módulo de 100 aves, registre datos verificables y pueda replicarse sin cambios estructurales.

## 21.9 Conclusión

Conviene iniciar por la tecnología, porque define la modularidad y la capacidad futura de NidoSmart. Pero debe desarrollarse como infraestructura mínima orientada a problemas reales, no como una plataforma completa creada en aislamiento. El proyecto deberá avanzar con un enfoque **technology-first, but business-validated**: tecnología primero en la secuencia técnica, y mercado, sanidad y operación en paralelo.

Este enfoque de desarrollo tecnológico previo al ingreso de las aves es una decisión estratégica registrada como [DEC-011 en el registro de decisiones](../governance/registro-de-decisiones.md#dec-011--desarrollo-tecnológico-previo-al-ingreso-de-las-aves).

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Gestión de riesgos](./21-gestion-de-riesgos.md)
- [Documento siguiente: Hoja de ruta](./23-hoja-de-ruta.md)
