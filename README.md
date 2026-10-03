# Drone GER

Quadricóptero do grupo de robótica. Voo por **Betaflight**. Microcontrolador e rádio do link ainda **a definir**. O que construímos: controle, link de rádio, estação no PC e, depois, vídeo + visão computacional.

## Arquitetura

```
[Controle (MCU)] --rádio--> [MCU no drone] --CRSF--> [FC Betaflight]
       |  <---- telemetria ----
      USB
       v
[PC: estação Python]  <---- vídeo Wi-Fi ---- [Raspberry Pi + câmera]   (futuro)
```

## Estrutura

| pasta                  | o quê                                                   |
|------------------------|---------------------------------------------------------|
| `docs/estudo/`         | tópicos de estudo e referências                         |
| `protocol/`            | especificação do nosso protocolo de pacotes             |
| `firmware/controle/`   | PlatformIO: controle (joysticks → rádio, ponte p/ PC)   |
| `firmware/drone-radio/`| PlatformIO: rádio no drone (rádio → CRSF p/ Betaflight)  |
| `ground/`              | Python: estação de solo (telemetria, depois vídeo)      |
| `sim/`                 | Python: simulador do link, para testar sem hardware     |

Código compartilhado entre os projetos PlatformIO: `firmware/lib/` (via `lib_extra_dirs`).

## Fases

0. Setup: PlatformIO instalado, microcontrolador e rádio escolhidos, blink na placa, fluxo de Git combinado.
1. Protocolo no papel (`protocol/`) + simulador do link (`sim/`) — sem hardware.
2. Link real: controle e drone trocando pacotes pelo rádio; medir latência, perda, alcance. Failsafe.
3. Controle físico: joysticks, calibração.
4. Bancada: MCU do drone → CRSF → Betaflight, motores **sem hélice**.
5. Primeiro voo, área aberta, failsafe testado antes.
6. Vídeo: Pi + câmera → PC; OpenCV.

## Fluxo de Git

`main` sempre funcionando. Uma branch por tarefa, PR com revisão de outra pessoa.
