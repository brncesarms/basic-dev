---
title: "Flutter (Linux): Instalação do Flutter SDK e Dependências C/C++"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - sdk
  - build
---

# 🚀 Flutter (Linux): Instalação do Flutter SDK e Dependências

> [!info] Instalação das dependências de compilação C/C++ para desktop Linux e configuração do Flutter SDK.

---

## 1. Instalação das Dependências de Compilação Linux Desktop

O Flutter Desktop no Linux requer bibliotecas nativas de compilação GTK e CMake:

```bash
sudo apt update
sudo apt install -y clang cmake ninja-build pkg-config libgtk-3-dev liblzma-dev
```

---

## 2. Instalação do Flutter SDK

```bash
# Instalação clássica via Snap
sudo snap install flutter --classic

# Validação do ambiente completo
flutter doctor
```

> [!tip] Caso utilize a instalação manual via Git tarball:
> Clone o repositório em `$HOME/development/flutter` e adicione `$HOME/development/flutter/bin` ao seu `PATH`.

---

## 🔗 Notas Relacionadas
- [Instalação do FVM](06_install_fvm.md) — Gerenciamento de múltiplas versões do Flutter.
- [Instalação do Android Studio](04_install_android_studio.md) — Emuladores e SDK Android.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral da preparação do ambiente.
