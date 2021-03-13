# Fundamentos de Arquitetura de Sistemas

## Conteúdos
1.[Vantagens e desenvolvimento de Web Services](#)

## Vantagens e desenvolvimento de Web Services
### O que são Web Services
    São soluções para aplicações se comunicarem independente de lingaguem, softwares e hardwares utilizados.
    Inicialmente os Web Services foram criados para troca de mensagens utilizando a linguagem XML sobre o protocolo HTTP sendo identificado por URI.
    Web Services são API's que se comunicam por meio de redes sobre o protocolo HTTP.
    O Web Service tem acesso ao banco de dados e disponibiliza um URI para que outra aplicação possa acessar essas URI e os dados possam ser trocados.
    A troca de informações são feitas através das linguagens de marcação: XML ou JSON.
    O Web service pode receber uma requisição na sua URI e pode também receber informações em XML ou JSON para que essas informações possam ser tratadas, por exemplo: Requisições POST em que se envia dados ao banco de dados.
    XML => Tags; JSON => Chave e Valor
    Vantagens: Linguagem comum de comunicação; Integração; Reutilização de implementação; Segurança; Custos;
    Principais Tecnologias: SOAP; REST; XML; JSON;
### Estrutura SOAP
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
    