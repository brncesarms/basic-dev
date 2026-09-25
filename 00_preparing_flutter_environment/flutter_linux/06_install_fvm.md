---
title: "Flutter (Linux): Instalação e Uso do FVM (Flutter Version Management)"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - fvm
  - versionamento
---

# 🎛️ Flutter (Linux): Instalação e Uso do FVM

> [!info] Instalação e operação do FVM (Flutter Version Management) para gerenciar versões distintas do SDK do Flutter por projeto sem conflitos.

---

## 1. Instalação Global do FVM via Dart Pub

```bash
# Ativar o pacote globalmente
dart pub global activate fvm
```

Certifique-se de que o diretório `$HOME/.pub-cache/bin` esteja no seu `PATH` (definido no `~/.bashrc`).

---

## 2. Comandos Operacionais Mais Usados

```bash
# Instalar uma versão específica do Flutter
fvm install 3.24.0

# Instalar a versão estável mais recente
fvm install stable

# Definir a versão do Flutter para o projeto atual
cd /caminho/do/seu/projeto
fvm use 3.24.0

# Executar comandos do flutter via FVM
fvm flutter pub get
fvm flutter run
```

---

## 🔗 Notas Relacionadas
- [Configuração de Variáveis no .bashrc](01_bashrc_config.md) — Export do .pub-cache/bin.
- [Instalação do Flutter SDK](05_install_flutter.md) — Instalação do SDK base.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral da preparação do ambiente.
