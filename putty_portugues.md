# PuTTY

## Sobre o PuTTY

Este documento contém informações sobre o PuTTY, seu funcionamento e suas principais aplicações.

### O que é o PuTTY?

O PuTTY é um software open source gratuito utilizado como emulador de terminal. Ele permite o acesso remoto a servidores e ativos de rede através de protocolos como SSH, RLogin e Telnet.

Além disso, o PuTTY implementa diversos procedimentos de segurança para criptografar dados durante a comunicação entre os sistemas.


### Funcionalidade

O PuTTY funciona como um cliente de conexões seguras, oferecendo uma interface configurável.

Através de comandos simples, é possível enviar e alterar arquivos, corrigir bugs, instalar aplicações, reiniciar o sistema, entre vários outros gerenciamentos feitos de um servidor para o outro.


### Aplicabilidade

- Acessar computadores e ativos de rede remotamente.
-  Viabilizar comunicações seguras entre servidores, mesmo em redes públicas.
- Comprimir dados extensos durante transferências, otimizando a conexão sem afetar o desempenho do programa.



## Como instalar o PuTTY

Confira os passos para baixar e instalar o PuTTY em sua máquina.

 1. Acesse putty.org.
 2. Clique em **Download PuTTY**.
 3. Selecione a versão compatível com seu sistema (32 ou 64 bits).
 4. Escolha a pasta de destino para o instalador do PuTTY e aperte **Salvar**.

Com o download concluído, siga para as próximas etapas:

 1. Abra o instalador do PuTTY na pasta em que foi salvo.
 2. Clique em **Next** para seguir com a instalação.
 3. Escolha a pasta de destino e aperte o botão **Next** novamente.
 4. Pressione **Install**.
 5. Conclua a instalação em **Finish**.


## Como mover arquivos no Windows via SSH no PuTTY

Este tutorial apresenta o passo a passo necessário para mover arquivos em um servidor Windows a partir de outro Windows usando o protocolo SSH no PuTTY.

> :warning:  **Importante** <br>
> Caso ainda não tenha o PuTTY, confira o tutorial [Como instalar o PuTTY](https://fakesiteportfolio.com).


### Passo 1: Configurar o OpenSSH no Windows

Para uma conexão bem-sucedida, o OpenSSH precisa estar configurado no servidor de destino.

 1. Pelo menu **Iniciar**, vá até **Configurações > Sistema > Recursos Opcionais**.
 2. Confira se o OpenSSH já está na lista. Se não estiver, clique em **Exibir recursos** na parte superior da página.
 3. Encontre **Cliente do OpenSSH** e **Servidor do OpenSSH** e selecione **Instalar**.
 4. No menu **Iniciar**, acesse **Serviços**.
 5. Na tela exibida, clique duas vezes em **Servidor OpenSSH SSH**.
 6. Na aba **Geral**, clique em **Tipo de inicialização** e escolha a opção **Automático**.
 7. Pressione **OK**.

Também é possível instalar o OpenSSH com o PowerShell 5.1 ou posterior. Para saber mais, consulte o guia [Como instalar o OpenSSH no Windows com o PowerShell](https://fakesiteportfolio.com).

### Passo 2: Abrir uma sessão no PuTTY

 1. No servidor de origem, abra o PuTTY na categoria **Session** e preencha as seguintes informações:
 a. **Host Name**: insira o endereço IP do servidor de destino (o IP pode ser encontrado em **Configurações > Rede e Internet > Wi-Fi > Propriedades**, na linha **Endereço IPv4**).
 b. **Connection type**: selecione a opção **SSH**.
 c. **Saved Sessions**: nomeie o servidor de destino.
 5. Para salvar os dados, clique em **Save**. Para iniciar a conexão, clique em **Open**.
 6. O terminal será exibido e uma mensagem de primeiro acesso surgirá na tela. Pressione **Accept** para seguir com a conexão.
7. Login e senha serão solicitados. Preencha com as informações da conta Microsoft do servidor de destino.

Com isso, os servidores estarão conectados e você já poderá executar comandos remotamente.


### Passo 3: Executar o comando para mover arquivos

Para mover arquivos dentro de um servidor Windows, execute o comando ```move``` seguido do caminho original do arquivo e para onde ele deve ser movido. Exemplo: `move C:\Users\nomedousuario\Documents\arquivo.txt C:\Users\nomedousuario\Destino`

Para indicar o sucesso da ação, a tela exibirá a mensagem **"1 arquivo(s) movido(s)"**.

Esse comando também pode ser usado para renomear um arquivo. Para isso, o caminho de destino será o mesmo de origem, alterando apenas o nome do arquivo para o desejado. Exemplo: `move C:\Users\nomedousuario\Documents\arquivo.txt C:\Users\nomedousuario\Documents\arquivonovo.txt`

>:grey_exclamation: **Info** <br>
>Se o nome do arquivo tem espaços, use aspas em ambos os caminhos. Exemplo:`move "C:\Users\nomedousuario\Documents\arquivo exemplo.txt" "C:\Users\nomedousuario\Destino"`

Para executar outras ações remotas com o PuTTY, confira o artigo [Comandos do PuTTY](https://fakesiteportfolio.com).






## Referência para Session

Neste artigo você encontrará informações sobre a tela Session, a principal do PuTTY. Nessa tela são informados os dados necessários para a conexão entre servidores.

> :grey_exclamation: **Info** <br>
> Para conferir explicações adicionais sobre a tela, clique no ícone **?** no lado superior direito. Uma interrogação aparecerá ao lado do cursor do mouse, indicando que o modo ajuda foi habilitado. Feito isso, clique em algum campo e uma janela será exibida com informações sobre ele.

### Basic options for your PuTTY session

| **Item** | **Descrição** | 
:--- | :--- 
| **Host Name (or ip address)** | Nome ou endereço IP  do servidor de destino. |
| **Port** | Seção preenchida automaticamente ao selecionar um tipo de conexão. |
| **Connection type** | O tipo de protocolo a ser escolhido. |


### Load, save or delete a stored session


 - **Saved Sessions**: campo para nomear o servidor de destino.
 - **Load**: botão para carregar o servidor selecionado.
 - **Save**: botão para salvar o nome e as informações já preenchidas sobre o servidor de destino.
 - **Delete**: botão para deletar o servidor selecionado.

### Close window on exit

 - **Always**: ao habilitar essa opção, a janela do terminal será sempre fechada ao fim de uma sessão.
 - **Never**: ao habilitar essa opção, a janela do terminal permanecerá aberta, mas inativa, ao fim de uma sessão.
 - **Only on clean exit**: ao habilitar essa opção, a janela do terminal será fechada se a sessão for encerrada normalmente. Caso a sessão finalize por um problema de conexão, a janela do terminal permanecerá aberta.

