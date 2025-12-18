# Proyecto: Control Bidireccional UART (STM32F10x)

## Descripción General

Este proyecto implementa la lógica principal para un sistema de control bidireccional simple utilizando el protocolo UART en un microcontrolador STM32F10x. El dispositivo actúa simultáneamente como transmisor y receptor.

* **Transmisión:** Lee el estado de dos botones (B0 y B1) y envía un código binario a través del pin TX para indicar qué botón(es) ha(n) sido presionado(s).
* **Recepción:** Recibe un código binario a través del pin RX (generalmente de otro dispositivo idéntico) y controla el estado de dos LEDs (LED12 y LED13) en función del código recibido.

El objetivo es lograr un sistema donde la presión de un botón en un dispositivo controle el LED correspondiente en el otro dispositivo, y viceversa.



## Módulos y Periféricos Utilizados

| Módulo/Periférico | Configuración | Propósito |
| :---------------- | :------------ | :-------- |
| **Clock (CLK)** | HSI (High-Speed Internal) | Configuración inicial del reloj del sistema. |
| **USART/UART** | Pines de GPIO (TX/RX) | Comunicación serial asíncrona. |
| **GPIO Port B** | Pines B0 y B1 | Entradas para **Botones** (Input pull-down). |
| **GPIO Port B** | Pines B12 y B13 | Salidas para **LEDs** (Output push-pull 50MHz). |



## Licencia

Este proyecto está licenciado bajo la Licencia **MIT**.

Consulte el archivo [LICENSE](LICENSE) para obtener los detalles completos.