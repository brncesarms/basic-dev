---
title: "Flutter (Windows): Instalar Chocolatey"
date_created: 2026-08-17
tags:
  - windows
  - flutter
  - gerenciador-pacotes
---

# 🍫 Flutter (Windows): Instalar o Chocolatey

> [!info] Instalação do gerenciador de pacotes Chocolatey no Windows, usado para instalar ferramentas de desenvolvimento.

---

## 1. Permitir execução de scripts

Abra o **PowerShell como Administrador** e habilite a execução de scripts:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
```

> [!tip] O escopo `Process` vale apenas para a sessão atual, sendo mais seguro que o `Unrestricted` permanente.

## 2. Instalar o Chocolatey

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

> [!info] Fonte oficial: <https://chocolatey.org/install>
