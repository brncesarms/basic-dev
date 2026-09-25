---
title: "Flutter (Windows): Instalação e Configuração de Java JDK"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - windows
  - java
  - jdk
  - powershell
---

# ☕ Flutter (Windows): Instalação e Configuração de Java JDK

> [!info] Procedimento de download, estruturação de diretórios e parametrização do PATH para Java JDK 8 e 11 no Windows.

---

## 1. Estruturação dos Diretórios de Instalação

Abra o **PowerShell como Administrador** e crie a árvore de diretórios canônica:

```powershell
New-Item -ItemType Directory -Path "C:\_devprograms\java\jdk\jdk11" -Force
New-Item -ItemType Directory -Path "C:\_devprograms\java\jdk\jdk8" -Force
New-Item -ItemType Directory -Path "C:\_devprograms\java\jre\jre8" -Force
```

---

## 2. Download e Instalação dos Binários

Faça o download dos instaladores oficiais do JDK ou instale versões comunitárias OpenJDK via WinGet:

```powershell
# Exemplo de instalação comunitária via WinGet (Microsoft Build of OpenJDK)
winget install --id=Microsoft.OpenJDK.17 -e --silent
```

---

## 3. Limpeza de Variáveis de PATH Legadas

Para evitar conflitos com versões antigas do Java do sistema:

```powershell
$keyword = "javapath"
$pathVariable = [Environment]::GetEnvironmentVariable("Path", "Machine")
$pathEntries = $pathVariable -split ";" | Where-Object { $_ -notlike "*$keyword*" }
$newPathVariable = $pathEntries -join ";"
[Environment]::SetEnvironmentVariable("Path", $newPathVariable, "Machine")
```

---

## 🔗 Notas Relacionadas
- [Instalação do Android Studio](04_install_android_studio_win.md) — Configuração do SDK e AVD.
- [Instalação do FVM](05_install_fvm_win.md) — Gerenciamento do Flutter SDK.
- [Flutter no Windows: Guia Completo](flutter_windows.md) — Visão geral do pipeline de ambiente.
