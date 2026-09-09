# smartDTE 3 — Normativa DTE 2.0 de MH

Distribución para Windows. Versión **3.0.1**.

Versión con soporte para la **Normativa de Cumplimiento de los Documentos
Tributarios Electrónicos 2.0 del Ministerio de Hacienda de El Salvador**.
Incluye sus estructuras, validaciones y catálogos para los flujos DTE y eventos
implementados en la aplicación. La versión 3 identifica la aplicación; cada
esquema DTE/evento mantiene la versión técnica que le corresponde en MH.

El ejecutable `smartDTE.exe` necesita la carpeta `_internal` que lo acompaña.
Para conservar una instalación, cerrar la app y mantener su carpeta `Documentos`
al actualizar el ejecutable y `_internal`. La base, licencia y configuración de
cada usuario se guardan localmente y están excluidas de Git.

Al pasar desde una instalación anterior, copiar localmente su carpeta `Documentos`
junto al ejecutable. No sobrescribirla con archivos de otra instalación.
La app aplica las migraciones pendientes al abrir la base; no requiere volver
a importar los DTE. `Diagnosticar.cmd` permite comprobar la instalación.

## Cambios 3.0.1

- Selección de distritos por nombre en contactos, emisor y facturación.
- Conversión conjunta de municipio antiguo a municipio nuevo y distrito.
- Migración del emisor y recuperación conservadora de distritos perdidos por
  versiones anteriores, cuando los documentos guardados permiten una coincidencia
  segura de identificación, dirección y municipio.
- Conservación de JSON históricos y de direcciones completas; los casos sin
  coincidencia suficiente permanecen pendientes para selección manual.
- Exportación de contactos con departamento y distrito.

Código fuente de esta distribución: commit `74348dc`.
Compilación: `20260909-021303-804489`. Verificada con la prueba de instalación
del ejecutable, 56 pruebas de migración/flujos fiscales y 53 de interfaz.

Este repositorio inicia el historial de la versión 3. Los datos privados de los
usuarios no forman parte de la distribución.
