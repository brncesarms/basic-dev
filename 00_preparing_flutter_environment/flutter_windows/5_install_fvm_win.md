### A. Instalando Flutter, dentro do diretório, abrindo terminal dentro do diretório abaixo sitado e colocando o comando abaixo:

```
C:\_devprograms
```

```
git clone https://github.com/flutter/flutter.git -b stable
```

#### B. No PowerShell do Windows 11, você pode criar uma nova variável de ambiente usando o seguinte comando:

```powershell
[Environment]::SetEnvironmentVariable("FLUTTER_HOME", "C:\_devprograms\flutter", "User")

```


#### C. Para adicionar à variável PATH do seu usuário no Windows 11, você pode usar o seguinte comando no PowerShell:

```powershell
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$newPath = "$existingPath;%FLUTTER_HOME%\bin"
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")

```

```powershell
flutter doctor
```

### Mude para JDK11
```
jdk11
```

```
flutter doctor --android-licenses
```

### Pub package
```
dart pub global activate fvm
```

#### D. Para adicionar à variável PATH do seu usuário no Windows 11, você pode usar o seguinte comando no PowerShell:

```powershell
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$newPath = "$existingPath;C:\Users\SEU_USUARIO\AppData\Local\Pub\Cache\bin"
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")

```

Config FVM

```
fvm config
```

Crie o diretório "FVM" antes de executar o comando abaixo
```
fvm config --cache-path C:\_devprograms\fvm
```
