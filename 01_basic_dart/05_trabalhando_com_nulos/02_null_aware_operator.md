---
title: "Dart: Operador Null-Aware (??)"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - null-safety
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# ➕ Dart: Operador Null-Aware (`??`)

> [!info] O operador `??` retorna o valor do lado direito caso o lado esquerdo seja nulo.

---

```dart
// Variável de nível superior
String? nome;

void main() {
  var sobrenome = 'Silva';

  // se 'nome' for nulo, utiliza 'João'
  var nomeCompleto = (nome ?? 'João') + sobrenome;
  print(nomeCompleto); // JoãoSilva (pois 'nome' é nulo)
}
```

> [!tip] Use `??` para fornecer um valor padrão (fallback) quando a variável puder ser nula.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Null Safety no Dart](01_null_safety.md) — Conceito essencial de nulabilidade.
- [Acesso Condicional a Propriedades](03_conditional_property_access.md) — Navegação com operador ?..
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
