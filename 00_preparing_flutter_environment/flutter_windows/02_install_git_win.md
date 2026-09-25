---
title: "Flutter (Windows): Instalação e Configuração do Git"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - windows
  - git
  - versionamento
  - winget
---

# 🐙 Flutter (Windows): Instalação e Configuração do Git

> [!info] Instalação não-interativa do Git para Windows via WinGet e configuração global de identidade do autor.

---

## 1. Instalação via WinGet

Abra o terminal do Windows e execute:

```powershell
winget install --id=Git.Git -e --silent --accept-package-agreements --accept-source-agreements
```

---

## 2. Configuração de Identidade Global

> [!warning] Substitua pelos seus dados
> Use o e-mail e o nome da sua conta do Git. Para ocultar o e-mail pessoal no GitHub, utilize o formato no-reply: `<id>+<nome>@users.noreply.github.com`.

```powershell
git config --global user.name "Bruno César"
git config --global user.email "brncesarms@users.noreply.github.com"
git config --global init.defaultBranch main
```

---

## 🔗 Notas Relacionadas
- [Instalação do Chocolatey](01_install_chocolatey_win.md) — Gerenciador de pacotes alternativo.
- [Instalação do Java JDK](03_install_java_jdk_win.md) — Compiladores Java para Android.
- [Flutter no Windows: Guia Completo](flutter_windows.md) — Visão geral do pipeline de ambiente.
- [Windows: Provisionamento via WinGet](../../../windows/17_winget.md) — Guia corporativo do WinGet.
