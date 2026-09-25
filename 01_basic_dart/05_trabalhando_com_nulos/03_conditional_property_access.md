---
title: "Dart: Conditional Property Access (?.)"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - null-safety
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🔍 Dart: Conditional Property Access (`?.`)

> [!info] O operador `?.` acessa uma propriedade/método apenas se a variável não for nula, evitando erros de null.

---

```dart
String? nomeCompleto;

void main() {
  // Verificação convencional com if
  if (nomeCompleto != null) {
    print(nomeCompleto!.toUpperCase());
  } else {
    print('Nome não preenchido');
  }

  // Utilizando Conditional Property Access (?.)
  // Só executa se a variável não for nula; se for nula, usa o fallback do '??'
  print(nomeCompleto?.toUpperCase() ?? 'Nome não preenchido');
}
```

> [!tip] `nomeCompleto?.toUpperCase()` retorna `null` se `nomeCompleto` for nulo; combinado com `??`, oferecemos um valor padrão em uma única expressão.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Listas e Null Safety](../06_listas/02_listas_nullsafety.md) — Coleções seguras contra nulos.
- [Operador Null-Aware](02_null_aware_operator.md) — Operador de coalescência nula.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
