---
tags: Arquitetura
---

# Reutilização de Software

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|  30/09/2021   |  1.0  |  Criação do Documento | Davi Antônio, Kleidson Alves, Lucas Gabriel , Lucas Rodrigues, Wellington Jonathan |
|   08/10/2021   |  1.1  |  Adição de Conteúdo ao Documento | Kleidson Alves, Lucas Rodrigues |
|   10/10/2021   |  1.2  |  Adicionar todas as bibliotecas | Davi Antônio da Silva Santos |
|   14/10/2021   |  1.3  |  Adicionando novas bibliotecas | Gabriel Batalha, Hugo Bezerra, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan |
|   15/10/2021   |  1.4  | Revisão do Documento | Hugo Bezerra, Lucas Rodrigues |

## Introdução
<div style="text-indent: 40px; text-align: justify">
<p>
A reutilização de software consiste no uso de soluções previamente elaboradas para a criação de um novo software. Essa reutilização pode ser aplicada em diferentes níveis do desenvolvimento do software, tais como no nível de requisitos, de design e de código. 
</p>
<p>
Há algumas técnicas que podem ser aplicadas para fazer a reutilização de software. Por exemplo, uso de frameworks, bibliotecas, engenharia de software baseada em componentes e arquitetura orientada a serviços. 
</p>
<p>
A decisão de aplicar essa estratégia de desenvolvimento de software está baseada nos objetivos de se diminuir os custos relacionados à manutenção e de realizar entregas mais rápidas, ainda mantendo a qualidade do produto de software. 
</p>
<p>
Esse documento tem o objetivo de apresentar como a reutilização foi aplicada no processo de desenvolvimento do projeto Donner, apresentando o Framework e as Bibliotecas utilizadas.
</p>
</div>

## Framework
<div style="text-indent: 40px; text-align: justify">
<p>
Um framework é uma aplicação parcialmente completa que possui uma coleção de interfaces e classes abstratas e concretas, formando uma estrutura genérica e permitindo reutilização por uma determinada categoria de software. Quando especializado, é capaz de produzir aplicações personalizadas.
</p>
</div>

### Flutter
<div style="text-indent: 40px; text-align: justify">
<p>
O framework utilizado para o desenvolvimento da aplicação Donner foi o Flutter. O Flutter é um framework de código aberto, desenvolvido pela Google, que tem como objetivo facilitar o desenvolvimento de aplicações mobile, tanto para Android quanto para IOS. Ele possui como linguagem base o Dart. Ao criar uma aplicação com o Flutter, o código é compilado para a linguagem base do dispositivo, tornando as aplicações realmente nativas. 
</p>
</div>


#### Hot-spots

<div style="text-indent: 40px; text-align: justify">
<p>
Os hot-spots representam aspectos variáveis de um framework projetados para serem genéricos e adaptados de acordo com as necessidades da aplicação. Alguns exemplos de hot-spots são as classes abstratas e os métodos abstratos. No projeto Donner, foram aplicados os seguintes <i>hot-spots</i>:
</p>
</div>

- **Widgets**: Os widgets podem ser entendidos como componentes personalizados utilizados para definir a interface da aplicação.



#### Frozen-spots

<div style="text-indent: 40px; text-align: justify">
<p>
O frozen-spots representam os aspectos imutáveis do framework para todas as aplicações, ou seja, não foram projetados para serem adaptados. Alguns exemplos de frozen-spots são as classes concretas e os métodos template.
</p>
</div>

- **StatelessWidget**: Um widget sem estado interno mutável. Não consegue ser modificado facilmente, e pode ter somente alguns de seus métodos sobrescritos


## Bibliotecas

<div style="text-indent: 40px; text-align: justify">
<p>
Em uma aplicação desenvolvida com o framework Flutter, o conceito de bibliotecas é entendido como <i>packages</i>, que são códigos modulares que podem ser facilmente compartilhados. No desenvolvimento da aplicação Donner, foram utilizados os seguintes <i>packages</i>:
</p>

</div>


- **material**: Biblioteca de UI básica do Flutter. Desenvolvida pela Google para permitir que os Widgets implementem o Material Design
- **font_awesome_flutter/font_awesome_flutter.dart**: Biblioteca que disponibiliza um conjunto de Ícones para o Flutter 
- **google_fonts**: Biblioteca de UI desenvolvida pela Google que permite o uso das fontes TrueType e OpenType disponíveis em fonts.google.com
- **mask_text_input_formatter**: Pacote com funções para formatação de texto de entrada
- **flutter_lints**: Pacote responsável por analisar código Dart e encorajar as boas práticas de programação
- **firebase_core**: permite que o programa acesse recursos básicos do Firebase usando a API Core
- **firebase_auth**: permite o uso da API de autenticação do Firebase (e-mail e senha, contas em provedores externos, número de telefone ou anônimo)
- **firebase_storage**: Biblioteca utilizada para acessar a API de armazenamento em nuvem do Firebase 
- **cloud_firestore**: permite o uso da API Cloud Firestore, que disponibiliza um banco de dados NoSQL hospedado em nuvem
- **google_sign_in**: permite o uso da autenticação segura do Google
- **shared_preferences**: permite leitura e escrita de dados no formato chave e valor usando métodos de armazenamento nativos
- **image_picker**: Plugin responsável por selecionar imagens da galeria IOS/Android ou tirar fotos com a câmera
- **dropdown_search**: widget já montado de um elemento dropdown com funcionalidade de pesquisa
- **estados_municipios**: Biblioteca que permite buscar todos os estados do Brasil e os municípios dos estados 

## Referências
> Reúso de Software. Disponível em:
[https://www.inf.ufpr.br/silvia/ES/reuso/reusoAl.pdf](https://www.inf.ufpr.br/silvia/ES/reuso/reusoAl.pdf). Data de acesso: 08/10/2021

> Reutilização de Software - Revista Engenharia de Software Magazine 39. Disponível em: [https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956](https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956). Data de acesso: 08/10/2021

> Flutter: Saiba tudo sobre esse novo framework. Disponível em: [https://www.opus-software.com.br/flutter-framework/](https://www.opus-software.com.br/flutter-framework/). Data de acesso: 08/10/2021.

> O que é Flutter? Disponível em: [https://www.treinaweb.com.br/blog/o-que-e-flutter](https://www.treinaweb.com.br/blog/o-que-e-flutter). Data de acesso: 08/10/2021

> Flutter: O que são widgets e qual sua importância?. Disponível em: [https://www.treinaweb.com.br/blog/flutter-o-que-sao-widgets-e-qual-sua-importancia](https://www.treinaweb.com.br/blog/flutter-o-que-sao-widgets-e-qual-sua-importancia). Data de acesso: 08/10/2021