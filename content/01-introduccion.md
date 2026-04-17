---
title: "1. Introducción"
---


Un osciloscopio digital es un instrumento que permite visualizar señales eléctricas en el dominio del tiempo, mostrando su forma de onda y permitiendo medir parámetros como amplitud, frecuencia, periodo y nivel de continua. En sistemas basados en FPGA, su implementación es especialmente interesante porque integra adquisición de datos, procesamiento digital y generación de vídeo en un mismo sistema.

## Componentes principales de un osciloscopio digital en FPGA

- **Adquisición de señal (ADC):** La señal analógica de entrada se convierte a formato digital mediante un conversor analógico-digital. La frecuencia de muestreo y la resolución del ADC determinan la fidelidad de la señal capturada.
- **Control de disparo (Trigger):** Define el instante de inicio de la captura o visualización según una condición (por ejemplo, cruce por nivel y flanco), permitiendo estabilizar la forma de onda en pantalla.
- **Memoria de captura (Buffer):** Almacena temporalmente las muestras adquiridas para su posterior lectura y visualización.
- **Procesamiento y escalado digital:** Transforma las muestras capturadas para adaptarlas a las escalas temporal y vertical de la pantalla.
- **Generación de vídeo:** Convierte las muestras procesadas en píxeles para representar la forma de onda.

## Aplicación en FPGA

En una FPGA como la **Altera Cyclone V**, estos bloques pueden implementarse como módulos hardware que trabajan de forma paralela para capturar, procesar y visualizar señales en tiempo real, permitiendo construir un osciloscopio funcional con fines didácticos y de experimentación.

## Qué trabajaréis en este proyecto

Con este diseño reforzaréis, desde el punto de vista de **diseño con HDL**:

- Diseño de sistemas de **adquisición de datos** en tiempo real.
- Uso de **memorias embebidas** como buffers de captura.
- Implementación de lógica de **trigger**.
- Implementación de **escalado vertical y horizontal** de señales.
- Integración de módulos mediante **interfaces de streaming (Avalon-ST)** y **Memory Mapped (Avalon-MM)**.

Desde el punto de vista de **verificación** trabajaréis con:

- **Simulación HDL** (ModelSim/QuestaSim).
- Verificación física mediante **SignalTap**.
- Verificación del sistema completo utilizando un **generador de señales externo**. En este proyecto utilizaremos una **RedPitaya** como generador de señales para alimentar la entrada del osciloscopio implementado en la FPGA.
