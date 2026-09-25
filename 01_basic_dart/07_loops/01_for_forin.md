---
title: "Dart: Loops (for e for-in)"
date_created: 2026-08-17
tags:
  - dart
  - loops
  - for
---

# 🔁 Dart: Loops `for` e `for-in`

> [!info] Estruturas de repetição para percorrer listas, com controle de iteração, `break` e `continue`.

---

## `for` convencional

> A estrutura é: `início`; `condição`; `incremento`.

```dart
void main() {
  var numeros = List.generate(10, (index) => index);
  var nomes = ['João', 'Maria', 'Ana'];

  // Imprimindo os números pelo índice
  for (var i = 0; i < numeros.length; i++) {
    print(numeros[i]);
  }

  // Imprimindo nomes com for convencional
  for (var i = 0; i < nomes.length; i++) {
    print(nomes[i]);
  }

  // For com 'break' (para a iteração ao encontrar 'Maria')
  for (var i = 0; i < nomes.length; i++) {
    print(nomes[i]);
    if (nomes[i] == 'Maria') {
      break;
    }
  }

  // For com 'continue' (pula a iteração i == 1)
  for (var i = 0; i < nomes.length; i++) {
    if (i == 1) {
      continue;
    }
    print(nomes[i]);
  }
}
```

## `for-in`

```dart
void main() {
  var numeros = List.generate(10, (index) => index);
  var nomes = ['João', 'Maria', 'Ana'];

  // Imprimindo números com for-in
  for (var numero in numeros) {
    print(numero);
  }

  // Imprimindo nomes com for-in e 'break'
  for (var nome in nomes) {
    print(nome);
    if (nome == 'Maria') {
      break;
    }
  }
}
```

> [!tip] O `for-in` percorre os elementos diretamente (sem índice), sendo mais legível quando o índice não é necessário.
