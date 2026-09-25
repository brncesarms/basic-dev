---
title: "Dart: Operadores Lógicos"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - operadores
  - logicos
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🧠 Dart: Operadores Lógicos

> [!info] Operadores `&&` (e), `||` (ou) e `!` (não) para combinar condições booleanas.

---

```dart
void main() {
  final sexo = 'M';
  final idade = 18;

  // Exemplo '&&' (E): TODAS as condições precisam ser verdadeiras
  if (sexo == 'M' && idade >= 18) {
    print('Pode entrar!');
  } else {
    print('Não pode entrar!');
  }

  // Exemplo '||' (OU): PELO MENOS UMA condição precisa ser verdadeira
  // true  && false = false
  // true  || false = true
  if (sexo == 'M' || idade >= 18) {
    print('Pode entrar!');
  } else {
    print('Não pode entrar!');
  }

  // Exemplo '!' (NÃO): inverte a condição
  if (!(idade >= 18)) {
    print('Menor de 18 anos');
  } else {
    print('Maior ou igual a 18 anos');
  }
}
```

## 🔗 Relacionados

- 🎯 [Basic Dart — Mapa de Conteúdo](../README.md)

---

## 🔗 Notas Relacionadas
- [Operadores Condicionais](01_operadores_condicionais.md) — Controle de fluxo de decisão.
- [Operador Ternário](04_ternario.md) — Expressão condicional ternária.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
