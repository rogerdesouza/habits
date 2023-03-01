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


extensões do code

tailwind
postCss
prisma
prisma - insider



// configurando no linux ubuntu

Linux (Ubuntu)
Dependências
Para configurar o ambiente Android e iOS no Linux (Ubuntu) utilizando Expo Managed Workflow (Expo GO), precisamos de 6 ferramentas principais:

cURL
Node.js (LTS);
npm (já vem instalado com o Node);
git
expo-cli
Expo GO (app a ser instalado no dispositivo Android e/ou iOS)
Instalando cURL
O cURL pode já vir instalado na sua distro. Para verificar, basta executar curl --version no seu terminal.

Para instalar no seu sistema, basta você executar no seu terminal o comando abaixo:

Copy
sudo apt-get install curl
Para verificar se a instalação foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documentação, a versão do cURL para Ubuntu mais recente é a 7.81.0.

Copy
curl --version
Se foi apresentado o valor da sua versão, a instalação foi um sucesso.

Instalando Node.js (LTS) e npm
Em seguida é preciso instalar o Node.js (LTS) e npm no nosso sistema.

Para instalar no seu sistema, você pode utilizar um gerenciador de pacotes como o n ou instalar utilizando o NodeSource. Nesse guia iremos utilizar o NodeSource, então basta acessar abrir o seu terminal e executar os comandos abaixo:

Copy
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
Se você já tiver o Node.js instalado em sua máquina, certifique-se que sua versão é a 14 ou mais recente.

Para verificar se a instalação foi um sucesso, basta executar os comandos abaixo:

No momento da escrita dessa documentação, a versão LTS do Node mais recente é a 16.16.0 e do npm é a 8.14.0.

Copy
node -v
npm -v
Git
O git pode já vir instalado na sua distro. Para verificar, basta executar git --version no seu terminal.

Para instalar no seu sistema, basta você executar no seu terminal o comando abaixo:

Copy
sudo apt-get install git
Para verificar se a instalação foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documentação, a versão do Git para Ubuntu mais recente é a 2.34.1.

Copy
git --version
Se foi apresentado o valor da sua versão, a instalação foi um sucesso.

expo-cli
Para instalar no seu sistema, você irá utilizar o seu gerenciador de pacotes npm. Abra o seu terminal e execute o comando:

Copy
npm install -g expo-cli
Caso ocorra um erro dizendo que você não possui permissão (EACESS), siga os passo desse link

Para verificar se a instalação foi um sucesso, basta executar o comando abaixo:

No momento da escrita dessa documentação, a versão do expo-cli mais recente é a 5.5.1.

Copy
expo --version
Se foi apresentado o valor da sua versão, a instalação foi um sucesso.

Caso apareça um erro dizendo que o comando expo não foi encontrado, siga os passos desse link

Expo GO
Com a CLI instalada no seu computador, você consegue criar projetos Expo e executar o metro bundler para servir o seu código, mas para executar o app no seu celular (ou emulador) você precisa instalar o aplicativo Expo GO. Ele é o responsável por pegar o código que o metro bundler envia e exibir em tela o seu app React Native.

Para instalá-lo no seu dispositivo físico, basta buscar nas lojas o aplicativo Expo Go:

Play Store
Apple Store
Para instalá-lo no seu emulador, basta executar o comando expo start e escolher qual emulador você deseja executar. Caso o Expo GO não esteja instalado, ele irá solicitar a sua autourização para instalar a versão necessária.

Emulador
Android
Com o Android Studio, é possível configurar um emulador Android e executar a sua aplicação nele.

Porém, esses emuladores consomem bastante recursos do seu computador. Por isso, se você possui um dispositivo físico Android e sua máquina possui configurações modestas (ex.: ⬇ i3, ⬇ 4gb RAM), é recomendado executar a aplicação no seu dispositivo físico pelo Expo GO.

Para aprender a instalar e configurar o seu emulador, siga esse guia

iOS
Disponível apenas para máquinas macOS. Windows e Linux não suportam iOS simulator.

Executando aplicação
Agora que você possui tudo que é necessário para executar sua aplicação Expo, basta seguir os seguintes passos:

Acesse a pasta do seu projeto pelo terminal
Execute o comando expo start
Abra o app no seu dispositivo via Expo GO
Se for dispositivo físico Android, basta abrir o app Expo GO, selecionar a opção Scan QR code e ler o QR Code apresentado no terminal.
Se for dispositivo físico iOS, basta abrir o app de camera do iOS, ler o QR Code apresentado no terminal e clicar no popup Open with Expo Go app
Se for emulador Android, basta digitar a no terminal.
Seguindo esses passo seu app deve abrir com sucesso no seu dispositivo 🎉




Linux
Capa

Intro
Nesse guia iremos assumir que você já possui o ambiente básico do React Native (Expo Managed Workflow). As dependências desse ambiente são:

cURL
Node.js (LTS);
npm (já vem instalado com o Node);
git
expo-cli
Expo GO (app a ser instalado no dispositivo Android e/ou iOS)
Caso você não possua esse ambiente, siga esses passos

Seguindo para configuração do ambiente Android no Linux utilizando Expo Bare Workflow ou React Native CLI, iremos realizar 2 instalações principais:

JDK 11 (LTS);
Android Studio e dependências.
JDK 11 (LTS)
Se você já tiver o JDK instalado em sua máquina, certifique-se que sua versão seja exatamente a versão 11.

Agora precisamos instalar a JDK (Java Development Kit) na versão 11 (LTS) com o seguinte comando:

Copy
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-11-jdk
Podemos testar a instalação do JDK executando o seguinte comando no terminal:

Copy
java -version
Caso apareça a versão do Java, a instalação foi um sucesso.

Se possuir outras versões do java, você pode selecionar a versão 11 como padrão usando o comando:

Copy
sudo update-alternatives --config java
Android Studio
Preparativos
Android

Crie uma pasta em um local desejado para instalação da SDK. Ex: ~/Android/Sdk

Anote esse caminho para ser utilizado posteriormente

Anote também o endereço de instalação do JDK 11. Exemplo:

Copy
/usr/lib/jvm/java-11-openjdk-amd64
Caso não tenha certeza do caminho, busque na pasta /usr/lib/jvm/ pela pasta referente ao JDK 11, que provavelmente iniciará com java-11.

Com esses caminhos, precisamos configurar algumas variáveis ambiente em nosso sistema. Procure pelo primeiro dos seguintes arquivos existentes no seu sistema: ~/.zshrc ou ~/.bashrc, e adicione essas seis linhas no arquivo (de preferência no início):

Se nenhum desses arquivos existir, crie o ~/.bashrc caso utilize o shell padrão (Bash) ou ~/.zshrc caso utilize o ZSH.

Copy
export JAVA_HOME=CAMINHO_ANOTADO_COM_SUA_VERSÃO
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
Não esqueça de substituir o valor na linha JAVA_HOME pelo caminho que você anotou anteriormente. Além disso, caso esteja utilizando uma pasta diferente para a SDK do Android, altere acima.

Instalação
Acesse a página do Android Studio e clique no botão Download Android Studio.

Vá até a pasta de download e abra o arquivo tar.gz.

Esse arquivo deve possuir uma pasta android-studio dentro. Extraia essa pasta em um local de preferência (Ex.: ~/).

Após a extração, adicione a seguinte variável ambiente no seu sistema:

Copy
export PATH=$PATH:~/android-studio/bin
A adição desse caminho possibilita a execução do Android Studio diretamente pelo terminal com o comando studio.sh. Caso tenha extraído em uma pasta diferente ou alterado o nome da pasta, ajuste o path acima para o que você utilizou.

Agora, abra o terminal (reinicie se já estiver aberto) e execute o seguinte comando:

Copy
studio.sh
Configuração
A primeira janela a ser apresentada deve ser perguntando sobre a importação de configurações de outro Android Studio. Selecione a opção Do not import settings e clique em OK.

Após o carregamento terminar, deve aparecer uma página de Welcome. Clique em Next.

Na sequência, será pedido o tipo de instalação. Escolha a opção Custom e clique em Next.

Nesse momento, será pedido para escolher a localização do pacote JDK instalado. Clique em ⬇ e verifique se a opção JAVA_HOME está apontando para a JDK 11. Se sim, escolha e Clique em Next. Caso contrário, clique no no botão ... e escolha a JDK 11 (você pode inclusive utilizar o caminho anotado no passo anterior para te ajudar).

JDK Location

Em seguida, será perguntado sobre qual tema será utilizado. Escolha o que preferir e clique em Next

Chegamos na etapa mais importante do processo, a instalação da SDK. A janela apresentará algumas opções, marque todas.

SDK Location

SDK é o pacote que vai possibilitar que sua aplicação React Native faça o build. Por padrão, ele instala a última SDK estável;
O Android Virtual Device vai criar um emulador padrão pronto para execução.
Um fator essencial nessa etapa é o caminho de instalação da SDK. Utilize a pasta que você criou na seção Preparativos para o Android Studio (Ex.: ~/Android/Sdk). Não utilize espaços ou caracteres especiais pois causará erros mais para frente.

Se tudo estiver correto, clique em Next.

Na sequência, temos uma janela avisando sobre a possibilidade de executar o Emulador com melhor performance usando o KVM (Kernel-mode Virtual Machine). Essa etapa não irá aparecer para todos pois nem todo computador é compatível com esse recurso. Caso tenha interesse em instalar essa ferramenta, será ensinado como na próxima seção. Finalizada essa etapa, clique em Next.

Em seguida, será apresentada uma janela com um resumo de todas as opções escolhidas até aqui. Verifique se está tudo certo, principalmente os caminhos da SDK e do JDK. Clique em Finish.

Por fim, será realizada a instalação das configurações selecionadas. Quando o programa terminar, clique em Finish.

Caso a instalação e configuração do Android Studio ocorra com sucesso, você deve se deparar com uma tela semelhante a essa:

Android Studio Menu

KVM (Extra)
Caso o seu Android Studio tenha acusado a possibilidade de instalar o KVM e você pretende executar sua aplicação React Native no Emulador, pode prosseguir com esse tutorial. Caso contrário, pode pular para o próximo

Para instalar o KVM, o processo é bem simples. Em sistemas Ubuntu/Debian e Linux Minti, instale o KVM executando o comando:

Copy
sudo apt install qemu-kvm
Em seguida, adicione o seu usuário no grupo do KVM:

Copy
sudo adduser $USER kvm
Por fim, reinicie (ou deslogue e log novamente) o sistema e execute o comando:

Copy
grep kvm /etc/group
Se o resultado for algo semelhante a:

Copy
kvm:x:NUMERO_QUALQUER:SEU_USUARIO
O kvm está instalado corretamente e pronto para uso.

Emulador
Com o Android Studio, é possível configurar um emulador Android e executar a sua aplicação nele.

Porém, esses emuladores consomem bastante recursos do seu computador. Por isso, se você possui um dispositivo físico Android e sua máquina tenha configurações modestas (ex.: ⬇ i3, ⬇ 4gb RAM), é recomendado executar a aplicação diretamente no dispositivo físico.

Para aprender a configurar o seu emulador no Android Studio e executar a sua aplicação React Native nele, clique aqui

Dispositivo Físico
Caso você tenha um dispositivo físico Android, também é possível executar a aplicação diretamente nele. Caso tenha interesse em configurar essa etapa, clique aqui




Android Emulator
Capa

Caso você possua um dispositivo físico Android e seu computador tenha configurações modestas (ex.: ⬇ i3, ⬇ 4gb RAM), é recomendado executar a aplicação diretamente no dispositivo físico. Para configurar seu aparelho, clique aqui

Android Studio
Para criar o seu emulador android, é preciso ter o Android Studio instalado. Abra o programa e, dependendo se você já abriu ou não um projeto android no Android Studio antes, a interface será diferente.

Se você não possui o Android Studio instalado, pode fazê-lo seguindo nossas docs de acordo com o seu sistema operacional (Windows, Linux e macOS).

Se nunca abriu um projeto android nele antes, basta clicar em More Actions no centro da tela e escolher a opção Virtual Device Manager.

AVD Manager

Se já abriu um projeto android antes, basta clicar nos três pontos no canto superior direito e escolher a opção Virtual Device Manager

AVD Manager

Virtual Device Manager
Na sequência, será apresentada uma tela com os emuladores instalados. Se você marcou a opção Android Virtual Device na etapa de configuração do Android Studio, deve aparecer um emulador já configurado e pronto para uso. Caso queira utilizar esse mesmo, pule para a próxima seção clicando nesse link.

Porém, caso queira criar seu próprio emulador, selecione a opção Create Device no canto superior esquerdo.

AVD Default

Nessa etapa, será perguntado qual Hardware você quer selecionar. Como exemplo, escolhi na aba Phone o Pixel 4. Após escolher, clique em Next.

AVD Hardware

Em seguida, você deverá escolher a imagem do sistema (API) do emulador a partir de uma das três listas: Recommended, x86 Images e Other Images. Se essa é sua primeira vez, provavelmente nenhuma imagem estará baixada.

Aqui, a escolha da imagem do sistema vai depender da arquitetura do seu processador.

Sugerimos que escolham exatamente a imagem que recomendarmos abaixo pois é a que testamos por aqui. Outras imagens podem não funcionar corretamente.

Caso o seu processador seja Intel ou AMD, escolha a aba x86 Images e clique no link de Download da imagem S, API Level 31, ABI x86_x64 e Target Android 12.0 (Google APIs).
AVD System Image Choice

Caso o seu processador seja Apple ARM (ex.: M1), escolha a aba Recommended e clique no link de Download da imagem S, API Level 31, ABI arm64-v8a e Target Android 12.0 (Google Play).
AVD System Image Choice

Uma nova janela irá abrir. Aceite as licenças e aguarde a instalação. Quando finalizar, clique em Finish

AVD System Image Installation

Com a sua imagem do sistema baixada, basta escolhê-la e clicar em Next

AVD System Image

Por fim, serão apresentadas algumas configurações do seu emulador (Android Virtual Device - AVD). No canto inferior esquerdo, clique na opção Show Advanced Settings.

AVD Configuration

Deslize a tela até encontrar a opção Memory and Storage. Nela, aumente o Internal Storage até o valor desejado. Por padrão, esse valor vem como 800 MB, o que é muito pouco e acaba causando erro na instalação dos apps React Native no dispositivo.

Sugerimos escolher um valor acima de 4000 MB, no exemplo escolhemos 8000 MB. Definido esse valor, clique em Finish.

AVD Configuration 2

Agora, o seu emulador deve estar aparecendo na lista.

AVD Devices List

Iniciando o Emulador
Com o emulador pronto, basta clicar no botão Play e aguardar o AVD iniciar. Esse processo pode demorar, principalmente na primeira execução.

Quando o emulador terminar de carregar, abra o seu terminal e execute o comando:

Copy
adb devices
Se estiver tudo certo, deve aparecer uma lista com o nome do seu emulador android aberto (normalmente emulator-5554) e status device.

AVD

Executando app no Emulador
Expo Bare Workflow
Para esse passo é preciso que você já tenha criado o seu projeto Expo Bare Workflow. Caso não tenha criado ainda, você pode criar com o comando expo init e escolher o template Bare Workflow.

Agora, com o emulador aberto, basta abrir um terminal, acessar a pasta do seu projeto e executar o comando:

Copy
npm run android
AVD Running Expo app

React Native CLI
Para esse passo é preciso que você já tenha criado o seu projeto React Native CLI. Caso não tenha criado ainda, você pode criar com o comando npx react-native init nomeDoSeuApp

Agora, com o emulador aberto, basta abrir dois terminais e acessar a pasta do seu projeto em cada um deles. Em seguida, execute os comandos:

Terminal 1
Copy
npm start
Terminal 2
Copy
npm run android
AVD Running CLI app







