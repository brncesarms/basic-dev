
#### A. Download e instalação do Java

- [Download Java JDK 11:](https://www.oracle.com/br/java/technologies/javase/jdk11-archive-downloads.html)
- [Download Java JDK 8:](https://www.oracle.com/br/java/technologies/javase/javase8-archive-downloads.html)

Install JDK in respective directories:
```powershell
New-Item -ItemType Directory -Path "C:\_devprograms\java\jdk\jdk11" -Force
New-Item -ItemType Directory -Path "C:\_devprograms\java\jdk\jdk8" -Force
New-Item -ItemType Directory -Path "C:\_devprograms\java\jre\jre8" -Force

```

#### B. Excluindo as variáveis do sistema

Excluir:
```powershell
$keyword = "javapath"
$pathVariable = [Environment]::GetEnvironmentVariable("Path", "Machine")
$pathEntries = $pathVariable -split ";" | Where-Object { $_ -notlike "*$keyword*" }
$newPathVariable = $pathEntries -join ";"
[Environment]::SetEnvironmentVariable("Path", $newPathVariable, "Machine")

```

#### C. **Chaveando** com as versões do JDK

PowerShell admin:
```powershell
New-Item -ItemType SymbolicLink -Path "C:\_devprograms\jdk\current" -Target "C:\_devprograms\jdk\jdk11" -Force
```
ou
```powershell
New-Item -ItemType SymbolicLink -Path "C:\_devprograms\jdk\current" -Target "C:\_devprograms\jdk\jdk8" -Force
```

#### D. No PowerShell do Windows 11, você pode criar uma nova variável de ambiente usando o seguinte comando:
```powershell
[Environment]::SetEnvironmentVariable("JAVA_HOME", "C:\_devprograms\jdk\current", "User")

```


#### E. Para adicionar à variável PATH do seu usuário no Windows 11, você pode usar o seguinte comando no PowerShell:

```powershell
$existingPath = [Environment]::GetEnvironmentVariable("Path", "User")
$newPath = "$existingPath;%JAVA_HOME%\bin"
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")

```

```powershell
keytool

```