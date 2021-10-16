# Documento de Arquitetura de Software

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   30/09/2021   |  1.0  |  Criação do Documento  | Gabriel Batalha,  Lucas Rodrigues
|   01/10/2021   |  1.1  |  Ajustes no tópico 1 e adição dos tópicos 2 e 3  | Gabriel Batalha,  Kleidson Alves,  Lucas Rodrigues
|   04/10/2021   |  1.2  | Atualização dos tópicos | Gabriel Batalha, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan |
|   06/10/2021   |  1.3  | Atualização no tópico de Visão de Dados | Hugo Bezerra, Kleidson Alves, Lucas Gabriel |
|   06/10/2021   |  1.4  | Adição de considerações sobre tamanho e desempenho | Davi Antônio, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan |
|   08/10/2021   |  1.5  | Adição dos tópicos de tamanho e desempenho e qualidade | Davi Antônio, Kleidson Alves, Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan |
|   15/10/2021   |  1.6    | Atualização da Visão de Dados | Hugo Bezerra, Lucas Rodrigues |
|   15/10/2021   |  1.7    | Revisão do Documento | Hugo Bezerra, Lucas Rodrigues |

## 1. Introdução

### 1.1 Propósito

<div style="text-indent: 40px; text-align: justify">
<p>
Esse documento tem o objetivo de oferecer uma visão geral da arquitetura do sistema de software Donner, buscando representar as decisões arquiteturais significativas que foram tomadas pela equipe. Para representar os aspectos do sistema a equipe utilizou diferentes visões da arquitetura, as quais foram documentadas por meio de tabelas, diagramas e outros artefatos produzidos.
</p>
</div>

### 1.2 Escopo

<div style="text-indent: 40px; text-align: justify">

<p>
O escopo desse documento é o Projeto Donner, uma aplicação voltada para fazer a conexão entre doadores e pessoas que necessitam de doação. O foco desse documento é apresentar o modelo de arquitetura utilizado para o desenvolvimento da aplicação e as decisões tomadas pela equipe em relação às modelagens. Dessa forma, busca-se apresentar um melhor entendimento do sistema e da construção de sua arquitetura.
</p>
</div>

### 1.3 Definições, Acrônimos e Abreviações
| Acrônimo | Significado |
| :-------: | :---------: |
|    MVC    | Model-View-Controller |
|   NoSQL   | Not Only Structured Query Language |

### 1.4 Visão Geral
O documento vai estar organizado da seguinte forma:
1. Introdução
2. Representação Arquitetural
3. Objetivos Arquiteturais e Restrições
4. Visão Lógica
5. Visão de Implementação
6. Visão de Dados
7. Tamanho e Desempenho
8. Qualidade

## 2. Representação Arquitetural

<div style="text-indent: 40px; text-align: justify">
<p>
A decisão da equipe para a arquitetura do projeto Donner foi uma arquitetura <ins>Cliente-Servidor</ins>. Nessa representação de arquitetura, o front-end representa o cliente e o Firebase, plataforma desenvolvida pela Google, atua como o servidor. A imagem abaixo ilustra um esquema simples que representa a aplicação dessa arquitetura no projeto Donner. 
</p>
</div>

![](https://i.imgur.com/JTjkHL7.png)

<div style="text-indent: 40px; text-align: justify">
<p>
Em relação ao front-end da aplicação, optou-se por utilizar a arquitetura MVC, pois a equipe julgou como mais adequada para o escopo do projeto.
</p>

<p>
Nesse documento, a arquitetura é representada através de três visões. Elas, com os diagramas que possuem, são:
</p>

</div>

- Visão Lógica: Diagrama de Classe, Diagrama de Sequência, Diagrama de Comunicação e Diagrama de Pacotes
- Visão de Implementação: Diagrama de Componentes
- Visão de Dados: Detalhamento do Banco de Dados. No nosso caso, iremos utilizar um banco de dados NoSQL (Firebase).

## 3. Objetivos Arquiteturais e Restrições

### Objetivos
- Extensibilidade: O software deve ser flexível e fácil de realizar manutenção e evolução.
- Confiabilidade: Devem ser evitadas falhas no funcionamento ou problemas de disponibilidade do software.
- Portabilidade: O software deve funcionar em dispositivos mobile.

### Restrições
- É necessário possuir conexão com a Internet.
- O sistema operacional Android deve ser suportado.
- O software será desenvolvido utilizando o toolkit Flutter e a linguagem de programação Dart.
- Os usuários devem utilizar uma conta do Google para cadastrar e realizar login.

## 4. Visão Lógica

<div style="text-indent: 40px; text-align: justify">
<p>
Representa a estrutura da arquitetura e exibe uma visão lógica do sistema, descrevendo as classes que envolvem o comportamento significativo do sistema em termos de arquitetura para uma melhor compreensão da organização do projeto.
</p>
</div>

### 4.1 Diagrama de Classe

<div style="text-indent: 40px; text-align: justify">
<p>
Foi utilizado, para mostrar as classes significativas, seus relacionamentos, métodos e atributos, o Diagrama de Classe. Abaixo pode ser observado a versão mais recente do diagrama e a versão completa pode ser vista na aba <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_classe">Diagrama de Classe</a>.
</p>
</div>

[![](https://i.imgur.com/Sy8te4n.png)](https://i.imgur.com/Sy8te4n.png)

### 4.2 Diagrama de Sequência
<div style="text-indent: 40px; text-align: justify">

No diagrama de sequência pode ser visualizada a interação entre os objetos do sistema e a ordem na qual as interações ocorrem. Os diagramas de sequência podem ser encontrados na aba <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_sequencia/">Diagrama de Sequência</a>.

</div>

Diagrama de Sequência: Administração de Postagens
[![](https://i.imgur.com/UWS9xMC.png)](https://i.imgur.com/UWS9xMC.png)

### 4.3 Diagrama de Comunicação

<div style="text-indent: 40px; text-align: justify">

O diagrama de comunicação foi utilizado para mostrar a interação entre diferentes partes do sistema. Apesar desse tipo de diagrama ser semelhante ao diagrama de sequência, ele possui foco na estrutura das mensagens transmitidas entre os objetos. Abaixo é mostrada o diagrama de comunicação representando a interação com os anúncios. Os outros diagramas podem ser encontrados na aba <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_comunicacao">Diagrama de Comunicação</a>.

</div>

Diagrama de Comunicação: Interação Anúncios
[![](https://i.imgur.com/JouiJCc.png)](https://i.imgur.com/JouiJCc.png)

### 4.4 Diagrama de Pacotes

<div style="text-indent: 40px; text-align: justify">
<p>
Para ter uma visão geral das camadas envolvidas na aplicação foi utilizado o Diagrama de Modelo, que é um diagrama estrutural auxiliar do Diagrama de Pacotes. A página completa pode ser encontrada na aba <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_pacotes">Diagrama de Pacotes</a>.
</p>
</div>

Diagrama de Pacotes: Modelo
[![](https://i.imgur.com/UQaAgnS.png)](https://i.imgur.com/UQaAgnS.png)

## 5. Visão de Implementação

<div style="text-indent: 40px; text-align: justify">
<p>
Descreve de forma geral o modelo de implementação para fornecer uma base que permitirá compreender a distribuição física do sistema em um conjunto de nós de processamento. A visão de implementação é refinada durante cada iteração.
</p>
</div>

### 5.1 Diagrama de Componentes

<div style="text-indent: 40px; text-align: justify">
<p>
Para a compreensão dos relacionamentos entre os componentes que constituem o sistema e de como cada componente interage com o restante do sistema foi utilizado o diagrama de componentes. A página completa pode ser encontrada na aba <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_componentes">Diagrama de Componentes</a>.
</p>
</div>

[![](https://i.imgur.com/GDI3YTT.png)](https://i.imgur.com/GDI3YTT.png)

## 6. Visão de Dados
<div style="text-indent: 40px; text-align: justify">
<p>
Esta visão é essencial ao projeto, pois ela diz respeito a camada de persistência. A visão de dados descreve o modelo de dados do sistema, apresentando um maior detalhamento de como o banco de dados está organizado.
</p>
</div>

### 6.1 Banco de Dados

<div style="text-indent: 40px; text-align: justify">
<p>
Em relação ao banco de dados da nossa aplicação, iremos utilizar o Firebase e com isso a implementação do banco de dados é feita com o Cloud Firestore, que "é um banco de dados de documentos NoSQL que permite armazenar, sincronizar e consultar dados facilmente para seus apps para dispositivos móveis e da Web, em escala global".


A base será composta por 5 categorias de documentos, sendo eles Users, Posts, Comments, Categories e Campaigns, onde um anúncio pertence a um usuário dono e um usuário pode possuir múltiplos anúncios (Posts). Esse relacionamento também pode ser observado no <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_comunicacao">Diagrama de Comunicação</a> e principalmente no documento de <a href="https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/arquitetura/database">Banco de Dados</a>.

</p>
</div>

|Users|Posts|Comments|Categories|Campaigns|
|--|--|--|--|--|
|city|categoryId|id|id|id|
|description|description|owner|description|description|
|email|id|post||start|
|id|isDonation|text||end|
|name|owner|||title|
|phone|title|
|photoUrl|
|state|

## 7. Tamanho e Desempenho
<div style="text-indent: 40px; text-align: justify">
<p>
O sistema será desenvolvido com foco em suportar até 10000 usuários mensais, mantendo um tempo médio de resposta 2 segundos para suas requisições e, inicialmente, a base de dados não ultrapassará 1 GiB de tamanho.
</p>
</div>

## 8. Qualidade
<div style="text-indent: 40px; text-align: justify">
<p>
O uso da arquitetura MVC com camada de persistência baseada no Cloud Firestore facilita a extensibilidade do projeto, pois garante a possibilidade de atender milhares de usuários mensais com possibilidade de aumento dos limites em planos pagos. Além disso, implica na confiabilidade, pois o sistema permanece disponível enquanto o Google Cloud estiver online. Por fim, garante a portabilidade, pois há bibliotecas para integração do serviço Cloud Firestore para as principais plataformas do mercado de aplicações móveis (Android, iOS e Web).
</p>
</div>

### Implicações
<div style="text-indent: 40px; text-align: justify">
<p>
O uso do Cloud Firestore traz implicações de privacidade, pois os dados dos usuários estão sujeitos às Políticas de Privacidade do Google. Também pode haver dificuldade de controlar os custos, pois em casos de se aplicar os planos pagos as cobranças são feitas com base nas interações dos usuários, o que pode causar altos custos inesperados.
</p>
<p>
O uso de um sistema de banco de dados NoSQL pode causar dificuldades em migrar o sistema para serviços semelhantes, e não implementa alguns recursos que facilitam buscas complexas oferecidos em sistemas tradicionais.
</p>
</div>

## Referências

> Documento de Arquitetura de Software. Disponível em [http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf](http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf). Data de acesso: 30/09/2021

> Artefato: Documento de Arquitetura de Software. Disponível em : [https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html](https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html). Data de acesso: 30/09/2021

> Sistemas Cliente-Servidor. Disponível em : [http://www.inf.ufsc.br/~r.fileto/Disciplinas/BD-Avancado/Aulas/03-ClienteServidor.pdf](http://www.inf.ufsc.br/~r.fileto/Disciplinas/BD-Avancado/Aulas/03-ClienteServidor.pdf). Data de acesso: 01/10/2021

> Exemplos de Arquitetura de Software . Disponível em : [https://www.marcosmonteiro.com.br/mm/Cursos/Arquitetura_Software/Exemplos_de_Arquiteturas.pdf](https://www.marcosmonteiro.com.br/mm/Cursos/Arquitetura_Software/Exemplos_de_Arquiteturas.pdf). Data de acesso: 01/10/2021

> Introdução ao Padrão MVC. Disponível em : [https://www.devmedia.com.br/introducao-ao-padrao-mvc/29308](https://www.devmedia.com.br/introducao-ao-padrao-mvc/29308). Data de acesso: 01/10/2021

> Donar. Disponível em : [http://repositorio.aee.edu.br/bitstream/aee/1106/3/TCC2_2018_2_GabrielLeiteDias_MatheusLimadeAlbuquerque_Apendice2.pdf](http://repositorio.aee.edu.br/bitstream/aee/1106/3/TCC2_2018_2_GabrielLeiteDias_MatheusLimadeAlbuquerque_Apendice2.pdf). Data de acesso: 04/10/2021

> Google. Uso e limites do Firebase Cloud Firestore. Disponível em: [https://firebase.google.com/docs/firestore/quotas](https://firebase.google.com/docs/firestore/quotas). Acesso em: 08/10/2021.

> Google. Plano de preços do Firebase. Disponível em: [https://firebase.google.com/pricing/](https://firebase.google.com/pricing/). Acesso em: 08/10/2021