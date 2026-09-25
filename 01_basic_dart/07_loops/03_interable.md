---
title: "Dart: Iterables (where, takeWhile, skipWhile, map)"
date_created: 2026-08-17
tags:
  - dart
  - iterable
  - loops
---

# 🔄 Dart: Iterables (`where`, `takeWhile`, `skipWhile`, `map`)

> [!info] Métodos funcionais para transformar e filtrar coleções no Dart.

---

## Exemplo base

```dart
void main() {
  var numeros = List.generate(10, (index) => index);

  // Equivalente com for + continue
  for (var i = 0; i < numeros.length; i++) {
    if (i == 5) {
      continue;
    }
    print(numeros[i]);
  }

  // O mesmo usando 'iterable': 'where' é um método de Iterable
  numeros
      .where((numero) => numero != 5)
      .forEach((numero) => print(numero));

  // 'takeWhile': pega elementos enquanto a condição for verdadeira
  final numerosAte5 = numeros.takeWhile((numero) => numero < 6);
  print(numerosAte5); // (0, 1, 2, 3, 4, 5)

  final numerosAte6 = numeros
      .takeWhile((numero) => numero < 7)
      .where((numero) => numero != 5)
      .toList();
  print(numerosAte6);

  // 'skipWhile': pula elementos enquanto a condição for verdadeira
  final numerosRemoverAte5 = numeros
      .skipWhile((numero) => numero < 6)
      .toList();
  print(numerosRemoverAte5); // [6, 7, 8, 9]
}
```

## `map`

```dart
void main() {
  var numeros = List.generate(10, (index) => index);

  // 'map' transforma (mapeia) cada elemento
  // ex: lista de inteiros -> lista de strings
  var numeroStrList = numeros.map((numero) {
    return 'número é $numero';
  }).toList();
  print(numeroStrList);
}
```

> [!tip] `map` transforma cada elemento; `where` filtra; `takeWhile`/`skipWhile` controlam até onde considerar a coleção.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)
