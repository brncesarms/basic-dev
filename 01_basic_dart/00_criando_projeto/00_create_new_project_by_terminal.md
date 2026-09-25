---
title: "Dart: Criar um Novo Projeto pelo Terminal"
date_created: 2026-08-17
tags:
  - dart
  - flutter
  - projeto
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
