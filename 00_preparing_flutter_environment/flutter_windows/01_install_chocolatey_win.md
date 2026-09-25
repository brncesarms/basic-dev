---
title: "Flutter (Windows): Instalação do Chocolatey Package Manager"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - windows
  - chocolatey
  - gerenciador-pacotes
---

# 🍫 Flutter (Windows): Instalação do Chocolatey Package Manager

> [!info] Instalação do gerenciador de pacotes Chocolatey no Windows 11 via PowerShell para provisionamento de ferramentas de desenvolvimento.

---

## 1. Habilitar Execução de Scripts no PowerShell

Abra o **PowerShell como Administrador** e aplique:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
```

> [!tip] O escopo `Process` afeta apenas a janela atual do PowerShell, sendo mais seguro do que alterar o sistema permanentemente.

---

## 2. Instalação do Chocolatey

Execute o script oficial de inicialização:

```powershell
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Valide a instalação:
```powershell
choco --version
```

---

## 🔗 Notas Relacionadas
- [Instalação do Git no Windows](02_install_git_win.md) — Instalação e parametrização do Git.
- [Instalação do Java JDK no Windows](03_install_java_jdk_win.md) — Configuração de JDK 8 e 11.
- [Flutter no Windows: Guia Completo](flutter_windows.md) — Visão geral do pipeline de ambiente.
- [Windows: Gerenciamento com Chocolatey](../../../windows/18_chocolatey.md) — Guia do cofre Windows.
