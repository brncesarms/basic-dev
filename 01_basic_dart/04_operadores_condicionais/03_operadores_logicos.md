---
title: "Dart: Operadores Lógicos"
date_created: 2026-08-17
tags:
  - dart
  - operadores
  - logicos
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
