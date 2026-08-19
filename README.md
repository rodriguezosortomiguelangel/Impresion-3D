# 🖨️ Práctica de Impresión 3D: Preparación, Laminado e Impresión

![Status](https://img.shields.io/badge/Estado-Completado-success?style=for-the-badge)
![Technology](https://img.shields.io/badge/Tecnología-FDM%2FFF3D-blue?style=for-the-badge)
![Material](https://img.shields.io/badge/Material-PLA_1.75mm-green?style=for-the-badge)

Documentación técnica y registro de proceso para la práctica de modelado, procesamiento de código G e impresión 3D mediante tecnología de modelado por deposición fundida (FDM).

---

## 📌 1. Descripción de la Práctica

El objetivo de esta práctica es dominar el flujo de trabajo completo de la fabricación aditiva: desde la verificación geométrica de la malla 3D, la configuración precisa de parámetros en el software laminador (*slicer*), hasta la calibración física del equipo y la ejecución exitosa de la impresión.

### 🎯 Objetivos Específicos
* **Validación de Archivos:** Inspeccionar y reparar mallas en formatos STL u OBJ previa laminación.
* **Optimización de Parámetros:** Ajustar temperaturas, velocidades, patrones de relleno y estructuras de soporte.
* **Calibración de Hardware:** Realizar la nivelación del entorno de trabajo (*bed leveling*) y controlar la adherencia de la primera capa.
* **Evaluación Post-Impresión:** Analizar la precisión dimensional, tolerancia mecánica y calidad superficial.

---

## 🧰 2. Especificaciones de Equipo y Materiales

### 🖥️ Hardware & Software
* **Impresora 3D:** Creality Ender 3 V2 / Prusa i3 MK3S+ *(Ajustar según modelo)*
* **Tecnología:** FDM (*Fused Deposition Modeling*)
* **Laminador (Slicer):** UltiMaker Cura / PrusaSlicer
* **Software CAD:** Blender / Tinkercad / Fusion 360

### 🧵 Material Utilizado
| Propiedad | Especificación Técnica |
| :--- | :--- |
| **Material** | PLA (*Polylactic Acid*) |
| **Diámetro Filamento** | 1.75 mm |
| **Diámetro Boquilla (Nozzle)** | 0.4 mm |
| **Temperatura de Extrusión** | 190°C - 210°C |

---

## ⚙️ 3. Parámetros de Laminado (*Slicer Settings*)

Configuración aplicada para la conversión del modelo en instrucciones de código G:

### 📐 Calidad & Estructura
* **Altura de Capa (*Layer Height*):** 0.2 mm
* **Altura de Primera Capa:** 0.28 mm
* **Ancho de Línea:** 0.4 mm
* **Grosor de Paredes:** 1.2 mm *(3 líneas)*
* **Capas Superior / Inferior:** 4 capas superiores / 4 inferiores

### 🧊 Relleno (*Infill*)
* **Densidad:** 20%
* **Patrón de Relleno:** Cúbico / Grid

### 🌡️ Temperatura & Enfriamiento
* **Temperatura Nozzle:** 200 °C
* **Temperatura Cama (*Bed*):** 60 °C
* **Ventilador de Capa:** 100% *(A partir de la capa 2)*

### ⚡ Velocidades & Adherencia
* **Velocidad de Impresión:** 50 mm/s
* **Velocidad Pared Exterior:** 25 mm/s
* **Velocidad Primera Capa:** 20 mm/s
* **Soportes:** Activados *(Ángulo > 50°, Estructura Tipo Árbol)*
* **Adherencia a la Cama:** Balsa (*Brim*) / Falda (*Skirt*)

---

## 🚀 4. Flujo de Trabajo y Procedimiento

1. **Inspección del Modelo:** Carga del archivo STL, verificación de dimensiones y orientación óptima para minimizar el uso de soportes.
2. **Generación de G-code:** Aplicación de parámetros, simulación capa por capa y exportación del archivo a la tarjeta SD.
3. **Calibración Física:** Limpieza de la plataforma con alcohol isopropílico (IPA) y calibración manual de la cama mediante galga de espesores o papel.
4. **Ejecución y Monitoreo:** Supervisión de la primera capa para asegurar el aplastamiento óptimo (*Z-Offset*) y evitar desprendimientos.

---

## 📊 5. Métricas y Resultados

* **⏱️ Tiempo Estimado:** 1h 45m
* **⏱️ Tiempo Real:** 1h 52m
* **⚖️ Material Consumido:** 24 g
* **📏 Longitud de Filamento:** 8.05 m

---

## 🔍 6. Control de Calidad

> **Primera Capa:** Adherencia uniforme sin presentar sobreextrusión ni líneas separadas.

* **Paredes Exteriores:** Acabado liso, líneas continuas y sin desplazamiento de capas (*layer shifting*).
* **Manejo de Hilado (*Stringing*):** Mínimo, corregido fácilmente en la etapa de limpieza post-impresión.
* **Remoción de Soportes:** Desprendimiento limpio sin comprometer la superficie de la pieza.

---

## 📝 7. Conclusiones

1. La orientación estratégica del modelo redujo la necesidad de soportes en un **20%**, acortando el tiempo total de impresión.
2. Mantener la cama limpia e inspeccionar la velocidad de la primera capa fue determinante para prevenir el pandeo (*warping*).
3. Los parámetros ajustados produjeron un balance ideal entre resistencia mecánica y velocidad de ejecución.
