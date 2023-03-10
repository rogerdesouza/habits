# habits

tecnologias:
	server
	  prod
	   - fastify
	   - prisma client
	   - dayjs
	   - zod
	  dev
	   - mermaid
	   - prisma
	   - prisma erd generator
	   - tsx
	   - typescript
	   
	web
	 prod
	   - react
	   - react dom
	   - dayjs
	   - axios
	 dev
	   - react types
	   - vite
	   - autoprefixer
	   - postcss
	   - tailwindcss
	   - typescript
	   
	mobile
	 prod
	   - react
	   - axios
	   - dayjs
	   - expo
	 dev
	   - babel
	   - react types
	   - react native
	   - tailwindcss
	   - typescript



1 - instalar o nvm

2 - instalar o node a partir do nvm

// dentro da pasta server / api

3 - npm init -y

4 - dev dependencies: npm i -D fastify typescript tsx prisma

// serve para rodar o ts no node
// devemos config. o pack.json criando o script dev: "tsx --watch src/server.js"

5 - npx tsc --init
// e mudar o target para es2020

6 - npm i @prisma/client @fastify/cors

7 - npx prisma init --datasource-provider SQLite

8 - comando que roda o migrate do prisma: npx prisma migrate dev

9 - navegar no banco criado: npx prisma studio

OBS (opcional).: ctrl+shift+p no vscode e configurar as preferencias do usuario (json) incluindo isso:
"[prisma]": {
        "editor.formatOnSave": true
    }

OBS (opcional).: instalar o prisma erd generator
        npm i -D prisma-erd-generator @mermaid-js/mermaid-cli
        e incluir no schema.prisma:
                generator erd {
                    provider = "prisma-erd-generator"
                }
        e rodar: npx prisma generate

OBS (seed): criar arquivo de seed
            colocar esse codigo no final do package.json
              "prisma": {
                    "seed": "tsx prisma/seed.ts"
                }
            rodar: npx prisma db seed

10 - configurar o cors

// para criar a web
// fora da pasta web

11 - npm create vite@latest // escolher react / typescript


// dentro da pasta web
12 - npm i

13 - npm i -D tailwindcss postcss autoprefixer

14 - npx tailwindcss init -p



// mobile

15 - npx create-expo-app mobile --template // escolher blank com typescript

16 - studio.sh // rodar o android studio

17 - npx expo start

18 - tem que instalar o expo go no emulador tb

19 - npx expo install expo-font @expo-google-fonts/inter


====

LEGAL
httpie - muito massa




====


extens??es do code

tailwind
postCss
prisma
prisma - insider



// configurando no linux ubuntu

Linux (Ubuntu)
Depend??ncias
Para configurar o ambiente Android e iOS no Linux (Ubuntu) utilizando Expo Managed Workflow (Expo GO), precisamos de 6 ferramentas principais:

cURL
Node.js (LTS);
npm (j?? vem instalado com o Node);
git
expo-cli
Expo GO (app a ser instalado no dispositivo Android e/ou iOS)
Instalando cURL
O cURL pode j?? vir instalado na sua distro. Para verificar, basta executar curl --version no seu terminal.

Para instalar no seu sistema, basta voc?? executar no seu terminal o comando abaixo:

Copy
sudo apt-get install curl
Para verificar se a instala????o foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documenta????o, a vers??o do cURL para Ubuntu mais recente ?? a 7.81.0.

Copy
curl --version
Se foi apresentado o valor da sua vers??o, a instala????o foi um sucesso.

Instalando Node.js (LTS) e npm
Em seguida ?? preciso instalar o Node.js (LTS) e npm no nosso sistema.

Para instalar no seu sistema, voc?? pode utilizar um gerenciador de pacotes como o n ou instalar utilizando o NodeSource. Nesse guia iremos utilizar o NodeSource, ent??o basta acessar abrir o seu terminal e executar os comandos abaixo:

Copy
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
Se voc?? j?? tiver o Node.js instalado em sua m??quina, certifique-se que sua vers??o ?? a 14 ou mais recente.

Para verificar se a instala????o foi um sucesso, basta executar os comandos abaixo:

No momento da escrita dessa documenta????o, a vers??o LTS do Node mais recente ?? a 16.16.0 e do npm ?? a 8.14.0.

Copy
node -v
npm -v
Git
O git pode j?? vir instalado na sua distro. Para verificar, basta executar git --version no seu terminal.

Para instalar no seu sistema, basta voc?? executar no seu terminal o comando abaixo:

Copy
sudo apt-get install git
Para verificar se a instala????o foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documenta????o, a vers??o do Git para Ubuntu mais recente ?? a 2.34.1.

Copy
git --version
Se foi apresentado o valor da sua vers??o, a instala????o foi um sucesso.

expo-cli
Para instalar no seu sistema, voc?? ir?? utilizar o seu gerenciador de pacotes npm. Abra o seu terminal e execute o comando:

Copy
npm install -g expo-cli
Caso ocorra um erro dizendo que voc?? n??o possui permiss??o (EACESS), siga os passo desse link

Para verificar se a instala????o foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documenta????o, a vers??o do expo-cli mais recente ?? a 5.5.1.

Copy
expo --version
Se foi apresentado o valor da sua vers??o, a instala????o foi um sucesso.

Caso apare??a um erro dizendo que o comando expo n??o foi encontrado, siga os passos desse link

Expo GO
Com a CLI instalada no seu computador, voc?? consegue criar projetos Expo e executar o metro bundler para servir o seu c??digo, mas para executar o app no seu celular (ou emulador) voc?? precisa instalar o aplicativo Expo GO. Ele ?? o respons??vel por pegar o c??digo que o metro bundler envia e exibir em tela o seu app React Native.

Para instal??-lo no seu dispositivo f??sico, basta buscar nas lojas o aplicativo Expo Go:

Play Store
Apple Store
Para instal??-lo no seu emulador, basta executar o comando expo start e escolher qual emulador voc?? deseja executar. Caso o Expo GO n??o esteja instalado, ele ir?? solicitar a sua autouriza????o para instalar a vers??o necess??ria.

Emulador
Android
Com o Android Studio, ?? poss??vel configurar um emulador Android e executar a sua aplica????o nele.

Por??m, esses emuladores consomem bastante recursos do seu computador. Por isso, se voc?? possui um dispositivo f??sico Android e sua m??quina possui configura????es modestas (ex.: ??? i3, ??? 4gb RAM), ?? recomendado executar a aplica????o no seu dispositivo f??sico pelo Expo GO.

Para aprender a instalar e configurar o seu emulador, siga esse guia

iOS
Dispon??vel apenas para m??quinas macOS. Windows e Linux n??o suportam iOS simulator.

Executando aplica????o
Agora que voc?? possui tudo que ?? necess??rio para executar sua aplica????o Expo, basta seguir os seguintes passos:

Acesse a pasta do seu projeto pelo terminal
Execute o comando expo start
Abra o app no seu dispositivo via Expo GO
Se for dispositivo f??sico Android, basta abrir o app Expo GO, selecionar a op????o Scan QR code e ler o QR Code apresentado no terminal.
Se for dispositivo f??sico iOS, basta abrir o app de camera do iOS, ler o QR Code apresentado no terminal e clicar no popup Open with Expo Go app
Se for emulador Android, basta digitar a no terminal.
Seguindo esses passo seu app deve abrir com sucesso no seu dispositivo ????




Linux
Capa

Intro
Nesse guia iremos assumir que voc?? j?? possui o ambiente b??sico do React Native (Expo Managed Workflow). As depend??ncias desse ambiente s??o:

cURL
Node.js (LTS);
npm (j?? vem instalado com o Node);
git
expo-cli
Expo GO (app a ser instalado no dispositivo Android e/ou iOS)
Caso voc?? n??o possua esse ambiente, siga esses passos

Seguindo para configura????o do ambiente Android no Linux utilizando Expo Bare Workflow ou React Native CLI, iremos realizar 2 instala????es principais:

JDK 11 (LTS);
Android Studio e depend??ncias.
JDK 11 (LTS)
Se voc?? j?? tiver o JDK instalado em sua m??quina, certifique-se que sua vers??o seja exatamente a vers??o 11.

Agora precisamos instalar a JDK (Java Development Kit) na vers??o 11 (LTS) com o seguinte comando:

Copy
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-11-jdk
Podemos testar a instala????o do JDK executando o seguinte comando no terminal:

Copy
java -version
Caso apare??a a vers??o do Java, a instala????o foi um sucesso.

Se possuir outras vers??es do java, voc?? pode selecionar a vers??o 11 como padr??o usando o comando:

Copy
sudo update-alternatives --config java
Android Studio
Preparativos
Android

Crie uma pasta em um local desejado para instala????o da SDK. Ex: ~/Android/Sdk

Anote esse caminho para ser utilizado posteriormente

Anote tamb??m o endere??o de instala????o do JDK 11. Exemplo:

Copy
/usr/lib/jvm/java-11-openjdk-amd64
Caso n??o tenha certeza do caminho, busque na pasta /usr/lib/jvm/ pela pasta referente ao JDK 11, que provavelmente iniciar?? com java-11.

Com esses caminhos, precisamos configurar algumas vari??veis ambiente em nosso sistema. Procure pelo primeiro dos seguintes arquivos existentes no seu sistema: ~/.zshrc ou ~/.bashrc, e adicione essas seis linhas no arquivo (de prefer??ncia no in??cio):

Se nenhum desses arquivos existir, crie o ~/.bashrc caso utilize o shell padr??o (Bash) ou ~/.zshrc caso utilize o ZSH.

Copy
export JAVA_HOME=CAMINHO_ANOTADO_COM_SUA_VERS??O
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
N??o esque??a de substituir o valor na linha JAVA_HOME pelo caminho que voc?? anotou anteriormente. Al??m disso, caso esteja utilizando uma pasta diferente para a SDK do Android, altere acima.

Instala????o
Acesse a p??gina do Android Studio e clique no bot??o Download Android Studio.

V?? at?? a pasta de download e abra o arquivo tar.gz.

Esse arquivo deve possuir uma pasta android-studio dentro. Extraia essa pasta em um local de prefer??ncia (Ex.: ~/).

Ap??s a extra????o, adicione a seguinte vari??vel ambiente no seu sistema:

Copy
export PATH=$PATH:~/android-studio/bin
A adi????o desse caminho possibilita a execu????o do Android Studio diretamente pelo terminal com o comando studio.sh. Caso tenha extra??do em uma pasta diferente ou alterado o nome da pasta, ajuste o path acima para o que voc?? utilizou.

Agora, abra o terminal (reinicie se j?? estiver aberto) e execute o seguinte comando:

Copy
studio.sh
Configura????o
A primeira janela a ser apresentada deve ser perguntando sobre a importa????o de configura????es de outro Android Studio. Selecione a op????o Do not import settings e clique em OK.

Ap??s o carregamento terminar, deve aparecer uma p??gina de Welcome. Clique em Next.

Na sequ??ncia, ser?? pedido o tipo de instala????o. Escolha a op????o Custom e clique em Next.

Nesse momento, ser?? pedido para escolher a localiza????o do pacote JDK instalado. Clique em ??? e verifique se a op????o JAVA_HOME est?? apontando para a JDK 11. Se sim, escolha e Clique em Next. Caso contr??rio, clique no no bot??o ... e escolha a JDK 11 (voc?? pode inclusive utilizar o caminho anotado no passo anterior para te ajudar).

JDK Location

Em seguida, ser?? perguntado sobre qual tema ser?? utilizado. Escolha o que preferir e clique em Next

Chegamos na etapa mais importante do processo, a instala????o da SDK. A janela apresentar?? algumas op????es, marque todas.

SDK Location

SDK ?? o pacote que vai possibilitar que sua aplica????o React Native fa??a o build. Por padr??o, ele instala a ??ltima SDK est??vel;
O Android Virtual Device vai criar um emulador padr??o pronto para execu????o.
Um fator essencial nessa etapa ?? o caminho de instala????o da SDK. Utilize a pasta que voc?? criou na se????o Preparativos para o Android Studio (Ex.: ~/Android/Sdk). N??o utilize espa??os ou caracteres especiais pois causar?? erros mais para frente.

Se tudo estiver correto, clique em Next.

Na sequ??ncia, temos uma janela avisando sobre a possibilidade de executar o Emulador com melhor performance usando o KVM (Kernel-mode Virtual Machine). Essa etapa n??o ir?? aparecer para todos pois nem todo computador ?? compat??vel com esse recurso. Caso tenha interesse em instalar essa ferramenta, ser?? ensinado como na pr??xima se????o. Finalizada essa etapa, clique em Next.

Em seguida, ser?? apresentada uma janela com um resumo de todas as op????es escolhidas at?? aqui. Verifique se est?? tudo certo, principalmente os caminhos da SDK e do JDK. Clique em Finish.

Por fim, ser?? realizada a instala????o das configura????es selecionadas. Quando o programa terminar, clique em Finish.

Caso a instala????o e configura????o do Android Studio ocorra com sucesso, voc?? deve se deparar com uma tela semelhante a essa:

Android Studio Menu

KVM (Extra)
Caso o seu Android Studio tenha acusado a possibilidade de instalar o KVM e voc?? pretende executar sua aplica????o React Native no Emulador, pode prosseguir com esse tutorial. Caso contr??rio, pode pular para o pr??ximo

Para instalar o KVM, o processo ?? bem simples. Em sistemas Ubuntu/Debian e Linux Minti, instale o KVM executando o comando:

Copy
sudo apt install qemu-kvm
Em seguida, adicione o seu usu??rio no grupo do KVM:

Copy
sudo adduser $USER kvm
Por fim, reinicie (ou deslogue e log novamente) o sistema e execute o comando:

Copy
grep kvm /etc/group
Se o resultado for algo semelhante a:

Copy
kvm:x:NUMERO_QUALQUER:SEU_USUARIO
O kvm est?? instalado corretamente e pronto para uso.

Emulador
Com o Android Studio, ?? poss??vel configurar um emulador Android e executar a sua aplica????o nele.

Por??m, esses emuladores consomem bastante recursos do seu computador. Por isso, se voc?? possui um dispositivo f??sico Android e sua m??quina tenha configura????es modestas (ex.: ??? i3, ??? 4gb RAM), ?? recomendado executar a aplica????o diretamente no dispositivo f??sico.

Para aprender a configurar o seu emulador no Android Studio e executar a sua aplica????o React Native nele, clique aqui

Dispositivo F??sico
Caso voc?? tenha um dispositivo f??sico Android, tamb??m ?? poss??vel executar a aplica????o diretamente nele. Caso tenha interesse em configurar essa etapa, clique aqui




Android Emulator
Capa

Caso voc?? possua um dispositivo f??sico Android e seu computador tenha configura????es modestas (ex.: ??? i3, ??? 4gb RAM), ?? recomendado executar a aplica????o diretamente no dispositivo f??sico. Para configurar seu aparelho, clique aqui

Android Studio
Para criar o seu emulador android, ?? preciso ter o Android Studio instalado. Abra o programa e, dependendo se voc?? j?? abriu ou n??o um projeto android no Android Studio antes, a interface ser?? diferente.

Se voc?? n??o possui o Android Studio instalado, pode faz??-lo seguindo nossas docs de acordo com o seu sistema operacional (Windows, Linux e macOS).

Se nunca abriu um projeto android nele antes, basta clicar em More Actions no centro da tela e escolher a op????o Virtual Device Manager.

AVD Manager

Se j?? abriu um projeto android antes, basta clicar nos tr??s pontos no canto superior direito e escolher a op????o Virtual Device Manager

AVD Manager

Virtual Device Manager
Na sequ??ncia, ser?? apresentada uma tela com os emuladores instalados. Se voc?? marcou a op????o Android Virtual Device na etapa de configura????o do Android Studio, deve aparecer um emulador j?? configurado e pronto para uso. Caso queira utilizar esse mesmo, pule para a pr??xima se????o clicando nesse link.

Por??m, caso queira criar seu pr??prio emulador, selecione a op????o Create Device no canto superior esquerdo.

AVD Default

Nessa etapa, ser?? perguntado qual Hardware voc?? quer selecionar. Como exemplo, escolhi na aba Phone o Pixel 4. Ap??s escolher, clique em Next.

AVD Hardware

Em seguida, voc?? dever?? escolher a imagem do sistema (API) do emulador a partir de uma das tr??s listas: Recommended, x86 Images e Other Images. Se essa ?? sua primeira vez, provavelmente nenhuma imagem estar?? baixada.

Aqui, a escolha da imagem do sistema vai depender da arquitetura do seu processador.

Sugerimos que escolham exatamente a imagem que recomendarmos abaixo pois ?? a que testamos por aqui. Outras imagens podem n??o funcionar corretamente.

Caso o seu processador seja Intel ou AMD, escolha a aba x86 Images e clique no link de Download da imagem S, API Level 31, ABI x86_x64 e Target Android 12.0 (Google APIs).
AVD System Image Choice

Caso o seu processador seja Apple ARM (ex.: M1), escolha a aba Recommended e clique no link de Download da imagem S, API Level 31, ABI arm64-v8a e Target Android 12.0 (Google Play).
AVD System Image Choice

Uma nova janela ir?? abrir. Aceite as licen??as e aguarde a instala????o. Quando finalizar, clique em Finish

AVD System Image Installation

Com a sua imagem do sistema baixada, basta escolh??-la e clicar em Next

AVD System Image

Por fim, ser??o apresentadas algumas configura????es do seu emulador (Android Virtual Device - AVD). No canto inferior esquerdo, clique na op????o Show Advanced Settings.

AVD Configuration

Deslize a tela at?? encontrar a op????o Memory and Storage. Nela, aumente o Internal Storage at?? o valor desejado. Por padr??o, esse valor vem como 800 MB, o que ?? muito pouco e acaba causando erro na instala????o dos apps React Native no dispositivo.

Sugerimos escolher um valor acima de 4000 MB, no exemplo escolhemos 8000 MB. Definido esse valor, clique em Finish.

AVD Configuration 2

Agora, o seu emulador deve estar aparecendo na lista.

AVD Devices List

Iniciando o Emulador
Com o emulador pronto, basta clicar no bot??o Play e aguardar o AVD iniciar. Esse processo pode demorar, principalmente na primeira execu????o.

Quando o emulador terminar de carregar, abra o seu terminal e execute o comando:

Copy
adb devices
Se estiver tudo certo, deve aparecer uma lista com o nome do seu emulador android aberto (normalmente emulator-5554) e status device.

AVD

Executando app no Emulador
Expo Bare Workflow
Para esse passo ?? preciso que voc?? j?? tenha criado o seu projeto Expo Bare Workflow. Caso n??o tenha criado ainda, voc?? pode criar com o comando expo init e escolher o template Bare Workflow.

Agora, com o emulador aberto, basta abrir um terminal, acessar a pasta do seu projeto e executar o comando:

Copy
npm run android
AVD Running Expo app

React Native CLI
Para esse passo ?? preciso que voc?? j?? tenha criado o seu projeto React Native CLI. Caso n??o tenha criado ainda, voc?? pode criar com o comando npx react-native init nomeDoSeuApp

Agora, com o emulador aberto, basta abrir dois terminais e acessar a pasta do seu projeto em cada um deles. Em seguida, execute os comandos:

Terminal 1
Copy
npm start
Terminal 2
Copy
npm run android
AVD Running CLI app







