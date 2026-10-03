# Rádio do drone

ESP32 no drone, ligado na UART da FC Betaflight.

Faz:
- Recebe comandos por ESP-NOW.
- Converte para CRSF e envia para a FC.
- Failsafe: sem comando válido por X ms → para de enviar (Betaflight assume).
- Envia telemetria de volta (bateria, estado; depois atitude via MSP).
