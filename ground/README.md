# Estação de solo (Python)

Faz:
- Lê frames da serial (controle real) ou UDP (simulador) — mesma interface para os dois.
- Mostra telemetria, conta pacotes perdidos, avisa perda de link.
- Testes com `pytest` usando os vetores de `protocol/`.
- Futuro: receber vídeo e rodar visão (OpenCV).
