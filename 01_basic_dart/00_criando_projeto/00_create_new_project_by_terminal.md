---
title: "Dart: Criar um Novo Projeto pelo Terminal"
date_created: 2026-08-17
tags:
  - publico
  - dart
  - flutter
  - projeto
author: "Bruno César"
privacy: public
last_modified: 2026-09-25
---
# 🚀 Criar um Novo Projeto pelo Terminal

> [!info] Comandos para criar um projeto Dart ou Flutter a partir do terminal.

---

## 1. Criar um projeto Dart

```bash
dart create -t console-full nome_do_projeto
```

```bash
cd nome_do_projeto
```

```bash
code .
```

## 2. Criar um projeto Flutter

```bash
flutter create --project-name nome_projeto --platforms android,web --org br.com.seuprojeto ./nome_projeto
```

```bash
cd nome_projeto
```

```bash
code .
```

> [!tip] Personalize `--org` com o domínio reverso da sua organização (ex: `br.com.empresa`).

---

## 🔗 Notas Relacionadas
- [Função Main](../01_funcao_main/01_funcao_main.md) — Ponto de entrada de qualquer aplicação Dart.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos da linguagem.
- [Mapa de Conteúdo Dart](../README.md) — Índice completo dos fundamentos de Dart.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — MOC de Flutter e Dart.
