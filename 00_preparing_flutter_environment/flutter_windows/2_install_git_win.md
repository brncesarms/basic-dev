```powershell
winget install --id=Git.Git -e --accept-package-agreements --accept-source-agreements
```

> [!warning] Substitua pelos seus dados
> Use o e-mail e o nome da sua conta do Git. Para ocultar o e-mail pessoal no GitHub, use o e-mail de privacidade `<id>+<nome>@users.noreply.github.com`.

```powershell
git config --global user.email "SEU_EMAIL@exemplo.com"
git config --global user.name "SEU_USUARIO"
```