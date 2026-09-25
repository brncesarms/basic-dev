---
title: "Dart: Modificadores const e final"
date_created: 2026-08-17
tags:
  - dart
  - modificadores
  - const
  - final
---

# 🔒 Dart: Modificadores `const` e `final`

> [!info] Modificadores que controlam a imutabilidade (se uma variável pode ou não ser alterada).

---

## `final`

```dart
void main() {
  final nome;             // pode ser declarada sem valor
  nome = 'João';          // primeira atribuição: OK
  // nome = 'José';       // ERRO! não pode ser alterado depois

  final nome2 = nome;     // CERTO! pode copiar o valor de outra variável
  // Variável 'final': não pode ser alterada após inicializada (imutável)
  // É definida em tempo de execução (Runtime)
}
```

## `const`

```dart
void main() {
  const nome = 'Maria';
  // nome = 'Ana';        // ERRO! não pode ser alterada

  // const nome2 = nome;  // ERRO! não pode receber valor de outra variável
  // Variável 'const': não pode ser alterada após inicializada (imutável)
  // É definida em tempo de compilação (Compile-Time)
  // 'const' exige valores conhecidos no momento da compilação
}
```

> [!tip] Regra prática: use `const` quando o valor for fixo em tempo de compilação; use `final` quando for definido uma vez em tempo de execução.
