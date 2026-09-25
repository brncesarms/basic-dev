---
title: "Dart: Manipulando Strings"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - strings
  - manipulacao
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 📝 Dart: Manipulando Strings

> [!info] Operações comuns de manipulação de textos no Dart: substrings, validação, caso, divisão e interpolação.

---

```dart
void main() {
  final nome = 'João Silva';

  var subStringNome1 = nome.substring(5);
  print(subStringNome1); // 'Silva'

  var subStringNome2 = nome.substring(0, 5);
  print(subStringNome2); // 'João '

  var subStringNome3 = nome.startsWith('Joã');
  print(subStringNome3); // true

  var subStringNome4 = nome.contains('Silva');
  print(subStringNome4); // true

  var subStringNome5 = nome.toLowerCase();
  print(subStringNome5); // 'joão silva'

  var subStringNome6 = nome.toUpperCase();
  print(subStringNome6); // 'JOÃO SILVA'
}
```

## Conhecendo o `.split`

```dart
void main() {
  var paciente = 'João Silva|34|Especialista Dart e Flutter|SP';
  var dadosPaciente = paciente.split('|');

  print(dadosPaciente);        // [João Silva, 34, Especialista Dart e Flutter, SP]
  print(dadosPaciente[0]);     // João Silva
  print(dadosPaciente[1]);     // 34
  print(dadosPaciente[2]);     // Especialista Dart e Flutter
  print(dadosPaciente[3]);     // SP

  for (var dados in dadosPaciente) {
    print(dados);
  }

  // ou
  dadosPaciente.forEach((dados) => print(dados));

  // ou com uma lista de pacientes
  var pacientes = [
    'João Silva|34|Especialista Dart e Flutter|SP',
    'Maria Santos|7|Estudante|SP',
    'Ana Souza|36|Esteticista|SP',
  ];

  // varrendo toda a lista de pacientes
  for (var paciente in pacientes) {
    var dados = paciente.split('|');
    var nomeCompleto = dados[0];
    var nomes = nomeCompleto.split(' ');
    print(nomes.last); // imprimindo o último nome
  }
}
```

## Interpolação

```dart
void main() {
  var primeiroNome = 'Ana';
  var segundoNome = 'Souza';
  var saudacao = 'Olá $primeiroNome $segundoNome!';
  print(saudacao); // 'Olá Ana Souza!'

  // Chamar um método exige envolver a expressão entre {}
  print('Olá ${primeiroNome.toUpperCase()}');
}
```

> [!note] Referência oficial: <https://api.flutter.dev/flutter/dart-core/String/substring.html>

---

## 🔗 Notas Relacionadas
- [Manipulando Números](02_manipulando_numeros.md) — Conversão e arredondamento numérico.
- [Mapa de Conteúdo Dart](../README.md) — Índice de fundamentos da linguagem.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
