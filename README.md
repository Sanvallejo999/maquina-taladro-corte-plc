# Máquina de taladrado y corte automatizada

Automatización de una máquina de taladrado y corte con un **PLC Siemens S7-1200 (CPU 1214C)** programado en **TIA Portal**. La máquina no tenía pantalla, así que se le diseñó una **HMI en una Raspberry Pi** con pantalla táctil y un programa en **Python** que se comunica con el PLC por Ethernet.

Proyecto académico · Ingeniería Electrónica · UCEVA · 2026

[Arrastra aquí la foto de la HMI]

## Qué hace

- Controla la banda transportadora, el taladro y la sierra.
- Trabaja en modo automático o manual.
- Arranca y se detiene desde la pantalla táctil o con los pulsadores del tablero.
- Cuenta las piezas procesadas y permite reiniciar el conteo.
- Muestra cuándo está activo el paro de emergencia.

## HMI

Desde la pantalla táctil el operador:

- Elige el modo automático o manual.
- Da marcha y paro a la máquina.
- Ve el estado de la banda, el taladro y la sierra.
- Lleva el conteo de piezas.
- Ve si la HMI está conectada al PLC.

## Tablero de control

[Arrastra aquí la foto del tablero]

| Componente | Uso |
| --- | --- |
| PLC Siemens S7-1200, CPU 1214C AC/DC/Rly | Control de la máquina |
| Contactores | Arranque de los motores del taladro y la sierra |
| Relés |
| Guardamotor | Protección del motor  |
| Breaker | Protección del circuito |
| Pulsadores y paro de emergencia | Mando físico de la máquina |
| Raspberry Pi V4 con pantalla táctil | HMI |

## Software

- **TIA Portal :** programa del PLC.
- **Python en Thonny:** programa de la HMI en la Raspberry Pi.
- **Comunicación:** Ethernet entre la Raspberry Pi y el PLC, usando.

## Contenido del repositorio

- `plc/`: proyecto de TIA Portal archivado (.zap)
- `hmi/`: código Python de la HMI
- `docs/`: diagramas de conexión



## Autores

- David Santiago Vallejo Rodríguez:  programación del PLC y HMI
