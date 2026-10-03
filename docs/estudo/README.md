# Estudo

Tópicos em ordem sugerida. Cada um vira uma issue de estudo; anotações de quem estudou vão em `docs/estudo/<topico>.md`.

## 1. Ferramentas
- PlatformIO: projetos, `platformio.ini`, envs, bibliotecas, `lib_extra_dirs`, unit testing (`native` + Unity).
- Git em time: branches, PR, revisão, conflitos.
- Refs: [PlatformIO docs](https://docs.platformio.org) · [Pro Git](https://git-scm.com/book/pt-br/v2)

## 2. Embarcados básicos
- GPIO, ADC, timers, interrupções, `millis()` vs `delay()`, loop não bloqueante.
- UART, I2C, SPI: diferenças, quando usar cada.
- Refs: [Arduino-ESP32 docs](https://docs.espressif.com/projects/arduino-esp32/en/latest/) · [SparkFun: Serial](https://learn.sparkfun.com/tutorials/serial-communication), [I2C](https://learn.sparkfun.com/tutorials/i2c), [SPI](https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi) · livro *Making Embedded Systems* (Elecia White)

## 3. Rádio 2.4 GHz e ESP-NOW
- Faixa 2.4 GHz, canais Wi-Fi, interferência, RSSI, alcance, antenas.
- ESP-NOW: pareamento, broadcast vs unicast, limite de payload, callbacks, criptografia.
- Comparar alternativas: nRF24L01, ExpressLRS, LoRa (por que não usamos).
- Refs: [ESP-IDF: ESP-NOW](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_now.html) · [Random Nerd Tutorials: ESP-NOW](https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/) · [ExpressLRS docs](https://www.expresslrs.org)

## 4. Protocolos binários
- Framing (byte de sincronismo, COBS), endianness, serialização sem `struct` crua.
- Detecção de erro: checksum vs CRC; número de sequência; failsafe/timeout.
- Ver como outros fazem: CRSF, MAVLink, MSP.
- Refs: *A Painless Guide to CRC Error Detection Algorithms* (Ross Williams) · [Catálogo de CRCs](https://reveng.sourceforge.io/crc-catalogue/) · [CRSF spec (crsf-wg)](https://github.com/crsf-wg/crsf/wiki) · [MAVLink: serialização](https://mavlink.io/en/guide/serialization.html) · [Python `struct`](https://docs.python.org/3/library/struct.html) · [Python sockets HOWTO](https://docs.python.org/3/howto/sockets.html)

## 5. Drone e Betaflight
- Partes: frame, motores BLDC (KV), ESC, hélices, FC, PDB; protocolos ESC (DShot).
- LiPo: células, C-rating, carga balanceada, armazenamento — **segurança**.
- Betaflight: Configurator, portas/UART, receptor serial CRSF, modos, failsafe, arming, PID tuning básico.
- Refs: [Betaflight docs](https://betaflight.com/docs/wiki) · [Oscar Liang](https://oscarliang.com) (guias de montagem, LiPo, Betaflight) · canal Joshua Bardwell (YouTube)

## 6. Controle (entender o que o Betaflight faz)
- PID, controle de taxa (acro) vs ângulo, mixer quad X, IMU (giro/acelerômetro), filtros.
- Refs: série *Drone Simulation and Control* e *Understanding PID Control* — MATLAB Tech Talks (Brian Douglas, YouTube)

## 7. Vídeo e visão (fase futura)
- Câmera no Raspberry Pi, codecs (MJPEG, H.264), streaming UDP/RTSP, latência.
- OpenCV em Python; integração com o drone (MSP do Betaflight; para autonomia avaliar INAV/ArduPilot).
- Refs: [Raspberry Pi camera docs](https://www.raspberrypi.com/documentation/computers/camera_software.html) · [GStreamer tutorials](https://gstreamer.freedesktop.org/documentation/tutorials/) · [OpenCV-Python tutorials](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html) · [ArduPilot Copter](https://ardupilot.org/copter/) · [INAV](https://github.com/iNavFlight/inav)
