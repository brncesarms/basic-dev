- [Download Android Studio:](https://developer.android.com/studio)

#### A. No PowerShell do Windows 11, você pode criar uma nova variável de ambiente usando o seguinte comando:
```powershell
[Environment]::SetEnvironmentVariable("ANDROID_HOME", "C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk", "User")

```

```powershell
[Environment]::SetEnvironmentVariable("ANDROID_SDK_ROOT", "C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk", "User")

```

> [!info] Substitua `SEU_USUARIO` pelo seu nome de usuário do Windows.
> Esse comando utiliza a classe `Environment` do .NET Framework para definir uma nova variável de ambiente chamada "ANDROID_HOME". O terceiro parâmetro "User" especifica que a variável deve ser definida no escopo do usuário atual.


#### B. Para adicionar à variável PATH do seu usuário no Windows 11, você pode usar o seguinte comando no PowerShell:

```powershell
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$newPath = "$existingPath;%ANDROID_HOME%\tools"
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")

```

```powershell
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$newPath = "$existingPath;%ANDROID_HOME%\platform-tools"
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")

```

```powershell
adb --version
```