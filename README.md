# 🔧 FerreInventario QR — Simulador Digital & Suite de Diagramas Interactivos

> **Asignatura:** Sistemas de Información (2026-2 C) — 8vo Semestre de Ingeniería de Sistemas  
> **Evaluación:** Segundo Corte II — Simulador Digital (Ponderación: 20 Puntos / 10%)  
> **Autor / Desarrollador:** Roger García  
> **GitHub:** [@rgamercm](https://github.com/rgamercm)  
> **URL Pública en Vivo:** [https://rgamercm.github.io/ferre-inventario-qr/](https://rgamercm.github.io/ferre-inventario-qr/)  
> **Versión:** v3.11.0 Production Ready (PWA Instalable Universal + Suite Unificada)  
> **Fecha:** Noviembre 2026  

---

## 📋 Descripción del Proyecto

Este proyecto es la solución completa para la actividad del **Simulador Digital**, aplicando rigurosamente las **Etapas del Ciclo de Vida del Software (SDLC)**. 

Se desarrolló una **Aplicación Móvil Responsiva Estilo Android con Simulador QR Real** para el control de inventario de una ferretería, integrada y unificada con **4 diagramas interactivos de ingeniería de software**:

1. **📅 Diagrama de Gantt Interactivo:** Planificación temporal y cronograma al 100% de ejecución.
2. **🔄 Diagrama de Flujo de Datos (DFD) Interactivo:** Modelado de los 6 procesos, 4 entidades externas y los 4 almacenes de datos (`D1` Usuarios, `D2` Productos, `D3` Movimientos, `D4` Registro Escaneos).
3. **⏱️ Diagrama de Secuencias UML Interactivo:** Modelado dinámico de las interacciones temporales para los 5 escenarios operativos:
   - 📷 **Escenario 1:** Escaneo de Código QR con cámara real y decodificación en vivo.
   - 📦 **Escenario 2:** Registro de Producto Nuevo con validación anti-duplicados y generación QR.
   - 📥 **Escenario 3:** Entrada de Mercancía con modal táctil y comprobante de recepción.
   - 📊 **Escenario 4:** Generación de Reportes y exportación en CSV (Excel) y PDF.
   - 🔐 **Escenario 5:** Autenticación de Usuario y control de sesiones.
4. **🏗️ Diagrama de Clases UML Interactivo:** Modelado estático de la arquitectura orientada a objetos (8 clases completas: `Usuario`, `Producto`, `Categoria`, `MovimientoInventario`, `CodigoQR`, `Proveedor`, `Reporte` y `Alerta`).
5. **📱 Aplicación Móvil Android Unificada:** Prototipo interactivo 100% responsivo con escáner QR en vivo (`jsQR`), generación ISO/IEC 18004, sincronización de tasas oficiales del **Banco Central de Venezuela (BCV)**, precios duales (Bs. y $ USD), CRUD completo de productos y auditoría diaria.

---

## 🧠 ¿Por qué se solicitaron estos diagramas antes de desarrollar la App? (Análisis del Prompt)

En el documento de la evaluación, el docente estructuró la secuencia de prompts solicitando primero los cuatro diagramas y luego pidiendo:

> *"Se comporte como un experto programación y genere la aplicación móvil estilo Android con qr para el control de un inventario de una ferretería y unifique todos los diagramas solicitados"*

### Justificación Metodológica en Ingeniería de Software:
1. **Etapa 1 — Planificación y Gestión (Diagrama de Gantt):**  
   Antes de escribir una sola línea de código, se debe estimar el tiempo, los recursos, las dependencias y las entregas críticas del proyecto. El Gantt desglosa las 6 fases (Requisitos, Diseño, Desarrollo, Pruebas, Despliegue y Mantenimiento) garantizando el cumplimiento del cronograma académico.
2. **Etapa 2 — Análisis de Requisitos y Flujo de Información (DFD):**  
   Permite visualizar cómo viajan los datos dentro del ecosistema de la ferretería: qué datos ingresa el Administrador, cómo interactúa la cámara con el sistema QR, cómo se consultan los Almacenes de Datos (`D1` a `D4`) y qué salidas se generan (Reportes, Alertas).
3. **Etapa 3 — Diseño del Comportamiento Dinámico (Diagrama de Secuencias):**  
   Establece el protocolo cronológico exacto de comunicación entre capas (Usuario → Vista App → Lector QR → Controlador → Base de Datos). Garantiza que cada caso de uso (escaneo, registro, reposición de stock, autenticación) tenga una ruta de ejecución validada.
4. **Etapa 4 — Diseño de Arquitectura Estructural (Diagrama de Clases):**  
   Define el modelo de dominio en Programación Orientada a Objetos (POO): las clases `Usuario`, `Producto`, `CodigoQR`, `Categoria`, `Proveedor`, `MovimientoInventario`, `Reporte` y `Alerta`, sus relaciones de agregación/asociación y sus métodos de negocio.
5. **Etapa 5 — Implementación y Prototipado (App Unificada):**  
   La app Android con QR final no es improvisada; es el **resultado ejecutable directo** que implementa fielmente los requisitos planificados en el Gantt, los flujos del DFD, las llamadas del diagrama de secuencias y los modelos del diagrama de clases.

---

## 🚀 Estructura de Archivos del Proyecto

```text
SimuladorDigital/
├── index.html                  # Aplicación principal móvil + Panel de Diagramas
├── diagrama-gantt.html         # Diagrama de Gantt interactivo (100% progreso)
├── diagrama-flujo-datos.html   # Diagrama de Flujo de Datos (DFD) SVG interactivo
├── diagrama-secuencias.html    # Diagrama de Secuencias UML con reproducción paso a paso
├── diagrama-clases.html        # Diagrama de Clases UML interactivo con inspector
├── js/
│   ├── qrcode.min.js          # Motor generador QR ISO/IEC 18004 (local, offline)
│   └── jsqr.min.js            # Motor decodificador QR en tiempo real (local, offline)
└── README.md                   # Documentación técnica, autoría y guía de despliegue
```

---

## 📱 Características de la Aplicación Móvil

- **Diseño Móvil Nativo:** 100% responsivo en smartphones y presentado con elegancia en escritorio.
- **Paleta de Colores Oficial:** `#2A363B` (Pizarra oscura), `#99B898` (Verde salvia), `#FECEAB` (Melocotón crema), `#FF847C` (Coral), `#E84A5F` (Carmesí).
- **Sincronización en Vivo con BCV:** Consulta las tasas oficiales de USD y EUR del Banco Central de Venezuela (`ve.dolarapi.com`), con ticker superior y ajuste manual de contingencia.
- **Precios Duales:** Muestra precios en Bolívares (`Bs.`) y Dólares (`$ USD`) en catálogo, ficha técnica, valorización y reportes.
- **Escáner QR Real (ISO/IEC 18004):** Cámara en vivo, subida de fotos, decodificador `jsQR` e historial de escaneos (Almacén `D4`).
- **CRUD Completo de Inventario:**
  - **Crear:** Registro de producto nuevo con anti-duplicados por código y nombre.
  - **Leer:** Catálogo filtrable por categorías, buscador en vivo y fichas técnicas.
  - **Actualizar:** Edición de productos y operaciones rápidas de stock (Entradas y Salidas con modal y comprobantes).
  - **Eliminar:** Eliminación segura con confirmación.
- **Gráfico Semanal de Barras Dobles:** Comparativa diaria de Entradas (Verde) vs Salidas (Rojo) con auditoría cronológica por día (`screenDayDetail`).
- **Reportes Operativos:** Exportación real a Excel (`.csv` con UTF-8 BOM) e impresión / guardado en PDF.
- **Centro de Perfil y Notificaciones:** Gestión de credenciales, configuración de tienda, alertas críticas y cierre de sesión.

---

## 🌐 Guía para Alojamiento Gratuito y Compartir la URL

El documento exige publicar la aplicación y compartir el enlace web (`URL`). A continuación se detallan las dos mejores opciones gratuitas:

### Opción 1: GitHub Pages (Recomendada — Con Autoría @rgamercm)
Esta opción es ideal porque la URL contendrá tu usuario de GitHub (`rgamercm.github.io`), demostrando de forma irrefutable tu autoría:

1. Entra a tu cuenta en [GitHub.com](https://github.com) (`@rgamercm`).
2. Crea un nuevo repositorio público llamado `ferre-inventario-qr` (o `simulador-digital`).
3. En la terminal dentro de esta carpeta, ejecuta:
   ```bash
   git remote add origin https://github.com/rgamercm/ferre-inventario-qr.git
   git push -u origin main
   ```
4. Ve a la pestaña **Settings** (Configuración) del repositorio en GitHub.
5. En el menú lateral izquierdo, haz clic en **Pages**.
6. En **Source** selecciona `Deploy from a branch`, elige la rama `main` y la carpeta `/ (root)`. Haz clic en **Save**.
7. En 1 minuto tu URL estará activa en:
   ```text
   https://rgamercm.github.io/ferre-inventario-qr/
   ```

---

### Opción 2: Netlify Drop (Instantánea — En 15 segundos sin comandos)
1. Ve a [app.netlify.com/drop](https://app.netlify.com/drop) en tu navegador.
2. Inicia sesión con tu cuenta de GitHub (`@rgamercm`).
3. Arrastra la carpeta completa `SimuladorDigital` y suéltala en el área de carga de Netlify.
4. Netlify generará instantáneamente una URL pública activa con certificado SSL HTTPS (ejemplo: `https://ferreinventario-rogergarcia.netlify.app`).

---

## 🔒 Declaración de Propiedad Intelectual

Este simulador digital, su código fuente, arquitectura de software y diagramas interactivos fueron desarrollados por **Roger García** ([@rgamercm](https://github.com/rgamercm)) para la asignatura de **Sistemas de Información** (8vo Semestre de Ingeniería de Sistemas). Prohibida su copia o plagio sin autorización.
