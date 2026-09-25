---
title: "Dart: Listas"
date_created: 2026-08-17
tags:
  - dart
  - listas
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
