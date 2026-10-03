# Simulador do link

Objetivo: desenvolver protocolo, failsafe e estação antes do hardware chegar.

Fazer:
- Drone falso e controle falso como processos separados, trocando pacotes por UDP local.
- Controle falso repassa telemetria à estação (como a USB serial faria).
- Canal "ruim" configurável: perda, atraso, bytes corrompidos.
- Verificar: estação detecta perda; drone entra em failsafe quando o link cai.

Sem física por enquanto — o voo fica com o Betaflight.
