# Changelog
Todos los cambios relevantes de este proyecto serán documentados en este archivo.

El formato sigue la convención de *Keep a Changelog*  
y el versionado es compatible con *Semantic Versioning*.

---

## [0.3.0] – 2026-01-20
### Added
- Integración completa con catálogos externos alojados en GitHub (RAW):
  - `work_items.json` (cómputo de materiales)
  - `materials_skus.json` (maestro de materiales)
  - `labor_catalog.json` (mano de obra)
- Interfaz por pasos mediante acordeón vertical:
  1. Cómputo de materiales  
  2. Lista de precios  
  3. Mano de obra  
  4. Datos de cliente  
  5. Reporte final
- Precarga automática de mano de obra vinculada al cómputo mediante `work_item_id`.
- Aplicación global de merma o desperdicio configurable por el usuario.
- Generación de reporte consolidado con:
  - Resumen económico
  - Cómputo de materiales
  - Mano de obra
- Exportación:
  - Envío por WhatsApp
  - Guardado en archivo `.txt`
  - Generación de nota extendida (2 páginas).

### Changed
- Se eliminó el cómputo hardcodeado y se migró a un sistema 100% gobernado por catálogos.
- La lista de precios ahora muestra únicamente los materiales efectivamente utilizados.
- La sección “Lista de precios” se desactiva automáticamente cuando los materiales están a cargo del cliente.
- Mejora general de la interfaz: jerarquía visual, sombras, tipografías y fluidez de uso.

### Fixed
- Corrección del uso incorrecto de URLs tipo `blob` de GitHub (reemplazadas por `raw.githubusercontent.com`).
- Normalización de esquemas JSON para tolerar variaciones de campos.
- Corrección de fallos donde la UI mostraba catálogos antiguos pese a actualizar la configuración.

---

## [Unreleased]
### Planned
- Ampliación del catálogo de cómputo:
  - Fundaciones completas
  - Losa cerámica y poliestireno
  - Carpetas por tipo
  - Hormigón por dosificación
  - Hierros por diámetro y longitud
- Ajustes finos de orden, nomenclatura y validaciones.
- Reglas avanzadas de cálculo (redondeos, mínimos, umbrales).
