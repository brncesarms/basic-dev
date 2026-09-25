---
title: "Dart: Operador Ternário"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - operadores
  - ternario
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# ❓ Dart: Operador Ternário

> [!info] O operador ternário é uma forma resumida do `if/else` em uma única expressão.

---

```dart
void main() {
  final idade = 20;

  // Usando operador ternário: (condição) ? valorSeVerdadeiro : valorSeFalso
  final eMaiorDeIdade = idade >= 18 ? true : false;

  // O equivalente usando if/else:
  bool eMaiorDeIdade2;
  if (idade >= 18) {
    eMaiorDeIdade2 = true;
  } else {
    eMaiorDeIdade2 = false;
  }

  print('É maior de idade? $eMaiorDeIdade');
}
```

> [!tip] Como a condição `idade >= 18` já retorna `bool`, o ternário poderia ser simplificado:
> ```dart
> final eMaiorDeIdade = idade >= 18;
> ```

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Estrutura Switch](05_switchs.md) — Decisões múltiplas por padrão.
- [Operadores Condicionais](01_operadores_condicionais.md) — Estrutura tradicional if/else.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
