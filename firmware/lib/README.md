# Bibliotecas compartilhadas

Cada pasta aqui é uma biblioteca usada por `controle/` e `drone-radio/` (via `lib_extra_dirs = ../lib`).

Formato esperado pelo PlatformIO:

```
lib/
└── nome_da_lib/
    └── src/
        ├── nome_da_lib.h
        └── nome_da_lib.cpp
```

Libs que não dependem da placa nem do framework (ex: Arduino) podem ser testadas no PC com `pio test -e native`.
