# Documento de Arquitetura

## Versionamento
| Data | Versão | Descrição | Autores |
| -------- | -------- | -------- | ---|
|   30/09/2021   |  1.0  |  Criação do Documento  | Gabriel Batalha,  Lucas Rodrigues
|   01/10/2021   |  1.1  |  Ajustes no tópico 1 e adição dos tópicos 2 e 3  | Gabriel Batalha,  Kleidson Alves,  Lucas Rodrigues
|   04/10/2021   |  1.2  | Atualização dos tópicos | Gabriel Batalha, Kleidson Alves,Lucas Gabriel, Lucas Rodrigues, Wellington Jonathan |

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
A decisão da equipe para a arquitetura do projeto Donner foi uma arquitetura <ins>Cliente-Servidor</ins>. Nessa representação de arquiteura, o frontend representa o cliente e Firebase, plataforma desenvolvida pela Google, atua como o servidor. A imagem abaixo ilustra um esquema simples que representa a aplicação dessa arquitetura no projeto Donner. 
</p>

![](https://i.imgur.com/JTjkHL7.png)

<p>
Em relação ao frontend da aplicação, optou-se por utilizar a arquitetura MVC, pois a equipe julgou como mais adequada para o escopo do projeto.
</p>

<p>
Nesse documento, a arquitetura é representada através de três visões. Elas, com os diagramas que possuem, são:
</p>

</div>

- Visão Lógica: Diagrama de Classe, Diagrama de Sequência, Diagrama de Comunicação e Diagrama de Pacotes
- Visão de Implementação: Diagrama de Componentes
- Visão de Dados: Detatalhamento do Banco de Dados, no nosso caso iremos utilizar um banco de dados NoSQL (Firebase).

## 3. Objetivos Arquiteturais e Restrições

### Objetivos
- Segurança: Os dados confidenciais dos usuários devem ser armazenados com segurança no servidor.
- Usabilidade: O software deve possuir uma navegação intuitiva e de fácil aprendizado.
- Manutenibilidade: O software deve seguir os padrões do modelo orientado a objetos e estar bem documentado para evitar custos adicionais de manutenção.

### Restrições
- É necessário possuir conexão com a Internet.
- Os sistemas operacionais Android e IOS devem ser suportados.
- O software será desenvolvido utilizando o toolkit Flutter e a linguagem de programação Dart.
- Os usuários devem utilizar uma conta do Google para cadastrar e realizar login.

## 4. Visão Lógica
<div style="text-indent: 40px; text-align: justify">

<p>
Representa a estrutura da arquitetura e exibe uma visão lógica do sistema, descrevendo as classes que envolvem o comportamento significativo do sistema em termos de arquitetura para uma melhor compreensão da organização do projeto.
</p>
</div>

### Diagrama de Classe
<div style="text-indent: 40px; text-align: justify">

<p>
Foi utilizado, para mostrar as classes significativas, seus relacionamentos, métodos e atributos, o Diagrama de Classe. Abaixo pode ser vista a versão mais recente do diagrama e a versão completa pode ser vista na aba [Diagrama de Classe](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_classe/).
[![](https://i.imgur.com/Sy8te4n.png)](https://i.imgur.com/Sy8te4n.png)
</p>

</div>
### Diagrama de Sequência
<div style="text-indent: 40px; text-align: justify">

No diagrama de sequência pode ser visualizada a interação entre os objetos do sistema e a ordem na qual as interações ocorrem. Os diagramas de sequência podem ser encontrados na aba [Diagrama de Sequência](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_sequencia/).

Diagrama de Sequência: Administração de Postagens
[![](https://i.imgur.com/UWS9xMC.png)](https://i.imgur.com/UWS9xMC.png)

</div>

### Diagrama de Comunicação

<div style="text-indent: 40px; text-align: justify">

O diagrama de comunicação foi utilizado para mostrar a interação entre diferentes partes do sistema. Apesar desse tipo de diagrama ser semelhante ao diagrama de sequência, ele possui foco na estrutura das mensagens transmitidas entre os objetos. Abaixo é mostrada o diagrama de comunicação da interação sobre os anúncios. Os outros diagramas podem ser encontrados na aba [Diagrama de Comunicação](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_comunicacao/).

Diagrama de Comunicação: Interação Anúncios
[![](https://i.imgur.com/JouiJCc.png)](https://i.imgur.com/JouiJCc.png)

</div>

### Diagrama de Pacotes

<div style="text-indent: 40px; text-align: justify">

<p>


Para ter uma visão geral das camadas envolvidas na aplicação foi utilizado o Diagrama de Modelo, que é um diagrama estrutural auxiliar do Diagrama de Pacotes. A página completa pode ser encontrada a aba [Diagrama de Pacotes](https://unbarqdsw2021-1.github.io/2021.1_G5_ProjetoDonner/pages/modelagem/diagrama_de_pacotes/).

</p>

[![](https://i.imgur.com/UQaAgnS.png)](https://i.imgur.com/UQaAgnS.png)

</div>

## 5. Visão de Implementação
<div style="text-indent: 40px; text-align: justify">

<p>
Descreve de forma geral o modelo de implementação para fornecer uma base que permitirá compreender a distribuição física do sistema em um conjunto de nós de processamento. A visão de implementação é refinada durante cada iteração.
</p>
</div>

### Diagrama de Componentes
<div style="text-indent: 40px; text-align: justify">
<p>
Para a compreensão dos relacionamentos entre os componentes que constituem o sistema e de como cada componente interage com o restante do sistema foi utilizado o diagrama de componentes.
</p>

![https://i.imgur.com/GDI3YTT.png](https://i.imgur.com/GDI3YTT.png)
</div>

## 6. Visão de Dados
<div style="text-indent: 40px; text-align: justify">
<p>
Essa é uma visão que estará presente quando o projeto possuir uma camada de persistência. A visão de dados descreve o modelo de dados do sistema, apresentando um maior detalhamento de como o banco de dados está organizado. 
</p>
</div>

## Referências

> Documento de Arquitetura de Software. Disponível em [http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf](http://www.facom.ufu.br/~flavio/pds1/files/2016-01/Documento%20de%20Arquitetura%20de%20Software%20do%20SPEU%201-Exemplo-RUP.pdf). Data de acesso: 30/09/2021

> Artefato: Documento de Arquitetura de Software. Disponível em : [https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html](https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/workproducts/rup_software_architecture_document_C367485C.html). Data de acesso: 30/09/2021

> Sistemas Cliente-Servidor. Disponível em : [http://www.inf.ufsc.br/~r.fileto/Disciplinas/BD-Avancado/Aulas/03-ClienteServidor.pdf](http://www.inf.ufsc.br/~r.fileto/Disciplinas/BD-Avancado/Aulas/03-ClienteServidor.pdf). Data de acesso: 01/10/2021

> Exemplos de Arquitetura de Software . Disponível em : [https://www.marcosmonteiro.com.br/mm/Cursos/Arquitetura_Software/Exemplos_de_Arquiteturas.pdf](https://www.marcosmonteiro.com.br/mm/Cursos/Arquitetura_Software/Exemplos_de_Arquiteturas.pdf). Data de acesso: 01/10/2021

> Introdução ao Padrão MVC. Disponível em : [https://www.devmedia.com.br/introducao-ao-padrao-mvc/29308](https://www.devmedia.com.br/introducao-ao-padrao-mvc/29308). Data de acesso: 01/10/2021

> Donar. Disponível em : [http://repositorio.aee.edu.br/bitstream/aee/1106/3/TCC2_2018_2_GabrielLeiteDias_MatheusLimadeAlbuquerque_Apendice2.pdf](http://repositorio.aee.edu.br/bitstream/aee/1106/3/TCC2_2018_2_GabrielLeiteDias_MatheusLimadeAlbuquerque_Apendice2.pdf). Data de acesso: 04/10/2021