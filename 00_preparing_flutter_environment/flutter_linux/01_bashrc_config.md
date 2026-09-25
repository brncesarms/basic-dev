---
title: "Flutter (Linux): Configuração de Variáveis no .bashrc"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - bashrc
  - ambiente
---

# 🐧 Flutter (Linux): Configuração de Variáveis no .bashrc

> [!info] Configuração canônica das variáveis de ambiente (`ANDROID_HOME`, `FLUTTER_HOME`, `PATH`) e aliases de versão do Java JDK no arquivo `~/.bashrc`.

---

## 🛠️ Variáveis e Caminhos no `~/.bashrc`

Abra seu `~/.bashrc` ou execute o bloco de comandos abaixo para registrar os caminhos essenciais no terminal:

```bash
# Adicionar variáveis ao final do ~/.bashrc
cat << 'EOF' >> ~/.bashrc

### Flutter & Android Development ###
alias jdk8="sdk default java 8.0.302-open"
alias jdk11="sdk default java 11.0.12-open"

export ANDROID_HOME=$HOME/Android/Sdk
export ANDROID_SDK_ROOT=$HOME/Android/Sdk
export FLUTTER_HOME=$HOME/snap/flutter/common/flutter

export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$FLUTTER_HOME/bin
export PATH=$PATH:$HOME/.pub-cache/bin
EOF

# Recarregar as configurações no terminal atual
source ~/.bashrc
```

---

## 🔗 Notas Relacionadas
- [Instalação e Configuração do Git](02_install_git.md) — Configuração de identidade de versionamento.
- [Instalação de Java JDK via SDKMAN](03_install_jdk.md) — Alternância entre versões de JDK.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral da preparação do ambiente.
- [Guia Principal de Desenvolvimento Básico](../../README.md) — Índice geral de Flutter e Dart.
