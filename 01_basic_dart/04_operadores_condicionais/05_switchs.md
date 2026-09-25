---
title: "Dart: Switch"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - condicionais
  - switch
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🔀 Dart: Switch

> [!info] A estrutura `switch` avalia uma expressão e executa o bloco do caso correspondente.

---

```dart
void main() {
  final diaDaSemana = 1;

  switch (diaDaSemana) {
    case 0:
      print('Domingo');
      break; // cada 'case' precisa de um ponto de parada
    case 1:
      print('Segunda-feira');
      break;
    default: // equivale ao 'else'
      print('Não identificado');
      break;
  }

  // O mesmo exemplo usando if/else
  if (diaDaSemana == 0) {
    print('Domingo');
  } else if (diaDaSemana == 1) {
    print('Segunda-feira');
  } else {
    print('Não identificado');
  }
}
```

> [!tip] Use `switch` quando houver vários casos fixos e bem definidos; o `if/else` é mais flexível para condições complexas.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Null Safety](../05_trabalhando_com_nulos/01_null_safety.md) — Tratamento de nulos em tempo de compilação.
- [Operadores Condicionais](01_operadores_condicionais.md) — Visão geral de controle de fluxo.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
