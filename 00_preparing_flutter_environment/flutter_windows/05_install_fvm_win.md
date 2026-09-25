---
title: "Flutter (Windows): Instalação do Flutter SDK e FVM"
date_created: 2026-08-17
last_modified: 2026-09-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - flutter
  - windows
  - fvm
  - sdk
  - powershell
---

# 🎛️ Flutter (Windows): Instalação do Flutter SDK e FVM

> [!info] Procedimento de clonagem do Flutter SDK stable, parametrização de variáveis de ambiente no Windows e adoção do FVM.

---

## 1. Clonagem do Flutter SDK no Diretório Canônico

```powershell
# Criar diretório base
New-Item -ItemType Directory -Path "C:\_devprograms" -Force
cd "C:\_devprograms"

# Clonar branch estável
git clone https://github.com/flutter/flutter.git -b stable
```

---

## 2. Configuração de Variáveis de Ambiente

```powershell
# Definir FLUTTER_HOME
[Environment]::SetEnvironmentVariable("FLUTTER_HOME", "C:\_devprogramslutter", "User")

# Adicionar binário ao PATH de Usuário
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
if ($existingPath -notlike "*C:\_devprogramslutterin*") {
    $newPath = "$existingPath;C:\_devprogramslutterin"
    [Environment]::SetEnvironmentVariable("Path", $newPath, "User")
}
```

---

## 3. Instalação e Ativação do FVM

Após reiniciar o PowerShell:
```powershell
dart pub global activate fvm
```

---

## 🔗 Notas Relacionadas
- [Instalação do Android Studio](04_install_android_studio_win.md) — Configuração do emulador e SDK.
- [Flutter no Windows: Guia Completo](flutter_windows.md) — Visão geral do pipeline de ambiente.
- [Dart Básico: Função Main](../../01_basic_dart/01_funcao_main/01_funcao_main.md) — Primeiros passos na sintaxe Dart.
