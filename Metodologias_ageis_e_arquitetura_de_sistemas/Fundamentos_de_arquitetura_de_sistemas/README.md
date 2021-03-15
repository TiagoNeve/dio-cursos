# Fundamentos de Arquitetura de Sistemas

## Conteúdos
1.[Vantagens e desenvolvimento de Web Services](#)

## Vantagens e desenvolvimento de Web Services
### 1. O que são Web Services
    São soluções para aplicações se comunicarem independente de lingaguem, softwares e hardwares utilizados.
    Inicialmente os Web Services foram criados para troca de mensagens utilizando a linguagem XML sobre o protocolo HTTP sendo identificado por URI.
    Web Services são API's que se comunicam por meio de redes sobre o protocolo HTTP.
    O Web Service tem acesso ao banco de dados e disponibiliza um URI para que outra aplicação possa acessar essas URI e os dados possam ser trocados.
    A troca de informações são feitas através das linguagens de marcação: XML ou JSON.
    O Web service pode receber uma requisição na sua URI e pode também receber informações em XML ou JSON para que essas informações possam ser tratadas, por exemplo: Requisições POST em que se envia dados ao banco de dados.
    XML => Tags; JSON => Chave e Valor
    Vantagens: Linguagem comum de comunicação; Integração; Reutilização de implementação; Segurança; Custos;
    Principais Tecnologias: SOAP; REST; XML; JSON;
### 2. Estrutura SOAP
    SOAP - Simple Object Access Protocol
    Protocolo baseado em XML para acessar serviços web principalmente por HTTP
    Foi desenvolvido para resolver integrações entre aplicações.
    Independente de plataforma e software.
    Meio de transporte genérico, ou seja, pode ser usado por outros protocolos além do HTTP.
    XML - Extensible Markup Language
    Linguagem de marcação criada na década de 90 pela W3C
    Facilita a separação de conteúdo
    Não tem limitação de criação de tags
    Linguagem comum para integrações entre aplicações.
    SOAP Message -> Possui uma estrutura única que deve ser seguida: 
    SOAP Envelope: Tudo fica dentro nessa tag. Primeiro elemento do documento e é usado para encapsular toda a mensagem SOAP.
    SOAP Header: Titulo das informações que serão transmitidas. Elemento onde possui informações de atributos e metadados da requisição.
    SOAP Body: Conteúdo da informação. Elemento que contém os detalhes da mensagem
    
### 3. Entendendo o que é WSDL e XSD
    WSDL - Web Services Description Langauge => Contrato de serviços
    Usado para descrever Web Services, funciona como um contrato do serviço
    A descrição é feito em um documento XML, onde é descrito o serviço, especificações de acesso, operações e métodos.
    XSD - XML Schema Definition
    É um schema no formato XML usado apra definir a estrutura de dados que será validada no XML.
    O XSD functiona como uma documentação de como deve ser montado o SOAP Message (XML) que será enviado através de Web Service
    soapui.com => Ferramenta de verificação de URI que respondem um SOAP
### 4. Aprenda o que são REST, API e JSON
    REST - Representational State Transfer
    É um estilo de arquitetura de software que define a implmentação de um serviço web.
    Podem trabalhar com os formatos XML, JSON ou outros.
    Permite integrações entre aplicações e também entre cliente e servidor em páginas web e aplicações
    Utiliza dos métodos HTTP para definir a operação que está sendo efetuada
    Arquitetura de fácil compreensão
    Quando uma aplicação web disponibiliza um conjunto de rotinas e padrões através de serviços web podemos chamar esse conjunto de API.
    API - Application Programming Interface
    São conjuntos de rotinas documentados e disponibilizados por uma aplicação para que outras aplicações possam consumir suas funcionalidades
    Ficou popular com o aumento dos web services
    As maiores plataformas de tecnologia disponibilizam APIs para acessos de suas funcionalidades, algumas delas são: Facebook, Twitter, Telegram, Whatsapp, GitHub...
    GET - Solicita a representação de um recurso
    POST - Solicita a criação de um recurso
    DELETE - Solicita a exclusão de um recurso
    PUT - Solicitar a atualização de um recurso
    JSON - JavaScript Object Notation
    Formatação leve utilizada para troca de mensagens entre sistemas.
    Usa-se de uma estrutura de chave e valor e também de listas ordenadas
    Um dos formatos mais populares e mais utilizados para troca de mensagens entre sistemas.
### 5. Veja sobre integração com REST e métodos HTTP na prática
    * Código de Estado
    Usado pelo servidor para avisar o cliente sobre o estado da operação solicitada
    1xx -> Informativo
    2xx -> Sucesso
    3xx -> Redirecionamento
    4xx -> Erro do Cliente
    5xx -> Erro do Servidor

## Conceitos de arquitetura em aplicações para Internet

### 1. introdução a arquitetura de sistemas
    Monolito: Clientes se conectam no servidor atraǘes de HTTP e o servidor executa as requisições do cliente
    Microserviços: Serviços dividios em nós que podem fazer coisas difrentes e ter responsabilidades diferentes, um serviço terá cada aplicação e responsabilidade, que podem ter conexões com bando de dados ou serviços externos e até próprios serviços internos. Existe várias formas de utilizar e organizar uma arquitetura de microserviços, vale a pena dar uma olhada em cada uma.
### 2. Comparando os modelos Monolito e Microserviços
    Monolito: Pros => Baixa complexidade, Monitoramento simplificado
    Contas => Stack única, Compartilhamento de recursos, Acoplamento, Mais complexo a escalabilidade
    Microserviços #1: Pros => Stack dinâmica, Simples escalabilidade
    Contra => Acoplamento, Monitoramento mais complexo, Provisionamento mais complexo
    Microserviços #2: Pros => Stack dinâmica, Simples escalabilidade, Desacoplamento
    Contra => Monitoramento mais complexo, Provisionamento mais complexo
    Microserviços #3: Pros => Stack dinâmica, Simples escalabilidade, Desacoplamento, Menor complexidade
    Contra => Provisionamento mais complexo, Plataforma inteira depende do gerenciador de pipeline
### 3. Gerenciamento de erros e volume de acesso
    Mais complexo em processos assíncronas e nos pipeline, a solução é criar um Dead letter queue, Filas de re-tentativas

## A arquitetura de aplicações móveis e internet das coisas

### 1. Conceitos da Internet das Coisas
    Conhecimentos fundamentais da internet. A internet das coisas são uma forma de coisas, objetos, possam acessar a internet e dessa
    maneira conseguir criar uma rede pessoal própria que se comuniquem entre si.
    Usar as Coisas, Nuvens e Inteligência. Basicamente as coisas vão se conectar com as Nuvens e a inteligência utiliza as Nuvens para 
    obter os dados ali presente e executar tarefas, rotinas.
    Utiliza sensores para poder estabelecer uma automação nas residências.
    Utiliza em wearables e na agricultura. Também em controle de veículos e também em cadeias de suprimentos.
    É possível utilizar a energia eficiente com IOT.
    Computação Ubíqua -> Quando a tecnologia toma conta das novas vidas, em que a tecnologia está completamente incorporada em nossas vidas.
    Desafios da Internet das Coisas -> Privacidade e Segurança; Quantidade exponencial de dispositivos conectadas na rede; Ser capaz de processar e armazenar uma enorme quantidade de informações; Gerar valor a partir dos dados coletados; 