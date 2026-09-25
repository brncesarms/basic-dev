---
title: "Flutter (Linux): Instalação do Java JDK via SDKMAN"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - java
  - sdkman
  - jdk
---

# ☕ Flutter (Linux): Instalação do Java JDK via SDKMAN

> [!info] Instalação do SDKMAN e gerenciamento de múltiplas versões do Java Development Kit (JDK 8, 11 e LTS) para compilação Android.

---

## 1. Preparação do Ambiente e Remoção de Versões Conflitantes

```bash
# Remover versões legadas de openjdk se existirem
sudo apt purge -y openjdk*

# Instalar utilitários essenciais
sudo apt update && sudo apt install -y curl zip unzip
```

---

## 2. Instalação do SDKMAN

```bash
# Baixar e instalar SDKMAN
curl -s "https://get.sdkman.io" | bash

# Inicializar no shell atual
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

---

## 3. Instalação dos JDKs Compatíveis

```bash
# Instalar Java 8 e Java 11 (AdoptOpenJDK / Temurin)
sdk install java 8.0.302-open
sdk install java 11.0.12-open

# Definir versão padrão para o ecossistema Android/Gradle
sdk default java 11.0.12-open
```

Verifique a instalação:
```bash
java -version
```

---

## 🔗 Notas Relacionadas
- [Configuração de Variáveis no .bashrc](01_bashrc_config.md) — Aliases para alternar entre JDK 8 e JDK 11.
- [Instalação do Android Studio](04_install_android_studio.md) — Configuração da IDE e Android SDK.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral do pipeline de ambiente.
