---
title: "Dart: Operador Null-Aware (??)"
date_created: 2026-08-17
tags:
  - dart
  - null-safety
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
