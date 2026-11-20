# 🔧 FerreInventario QR — Simulador Digital & Suite de Diagramas Interactivos

> **Asignatura:** Sistemas de Información (2026-2 C) — 8vo Semestre de Ingeniería de Sistemas  
> **Evaluación:** Segundo Corte II — Simulador Digital (Ponderación: 20 Puntos / 10%)  
> **Autor / Desarrollador:** Roger García  
> **GitHub:** [@rgamercm](https://github.com/rgamercm)  
> **Fecha:** Noviembre 2026  

---

## 📋 Descripción del Proyecto

Este proyecto es la solución completa para la actividad del **Simulador Digital**, aplicando rigurosamente las **Etapas del Desarrollo de Software (SDLC)**. 

Se desarrolló una **Aplicación Móvil Estilo Android con Simulador QR** para el control de inventario de una ferretería, integrada y unificada con **4 diagramas interactivos de ingeniería de software**:

1. **📅 Diagrama de Gantt Interactivo:** Planificación temporal y cronograma de fases del proyecto.
2. **🔄 Diagrama de Flujo de Datos (DFD) Interactivo:** Modelado de procesos, entidades externas y almacenes de datos.
3. **⏱️ Diagrama de Secuencias UML Interactivo:** Modelado dinámico de las interacciones temporales para los 5 escenarios operativos principales.
4. **🏗️ Diagrama de Clases UML Interactivo:** Modelado estático de la arquitectura orientada a objetos (clases, atributos, métodos y multiplicidades).
5. **📱 Aplicación Móvil Android Unificada:** Prototipo interactivo en frame de smartphone Android con escáner QR en tiempo real, gestión de productos, alertas de stock bajo, movimientos y reportes.

---

## 🧠 ¿Por qué se solicitaron estos diagramas antes de desarrollar la App? (Análisis del Prompt)

En el documento de la evaluación, el docente estructuró la secuencia de prompts solicitando primero los cuatro diagramas y luego pidiendo:

> *"Se comporte como un experto programación y genere la aplicación móvil estilo Android con qr para el control de un inventario de una ferretería y unifique todos los diagramas solicitados"*

### Justificación Metodológica en Ingeniería de Software:
1. **Etapa 1 — Planificación y Gestión (Diagrama de Gantt):**  
   Antes de escribir una sola línea de código, se debe estimar el tiempo, los recursos, las dependencias y las entregas críticas del proyecto. El Gantt desglosa las 6 fases (Requisitos, Diseño, Desarrollo, Pruebas, Despliegue y Mantenimiento) en un horizonte de 12 semanas.
2. **Etapa 2 — Análisis de Requisitos y Flujo de Información (DFD):**  
   Permite visualizar cómo viajan los datos dentro del ecosistema de la ferretería: qué datos ingresa el Administrador, cómo interactúa la cámara con el sistema QR, cómo se consultan los Almacenes de Datos (BD Productos, BD Movimientos) y qué salidas se generan (Reportes, Alertas).
3. **Etapa 3 — Diseño del Comportamiento Dinámico (Diagrama de Secuencias):**  
   Establece el protocolo cronológico exacto de comunicación entre capas (Usuario → Vista App → Lector QR → Controlador → Base de Datos). Garantiza que cada caso de uso (escaneo, registro, reposición de stock, autenticación) tenga una ruta de ejecución validada.
4. **Etapa 4 — Diseño de Arquitectura Estructural (Diagrama de Clases):**  
   Define el modelo de dominio en Programación Orientada a Objetos (POO): las clases `Usuario`, `Producto`, `CodigoQR`, `Categoria`, `Proveedor`, `MovimientoInventario`, `Reporte` y `Alerta`, sus relaciones de agregación/asociación y sus métodos de negocio.
5. **Etapa 5 — Implementación y Prototipado (App Unificada):**  
   La app Android con QR final no es improvisada; es el **resultado ejecutable directo** que implementa fielmente los requisitos planificados en el Gantt, los flujos del DFD, las llamadas del diagrama de secuencias y los modelos del diagrama de clases.

---

## 🚀 Estructura de Archivos

```text
SimuladorDigital/
├── index.html                  # Aplicación principal: Móvil Android + Panel de Diagramas
├── diagrama-gantt.html         # Diagrama de Gantt interactivo a pantalla completa
├── diagrama-flujo-datos.html   # Diagrama de Flujo de Datos (DFD) SVG interactivo
├── diagrama-secuencias.html    # Diagrama de Secuencias UML con reproducción interactiva
├── diagrama-clases.html        # Diagrama de Clases UML interactivo con modal de detalles
└── README.md                   # Documentación técnica, autoría y guía de despliegue
```

---

## 📱 Características de la Aplicación Móvil (Android Frame)

- **Mockup Android Realista:** Marco de smartphone con notch, barra de estado (hora, red, batería) y navegación Material Design.
- **Splash Screen:** Pantalla de bienvenida con logo, animación y créditos a Roger García (@rgamercm).
- **Módulo de Autenticación:** Login simulado con roles de usuario (Administrador / Empleado).
- **Dashboard Operativo:** Indicadores KPI en tiempo real (Total Productos, Stock Bajo, Movimientos, Valoración de Inventario) y gráfica semanal de movimientos.
- **Escáner QR Interactivo:**
  - Simulación de viewport de cámara con cuadrícula y mira de enfoque.
  - Animación de rayo láser escaneador.
  - Detección de productos con visualización inmediata de ficha técnica.
  - Modo de escaneo manual por código (`FER-001`, `FER-002`, etc.).
- **Catálogo de Ferretería Completo:**
  - Productos precargados: Martillos, Destornilladores, Pintura Galón, Cable eléctrico, Llaves ajustables, Teflón, Tornillería Drywall, Tubos PVC, etc.
  - Búsqueda en tiempo real y filtrado por categorías.
  - Alertas visuales automáticas cuando el stock es menor al mínimo.
  - Modal para agregar nuevos productos con generación de código QR.
- **Detalle de Producto:** Ficha completa con código QR generado en vivo, historial de movimientos y botones para entradas/salidas de mercancía.
- **Módulo de Reportes:** Generación de resúmenes de inventario, stock crítico y valorización.
- **Perfil de Usuario:** Ficha del administrador (Roger García).

---

## 🌐 Guía para Alojamiento Gratuito y Compartir la URL

El documento exige publicar la aplicación y compartir el enlace web (`URL`). A continuación se detallan las 3 mejores opciones gratuitas:

### Opción 1: GitHub Pages (Recomendada — Con Autoría @rgamercm)
Esta opción es ideal porque la URL contendrá tu usuario de GitHub (`rgamercm.github.io`), demostrando de forma irrefutable tu autoría:

1. Entra a tu cuenta en [GitHub.com](https://github.com) (`@rgamercm`).
2. Crea un nuevo repositorio público llamado `ferreteria-inventario-qr` (o `simulador-digital`).
3. Sube los archivos de la carpeta `SimuladorDigital` (`index.html`, los 4 archivos de diagramas y el `README.md`).
4. Ve a la pestaña **Settings** (Configuración) del repositorio.
5. En el menú lateral izquierdo, haz clic en **Pages**.
6. En **Source** selecciona `Deploy from a branch`, elige la rama `main` (o `master`) y la carpeta `/ (root)`. Haz clic en **Save**.
7. En 1-2 minutos tu URL estará activa en:
   ```
   https://rgamercm.github.io/ferreteria-inventario-qr/
   ```

---

### Opción 2: Netlify Drop (La más rápida — En 30 segundos)
1. Ve a [app.netlify.com/drop](https://app.netlify.com/drop) en tu navegador.
2. Inicia sesión con tu cuenta de GitHub (`@rgamercm`).
3. Arrastra la carpeta completa `SimuladorDigital` y suéltala en el círculo verde de Netlify.
4. Netlify generará instantáneamente una URL pública (ejemplo: `https://ferreinventario-rgamercm.netlify.app`).

---

### Opción 3: Vercel
1. Ve a [vercel.com](https://vercel.com) e inicia sesión con tu GitHub (`@rgamercm`).
2. Haz clic en **Add New Project**.
3. Importa el repositorio donde subiste los archivos y haz clic en **Deploy**.
4. Te entregará una URL gratuita con certificado SSL automático (ejemplo: `https://ferreteria-qr.vercel.app`).

---

## 🔒 Declaración de Propiedad Intelectual

Este simulador digital, su código fuente, arquitectura de software y diagramas interactivos fueron desarrollados por **Roger García** ([@rgamercm](https://github.com/rgamercm)) para la asignatura de **Sistemas de Información** (8vo Semestre de Ingeniería de Sistemas). Prohibida su copia o plagio sin autorización.
