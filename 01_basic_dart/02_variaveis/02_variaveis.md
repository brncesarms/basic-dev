---
title: "Dart: Variáveis e Tipos"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - variaveis
  - null-safety
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 📦 Dart: Variáveis e Tipos

> [!info] Guia de variáveis e tipos no Dart, incluindo `int`, `double`, `String`, `bool`, `var` e noções de Null Safety.

---

## Estrutura de criação de uma variável

```dart
void main() {
  // TIPO: 'int' - inteiro, sem casas decimais
  int idade = 34;

  // TIPO: 'double' - contém casas decimais
  double altura = 1.76;

  // TIPO: 'String' - textos
  String nome = 'João';

  // TIPO: 'bool' - valores verdadeiros ou falsos
  bool eHomem = true;
  bool eMulher = false;

  // TIPO: 'var' - o tipo é inferido pelo valor atribuído
  var qualquer = 34;
  var outro = 'texto';

  // EVITE 'Object' e 'dynamic' (tipagem permissiva demais)
  Object objetoQualquer = 1.2; // Object: todas as classes herdam dele
  dynamic dynamicQualquer = 'Oi'; // dynamic: tipagem dinâmica
}
```

## Null Safety em variáveis

```dart
String nomeCompletoSuperior = 'João Silva';
// Variáveis de nível superior NÃO podem ser inicializadas depois,
// ou seja, precisam receber valor já na declaração.

void main() {
  // Com Null Safety, o compilador detecta possíveis acessos a null em tempo de compilação.

  // Antigamente era possível fazer isto, mas hoje é um erro:
  // String nomeCompleto = null;

  // Com '?' garantimos que a variável pode ser nula
  String? nomeCompleto;
  nomeCompleto = 'João Silva';

  // Eu garanto que ela não será nula neste ponto
  print(nomeCompleto!.length);
}
```

> [!note] Referência oficial: <https://dart.dev/language/variables>

---

## 🔗 Notas Relacionadas
- [Modificadores const e final](../03_modificadores/03_const_final.md) — Controle de imutabilidade de variáveis.
- [Função Main](../01_funcao_main/01_funcao_main.md) — Estrutura do método principal.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
