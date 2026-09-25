---
title: "Dart: Loops (while e do-while)"
date_created: 2026-08-17
tags:
  - dart
  - loops
  - while
---

# 🔁 Dart: Loops `while` e `do-while`

> [!info] Estruturas de repetição baseadas em condição. Enquanto o `while` checa antes de executar, o `do-while` executa pelo menos uma vez.

---

```dart
void main() {
  // O 'while' só tem a condição (não tem início/incremento explícitos como o for)

  // while convencional
  var numero = 0;
  while (numero < 10) {
    print(numero);
    numero++;
  }

  // do-while
  // Mesmo que a condição seja falsa, ele executa pelo menos uma vez
  var indice = 0;
  do {
    print(indice);
    indice++;
  } while (indice < 5);
}
```

> [!tip] Use `do-while` quando o bloco deve rodar ao menos uma vez antes de avaliar a condição.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)
