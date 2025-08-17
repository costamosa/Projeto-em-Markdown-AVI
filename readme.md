# Introdução

 Este relatório tem como objetivo apresentar conceitos fundamentais da área de **Engenharia de Software e Redes de Computadores**, abordando desde ferramentas de versionamento, como **Git e GitHub**, até os principais **protocolos de rede** e conceitos que estruturam a web moderna. 
O conteúdo foi elaborado de forma **didática e objetiva**, destacando o que cada tecnologia é, sua função prática e exemplos de aplicação no dia a dia. 

# Git vs GitHub — O que é cada um e qual sua função?

## Git 


**O que é:**  

O **Git** é um **sistema de controle de versão distribuído** (DVCS). Ele permite acompanhar e gerenciar todas as mudanças feitas em arquivos de um projeto, criando um histórico completo.  
Criado por Linus Torvalds em 2005 diferente de sistemas antigos, o Git é **distribuído**: cada desenvolvedor tem em seu computador uma cópia completa do repositório, incluindo todo o histórico, o que traz **segurança** (não há risco de perder dados se o servidor cair) e **flexibilidade** (é possível trabalhar mesmo sem internet).

**Funções principais:**
-   **Versionar** arquivos: salvar “checkpoints” (_commits_) com mensagens explicando mudanças.
-   **Trabalhar em ramos (branches):** desenvolver novas funcionalidades ou corrigir erros em paralelo sem afetar a versão principal.
-   **Mesclar (merge/rebase):** integrar trabalhos de diferentes branches no projeto principal.
-   **Trabalhar offline:** todo o histórico está disponível localmente, sem depender da nuvem.
    
**Termos-chave:** _repositório (repo), commit, branch, merge/rebase, stash, tag, diff, remote_.

## GitHub


O **GitHub** é uma **plataforma online** (lançada em 2008) que usa o Git como base, mas adiciona recursos de **colaboração e compartilhamento**. Ele funciona como um **repositório remoto** na nuvem, permitindo que equipes trabalhem juntas, de qualquer lugar do mundo, em um mesmo projeto.

**Funções principais:**
-   **Hospedar repositórios Git** na nuvem, facilitando o acesso e backup.
-   **Colaboração:** várias pessoas podem contribuir com código por meio de _pull requests_.
-   **Controle de acesso:** gerencia permissões de quem pode visualizar ou alterar o projeto.
-   **Integrações:** oferece ferramentas extras como _issues_ (tarefas e bugs), _actions_ (automação de testes e deploys) e wikis (documentação).

## Como o Git e o GitHub trabalham juntos

-   O **Git** é o sistema que controla versões dos arquivos.
-   O **GitHub** é a plataforma online onde esses arquivos (repositórios Git) ficam guardados para colaboração.
    
-   Você pode:
     -   Trabalhar diretamente no navegador (criar repo, branch, editar arquivos).
    -   Ou trabalhar no computador e depois **sincronizar** com o GitHub (via _push_ e _pull_).
-   No trabalho em equipe:
     -   Faz **pull** para trazer as últimas mudanças.
     -   Faz **push** para enviar suas alterações.
        
-   O **Git** cuida da fusão (merge) das mudanças e o **GitHub** oferece ferramentas como **pull requests** para gerenciar o fluxo.

**Em resumo**, Git é a ferramenta que controla versões do seu código, Github é a plataforma que utiliza o Git e adiciona recursos de colaboração e hospedagem online.

&nbsp;
# Protocolos de Rede e Comunicação, o que é e pra que servem?

Protocolos de rede e comunicação são conjuntos de regras que organizam e padronizam a troca de dados entre sistemas em redes, como a internet. Sua função é garantir que as informações enviadas de um ponto cheguem ao destino de forma correta e compreensível.
Cada protocolo possui uma finalidade específica e opera em portas padrão, que servem como canais para identificar o tipo de comunicação. A seguir, vamos abordar alguns dos mais importantes: **HTTP, HTTPS, WebSockets, FTP, SSH e SSL**.

### HTTP (HyperText Transfer Protocol)
-   **O que é:** protocolo de comunicação usado para transferir páginas e dados na web.
-   **Para que serve:** permite que navegadores (clientes) solicitem e recebam conteúdos de servidores, como textos, imagens e vídeos.
    -   **Porta padrão:** **80**.

### HTTPS (HyperText Transfer Protocol Secure)

-   **O que é:** versão segura do HTTP, que usa criptografia SSL/TLS para proteger os dados.
-   **Para que serve:** garante que a comunicação entre cliente e servidor seja criptografada, evitando espionagem e ataques.
    -   **Porta padrão:** **443**.

### WebSockets
-   **O que é:** protocolo que permite comunicação **bidirecional** e contínua entre cliente e servidor.
-   **Para que serve:** usado em aplicações que precisam de atualização em tempo real (ex.: chats, jogos online, notificações).
    -   **Porta padrão:** **80** (quando usado com HTTP) e **443** (quando usado com HTTPS).

### FTP (File Transfer Protocol)
-   **O que é:** protocolo para **transferência de arquivos** entre computadores em rede.
-   **Para que serve:** enviar e baixar arquivos de servidores, muito usado em hospedagem de sites.
    -   **Porta padrão:** **21** (comandos) e **20** (transferência de dados).

### SSH (Secure Shell)
-   **O que é:** protocolo de rede seguro para acessar computadores remotamente.
-   **Para que serve:** permite login remoto em servidores, execução de comandos e transferência de arquivos de forma criptografada.
    -   **Porta padrão:** **22**.

### SSL/TLS (Secure Sockets Layer / Transport Layer Security)
-   **O que é:** protocolos de segurança que fornecem criptografia para comunicações na internet. TLS é a evolução do SSL.
-   **Para que serve:** proteger dados sensíveis (como senhas, pagamentos online, informações pessoais).
    -   **Porta padrão:** não tem porta própria, mas é usado em conjunto com outros protocolos (ex.: HTTPS na porta **443**, SMTPS na **465**).

&nbsp;

#	Arquitetura Cliente-Servidor


A **arquitetura cliente-servidor** é um **modelo de comunicação em redes de computadores** no qual há uma divisão clara de papéis:

-   O **cliente** faz solicitações (requisições).
-   O **servidor** processa essas solicitações e devolve respostas.
    
Esse modelo é a base de grande parte da **internet** e dos **sistemas distribuídos** atuais, pois organiza como diferentes dispositivos e serviços interagem.

### Como funciona:
1.  O **cliente** (navegador, aplicativo ou programa) envia um pedido de serviço.
2.  O **servidor** recebe, processa e devolve o recurso solicitado (ex.: página web, arquivo ou dados de banco de dados).
3.  A comunicação é feita por meio de **protocolos de rede**, como HTTP/HTTPS, FTP ou outros.
    
### Exemplos práticos:

-   **Acesso a sites:** o navegador (cliente) solicita a página e o servidor web envia os arquivos.
-   **Aplicativos de mensagens:** o app (cliente) envia a mensagem, o servidor central recebe e entrega ao destinatário.
-   **Jogos online:** o console ou PC (cliente) envia ações dos jogadores e o servidor mantém o estado do jogo em tempo real.

# Funcionamento do DNS e de Proxies

-   **DNS (Domain Name System):** funciona como uma “agenda da internet”. Ele traduz nomes de sites (ex.: `google.com`) para endereços IP que os computadores entendem. Assim, quando você digita um site, o DNS encontra o servidor certo e conecta o navegador até ele.
-   **Proxy:** é um intermediário entre o cliente e o servidor. Ele pode **ocultar o IP**, **filtrar acessos** e até **guardar páginas em cache** para acelerar a navegação. O cliente fala com o proxy, e o proxy fala com o servidor em seu lugar.

# Diferenças entre HTTP e HTTPS

-   **HTTP (HyperText Transfer Protocol):** protocolo usado para transferir dados na web. Ele funciona bem, mas **não possui criptografia**, o que permite que informações sejam interceptadas por terceiros.
    
-   **HTTPS (HyperText Transfer Protocol Secure):** é a versão **segura** do HTTP. Usa **SSL/TLS** para **criptografar** os dados, garantindo privacidade, autenticidade do site e integridade das informações. É hoje o **padrão da web**. Esse padrão você consegue observar o cadeado no link do seu navegador.


#	Principais categorias de códigos HTTP e verbos de requisição
Quando um cliente (como o navegador) faz uma requisição a um servidor, a resposta vem acompanhada de um **código HTTP**, que indica o resultado (sucesso, redirecionamento, erro etc.).  
Além disso, cada requisição usa um **verbo HTTP**, que define a ação desejada — como **buscar**, **enviar**, **atualizar** ou **remover** informações.

### Categorias de Códigos HTTP
-   **2xx – Sucesso:** a requisição foi processada corretamente.
     -   Ex.: **200 OK** (requisição bem-sucedida).
 -   **3xx – Redirecionamento:** o cliente deve acessar o recurso em outro endereço.
     -   Ex.: **301 Moved Permanently** (mudança definitiva).
        
-   **4xx – Erro do Cliente:** problema na requisição feita pelo usuário.
     -   Ex.: **404 Not Found** (página não encontrada).
-   **5xx – Erro do Servidor:** falha no servidor ao tentar responder.
      -   Ex.: **500 Internal Server Error**.
        
Esses códigos muitas vezes aparecem no navegador, como o famoso erro **404** quando uma página não existe, com certeza você já deve ter visto.

### Verbos de Requisição HTTP

-   **GET:** solicita dados do servidor (ex.: abrir uma página).
-   **POST:** envia dados para o servidor (ex.: cadastro, login).
-   **PUT:** substitui/atualiza dados já existentes.
-   **PATCH:** altera apenas parte de um recurso.
-   **DELETE:** remove dados.
-   **HEAD:** retorna apenas os cabeçalhos da resposta, sem o conteúdo.

**Resumindo**, os **códigos HTTP** informam o resultado da requisição, já os **verbos HTTP** indicam a ação que o cliente deseja executar.

# Principais tags do HTML

O **HTML (HyperText Markup Language)** é a linguagem usada para estruturar páginas na web.  
Ele utiliza **tags** (marcadores) que indicam como cada parte do conteúdo deve aparecer ou se comportar no navegador.

### Os principais marcadores(tags) mais utilizados:

-   **`<html>`**: define o início e o fim de um documento HTML.
``` <html>
  <head>
    <title>Exemplo</title>
  </head>
  <body>
    <p>Olá, mundo!</p>
  </body>
</html>
```
-   **`<head>`**: contém informações sobre a página (título, links de estilos, metadados).
```<head>
  <meta charset="UTF-8">
  <title>Minha Página</title>
  <link rel="stylesheet" href="estilos.css">
</head>
```
-   **`<title>`**: define o título da aba do navegador.
```
<title>Página de Exemplo</title>
```
-   **`<body>`**: área onde fica o conteúdo visível (textos, imagens, links etc.).
```
<body>
  <h1>Bem-vindo!</h1>
  <p>Este é o conteúdo visível da página.</p>
</body>
```
-   **`<h1>` a `<h6>`**: títulos e subtítulos, do mais importante (`h1`) ao menos (`h6`).
```
<h1>Título principal</h1>
<h2>Subtítulo</h2>
<h3>Seção</h3>
<h4>Subseção</h4>
<h5>Tópico menor</h5>
<h6>Detalhe</h6>
```
-   **`<p>`**: define parágrafos de texto.
```
<p>Este é um parágrafo de exemplo.</p>
```
-   **`<a>`**: cria links para outras páginas ou seções.
```
<a href="https://www.google.com">Visite o Google</a>
```
-   **`<img>`**: insere imagens.
```
<img src="imagem.jpg" alt="Descrição da imagem">
```
-   **`<ul>` e `<ol>`**: listas (não ordenada e ordenada).
```
<ul>
  <li>Item A</li>
  <li>Item B</li>
</ul>

<ol>
  <li>Primeiro</li>
  <li>Segundo</li>
</ol>
```
-   **`<li>`**: itens dentro de listas.
```
<ul>
  <li>Arroz</li>
  <li>Feijão</li>
  <li>Carne</li>
</ul>
```
-   **`<div>`**: divisão genérica para organizar conteúdo.
```
<div class="caixa">
  <p>Texto dentro da div</p>
</div>
```
-   **`<span>`**: destaca trechos pequenos dentro de um texto.
```
<p>O preço é <span style="color:red;">R$ 50,00</span></p>
```
-   **`<form>`**: cria formulários para enviar dados.
```
<form>
  <label>Nome:</label>
  <input type="text" name="nome">
  <button>Enviar</button>
</form>
```
-   **`<input>`**: campo de entrada em formulários (texto, senha, checkbox etc.).
```
<input type="text" placeholder="Digite seu nome">
<input type="password" placeholder="Digite sua senha">
<input type="checkbox"> Aceito os termos
```
-   **`<button>`**: define botões clicáveis.
```
<button type="submit">Enviar</button>
```

As **tags HTML** dão a “estrutura” da página: algumas organizam o conteúdo (como `<div>` e `<p>`), outras inserem elementos (como `<img>` e `<a>`) e outras criam interatividade (como `<form>` e `<button>`).

# Seletores do CSS

O **CSS (Cascading Style Sheets)** é usado para controlar a **aparência e o layout** das páginas web.  
Os **seletores** são as “chaves” que dizem **quais elementos do HTML** receberão determinado estilo.  
Eles podem selecionar elementos **pela tag**, **pela classe**, **pelo ID** ou até **pela posição** dentro de outros elementos, permitindo desde ajustes simples (como mudar a cor de um texto) até personalizações avançadas no design da página.

### Tipos principais de seletores:
-   **Seletor de elemento:** aplica estilo a todas as tags de um tipo.
``` css

p { color: blue; }
```
Todos os parágrafos `<p>` ficam azuis.

-    **Seletor de classe:** usa o atributo class e é chamado com **.** (ponto).
```css

.destaque { font-weight: bold; }
```
Aplica estilo a elementos com `class="destaque"`


-    **Seletor de ID:** usa o atributo **id** e é chamado com **#** (jogo da velha).
``` css

#menu { background: black; }
```
Aplica estilo ao elemento com `id="menu"`

-    **Seletor universal:** seleciona todos os elementos da página.
``` css

* { margin: 0; padding: 0; }
```
-    **Seletores hierárquicos/combinados:** aplicam estilo baseado na relação entre elementos.
``` css

div p { color: red; }   /* Descendente: todos <p> dentro de <div> */
div > p { color: green; } /* Filho direto: apenas <p> filhos imediatos da <div> */
```

Resumindo, os seletores **CSS** permitem apontar elemtentos específicos do **HTML** para aplicar estilos, com isso eles se tornam fundamentais para dar **personalização**, **organização** e **identidade visual** as páginas.

# O que é uma Webview

   Uma **WebView** é um **componente de software** usado em aplicativos para exibir páginas da web **diretamente dentro do app**, sem precisar abrir um navegador externo.  
    Ela funciona como um **navegador embutido**, mas com **mais controle para o desenvolvedor**, que pode definir quais sites abrir, se permite JavaScript, ou até bloquear certos recursos.  
Por isso, é muito usada em **apps híbridos** (que combinam código nativo e web), pois possibilita que partes do aplicativo sejam construídas em HTML, CSS e JavaScript, mantendo a experiência dentro do próprio app.

### Como funciona:
-   O app usa a WebView para carregar e mostrar conteúdo da web (HTML, CSS, JavaScript).
-   Pode exibir tanto páginas da internet quanto conteúdos locais do próprio aplicativo.
-   O desenvolvedor decide quais sites ou recursos podem ser acessados, dando mais controle e segurança.

### Exemplos práticos

-   **Aplicativos de delivery** (como iFood, Rappi, Uber Eats): partes do app carregam cardápios e informações vindas direto da web.
-   **Aplicativos de e-commerce** (como Shopee, Mercado Livre, Amazon): algumas telas são feitas em WebView para atualizar ofertas e banners em tempo real.
-   **Aplicativos de redes sociais**: quando você clica em um link dentro do Facebook, Instagram ou Twitter, e ele abre sem sair do app, isso é uma WebView.
-   **Aplicativos de banco** que carregam extratos ou serviços via web.
-   **Apps híbridos** parte nativa + parte web.
-   Quando você abre um link dentro de um app (ex.: Instagram ou WhatsApp) sem sair dele.


Resumindo a **WebView** é como um **mini navegador dentro do aplicativo**, permitindo carregar páginas da web sem sair do app.  Ela é muito útil para criar **apps híbridos**, integrar **funcionalidades online** (como cardápios, extratos ou ofertas) e oferecer uma experiência **fluida e controlada** ao usuário.  
Com ela, o desenvolvedor consegue misturar o melhor do **código nativo** com o **conteúdo da web**, sem depender de abrir navegadores externos.


## Referências

- [Documentação oficial no Git.](https://docs.github.com/pt/get-started/start-your-journey/about-github-and-git)  
- [HTML Linguagem de marcação de hipertexto.](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
- [Estruturação do texto.](https://gemini.google.com/app)
- [Criação do Relatório.](https://stackedit.io/app#)

###### Feito por Mosá Costa