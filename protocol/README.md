# Protocolo

Escrever aqui `spec.md`: a fonte da verdade dos pacotes trocados entre controle, drone e PC. Firmware (C++) e estação (Python) implementam a partir dela.

Decidir e documentar:
- Quais mensagens existem (comando, telemetria, ...) e seus campos, tipos e unidades.
- Formato do frame: como achar início/fim num stream serial, tamanho, versão.
- Detecção de erro (CRC? qual?) e de perda (número de sequência?).
- Endianness e por que não mandar `struct` crua.
- Taxas de envio e regra de failsafe (quanto tempo sem pacote = perda de link).
- Vetores de teste: pacotes de exemplo em bytes, usados pelos testes dos dois lados.
