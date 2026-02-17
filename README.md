# Google Sheets Automation Engine – Asignación y Trazabilidad

## Descripción General
Este repositorio contiene una implementación de **automatización operativa en Google Sheets** utilizando **Google Apps Script**, orientada a la **gestión de solicitudes**, **registro de eventos** y **asignación automática de responsables** mediante reglas centralizadas.

El proyecto transforma una hoja de cálculo tradicional en un **sistema reactivo**, capaz de ejecutar lógica de negocio en tiempo real ante acciones del usuario.

---

## Objetivo del Proyecto
Automatizar procesos repetitivos y sensibles a errores humanos, proporcionando:

- Registro automático de eventos (timestamps)
- Sincronización de contexto entre hojas
- Asignación controlada de responsables
- Centralización de reglas de negocio
- Trazabilidad operativa básica

---

## Arquitectura Funcional

```text
Usuario edita celda
        ↓
Trigger onEdit
        ↓
┌───────────────────────────┐
│ Registro de timestamp     │
│ (auditoría de eventos)    │
└───────────────────────────┘
        ↓
┌───────────────────────────┐
│ Sincronización de contexto│
│ hacia hoja de control     │
└───────────────────────────┘
        ↓
┌───────────────────────────┐
│ Motor de reglas           │
│ (asignación responsable) │
└───────────────────────────┘

