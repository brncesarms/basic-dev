---
title: "Dart: Switch"
date_created: 2026-08-17
tags:
  - dart
  - condicionais
  - switch
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
