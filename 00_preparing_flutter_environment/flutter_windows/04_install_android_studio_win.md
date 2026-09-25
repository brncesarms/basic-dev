---
title: "Flutter (Windows): Instalação do Android Studio e Configuração de Variáveis"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - windows
  - android
  - sdk
  - powershell
---

# 📱 Flutter (Windows): Instalação do Android Studio e Configuração de Variáveis

> [!info] Instalação do Android Studio e configuração determinística das variáveis de ambiente (`ANDROID_HOME`, `ANDROID_SDK_ROOT` e `PATH`) via PowerShell.

---

## 1. Instalação do Android Studio

Pode ser instalado diretamente pelo instalador oficial ou via WinGet:

```powershell
winget install --id=Google.AndroidStudio -e --silent --accept-package-agreements --accept-source-agreements
```

---

## 2. Configuração de Variáveis de Ambiente no Escopo de Usuário

No PowerShell, configure as variáveis de ambiente apontando para o diretório padrão do SDK:

```powershell
# Definir variáveis de usuário
[Environment]::SetEnvironmentVariable("ANDROID_HOME", "$env:LOCALAPPDATA\Android\Sdk", "User")
[Environment]::SetEnvironmentVariable("ANDROID_SDK_ROOT", "$env:LOCALAPPDATA\Android\Sdk", "User")

# Adicionar ferramentas do SDK ao PATH de usuário
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$toolsPath = "$env:LOCALAPPDATA\Android\Sdk	ools;$env:LOCALAPPDATA\Android\Sdk\platform-tools"

if ($existingPath -notlike "*$env:LOCALAPPDATA\Android\Sdk\platform-tools*") {
    $newPath = "$existingPath;$toolsPath"
    [Environment]::SetEnvironmentVariable("Path", $newPath, "User")
}
```

---

## 🔗 Notas Relacionadas
- [Instalação do Java JDK](03_install_java_jdk_win.md) — Suporte a compilação Gradle.
- [Instalação do FVM e Flutter](05_install_fvm_win.md) — Configuração do Flutter SDK.
- [Flutter no Windows: Guia Completo](flutter_windows.md) — Visão geral do pipeline de ambiente.
