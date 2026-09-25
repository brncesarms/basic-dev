---
title: "Dart: Manipulando Números"
date_created: 2026-08-17
tags:
  - dart
  - numeros
  - manipulacao
---

# 🔢 Dart: Manipulando Números

> [!info] Operações comuns de arredondamento, validação e conversão de números no Dart.

---

```dart
void main() {
  final idade = 30;
  print('Sua idade é $idade');

  // Verifica se o valor é negativo
  final valor = -20;
  if (valor.isNegative) {
    print(valor);
  }

  // Arredondamento
  final valorDouble = 10.65;
  print(valorDouble.round());         // arredonda: 11
  print(valorDouble.roundToDouble()); // arredonda mantendo double: 11.0

  // Conversão de texto para número
  final valorString = '30';
  final valorInt = int.parse(valorString);
  print(valorInt);

  // Formatando casas decimais
  final precoCamiseta = 30.27876;
  print(precoCamiseta.toStringAsFixed(2)); // imprime até duas casas: 30.28
}
```

> [!tip] Use `int.parse`/`double.parse` para converter strings em números, e `toStringAsFixed` para limitar casas decimais na exibição.

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)
