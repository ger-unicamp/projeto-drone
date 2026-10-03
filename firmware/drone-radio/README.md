# Rádio do drone

Microcontrolador no drone (a definir), ligado na UART da FC Betaflight.

Faz:
- Recebe comandos pelo rádio.
- Converte para CRSF e envia para a FC.
- Failsafe: sem comando válido por X ms → para de enviar (Betaflight assume).
- Envia telemetria de volta (bateria, estado; depois atitude via MSP).
