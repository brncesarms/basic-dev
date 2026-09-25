---
title: "Flutter (Linux): Instalação do Android Studio e SDK"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - android
  - sdk
  - ide
---

# 📱 Flutter (Linux): Instalação do Android Studio e SDK

> [!info] Instalação do Android Studio, bibliotecas de compatibilidade de 32-bit e configuração do SDK Manager para emulação e build nativo.

---

## 1. Instalação das Bibliotecas de 32-Bit (Dependências do SDK)

```bash
# Habilitar arquitetura i386 e instalar bibliotecas auxiliares
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install -y libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
```

---

## 2. Instalação do Android Studio

O método recomendado via pacote canônico Snap:

```bash
sudo snap install android-studio --classic
```

---

## 3. Configuração do SDK & Linhas de Comando

1. Abra o Android Studio e conclua o assistente de primeira inicialização.
2. Em **More Actions** -> **SDK Manager**:
   - Aba **SDK Platforms**: Instale a versão mais recente e estável do Android SDK.
   - Aba **SDK Tools**: Marque e instale **Android SDK Command-line Tools (latest)** e **Android SDK Platform-Tools**.
3. Aceite as licenças do Android via terminal:
```bash
flutter doctor --android-licenses
```

---

## 🔗 Notas Relacionadas
- [Configuração de Variáveis no .bashrc](01_bashrc_config.md) — Caminho do `ANDROID_HOME`.
- [Instalação do Flutter SDK](05_install_flutter.md) — Validação com flutter doctor.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral da preparação do ambiente.
