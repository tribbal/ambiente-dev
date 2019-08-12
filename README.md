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
   5.6 -sdkmanager  "platform-tools" "platforms;android-27" "build-tools;27.0.3"
   5.7 - avdmanager create avd -n "teste"  -k "system-images;android-26;google_apis;x86"
   5.8 - emulator -avd teste
        Caso de o erro abaixo
        [13300]:ERROR:android/android-emu/android/qt/qt_setup.cpp:28:Qt library not found at ..\emulator\lib64\qt\lib
        Could not launch 'C:\Users\marcu\..\emulator\qemu\windows-x86_64\qemu-system-i386.exe': No such file or directory
        Coloque o dirotorio do  EMULATOR no PATH do Windows
        
    5.9 - sdkmanager extras;intel;Hardware_Accelerated_Execution_Manager ( Instalando Acelerador Grafico Intel )
    5.10 - Com passo anterior foi criada a EXTRAS no diretorio do SDK. EntrE em extras\intel\Hardware_Accelerated_Execution_Manager  e click no arquivo intelhaxm-android.exe, e inicie a instalação.(next,next,next)
    5.11 - Finalmenente podemos subir o AVD com o seguinte comand emulator -avd teste 
    Ufa!

 6 - [ Instalando ambiente FLUTTER ]
 6.1 instalando o SDK do Dart - choco install dart-sdk
     Teste Drive - dart --version
 6.2 instalando Flutter - choco install flutter
     Teste Driver - flutter doctor
     Tive que setar manulmente o PATH do flutter pois a instalação estava com o endereço errado
     Seteir "C:\tools\fluttter\fltter\bin" e rodei novamente "flutter doctor"
 6.3 - Executando checklist do "flutter doctor"
       6.3.1 Setar o PATH do SDK Android Tools
              
        
      
    
    ConEmus
    Maquina Virtual8 - Ubuntu na Maquina Virtual 
    No Ubunto ambiente de Backend
   
     




