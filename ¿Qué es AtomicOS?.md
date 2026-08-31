# Atomic OS

AtomicOS es un sistema operativo para ejecutarse directamente en el microcontrolador (Baremetal System). El sistema se debe ejecutar sobre una placa Raspberry PI Pico 2040 o derivados que posean un microprocesador ARM Cortex M0+.

**Problema**
Aprender de forma lúdica el desarrollo a bajo nivel en microcontroladores.

**Objetivo:** El sistema operativo se desarrolla para fines educativos, como el aprendizaje de como funciona el sistema de arranque de un sistema operativo, la gestión de multitasking a través de un scheduler, y la comunicación con un modulo de pantalla para la interfaz de comunicación cliente<->hardware además de la estructuración modular del sistema para un desarrollo progresivo y organizado. También se realiza para aprender mejor el funcionamiento del microcontrolador a bajo nivel.

**¿Cómo se va a desarrollar?**
Se desarrollará utilizando meramente ensamblador ARMv6 M0+, se desarrollará bajo una arquitectura modular donde cada módulo se compila y se enlaza por separado utilizando la herramienta Make para construir un sistema de compilación que se adapte a cada módulo.

## Características del Hardware
Se utilizará una tarjeta de desarrollo basada en el microcontrolador Raspberry Pi RP2040, configurada externamente en formato compatible con Raspberry Pi Pico con interfaz USB Tipo-C.
![[Pasted image 20260830163717.png|196]]   ![[Pasted image 20260830164330.png|198]]

**Especificaciones Técnicas Principales**
- **Microcontrolador:** Raspberry Pi RP2040 con arquitectura Dual-Core ARM Cortex-M0+ a una frecuencia de reloj de hasta 133 MHz.
- **Interfaz de Comunicación/Alimentación:** Conector USB Tipo-C para suministro eléctrico, transferencia de datos y programación mediante protocolo UF2.
- **Memoria Interna:** 264 KB de SRAM multipropósito integrada en chip.
- **Memoria Flash Externa:** De 4 MB a 16 MB (almacenamiento ampliado mediante chip SPI Flash, superando los 2 MB del modelo oficial).
- **Voltaje de Operación:** Lógica a 3.3 V con regulador lineal interno (acepta alimentación externa por USB a 5 V o rango extendido mediante pin VSYS de 1.8 V a 5.5 V).
**Periféricos de Hardware e Entradas/Salidas**
- **Pines GPIO:** 26 pines multifunción configurables por software.
- **Entradas Analógicas (ADC):** 3 canales con resolución de 12 bits (pines GP26_A0, GP27_A1 y GP28_A2) más un canal interno para sensor de temperatura.
- **Puertos Serie Dedicados:** 2 × SPI, 2 × I2C y 2 × UART asignables a múltiples pines.
- **Modulación por Ancho de Pulso (PWM):** 16 canales independientes.
- **Bloque PIO (Programmable I/O):** 8 máquinas de estado programables para emular protocolos de comunicación o hardware personalizado a alta velocidad.
**Gestión de Alimentación y Control**
- **VBUS:** Entrada/salida directa de 5 V provista por el conector USB-C.
- **VSYS:** Pin de alimentación principal de la tarjeta para baterías o fuentes externas.
- **3V3_EN:** Pin de habilitación para desactivar el regulador de voltaje interno de 3.3 V.
- **RUN:** Pin de reinicio (_Reset_) del microcontrolador mediante conexión a masa (GND).
- **Interfaz SWD:** Pines dedicados (SWDIO, SWCLK, GND) en la parte inferior para depuración por hardware (_hardware debugging_).

**Compatibilidad de Software**
Plena compatibilidad con los entornos oficiales de desarrollo: SDK oficial en C/C++, MicroPython, CircuitPython y soporte a través de Arduino IDE.

## Enlaces y Documentación

### Raspberry Pi Pico
https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html#pico1
### MicroPython
https://www.raspberrypi.com/documentation/microcontrollers/micropython.html#what-is-micropython
### **The C/C++ SDK**
https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html#sdk-setup
### Raspberry Pi Pico SDK
https://www.raspberrypi.com/documentation/pico-sdk/index_doxygen.html#raspberry-pi-pico-sdk
### Cortex-M0+ARM Processor Instruction Set & ARM Assembly Basics
https://www.scribd.com/document/940289019/ppt-04
















