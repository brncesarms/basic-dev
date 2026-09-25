---
title: "Dart: Operadores Condicionais (if / else)"
date_created: 2026-08-17
tags:
  - dart
  - condicionais
  - if-else
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
