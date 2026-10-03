# Controle

Placa a definir. Depois de escolher, adicionar o env dela no `platformio.ini` (ver comentário lá).

Faz:
- Lê joysticks/botões (ADC), calibra centro e limites.
- Monta pacote de comando e envia pelo rádio numa taxa fixa.
- Recebe telemetria do drone e repassa ao PC pela USB serial.
- Testes do protocolo rodando no PC: env `native` + Unity (`pio test -e native`).
