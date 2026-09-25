# **4. Install Android Studio**
<details><summary>A. Install Android Studio</summary>

```bash
sudo apt install -y libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386

```

```bash
sudo snap install android-studio --classic

```
</details><br><br>


<details><summary>X. This part is already present in "1_bashrc_config.md"</summary>

```bash
echo '' >> ~/.bashrc
echo 'export ANDROID_HOME=/home/$USER/Android/Sdk' >> ~/.bashrc
echo 'export ANDROID_SDK_ROOT=/home/$USER/Android/Sdk' >> ~/.bashrc
echo '' >> ~/.bashrc
echo 'export PATH=$PATH:$ANDROID_HOME/tools' >> ~/.bashrc
echo 'export PATH=$PATH:$ANDROID_HOME/platform-tools' >> ~/.bashrc

```

```bash
source ~/.bashrc

```

```bash
# Status Android Studio
adb --version

```
</details><br><br>


<details><summary>C. Configuração gráfica (GUI) e emulador</summary>

1. Abra o **Android Studio** e conclua a configuração inicial (First Run / Import Settings).
2. Clique em **More Actions -> SDK Manager**.
3. Na aba **SDK Platforms**, marque as versões do Android que deseja (ex: Android 11 e 12).
4. Na aba **SDK Tools**, marque **Android SDK Command-line Tools**.
5. Na aba **Plugins**, procure por *Flutter* e clique em **Install**.
6. Em **More Actions -> SDK Manager**, copie o endereço de **Android SDK Location**.
7. No terminal, confirme o `adb --version` usando esse caminho em `ANDROID_HOME` (já configurado no `1_bashrc_config.md`).

**Criar um emulador:**
1. Clique em **More Actions -> Virtual Device Manager**.
2. Clique em **Create Device** e escolha um perfil (ex: Pixel) com as configurações recomendadas.
3. Selecione uma imagem de sistema compatível e finalize.

> [!tip] Ao final, teste se tudo está funcionando fechando e abrindo um novo terminal e rodando `adb --version`.
</details><br><br>
