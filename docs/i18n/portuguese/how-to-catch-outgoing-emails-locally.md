> **Observação:** esta é uma etapa **opcional** e é necessária somente quando trabalhando com fluxos de e-mail

- [Introdução](#introduction)
- [Instalando o MailHog](#installing-mailhog)
- [Usando o MailHog](#using-mailhog)
- [Links úteis](#useful-links)

## Introdução

Alguns fluxos de e-mail, como atualizar o e-mail de um usuário, requerem que o servidor da api do back-end envie e-mails de saída. Uma alternativa ao uso de um provedor de serviço de e-mail para enviar mensagens reais de e-mail é o Mailhog. Ele é uma ferramenta de desenvolvedor para teste de e-mail que vai pegar as mensagens de e-mail enviadas pela sua instância de freeCodeCamp.

## Instalando o MailHog

O MailHog pode ser instalado no macOS, Windows e Linux ou usado via Docker

<details><summary>Instalando o MailHog no Docker</summary>

Se você tem o Docker instalado, então você pode usar

```bash
docker run -d --name mailhog --rm mailhog/mailhog
```

para iniciar o MailHog em segundo plano e

```bash
docker stop mailhog
```

para para-lo.

Quando a instalação for concluída, você pode começar a [usar o MailHog](#using-mailhog). </details>

<details><summary>Instalando o MailHog no macOS</summary>

Instale o MailHog no macOS com o [Homebrew](https://brew.sh/):

```bash
brew install mailhog
brew services start mailhog
```

Os comandos acima iniciarão um serviço do mailhog em segundo plano.

Quando a instalação for concluída, você pode começar a [usar o MailHog](#using-mailhog). </details>

<details><summary>Instalando o MailHog no Windows</summary>

Baixe a versão mais recente do MailHog no [repositório oficial do MailHog](https://github.com/mailhog/MailHog/releases). Localize e clique no link para a sua versão do Windows (32 ou 64 bits) e um arquivo .exe será baixado no seu computador.

Quando o download terminar, clique para abrir o arquivo. Uma notificação de firewall do Windows pode aparecer, solicitando permissão de acesso para MailHog. Um prompt de linha de comando padrão do Windows abrirá onde o MailHog será executado quando o acesso ao firewall for concedido.

Feche o MailHog fechando a janela do prompt. Para iniciar o MailHog novamente, clique no executável do MailHog (.exe) arquivo que foi baixado inicialmente - não é necessário baixar um novo arquivo de instalação do MailHog.

Comece a [usar o MailHog](#using-mailhog). </details>

<details><summary>Instalando o MailHog no Linux</summary>

Primeiro, instale o [Go](https://golang.org).

Execute os seguintes comandos para instalar GO em sistemas baseados em Debian, como o Ubuntu e o Linux Mint.

```bash
sudo apt-get install golang
```

Execute os seguintes comandos para instalar GO em sistemas baseados em RPM, como CentOS, Fedora, Red Hat Linux, etc.

```bash
sudo dnf install golang
```

Como alternativa, execute os seguintes comandos para instalar o GO.

```bash
sudo yum install golang
```

Agora defina o caminho para o Go com os seguintes comandos.

```bash
echo "export GOPATH=$HOME/go" >> ~/.profile
echo 'export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin' >> ~/.profile
source ~/.profile
```

Finalmente, digite os comandos abaixo para instalar e executar MailHog.

```bash
go get github.com/mailhog/MailHog
sudo cp /home/$(whoami)/go/bin/MailHog /usr/local/bin/mailhog
mailhog
```

Comece a [usar o MailHog](#using-mailhog). </details>

## Usando o MailHog

Abra uma nova guia ou janela do navegador e navegue até [http://localhost:8025](http://localhost:8025) para abrir sua caixa de entrada do MailHog quando a instalação do MailHog for concluída e o MailHog estiver em execução. A caixa de entrada será similar à imagem abaixo.

![Captura de tela do MailHog 1](https://contribute.freecodecamp.org/images/mailhog/1.jpg)

E-mails enviados pela instalação do seu freeCodeCamp aparecerão assim

![Captura de tela MailHog 2](https://contribute.freecodecamp.org/images/mailhog/2.jpg)

Duas guias que permitem que você veja texto simples ou conteúdo fonte estarão disponíveis quando você abrir um determinado e-mail. Certifique-se de que a aba de texto simples esteja selecionada como abaixo.

![Captura de tela MailHog 3](https://contribute.freecodecamp.org/images/mailhog/3.jpg)

Todos os links no e-mail devem ser clicáveis e redirecionar para a URL deles.

## Links úteis

- Confira o repositório [MailHog](https://github.com/mailhog/MailHog) para mais informações relacionadas ao MailHog. Informações adicionais também estão disponíveis sobre configurações personalizadas do MailHog.
