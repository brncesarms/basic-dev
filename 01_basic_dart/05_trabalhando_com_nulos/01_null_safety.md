---
title: "Dart: Null Safety"
date_created: 2026-08-17
tags:
  - dart
  - null-safety
---

# ☑️ Dart: Null Safety

> [!info] Como o Dart lida com valores nulos em tempo de compilação.

---

```dart
// Variável de nível superior: precisa ser declarada com '?' se puder ser nula
String? nomeSuperior;

void main() {
  // 1. Checagem de nulo para 'variáveis de nível superior' NÃO funciona como esperado
  // A promoção de tipo não acontece para variáveis de nível superior.
  if (nomeSuperior != null) {
    // nomeSuperior.isEmpty; // não é promovido; seria necessário nomeSuperior!.isEmpty
    print(nomeSuperior!.isEmpty);
  }

  // 2. Criando uma variável local associada à superior
  // Variáveis locais SÃO promovidas após a checagem de null.
  String? nomeLocal = nomeSuperior;
  if (nomeLocal != null) {
    nomeLocal.isEmpty; // OK, promovida para não-nula
  }

  // Trabalhando com nulos
  String nome = '';
  String? nomeNula;

  // Exemplo de checagem de nulo (variável local, é promovida)
  if (nomeNula != null) {
    nomeNula.isEmpty;
  }
}
```

> [!warning] Variáveis de nível superior/top-level não são promovidas a não-nulas pelo tipo. Atribua a uma variável local (ou use `!`) para acessar com segurança após checar `!= null`.
