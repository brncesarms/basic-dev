---
title: "Dart: Listas e Null Safety"
date_created: 2026-08-17
tags:
  - dart
  - listas
  - null-safety
---

# ☑️ Dart: Listas e Null Safety

> [!info] Diferenças entre listas que podem ser nulas e listas que aceitam itens nulos.

---

```dart
void main() {
  // '?' = Nullable (aceita nulo)

  // Exemplo 1:
  // NÃO aceita nulos
  var nomes = <String>[]; // itens não podem ser null

  // Minha LISTA pode ser nula (mas os itens não)
  List<String>? nomesNulos;

  // Minha lista NÃO pode ser nula, mas aceita itens nulos
  List<String?> nomesInternosNulos = [null, 'João'];

  // Minha LISTA pode ser nula E também aceita itens nulos
  List<String?>? nomesInternosNulos2 = null;
  List<String?>? nomesInternosNulos3 = [null, 'João'];
}
```

> [!tip] `List<Type?>` aceita itens nulos; `List<Type>?` é uma lista que pode ser nula; `List<Type?>?` combina ambos.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)
