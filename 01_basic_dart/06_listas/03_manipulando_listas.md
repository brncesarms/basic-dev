---
title: "Dart: Manipulando Listas"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - listas
  - manipulacao
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🔧 Dart: Manipulando Listas

> [!info] Operações comuns de adição, remoção, inserção e geração de listas no Dart.

---

```dart
void main() {
  final numeros = [1, 2, 3];
  final nomes = ['João', 'Maria', 'Ana'];

  // Adicionando um item à lista
  numeros.add(4);
  nomes.add('Ana Clara');

  // Índice   0      1       2
  // final nomes = ['João', 'Maria', 'Ana'];
  // Acessando um item pelo índice
  print(nomes[1]); // 'Maria'

  // 'Adicionando' um item na posição 0
  nomes.insert(0, 'José'); // ['José', 'João', 'Maria', 'Ana', 'Ana Clara'];

  // 'Removendo' um item da lista
  nomes.remove('José'); // ['João', 'Maria', 'Ana', 'Ana Clara'];

  // 'Removendo' através de uma função (removeWhere)
  // Percorre a lista e remove os itens para os quais a condição retornar true
  nomes.removeWhere((nome) {
    if (nome == 'João') {
      return true;
    } else {
      return false;
    }
  });

  // 'Imprimindo' o primeiro e o último item da lista
  print(nomes.first);
  print(nomes.last);

  // Gerando uma lista
  final numerosGerados = List.generate(10, (index) => index + 1);
  print(numerosGerados); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

  // Adicionando uma lista a outra (operador spread '...')
  var listaNumerosSpread1 = [4, 5, 6];
  var listaNumerosSpread2 = [1, 2, 3, ...listaNumerosSpread1];
  print(listaNumerosSpread2); // [1, 2, 3, 4, 5, 6]
}
```

> [!tip] O operador `...` (spread) expande os elementos de uma lista dentro de outra.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Loops for e for-in](../07_loops/01_for_forin.md) — Iteração sobre coleções.
- [Iterables Funcionais](../07_loops/03_interable.md) — Transformações com where, map e takeWhile.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
