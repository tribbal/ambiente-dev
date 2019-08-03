Organizando as ideias para montar um abiente de desenvolvimento mobile

[ ROTEIRO ]
1 - Instalar o Windows 10 
    1.1 - Fazer Backup de Arquivos
    1.2 - Criar Pendrive Bootavel
    1.3 - Configurar Sequencia de Boot( BOOT UIFI)
    1.4 - Particinar HD
    1.5 - Instalar Win10
2 - Instalar Gerenciador de Pacotes Chocolatey
LINHA DE COMANDO PARA INSTALAR CHOCOLATYE pelo CMD
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

3 - Instalar Ambiente Basico de Desenvolvimento
3.1 - Instalar GIT choco install git
      3.1.1 - Configurar usuario global  do GIT 
               git config --global user.email "you@example.com"
               git config --global user.name "Your Name"
               uTILIze seu usuario do GITHUB
3.2 - Instalar VSCODE - choco install vscode
3.3 - Instalar Node JS(NPM) - choco install nodejs-lts 
3.4 - Crome - choco install googlechrome
3.5 - Instalar JAVA - choco install jdk8
      teste com java -version
3.6 - Android SDK - choco install android-sdk

4 - [ TESTANDO ANDROID SDK ]
    4.1 - Abra o prompt(cmd, conEmue, Powershell)
    4.2 - Digite adb na linha de comando : adb -- help  
5 - Criando AVD para emular culular Android
   5.1. sdkmanager ( Cria/atualiza lista repositorios)
        Se der uma mensagem "Warning: Fiel C:Users\nomeDoUsuario\.android\repositories.cfg could not be load"
        Crie o arquivo repositories.cfg no diretorio .android que esta seur diretorio de usuari em Users ou Usuarios 
   5.2. sdkmanager --licenses ( este comando baixa as lincensas necessarias para utilizar as imagens)
        Após esse comando o sistema vai lhe pedir permissão para instalar as lincessas é digitar  "y"
   5.3. sdkmanager --list ( exibe lista das imagens disponiveis para baixar do repositorio )
   5.4. sdkmanager "system-images;android-26;google_apis;x86" (baixando imagem, e api - AVD )
   5.5. sdkmanager "platform-tools" "platforms;android-26"
   5.6 - 
   5.7 - avdmanager create avd -n "teste"  -k "system-images;android-26;google_apis;x86"
   5.8 - emulator -avd teste
        Caso de o erro abaixo
        [13300]:ERROR:android/android-emu/android/qt/qt_setup.cpp:28:Qt library not found at ..\emulator\lib64\qt\lib
        Could not launch 'C:\Users\marcu\..\emulator\qemu\windows-x86_64\qemu-system-i386.exe': No such file or directory
        Coloque o dirotorio do  EMULATOR no PATH do Windows
      
    - Firefox 
    - ConEmu ( Prompt de Comandu )- choco install conemu
3 - Instala4 - VSCODE
5 - SDK AVD Only
6 - Fluter 
7 - Maquina Virtual
8 - Ubuntu na Maquina Virtual 
    No Ubunto ambiente de Backend
   
     




