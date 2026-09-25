---
title: "Dart: Listas"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - listas
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 📋 Dart: Listas

> [!info] A `List` é a representação de uma coleção ordenada de elementos no Dart.

---

```dart
void main() {
  // Estrutura básica de uma lista

  // Exemplo 1: declare a tipagem em listas vazias
  List<int> listNumeros = <int>[];
  var listNomes = <String>[];

  // Exemplo 2: listas com valores iniciais
  var listNumeros2 = [1, 2, 3];
  var nomes = ['João', 'Maria', 'Ana'];
}
```

> [!tip] Sempre declare o tipo das listas vazias (`<int>[]`, `<String>[]`) para manter a segurança de tipos.

---

## 🔗 Notas Relacionadas
- [Listas e Null Safety](02_listas_nullsafety.md) — Listas nuláveis vs itens nuláveis.
- [Manipulando Listas](03_manipulando_listas.md) — Métodos de adição, remoção e ordenação.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
