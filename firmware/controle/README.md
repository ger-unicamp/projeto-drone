# Controle

Criar com `pio project init --board esp32dev` (ou pela extensão do VS Code).

Faz:
- Lê joysticks/botões (ADC), calibra centro e limites.
- Monta pacote de comando e envia por ESP-NOW numa taxa fixa.
- Recebe telemetria do drone e repassa ao PC pela USB serial.
- Testes do protocolo rodando no PC: env `native` + Unity (`pio test -e native`).
