---
title: "Flutter (Linux): Instalação e Configuração do Git"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - linux
  - git
  - versionamento
---

# 🐙 Flutter (Linux): Instalação e Configuração do Git

> [!info] Procedimento de instalação do Git oficial via PPA atualizado e parametrização das credenciais globais de autor no Linux.

---

## 1. Instalação do Git

Para garantir a versão mais recente em distribuições baseadas em Ubuntu/Debian:

```bash
# Adicionar repositório oficial do Git
sudo add-apt-repository ppa:git-core/ppa -y

# Atualizar índices e instalar
sudo apt update
sudo apt install -y git
```

---

## 2. Configuração Global de Identidade

Configure seu nome de exibição e e-mail vinculados aos commits do GitHub:

> [!warning] Substitua pelos seus dados
> Use o e-mail e o nome da sua conta do Git. Para ocultar o e-mail pessoal no GitHub, use o e-mail no-reply: `<id>+<nome>@users.noreply.github.com`.

```bash
git config --global user.name "Bruno César"
git config --global user.email "brncesarms@users.noreply.github.com"
git config --global init.defaultBranch main
```

---

## 🔗 Notas Relacionadas
- [Configuração de Variáveis no .bashrc](01_bashrc_config.md) — Configuração das variáveis de ambiente.
- [Instalação do Flutter SDK](05_install_flutter.md) — Obtenção do SDK via Snap ou Git.
- [Linux: Instalação e Configuração do Git](../../../linux/11_git_instalacao_configuracao.md) — Guia aprofundado de Git corporativo.
- [Flutter no Linux: Guia Completo](flutter_linux.md) — Visão geral da preparação do ambiente.
