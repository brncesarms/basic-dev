---
title: "Dart: Operadores Condicionais (if / else)"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - condicionais
  - if-else
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🔀 Dart: Operadores Condicionais (`if` / `else`)

> [!info] Estruturas de decisão `if`, `else if` e `else` no Dart.

---

```dart
void main() {
  // Exemplo: é preciso ter 18 anos ou mais para obter habilitação
  final idade = 20;

  if (idade > 18) {
    print('Você PODE fazer habilitação');
  } else if (idade == 18) {
    print('Você PODE fazer habilitação');
  } else {
    print('Ainda não posso fazer habilitação');
  }
}
```

> [!tip] Como `idade > 18` e `idade == 18` levam ao mesmo resultado, o exemplo poderia ser simplificado com `>=`:
> ```dart
> if (idade >= 18) {
>   print('Você PODE fazer habilitação');
> } else {
>   print('Ainda não posso fazer habilitação');
> }
> ```

---

## 🔗 Notas Relacionadas
- [Operadores Relacionais](02_operadores_relacionais.md) — Comparações numéricas e de igualdade.
- [Operadores Lógicos](03_operadores_logicos.md) — Operadores AND, OR e NOT.
- [Operador Ternário](04_ternario.md) — Sintaxe concisa para if/else.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
